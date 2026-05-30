# Konut Fiyat Tahmini (House Price Prediction) 🏡📊

Bu proje, çeşitli fiziksel ve konumsal özelliklerine göre konut fiyatlarını tahmin etmeyi amaçlayan kapsamlı bir makine öğrenmesi (Machine Learning) çalışmasıdır. Veri bilimi ve makine öğrenmesi süreçlerinin (veri ön işleme, keşifçi veri analizi, özellik seçimi, model eğitimi ve değerlendirme) adım adım uygulandığı bir yapıya sahiptir.

## 📋 Veri Seti (Dataset)

Projede kullanılan veri seti (`Housing.csv`), bir evin fiyatını etkileyebilecek özellikleri içermektedir. Veri setinde yer alan özellikler şunlardır:

* **`price`**: Konutun fiyatı (Hedef Değişken / Target Variable)
* **`area`**: Evin toplam alanı
* **`bedrooms`**: Yatak odası sayısı
* **`bathrooms`**: Banyo sayısı
* **`stories`**: Evin kat sayısı
* **`mainroad`**: Ana yola yakınlık durumu (Evet/Hayır)
* **`guestroom`**: Misafir odası olup olmadığı (Evet/Hayır)
* **`basement`**: Bodrum katı olup olmadığı (Evet/Hayır)
* **`hotwaterheating`**: Sıcak su ısıtma sistemi durumu (Evet/Hayır)
* **`airconditioning`**: Klima durumu (Evet/Hayır)
* **`parking`**: Otopark kapasitesi (Araç sayısı)
* **`prefarea`**: Tercih edilen bir bölgede olup olmadığı (Evet/Hayır)
* **`furnishingstatus`**: Eşya durumu (Eşyalı, Yarı Eşyalı, Eşyasız)

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler

Projenin geliştirilmesinde Python programlama dili ve popüler veri bilimi kütüphaneleri kullanılmıştır:

* **Veri Manipülasyonu ve Analizi:** `pandas`, `numpy`
* **Veri Görselleştirme:** `matplotlib`, `seaborn`
* **Makine Öğrenmesi Modelleri ve Metrikler:** `scikit-learn`
* **Gelişmiş Algoritmalar:** `xgboost`, `lightgbm`, `catboost`
* **İstatistiksel Analizler:** `statsmodels`

## 🧠 Uygulanan Makine Öğrenmesi Modelleri

Projeyle farklı model mimarileri denenerek en yüksek performanslı tahminleyici bulunmaya çalışılmıştır:

* Çoklu Doğrusal Regresyon (Multiple Linear Regression)
* Ridge ve Lasso Regresyon (L1/L2 Regülarizasyonu)
* ElasticNet Regresyon
* Destek Vektör Regresyonu (SVR)
* Rastgele Orman Regresyonu (Random Forest Regressor)
* Gradyan Artırma Regresyonu (Gradient Boosting Regressor)
* XGBoost, LightGBM ve CatBoost Regressor

## 🚀 Proje İş Akışı

1. **Veri Ön İşleme (Data Preprocessing):** Eksik veri kontrolü ve kategorik değişkenlerin makine öğrenmesi modellerinin anlayabileceği sayısal formata dönüştürülmesi (One-Hot Encoding). Değişkenlerin farklı ölçeklerde olmasından kaynaklanacak sapmaları önlemek için veri ölçeklendirme (MinMaxScaler/StandardScaler).
2. **Keşifçi Veri Analizi (Exploratory Data Analysis - EDA):** Değişkenlerin dağılımlarının incelenmesi, aykırı değer analizi ve özelliklerin hedef değişken olan `price` ile korelasyonlarının görselleştirilmesi.
3. **Özellik Seçimi (Feature Selection):** Gereksiz özellikleri eleyerek karmaşıklığı azaltmak ve model performansını artırmak amacıyla Varyans Şişme Faktörü (VIF) gibi istatistiksel tekniklerin kullanılması.
4. **Model Eğitimi ve Değerlendirme:** Veri setinin Eğitim (Train) ve Test olarak ayrılması. Çeşitli algoritmaların eğitilmesi ve $R^2$ Score, MAE (Ortalama Mutlak Hata), MSE (Ortalama Kare Hata) gibi başarı metrikleriyle performanslarının kıyaslanması.

## 💻 Kurulum ve Çalıştırma

Projeyi kendi ortamınızda incelemek ve çalıştırmak isterseniz aşağıdaki adımları takip edebilirsiniz:

**1. Repoyu Klonlayın**
```bash
git clone https://github.com/tahayasincicek/Konut-Fiyat-Tahmini.git
cd Konut-Fiyat-Tahmini
```

**2. Gerekli Kütüphaneleri Yükleyin**
Sisteminizde ilgili kütüphaneler yoksa, `pip` kullanarak kurabilirsiniz:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm catboost statsmodels
```

**3. Projeyi Çalıştırın**
Jupyter Notebook ortamında ana dosyayı açarak tüm analizleri ve model eğitim adımlarını inceleyebilirsiniz:
```bash
jupyter notebook "ev_fiyat_tahmini (5).ipynb"
```
