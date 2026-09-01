# İnsan Kaynakları (HR) Analiz Dashboard'u

Bu Power BI raporu, bir şirketin insan kaynakları verilerini analiz etmek; personel sayısı, cinsiyet dağılımı, departman bazlı yoğunluk ve işten ayrılma (turnover) oranlarını dinamik olarak takip etmek amacıyla tasarlanmıştır.


## 📊 DAX Ölçümleri (Measures)

Projede kullanılan temel DAX formülleri ve işlevleri:

### 1. Toplam Personel Sayısı
Veri setindeki toplam çalışan sayısını hesaplar.
```dax
Personel Sayısı = COUNTA(Tablo33[İsim Soyisim])
```
### 2. Kadın Personel Sayısı
Toplam personel sayısı içerisinden cinsiyeti "kadın" olan çalışanları filtreleyerek hesaplar.
```dax
Kadın Personel Sayısı = CALCULATE([Personel Sayısı], Tablo33[Cinsiyet] = "kadın")
```
### 3. Ayrılan / Çalışan Personel Oranı
Şirketten ayrılan personellerin toplam personel sayısına oranını (Turnover / Attrition Rate) hesaplar.
```dax
Çalışan Personel Sayısı = DIVIDE(CALCULATE([Personel Sayısı], Tablo33[Durum] = "Ayrıldı"), [Personel Sayısı])
```
<img width="1361" height="730" alt="insan_kaynaklari_1" src="https://github.com/user-attachments/assets/553ccfc9-e990-4d71-9c66-20c0e953f652" />

## 📈 Rapor Görselleri ve Bileşenler
### KPI Kartları (Üst Panel):

Toplam Maaş (1.60M): Şirketin toplam maaş maliyetini gösterir.

Personel Sayısı (68): Şirket bünyesindeki toplam kayıtlı çalışan sayısı.

Kadın Personel Sayısı (38): Kadın çalışan sayısı.

Çalışan Personel Sayısı Oranı (%29.41): Şirketten ayrılan personellerin toplam personele oranı.

### Toplam Çalışan Sayısı (Sütun Grafiği):

Departman bazında (İnsan Kaynakları, Üretim, Pazarlama, Bilgi Teknolojileri, Satış, Yönetim, Muhasebe) personel dağılımını azalan sırada görselleştirir.

### Personel Durumu (Halka Grafik):

Aktif olarak çalışan personeller (%70.59) ile şirketten ayrılan personellerin (%29.41) oransal dağılımını gösterir.

### Dinamik Slicer / Filtre Paneli (Sol Panel):

Cinsiyet ve Durum Butonları: Erkek, Kadın, Ayrıldı, Çalışıyor durumlarına göre anlık filtreleme sağlar.

### Şehir Dilimleyicisi (Location Slicer): 
Şehirlere göre tüm panoyu dinamik olarak filtreler.
