# Laptop Price Prediction (Jupyter Notebook)

Bu proje, `laptop_price.csv` veri setindeki laptop özelliklerini kullanarak laptop fiyatını (`Price_euros`) tahmin etmeyi amaçlar. Notebook içinde veri temizleme, özellik mühendisliği (feature engineering), one-hot encoding, korelasyon analizi, özellik seçimi ve farklı regresyon modellerinin karşılaştırılması yapılmıştır.

## Proje İçeriği

- Veri yükleme ve ön işleme
- Kategorik değişkenler için one-hot encoding
- Metin alanlarından yeni özellikler çıkarma
  - Ekran çözünürlüğünden `Screen Width` ve `Screen Height`
  - CPU bilgisinden `CPU Brand` ve `CPU Frequency`
  - RAM’i sayısala çevirme
  - Memory alanından `Memory Amount` ve `Memory Type` çıkarma (GB/TB -> MB dönüşümü)
  - Weight alanını sayısala çevirme
  - GPU markasını one-hot encoding ile dönüştürme
- Korelasyon (heatmap) analizi
- `Price_euros` ile en çok ilişkili sayısal özelliklerden **top ~21** özelliğin seçimi
- Model eğitimi ve karşılaştırma
  - Linear Regression
  - Lasso
  - Ridge
  - Decision Tree Regressor
  - Random Forest Regressor
- Değerlendirme metrikleri
  - R²
  - Adjusted R²
  - MAE
  - MSE
  - RMSE
- Tahmin vs Gerçek (scatter) görselleştirmeleri

## Dosyalar

- `laptop-price-prediction.ipynb` : Tüm analiz ve modelleme adımlarının olduğu notebook
- `laptop_price.csv` : Veri seti 

> Not: Veri seti size ait değilse/telifli ise `*.csv`’yi `.gitignore` ile dışarıda bırakıp README’ye indirme kaynağı eklemeniz önerilir.

## Kurulum

Gerekli paketler
pip install pandas numpy scikit-learn matplotlib seaborn

1) Python (3.9+ önerilir) kurulu olmalı.

2) Sanal ortam oluşturup aktif edin:

### Windows (PowerShell)
```bash
python -m venv .venv
.\.venv\Scripts\activate




