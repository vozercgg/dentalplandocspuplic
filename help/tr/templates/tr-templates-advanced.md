# 🚀 Gelişmiş Şablon Yönetimi ve Sayfa Oluşturma

Standart şablonların ötesine geçerek; dinamik veri sayfaları oluşturabilir, tasarımları diller arası transfer edebilir ve hangi sayfaların hastalara "standart" olarak gideceğini belirleyebilirsiniz.

📍 **Yol:** `Sol Menü > Taslaklar` (Sağ Üst Panel ve Sayfa Kartları)

## 1. 📄 Sayfa Oluşturma: Tam Sayfa vs. Data Sayfası
Sağ üst panelden yeni sayfa eklerken ihtiyacınıza göre iki farklı yöntem vardır:

### A. Tam Sayfa Oluştur (Full Page)
Tasarımı tamamen size ait olan, serbest sayfalar için kullanılır.

* **Tür Seçimi Neden Önemli?** Açılan pencerede sayfa türünü (Örn: *Doktorlar, Oteller, İletişim, Çalışmalar*) doğru seçmek kritiktir.
    * *Örneğin:* **"Doktorlar"** türünü seçerseniz, editörde o sayfaya özel "Doktor Adı", "Uzmanlık" gibi veri alanları otomatik olarak gelir.

### B. Data Sayfası Oluştur (Dinamik)
İçeriği hastaya göre değişen, liste mantığındaki sayfalar (Tedavi Tablosu, Teşhis, Ekstralar) için kullanılır.

* **Farkı Nedir?** Tam sayfanın aksine, bu sayfaların şablonu "kısıtlıdır" ve akıllıdır.
* **Avantajı:** Hastanın tedavi listesi ne kadar uzun olursa olsun, sistem tabloyu bu sınırlara göre otomatik ayarlar ve verileri (Fiyatlar, Diş numaraları) kusursuz yerleştirir.

## 2. 🔄 Kopyalama ve Klonlama (Diller Arası Transfer)
Tasarımlarınızı tekrar tekrar yapmanıza gerek yok. Hazır sayfaları başka dillere veya setlere aktarabilirsiniz:

* **Toplu Kopyalama (Sayfaları Kopyala):** Mevcut dildeki (Örn: TR) **tüm yapıyı** hedef dile (Örn: EN) tek tıkla aktarır.
* **Tekli Klonlama (Clone):** Sayfa kartının altındaki **Klonla** butonu ile, sadece o sayfayı başka bir dile veya şablon setine (Örn: Klasik -> Modern) kopyalayabilirsiniz.

## 3. 🔢 Sıralama ve Varsayılan (Default) Seçimi
Sağ üstteki **"Sıralamayı Düzenle"** butonuna tıkladığınızda iki önemli ayar yaparsınız:

### A. Sayfa Sıralaması
Sayfaları sürükle-bırak yöntemiyle taşıyarak PDF içindeki yerlerini (Örn: Önce Kapak, sonra Hakkımızda) belirlersiniz.

### B. Otomatik Seçim (Check it by Default)
Düzenleme modunda her sayfanın altında beliren **"Check it by Default"** (Varsayılan Olarak Seç) kutucuğu hayati önem taşır:

* **İşlevi:** Eğer bir sayfanın altındaki bu kutucuğu işaretlerseniz; yeni bir hasta için doküman oluşturduğunuzda **o sayfa otomatik olarak seçili (tikli) gelir.**
* **Kullanım Alanı:** Her hastaya mutlaka gitmesini istediğiniz standart sayfalarınız (Örn: *Standart Kapak, Giriş Yazısı, Arka Kapak*) için bu kutucuğu işaretleyin.
* **Esneklik:** Bu bir zorunluluk değildir; sadece başlangıç ayarıdır. Dilerseniz hasta özelinde doküman oluştururken bu tikleri kaldırabilir veya varsayılan olmayan diğer sayfaları da seçebilirsiniz.