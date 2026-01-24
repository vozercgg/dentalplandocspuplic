# 📄 Sayfa Türleri ve Veri Mantığı

Taslak editöründe her sayfanın davranışı aynı değildir. İki ana sayfa türünü ve bunların düzenleme kurallarını bilmek, hatasız şablonlar oluşturmanızı sağlar.

**Yol:** `Sol Menü > Taslaklar`

## 1. Tam Sayfa (Full Page) Düzenleme
Kapak, Giriş (Intro), Arka Kapak gibi serbest tasarımlı sayfalardır.

* **Özgürlük:** Bu sayfalarda metinleri, görselleri ve şekilleri sayfanın dilediğiniz yerine koyabilir, tamamen özgürce tasarım yapabilirsiniz.
* **Veriler:** Sayfa türüne göre (Örn: Doktorlar Sayfası) sol paneldeki **"Veriler"** sekmesinden ilgili değişkenleri (Doktor Adı, Ünvanı vb.) sürükleyip sayfaya bırakabilirsiniz.

## 2. Data Sayfası (Dinamik İçerik) Düzenleme
Tedavi Tablosu, Teşhis (Diagnosis) ve Ekstralar gibi içeriği "liste" halinde olan sayfalardır. Bu sayfalar 3 ana bölüme ayrılmıştır ve çizgilerle belirtilir:

1.  **Sayfa Başlığı (Header):** Üst kısım.
2.  **İçerik Başlığı** İçerik ile ilgili görseller ve başlıkların düzenlendiği için
3.  **İçerik Gövdesi (Body):** Verilerin listelendiği orta kısım.
4.  **İçerik Altbilgi** Verilerin toplam satırları gibi değişkenlerin düzenlendiği kısım.
5.  **Sayfa Alt Bilgisi (Footer):** Alt kısım.

### ⚠️ Kritik Uyarı: "Dokunulmaz Bölge"
Data sayfalarında düzenleme yaparken çok dikkatli olmalısınız:

> **Lütfen Dikkat:**
> Editörde görünen bölümleri ayıran çizgilerinin arasına manuel olarak metin, görsel veya şekil **EKLEMEYİNİZ.**
>
> * **Neden?** Bu alan, hastanın tedavi listesine göre (Örn: 10 diş veya 2 diş) otomatik olarak uzayıp kısalır.
> * **Sonuç:** Eğer bu araya sabit bir obje (Örn: Logo) koyarsanız, liste uzadığında o obje verilerin altında kalır, kaybolur veya dökümanın bozuk (render hatası) çıkmasına neden olur.
> * **Doğru Yöntem:** Düzenlemelerinizi her zaman iki çizgi arasına gelecek şekilde yerleştirin.

## 3. Veri Paneli (Data Variables)
Sol panelde bulunan **Veriler** sekmesi, sayfa türüne göre değişen akıllı etiketler içerir.

* **Kullanım:** Örneğin "Ekstralar" sayfasındaysanız, panelde "Ekstra Web Sitesi" gibi veriler belirir. Bunları sayfaya sürükleyip bırakarak, hastaya özel bilgilerin otomatik dolmasını sağlayabilirsiniz.