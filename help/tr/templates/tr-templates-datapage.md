# 📊 Data Sayfası (Dinamik İçerik) Oluşturma ve Yapısı

Tedavi Tablosu, Teşhis (Diagnosis) ve Ekstralar gibi içeriği "liste" halinde olan ve hastaya göre uzayıp kısalabilen sayfaların rehberidir.

📍 **Yol:** `Sol Menü > Taslaklar`

## 1. ➕ Data Sayfası Oluşturma
İçeriği değişken olan bir sayfa eklemek için:

1.  Sağ üst panelden **"Data Sayfası Oluştur"** seçeneğine tıklayın.
2.  Sayfa türünü seçin (Tedavi, Diagnoz vb.).

* **Avantajı:** Hastanın tedavi listesi ne kadar uzun olursa olsun (3 satır veya 20 satır), sistem tabloyu sınırlara göre otomatik ayarlar ve verileri kusursuz yerleştirir.

## 2. 📐 Sayfa Yapısı ve Bölümler
Data sayfaları, verilerin doğru işlenmesi için 5 ana bölüme ayrılmıştır ve editörde çizgilerle belirtilir:

1.  **Sayfa Başlığı (Header):** Sayfanın en üst kısmıdır. (Sabit alan)
2.  **İçerik Başlığı:** Listenin hemen üzerindeki alandır. İçerik ile ilgili başlıklar veya sütun isimleri burada düzenlenir.
3.  **İçerik Gövdesi (Body):** Verilerin listelendiği, dinamik orta kısımdır. (Tedavi satırları buraya gelir).
4.  **İçerik Altbilgi:** Verilerin bittiği yerdir. Toplam fiyat, ara toplam gibi değişkenlerin düzenlendiği kısımdır.
5.  **Sayfa Alt Bilgisi (Footer):** Sayfanın en alt kısmıdır. (Sabit alan)

## 3. ⚠️ Kritik Uyarı: "Dokunulmaz Bölge"
Data sayfalarında düzenleme yaparken, listenin bozulmaması için şu kurala **kesinlikle** uymalısınız:

> **Lütfen Dikkat:**
> Editörde görünen bölümleri ayıran çizgilerin arasına (özellikle İçerik Gövdesi'ne) manuel olarak metin, görsel veya şekil **EKLEMEYİNİZ.**
>
> * **Neden?** Bu alan, hastanın tedavi listesine göre otomatik olarak uzayıp kısalır.
> * **Sonuç:** Eğer bu araya sabit bir obje (Örn: Logo) koyarsanız; liste uzadığında o obje verilerin altında kalır, kaybolur veya dökümanın bozuk (render hatası) çıkmasına neden olur.
> * **Doğru Yöntem:** Düzenlemelerinizi ve süslemelerinizi her zaman çizgilerin oluşturduğu güvenli alanlara (Header veya Footer) yerleştirin.

## 4. 🔗 Veri Kullanımı
Sol paneldeki **Veriler** sekmesi, bu sayfalarda hayati önem taşır:

* Örneğin "Ekstralar" sayfasındaysanız, panelde "Ekstra Web Sitesi", "Ekstra Fiyatı" gibi veriler belirir.
* Bu verileri sürükleyip ilgili satırlara (genellikle İçerik Gövdesi içindeki tanımlı alanlara) bırakarak şablonu kurgulayabilirsiniz.