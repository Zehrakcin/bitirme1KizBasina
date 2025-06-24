# bitirme1KizBasina
# Airline Passenger Satisfaction Analizi

Bu proje, bir havayolu şirketine ait müşteri memnuniyeti verilerini analiz ederek yolcu deneyimini etkileyen faktörleri incelemeyi ve makine öğrenmesi süreçlerine uygun bir şekilde veri hazırlamayı amaçlamaktadır.

---

## Veri Seti

- **Kaynak:** https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction
- **Satır Sayısı:** 103,904
- **Sütun Sayısı:** 25
- **Hedef Değişken:** `satisfaction` (binary: `satisfied`, `neutral or dissatisfied`)
- **Açıklamalar:**
  - Müşteri tipi, yaş, uçuş mesafesi gibi demografik veriler
  - Uçuş deneyimiyle ilgili hizmet değerlendirme puanları (0–5 arası)
  - Kalkış ve varış gecikme süreleri
  - Yolculuk tipi, sınıf bilgisi

---

## Proje Adımları

### 1. **Veri Keşfi (EDA)**
- `df.info()`, `df.describe()` ile genel yapı incelendi.
- Eksik ve aykırı veriler tespit edildi.

### 2. **Eksik Veri Doldurma**
- `Arrival Delay in Minutes` sütununda 83 eksik veri vardı.
- **Medyan** kullanılarak dolduruldu (dağılım simetrik olmadığından).

### 3. **Aykırı Değer Tespiti ve Temizliği**
- IQR yöntemiyle outlier analizleri yapıldı.
- Özellikle uçuş mesafesi ve gecikme sütunlarında kırpma (capping) uygulandı.

### 4. **Görselleştirme**
- Boxplot, Histogram, KDE, Bar chart ve Countplot kullanıldı.
- Korelasyon matrisi ile sayısal değişkenler arası ilişkiler analiz edildi.
- Kategorik değişkenlerin memnuniyet üzerindeki etkisi görselleştirildi.

### 5. **Veri Hazırlığı**
- Temizlenmiş, eksiksiz ve aykırı değerlerden arındırılmış veri kümesi oluşturuldu.
- Modelleme öncesi veri analizi tamamlandı.
