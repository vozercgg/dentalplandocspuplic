## Node.js (Crypto)

```js
import crypto from "crypto";

const API_KEY = "pk_xxx";
const SECRET_B64U = "your_base64url_secret";

function b64uDecode(b64u) {
  let s = b64u.replace(/-/g, "+").replace(/_/g, "/");
  while (s.length % 4) s += "=";
  return Buffer.from(s, "base64");
}

function b64uEncode(buf) {
  return buf
    .toString("base64")
    .replace(/=+$/, "")
    .replace(/\+/g, "-")
    .replace(/\//g, "_");
}

function sha256Hex(str) {
  return crypto.createHash("sha256").update(str ?? "", "utf8").digest("hex");
}

export function sign({ method, pathAndQuery, bodyRaw = "" }) {
  const ts = Math.floor(Date.now() / 1000).toString();
  const bodyHash = sha256Hex(bodyRaw);

  const canonical = `${method.toUpperCase()}\n${pathAndQuery}\n${ts}\n${bodyHash}`;

  const mac = crypto
    .createHmac("sha256", b64uDecode(SECRET_B64U))
    .update(canonical, "utf8")
    .digest();

  return {
    "X-Api-Key": API_KEY,
    "X-Timestamp": ts,
    "X-Signature": b64uEncode(mac),
    "Content-Type": "application/json"
  };
}
```

---

## .NET (C#)

```csharp
using System;
using System.Security.Cryptography;
using System.Text;

public static class DentalPlanHmac
{
    const string API_KEY = "pk_xxx";
    const string SECRET_B64U = "your_base64url_secret";

    static byte[] B64uDecode(string s)
    {
        s = s.Replace("-", "+").Replace("_", "/");
        while (s.Length % 4 != 0) s += "=";
        return Convert.FromBase64String(s);
    }

    static string B64uEncode(byte[] b)
        => Convert.ToBase64String(b).TrimEnd('=').Replace('+','-').Replace('/','_');

    static string Sha256Hex(string s)
    {
        using var sha = SHA256.Create();
        var hash = sha.ComputeHash(Encoding.UTF8.GetBytes(s ?? ""));
        return BitConverter.ToString(hash).Replace("-", "").ToLowerInvariant();
    }

    public static (string ts, string sig) Sign(string method, string pathAndQuery, string bodyRaw)
    {
        var ts = DateTimeOffset.UtcNow.ToUnixTimeSeconds().ToString();
        var bodyHash = Sha256Hex(bodyRaw);

        var canonical = $"{method.ToUpper()}\n{pathAndQuery}\n{ts}\n{bodyHash}";

        using var hmac = new HMACSHA256(B64uDecode(SECRET_B64U));
        var sig = B64uEncode(hmac.ComputeHash(Encoding.UTF8.GetBytes(canonical)));

        return (ts, sig);
    }
}
```

---

## Python 

```python
import base64, hashlib, hmac, time

API_KEY = "pk_xxx"
SECRET_B64U = "your_base64url_secret"

def b64u_decode(s):
    s = s.replace("-", "+").replace("_", "/")
    s += "=" * (-len(s) % 4)
    return base64.b64decode(s)

def b64u_encode(b):
    return base64.b64encode(b).decode().rstrip("=").replace("+","-").replace("/","_")

def sha256_hex(s):
    return hashlib.sha256((s or "").encode()).hexdigest()

def sign(method, pathAndQuery, bodyRaw=""):
    ts = str(int(time.time()))
    bodyHash = sha256_hex(bodyRaw)

    canonical = f"{method.upper()}\n{pathAndQuery}\n{ts}\n{bodyHash}"

    sig = hmac.new(
        b64u_decode(SECRET_B64U),
        canonical.encode(),
        hashlib.sha256
    ).digest()

    return {
        "X-Api-Key": API_KEY,
        "X-Timestamp": ts,
        "X-Signature": b64u_encode(sig),
        "Content-Type": "application/json"
    }
```

---

DentalPlan API  
**Secure by Design 🚀**
