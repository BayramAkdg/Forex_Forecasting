# EUR/USD Forex Tahmin Projesi

Bu proje, EUR/USD döviz çifti üzerinde saatlik veriler kullanarak gelecekteki döviz kurunu tahmin etmek için bir LSTM (Long Short-Term Memory) modeli geliştirmeyi amaçlamaktadır.
Projede Python programlama dili ve ilgili veri bilimi kütüphaneleri kullanılmıştır.

---

# Veri Seti Hakkında

- **Kaynak**: [Kaggle - EUR/USD Forex Pair Historical Data](https://www.kaggle.com/)
  - **Dosyalar**:
  - `eurusd_hour.csv`: Saatlik döviz verileri.
  - `eurusd_minute.csv`: Dakikalık döviz verileri.
  - `eurusd_news.csv`: Haber kaynaklı analizler.
- **Özellikler**:
  - **Date**: Tarih ve zaman bilgisi.
  - **BC (Bid Close)**: Kapanış fiyatı.
  - **BA (Bid Ask)**: Teklif alış fiyatı.
  - Diğer sütunlar (Örnek: Yüksek, düşük fiyatlar).

Veri setindeki eksik veriler tespit edilip temizlenmiştir. 

---

## Kullanılan Kütüphaneler

Projede aşağıdaki Python kütüphaneleri kullanılmıştır:

- **Veri İşleme**:
  - `pandas`: Veri çerçeveleri üzerinde işlem yapmak için.
  - `numpy`: Matematiksel işlemler ve diziler için.
  
- **Veri Görselleştirme**:
  - `matplotlib`: Grafikler ve veri görselleştirme için.

- **Makine Öğrenimi ve Derin Öğrenme**:
  - `sklearn.preprocessing`: Veriyi normalleştirmek için (MinMaxScaler).
  - `tensorflow.keras`: LSTM modeli oluşturmak ve eğitmek için.

---

## Projede Yapılan Analizler ve İşlemler

1. **Veri Yükleme ve İşleme**:
   - Kaggle üzerinden veri seti yüklendi.
   - Tarih sütunu indeks olarak ayarlandı.
   - `BC (Bid Close)` sütunu filtrelenerek analiz için seçildi.
   - Eksik değerler kontrol edilip temizlendi.

2. **Veri Görselleştirme**:
   - Döviz çiftinin zaman serisi grafiği çizildi.
   - Modelin eğitim ve tahmin sonuçları karşılaştırmalı olarak görselleştirildi.

3. **Normalizasyon**:
   - Veriler, MinMaxScaler ile 0-1 arasında normalleştirildi.

4. **Model Eğitimi**:
   - LSTM modeli oluşturuldu.
   - Eğitim verisiyle model eğitildi.

5. **Tahminler**:
   - Test verileri üzerinde tahminler yapıldı.
   - Tahminler, gerçek değerlerle karşılaştırıldı.

## Çıktılar

- Proje sonunda elde edilen model, döviz çiftinin gelecekteki fiyatlarını tahmin etmede etkili sonuçlar verdi.
- Tahmin sonuçları grafiklerle görselleştirildi ve modelin doğruluğu analiz edildi.
