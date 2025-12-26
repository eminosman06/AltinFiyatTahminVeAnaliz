
# 📈 Altın Fiyat Tahmini ve Analizi (Gold Price Prediction & Analysis)

Bu proje, altın fiyatlarının tarihsel verileri kullanılarak hem klasik makine öğrenmesi yöntemleri hem de derin öğrenme (LSTM) ile fiyat tahmini yapılmasını amaçlamaktadır. Projede veri ön işleme, görselleştirme, zaman serisi analizi ve farklı regresyon modellerinin karşılaştırılması yer almaktadır.

## ⚠️ Önemli Nokta: Bu proje Mayıs 2024 tarihinde Makine Öğrenmesi dersi dönem projesi olarak yapılmış olup projede derste işlenen makine öğrenmesi metotlarının uygulanması zorunlu tutulmuştur. Projede altın fiyat analizinde ya da tahmininde yani zaman serisi sorununda kullanılmayan KNN, SVM, Random Forest gibi algoritmalara da yer verilmiş ancak projede anlamsızlıkları da sunum esnasında anlatılmıştır. Tüm bunlara ek olarak derste işlenmeyen ve Derin Öğrenme algoritması olan LSTM algoritması bu projede kullanıldığı için ciddi puan kırıldığından dersten kaldım. Bu projeye forklayacağım ikinci proje yine bu projenin aynısı olsa da ders için ideal haldedir.

## 📌 Çalışma, Jupyter Notebook / Google Colab ortamında geliştirilmiştir.

## 📊 Kullanılan Veri Seti

Veri seti goldstock.csv dosyasında yer almakta olup aşağıdaki sütunları içermektedir:

Sütun	Açıklama
Date	Tarih
Open	Açılış fiyatı
High	Gün içi en yüksek fiyat
Low	Gün içi en düşük fiyat
Close	Kapanış fiyatı (hedef değişken)
Volume	İşlem hacmi

## 📌 Hedef değişken: Close (Kapanış Fiyatı)

## ⚙️ Kullanılan Kütüphaneler
pip install pandas numpy matplotlib seaborn plotly scikit-learn tensorflow keras mplfinance


## Projede kullanılan başlıca teknolojiler:

Pandas / NumPy – Veri işleme

Matplotlib / Seaborn / Plotly / mplfinance – Görselleştirme

Scikit-learn – Regresyon modelleri

TensorFlow / Keras – LSTM tabanlı derin öğrenme modeli

## 🔎 Proje Aşamaları
## 1️⃣ Veri Ön İşleme

Eksik veri kontrolü

Tarih (Date) kolonunun datetime formatına dönüştürülmesi

Zaman sıralamasına göre düzenleme

Normalizasyon (MinMaxScaler)

## 2️⃣ Veri Görselleştirme

Candlestick (Mum Grafik) – mplfinance

Zaman serisi çizgi grafikleri

Eğitim / test veri ayrımının görselleştirilmesi

## 📊 Amaç: Altın fiyatlarının zaman içindeki trend ve dalgalanmalarını gözlemlemek

## 3️⃣ LSTM ile Zaman Serisi Tahmini (Derin Öğrenme)

🔹 Pencere Boyutu (Window Size): 60 gün
🔹 Test Seti: 2023 yılı (250 gün)

## Model Mimarisi:

3 adet LSTM katmanı (64 nöron)

Dropout katmanları (overfitting önleme)

Dense katmanlar

Optimizer: Nadam

## Kayıp fonksiyonu: Mean Squared Error (MSE)

Input → LSTM → Dropout → LSTM → Dropout → LSTM → Dense → Output

## 📈 LSTM Model Sonuçları
Metrik	Değer
Test Loss (MSE)	0.00094
MAPE	%2.8
Accuracy	%97.19

📌 Gerçek test verisi ile tahmin edilen değerler grafik üzerinde karşılaştırılmıştır.

## 4️⃣ Klasik Makine Öğrenmesi Modelleri

LSTM dışında karşılaştırma amacıyla aşağıdaki modeller de uygulanmıştır:

✔ Linear Regression
✔ Polynomial Regression (Degree = 2)
✔ Lasso Regression
✔ Ridge Regression

## Bu modeller:

Open, High, Low, Volume → Close tahmini için kullanılmıştır.

Gerçek vs tahmin edilen değerler scatter plot ile görselleştirilmiştir.

## 📊 Model Karşılaştırması
Model	Kullanım Amacı
Linear Regression	Baseline model
Polynomial Regression	Non-lineer ilişki yakalama
Lasso / Ridge	Regularization etkisi
LSTM	Zaman serisi bağımlılığını öğrenme

## 📌 En başarılı sonuç LSTM modeli ile elde edilmiştir.

## 🚀 Nasıl Çalıştırılır?
Google Colab

Notebook’u aç

Gerekli kütüphaneleri yükle

goldstock.csv dosyasını yükle

Hücreleri sırayla çalıştır

Lokal Ortam
git clone https://github.com/eminosman06/AltinFiyatTahminVeAnaliz.git
cd AltinFiyatTahminVeAnaliz
jupyter notebook

## 🧠 Geliştirme Önerileri

🔹 ARIMA / SARIMA / Prophet eklenebilir

🔹 Makroekonomik veriler entegre edilebilir

🔹 Çok değişkenli LSTM (multivariate)

🔹 Gerçek zamanlı veri (API) ile canlı tahmin

🔹 Model karşılaştırma tablosu (RMSE, R²)

## ⚠️ Uyarı

Bu proje akademik ve deneysel amaçlıdır.
Yatırım tavsiyesi değildir.

## 👤 Geliştirici

Emin Osman Toprak
Computer Engineering | Data Science & AI | Cybersecurity
