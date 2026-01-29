# DentalPlan API – HMAC İmzalı Entegrasyon Dokümantasyonu

Bu doküman, DentalPlan API ile entegrasyon yapmak isteyen geliştiriciler için hazırlanmıştır.  
Tüm istekler **HMAC-SHA256** ile imzalanmalıdır.

---

## Genel Bilgiler

- **Base URL:** https://api.smileapp.me
- **Content-Type:** application/json
- **Auth:** HMAC-SHA256 (Base64Url)
- **Idempotent:** Evet
- **Callback:** Desteklenir

---

## Güvenlik – HMAC İmzalama

Her HTTP isteği aşağıdaki header’lar ile gönderilmelidir:

| Header | Açıklama |
|------|---------|
| X-Api-Key | Public API Key |
| X-Timestamp | Unix timestamp (saniye) |
| X-Signature | HMAC-SHA256 imzası (Base64Url) |

---

## Canonical String

```
METHOD
PATH_AND_QUERY
TIMESTAMP
SHA256(BODY)
```

---

## Patient – Insert

### Endpoint
```
POST /api/Patient/Insert
```

### Request Body

Request body, hasta bilgileri ve işlem tamamlandığında kullanılacak
callback yapılandırmasını içerir.


```json
{
  "correlation_id": "c7f3b6a4-8c2e-4f9d-9a3b-1e2d7a6c5b44",
  "callback_url": "https://yourdomain.com/callback",
  "smileCases": {
    "name": "Deneme",
    "surname": "Hasta",
    "phone": "+90-5550000000",
    "email": "info@domain.com",
    "gender": 2
  }
}
```

#### Alanlar

| Alan | Tip | Zorunlu | Açıklama |
|----|----|--------|---------|
| `correlation_id` | `string` | Evet | İstek ve callback eşleştirmesi için kullanılan **benzersiz GUID (UUID v4)**. Her istek için farklı olmalıdır. |
| `callback_url` | `string` | Evet | İşlem tamamlandığında sonucun gönderileceği **HTTPS** callback adresi. |
| `smileCases` | `object` | Evet | Hasta bilgilerini içeren ana nesne. |
| `smileCases.name` | `string` | Evet | Hastanın adı. |
| `smileCases.surname` | `string` | Evet | Hastanın soyadı. |
| `smileCases.phone` | `string` | Evet | Hastanın telefon numarası (uluslararası format önerilir). |
| `smileCases.email` | `string` | Evet | Hastanın e-posta adresi. |
| `smileCases.gender` | `number` | Evet | Hastanın cinsiyeti. `1 = Erkek`, `2 = Kadın`. |


### Response
```json
{
  "status": "accepted",
  "plan_url": "https://api.smileapp.me/24HkiJ",
  "correlation_id": "123",
  "idempotent": true
}
```

---

## Callback URL

`callback_url`, DentalPlan API tarafından işlem tamamlandığında sonuçların
istemci sistemine geri iletilmesi için kullanılan **zorunlu** bir alandır.

---

### Genel Kurallar

- `callback_url` **zorunludur**
- Mutlaka **HTTPS** olmalıdır
- `POST` methodu ile çağrılır
- `Content-Type: application/json`
- Callback çağrısı **asenkron** olarak yapılır

---

```json
{
  "correlation_id": "c7f3b6a4-8c2e-4f9d-9a3b-1e2d7a6c5b44",
  "patient_id": "456",
  "planresponse": [
    {
      "urlShorter": "https://api.smileapp.me/24HkiJ",
      "id": "plan_id",
      "header": "Tedavi Planı",
      "PlanDate": "2025-01-01",
      "treatmentNote": "Tedavi notları"
    }
  ]
}
```

---

---


