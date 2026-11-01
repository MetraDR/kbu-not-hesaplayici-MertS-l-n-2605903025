# KBÜ Not Hesaplayıcı (Vize - Final/Bütünleme)

Karabük Üniversitesi Ön-Lisans ve Lisans eğitim-öğretim yönetmeliğine göre tasarlanmış, vize ve final/bütünleme notları üzerinden ders başarı durumu ve harf notu hesaplayan tek sayfalık Vanilla JS web uygulamasıdır.

## 🧮 Hesaplama Mantığı (KBÜ Kuralları)

- **Başarı Notu Ağırlığı:** Yıl içi etkinliklerinin (Vize/Ara sınav) %40'ı ile Genel sınavın (Final veya Bütünleme) %60'ı toplanarak elde edilir. Yıl içi notu ayrıca girilmezse Vize notu baz alınır.
- **Geçme Koşulları:** Bir öğrencinin dersten geçebilmesi için;
  1. Genel/Bütünleme sınavından en az **50** alması zorunludur.
  2. Hesaplanmış Ders Başarı Notunun en az **60** olması zorunludur.
- **Başarısızlık (Kalma) Nedenleri:**
  - **F1:** Devamsızlık (Sınav hakkı yoktur).
  - **F2:** Devam şartını sağlayıp Genel/Bütünleme sınavına girmeme.
  - **F3:** Final/Bütünleme notunun 50 altında kalması veya Başarı Notunun 60'ın altında kalması.
- **Geçme Harf Notları:** 
  - 90–100 → A1 (4.00)
  - 80–89 → A2 (3.50)
  - 70–79 → B1 (3.00)
  - 65–69 → B2 (2.75)
  - 60–64 → C (2.50)

## 🚀 Kullanım Talimatı

Uygulama herhangi bir kütüphane veya veritabanı kurulumu gerektirmez:
1. Projeyi klonlayın veya zip formatında indirin.
2. Bilgisayarınızdaki klasörü açıp `index.html` dosyasını favori tarayıcınızda (Chrome, Edge vb.) başlatın.
3. Form ekranında notlarınızı girdikten sonra **Enter** tuşuna basarak veya **Hesapla** butonuna tıklayarak sonucunuzu görebilirsiniz.
4. Yeni bir hesaplama yapmak için **Sıfırla** butonunu kullanabilirsiniz.

## 🧪 Test Senaryoları (Beklenen Sonuçlar)

1. **Vize: 70, Final: 60**
   - Hesap: (70 * 0.40) + (60 * 0.60) = 28 + 36 = **64**
   - Sonuç: Harf Notu C, **Geçti**.
2. **Vize: 95, Final: 48**
   - Sonuç: Başarı notu yeterli olsa da Final notu 50 barajını geçemediği için **F3 (Kaldı)**.
3. **Vize: 58, Final: 40, Bütünleme: 55**
   - Hesap: (58 * 0.40) + (55 * 0.60) = 23.2 + 33 = **56.20**
   - Sonuç: Bütünleme barajı geçildi fakat Başarı Notu 60 altında kaldığı için **F3 (Kaldı)**.
4. **Devamsız (F1)** işareti seçildiğinde,
   - Sonuç: Başka nota bakılmaksızın **F1 (Kaldı)**.