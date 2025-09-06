# 🎮 Steam Game Price Prediction

Proyek ini bertujuan untuk menganalisis dan memprediksi harga gim di platform Steam menggunakan pendekatan regresi linier. Dataset yang digunakan berasal dari [Kaggle](https://www.kaggle.com/datasets), dan mencakup berbagai fitur seperti rating, jumlah ulasan, diskon, harga asli, dan dukungan platform.

## 📦 Dataset
- Jumlah data: 1108 gim
- Fitur utama:
  - `rating`
  - `#reviews`
  - `discount%`
  - `original_price_(€)`
  - `price_(€)`
  - `windows`, `linux`, `macos`

## 🔍 Exploratory Data Analysis (EDA)
- Korelasi antar fitur menggunakan heatmap
- Pairplot untuk melihat hubungan visual antar variabel
- Scatter plot untuk `rating` vs `price` dan `#reviews` vs `price` (log scale)
- Bar chart jumlah gim per platform

## 🧠 Modeling
- Algoritma: Linear Regression
- Split data: 80% training, 20% testing
- Fitur input: rating, reviews, diskon, harga asli, platform
- Target: `price_(€)`

## 📊 Evaluasi Model
| Metrik | Nilai |
|--------|-------|
| MSE    | 9.79  |
| RMSE   | 3.13  |
| MAE    | 2.29  |
| MAPE   | 29.06% |

Model menunjukkan performa yang cukup baik untuk prediksi harga gim pada rentang rendah hingga menengah. Kesalahan prediksi rata-rata sekitar €2–€3, dan MAPE masih dapat ditoleransi untuk data yang skewed ke kanan.

## 💡 Insight
- Harga akhir gim sangat dipengaruhi oleh harga original dan diskon.
- Fitur seperti rating dan jumlah ulasan tidak memiliki pengaruh signifikan terhadap harga.
- Platform rilis (Windows, Linux, MacOS) tidak konsisten memengaruhi harga.
- Distribusi harga gim skewed ke kanan → transformasi log dapat membantu stabilisasi model.

## 🚀 Pengembangan Selanjutnya
- Coba model non-linear seperti Random Forest atau Decision Tree
- Implementasi K-Fold Cross Validation untuk validasi yang lebih kuat
- Visualisasi residual dan segmentasi harga
- Transformasi log harga untuk mengurangi efek outlier

## 📬 Kontak
Jika Anda memiliki saran, kritik, atau ingin berdiskusi lebih lanjut, silakan hubungi saya melalui LinkedIn atau GitHub. Masukan yang membangun sangat saya apresiasi untuk pengembangan wawasan di bidang data science.

---

