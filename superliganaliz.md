# EXCEL SÜPERLİG ANALİZ

Bu proje; Süper Lig kulüplerinin Mağlubiyet (M), Beraberlik (B), Galibiyet gibi farklı performans metriklerini seçilen takımlar bazında dinamik olarak kıyaslamak amacıyla Microsoft Excel ortamında geliştirilmiş etkileşimli bir analiz aracıdır.

<img width="1605" height="685" alt="superlig_analiz_excel" src="https://github.com/user-attachments/assets/80087c26-2975-46cb-aa57-3e027b5a6193" />

🔑 Pano Yapısı ve Öne Çıkan Özellikler
Çift Metrik Karşılaştırma Seçimi (Dinamik Parametreler):

Karşılaştırma 1 & Karşılaştırma 2: Açılır menüler (Drop-down) üzerinden kıyaslanmak istenen metrikler (örneğin Mağlubiyet ve Beraberlik) esnek bir şekilde seçilebilir.

Grafik başlığı ve göstergeler (M - B) seçilen parametrelere göre dinamik olarak güncellenir.

Çoklu Takım Seçim Alanı (Veri Doğrulama):

Kullanıcının odaklanmak istediği 5 farklı takımı (örn. Fatih Karagümrük, Çaykur Rizespor, Konyaspor, Göztepe, Başakşehir) bağımsız olarak seçebilmesine olanak tanır.

Dinamik Hibrit Grafik Yapısı:

Sütun + Yüzen Çizgi/İşaretçi Grafiği (Combined Chart): Karşılaştırılan ilk metriği yeşil sütunlar ile, ikinci metriği ise turuncu yatay işaretçiler ile sunarak iki farklı istatistiği tek bir görsel üzerinde net bir şekilde çakıştırmadan kıyaslama imkanı verir.

📌 Kullanılan Excel Teknikleri
Arama & Eşleştirme Formülleri: Seçimlere göre veriyi dinamik çekmek için DÜŞEYARA (VLOOKUP), İNDİS (INDEX) veya KAÇINCI (MATCH) kullanımı.

Dinamik Metin & Grafik Başlıkları: Hücre birleştirme formülleri (& veya BİRLEŞTİR) ile grafik başlığının dinamikleştirilmesi.

Veri Doğrulama (Data Validation): Takım ve metrik seçimleri için dinamik liste yapıları.

Gelişmiş Grafik Özelleştirme: Özel sütun ve çizgi/işaretçi (Marker) kombinasyonlu grafik tasarımı.
