# 🎬 Tedavi Animasyonu ve Yapay Zeka Anlatımı

Oluşturduğunuz tedavi planını, hastanızın kolayca anlayabileceği 3D bir animasyona dönüştürün. Bu özellik, hastayı ikna etmek ve tedavi sürecini profesyonelce görselleştirmek için kullanılır.

📍 **Yol:** `Hastalar > [Hasta Adı] > Animasyon`

## 1. 🎞️ Animasyon Akışı ve Sıralama
Ekranın sol panelinde, yapılacak tedavilerin oynatılma sırasını (Örn: Önce çekim, sonra implant) görürsünüz.

* **Sıralamayı Değiştirme:** Listeki işlemleri sürükle-bırak yöntemiyle aşağı veya yukarı taşıyarak animasyonun akışını değiştirebilirsiniz.

> ⚠️ **Kritik Senkronizasyon Uyarısı:**
> Animasyon ekranında yaptığınız sıralama değişikliği, **"Tedavi" sekmesindeki asıl planın sırasını da değiştirir.**
> Eğer burada sıralamayı bozarsanız (Örn: Kronu İmplantın önüne alırsanız), tedavi tablosunda da sıralama değişir. Bu nedenle sıralamayı her zaman klinik işlem mantığına göre yapınız.

## 2. 🤖 Yapay Zeka ile Hikaye ve Ses
Animasyonun sağ panelinde, hastaya yapılacak işlemleri anlatan akıllı araçlar bulunur:

* **📝 Anlatım (Hikaye) Oluştur:** "Yapay Zeka Anlatımı Oluştur" butonuna tıkladığınızda sistem, tedavi planına uygun profesyonel bir metin yazar.
* **🗣️ Seslendirme (Voiceover):** Hikayenin hemen altındaki "Yapay Zeka Sesi Oluştur" butonu ile bu metni sesli anlatıma çevirebilirsiniz.
    * **Özelleştirme:** Oluşan sesi dinleyebilir, ses tonunu değiştirebilir veya beğenmezseniz **"Sil"** diyerek kaldırabilirsiniz.

> 🌍 **Dil Seçimi Hakkında Önemli Not:**
> Yapay zeka tarafından oluşturulan hikaye metni ve seslendirme, plan ayarlarında seçtiğiniz **Tedavi Dili**ne göre otomatik belirlenir.
>
> *Örneğin:* Tedavi dilini **İngilizce** seçerseniz, yapay zeka anlatımı ve seslendirmesi **tamamen İngilizce** olarak oluşturulacaktır.

## 3. 📲 Paylaşma Seçenekleri
Hazırladığınız görsel şöleni hastanıza iletmek için sağ üstteki **"Paylaş & Kaydet"** alanını kullanın:

* **WhatsApp:** En hızlı yöntemdir. Tıkladığınızda hastanın numarasına hazır bir mesaj ve animasyon linki oluşturur.
* **QR Kod:** Hasta o an yanınızdaysa, ekranda çıkan kodu hastanın telefon kamerasına okutarak animasyonu kendi cihazında izlemesini sağlayabilirsiniz.
* **Link Kopyala:** Animasyonun web bağlantısını kopyalar; E-posta, SMS veya Instagram üzerinden manuel olarak gönderebilirsiniz.