# 💰 Tedavi Listesi ve Fiyat Ayarları

Kliniğinizde uygulanan tedavilerin standart fiyatlarını, sistemdeki isimlerini, 3D modellerini ve hastalara animasyonda görünecek açıklamalarını buradan belirlersiniz.

📍 **Yol:** `Sol Menü > Tarife Ayarları > Tedavi (Üst Sekme)`

## 1. 🌍 Dil ve Para Birimi Seçimi
Listeyi düzenlemeye başlamadan önce üst paneldeki ayarları kontrol etmeniz çok önemlidir:

* **Tedavi Dili:** Listeyi hangi dil için düzenlediğinizi seçin (Örn: `EN` seçerseniz, İngilizce tekliflerde çıkacak *Extraction* ismini düzenlersiniz. `TR` seçerseniz *Çekim* ismini).
* **Para Birimi:** Fiyatların varsayılan birimini (TL, USD, EUR) belirleyin.

## 2. 📝 Liste Düzenleme Alanları
Tablodaki her satır bir tedaviyi temsil eder. Buradaki sütunların anlamları şöyledir:

* **Tedavi Adı:** Hem klinik personelinin sistemde göreceği, **hem de hastaya verilen Teklif dosyasında yazacak olan** resmi isimdir. (Örn: *Kompozit Dolgu - Tek Yüzlü*)
* **Animasyon Yazısı (Sadece Video):** Bu yazı **SADECE** 3D animasyon oynatılırken ekranın altında çıkar. Teklif dökümanlarında görünmez.
    * *Kullanım Amacı:* Animasyon izlenirken hastaya daha basit bir dil kullanmak içindir. (Örn: *Diş çürüğü temizleniyor*)
* **Fiyat:** Tedavinin standart birim fiyatıdır.
    * *Üye Başına:* Diş sayısı ile çarpılır.
    * *Sabit:* Diş sayısından bağımsız tek fiyattır.
* **Model Değiştir (3D ve Renk):** Satırın sonundaki bu butona tıklayarak, tedavinin görselini özelleştirebilirsiniz:
    * **Model Seçimi:** Tedaviyi temsil edecek 3D objeyi (İmplant vidası, Kaplama türü vb.) seçebilirsiniz.
    * **Renk Ayarı:** Seçilen model destekliyorsa, açılan paletten **rengini** değiştirebilirsiniz (Örn: Dolgu rengi veya metal rengi).
    * *Not:* Bazı sabit modellerde renk veya şekil değişikliği yapılamayabilir. Değişiklik yaptıktan sonra **Onayla** butonuna basmayı unutmayın.

## 3. ➕ Yeni Tedavi Ekleme
Listede olmayan özel bir işlem tanımlamak için:

1.  Listenin en altına inin veya ilgili grubun altındaki **"Tedavi Ekle"** butonuna basın.
2.  Yeni satıra resmi ismini, fiyatını ve animasyon açıklamasını girin.
3.  Eğer özel bir görüntüsü olacaksa **Model Değiştir** ile 3D karşılığını ve rengini atayın.

> 💾 **Çok Önemli Uyarı: KAYDETME**
> Yaptığınız fiyat, isim veya model değişikliklerinin geçerli olması için sağ üst köşedeki **KAYDET** butonuna mutlaka basmalısınız. Kaydetmeden sayfadan ayrılırsanız tüm değişiklikler kaybolur.