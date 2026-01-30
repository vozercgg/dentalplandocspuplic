# 🔗 Akıllı Veri (Data Variables) ve Otomasyon

Şablonlarınızı her hasta için tek tek elle düzenlemek zorunda değilsiniz. Bu panel, oluşturduğunuz tasarımı binlerce hastaya uyarlayabilen "Akıllı Etiketler" sistemidir.

**Yol:** `Sol Menü > Veriler (Data)`

## 1. ❓ Nedir ve Neden Kullanılır?
Akıllı Veri, şablonun içine yerleştirdiğiniz dinamik bir yer tutucudur (Placeholder).

* **Manuel Yöntem (Yanlış):** Sayfaya elle *"Sayın Ahmet Yılmaz"* yazarsanız, bu şablonu başka hastada kullanamazsınız.
* **Akıllı Yöntem (Doğru):** Sayfaya `{Hasta Adı}` etiketini koyarsanız; sistem her PDF oluşturduğunda o anki hastanın ismini (Ayşe, Mehmet, John) otomatik olarak oraya yazar.

## 2. 🧠 Bağlamsal Değişkenler (Context Sensitivity)
Sol paneldeki **Veriler** listesi sabit değildir; üzerinde çalıştığınız **sayfa türüne göre otomatik değişir.**

* **Kapak Sayfasındaysanız:** Listede *Klinik Adı, Klinik Adresi, Hasta Adı* gibi genel verileri görürsünüz.
* **Tedavi Sayfasındaysanız:** Listede *Diş Numarası, Tedavi Bilgisi, Fiyat, Toplam Tutar* gibi tablo verilerini görürsünüz.
* **Doktorlar Sayfasındaysanız:** Listede *Doktor Adı, Ünvanı, Uzmanlık alanı* gibi personel verilerini görürsünüz.

## 3. 🚀 Nasıl Kullanılır?
Tasarımınıza akıllı veri eklemek sadece 3 saniyenizi alır:

1.  Sol panelden **🔗 Veriler** sekmesine tıklayın.
2.  İhtiyacınız olan etiketi (Örn: `Hasta Adı`) listede bulun.
3.  Etiketi mouse ile tutup, sayfanın üzerinde görünmesini istediğiniz yere **sürükleyip bırakın.**

> 🎨 **Stil İpucu:**
> Sürükleyip bıraktığınız etikete (Örn: `{Patient Name}`) tıkladıktan sonra, üst panelden rengini ve boyutunu değiştirebilirsiniz. Sağ panelden arka plan ve gölge ekleyerek tasarımınızı hareket ekleyebilirsiniz.  Sistem, hastanın gerçek ismini yazarken sizin belirlediğiniz bu stili kullanır.

## 4. ✨ Sonuç: Tek Şablon, Binlerce Hasta
Siz tasarımı bir kez yaparsınız:

> *"Sayın {Hasta Adı}, {Tarih} tarihli tedavi planınız aşağıdadır."*

Sistem, PDF oluştururken bunu otomatik dönüştürür:

> *"Sayın **Zeynep Kaya**, **24.01.2025** tarihli tedavi planınız aşağıdadır."*

## ⚠️ Data Sayfaları İçin Kritik Uyarılar
Bu verilerin kullanıldığı dinamik sayfalarda (Tedavi Tablosu vb.) çalışırken şu kurallara dikkat edin:

1.  **📏 Kılavuz Çizgisi Hatası:** Eğer *"İçerikler çizgilerin dışında"* uyarısı alırsanız; eklediğiniz objenin sayfayı bölen çizgilerin **tam üzerine** gelmediğinden emin olun. Obje çizgiyi kesmemeli, bir alanın (Header veya Footer) içinde tam durmalıdır.
2.  **🚫 Yasak Bölge (Body):** Sayfanın orta kısmı (Body) dinamiktir ve tedavi sayısına göre uzayıp kısalır. Bu araya **asla sabit metin veya logo koymayınız.** Sabit görsellerinizi her zaman en üstteki **Header** veya en alttaki **Footer** alanlarına yerleştirin.