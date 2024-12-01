# Capstone-Project-3 Prediksi Harga Mobil Bekas Syarah.com
Saudi Arabia Used car price prediction

## Introduction

Proyek ini bertujuan untuk memprediksi harga jual mobil bekas yang terdaftar di Syarah.com menggunakan model pembelajaran mesin. Dataset berisi berbagai fitur terkait mobil, seperti merek, model, tahun, jarak tempuh, dan lainnya. Tujuannya adalah mengembangkan model yang dapat memprediksi harga dengan akurat berdasarkan fitur-fitur tersebut.

## Daftar Isi

1. [Business Problem Understanding](#Business-Problem-Understanding)
2. [Data Understanding](#Data-Understanding)
3. [Data Pre-Processing](#Data-Pre-Processing)
4. [Modelling](#Modelling)
5. [Evaluation](#Evaluation)
6. [Conclusion](#Conclusion)
7. [Recommendation](#Recommendation)

## Business Problem Understanding

### Context

Syarah adalah platform e-commerce terkemuka di Arab Saudi yang berfokus pada penjualan mobil baru dan bekas. Didirikan pada tahun 2015 dan berkantor pusat di Riyadh, Syarah telah menjadi pusat transaksi otomotif yang signifikan di wilayah tersebut. Platform ini menawarkan proses yang ramah pengguna untuk menjual mobil bekas, di mana pengguna dapat mendapatkan perkiraan harga dengan memasukkan spesifikasi mobil.

### Problem Statement

Syarah menghadapi tantangan dalam menentukan harga jual mobil bekas dengan cepat dan akurat berdasarkan spesifikasi yang dimasukkan oleh penjual potensial. Tanpa perkiraan harga yang akurat, ada risiko menetapkan harga terlalu tinggi atau terlalu rendah, yang dapat mempengaruhi penjualan dan kepercayaan pelanggan.

### Goals

1. Mengembangkan model pembelajaran mesin untuk memprediksi harga mobil bekas dengan:
    - MAE (Mean Absolute Error) kurang dari 9.500 SAR.
    - MAPE (Mean Absolute Percentage Error) kurang dari 20%.
    - R-Squared lebih dari 0,85.
2. Mengintegrasikan model ke dalam situs web Syarah.com untuk estimasi harga secara real-time.
3. Meningkatkan volume transaksi di Syarah.com setelah mengimplementasikan model.

### Evaluation Metrics

Model dievaluasi menggunakan metrik berikut:
- **Mean Absolute Error (MAE)**
- **Mean Absolute Percentage Error (MAPE)**
- **R-Squared (R²)**

## Data Understanding

### Dataset

Dataset berisi 5624 catatan mobil bekas yang dikumpulkan dari Syarah.com. Setiap catatan mencakup informasi seperti nama merek, model, tahun pembuatan, asal, opsi, kapasitas mesin, jenis transmisi, jarak tempuh, wilayah, harga, dan status negosiasi.

### Feature

- **Type**: Nama model mobil.
- **Region**: Wilayah tempat mobil dijual.
- **Make**: Produsen mobil.
- **Gear_Type**: Jenis transmisi (manual atau otomatis).
- **Origin**: Asal mobil (lokal atau impor).
- **Options**: Fitur tambahan mobil.
- **Year**: Tahun pembuatan mobil.
- **Engine_Size**: Kapasitas mesin mobil.
- **Mileage**: Jarak tempuh mobil.
- **Negotiable**: Menunjukkan apakah harga dapat dinegosiasikan.
- **Price**: Harga jual mobil.

## Data Preprocessing

### Langkah-langkah

1. **Menangani Missing Value**: Tidak ditemukan nilai hilang dalam dataset.
2. **Menghapus Duplicate**: Baris duplikat diidentifikasi dan dihapus.
3. **Menangani Outlier**: Outlier pada kolom `Price`, `Year`, dan `Mileage` diidentifikasi dan ditangani menggunakan teknik capping.
4. **Feature Engineering**: Agregasi kategori langka, encoding variabel kategorikal, dan skala fitur numerik.
5. **Feature Selection**: Menghapus fitur yang tidak relevan dan melakukan uji statistik untuk mengidentifikasi fitur yang signifikan.

## Modelling

### Model yang Digunakan

- Linear Regression
- KNN Regression
- Decision Tree Regressor
- Random Forest Regressor
- XGBoost Regressor
- LightGBM Regressor
- Ridge Regression
- Lasso Regression
- Huber Regressor
- Quantile Regressor
- Support Vector Regression (SVR)
- AdaBoost Regressor

### Model Terbaik

Model dengan kinerja terbaik adalah XGBoost Regressor, yang mencapai metrik berikut:
- **MAE**: 9216.23
- **MAPE**: 0.167
- **R-Squared**: 0.874

## Conclusion

XGBoost Regressor diidentifikasi sebagai model terbaik untuk memprediksi harga mobil bekas di Syarah.com. Model ini diintegrasikan ke dalam situs web untuk memberikan estimasi harga secara real-time kepada pengguna.

## Recommendation

1. Secara rutin memperbarui model dengan data baru untuk menjaga akurasi.
2. Memantau kinerja model dan melatih ulang secara berkala.
3. Mengeksplorasi fitur tambahan dan teknik pemodelan lanjutan untuk meningkatkan akurasi lebih lanjut.

## How to Use

1. Clone repository.
2. Instal dependensi yang diperlukan.
3. Jalankan notebook Jupyter untuk pra-pemrosesan data, melatih model, dan mengevaluasi kinerjanya.
4. Gunakan model terbaik untuk memprediksi harga mobil bekas.

## Dependensi

- pandas
- numpy
- matplotlib
- seaborn
- missingno
- statsmodels
- category_encoders
- scikit-learn
- xgboost
- lightgbm
- shap
- plotly

## Lisensi

Proyek ini dilisensikan di bawah Lisensi MIT.
