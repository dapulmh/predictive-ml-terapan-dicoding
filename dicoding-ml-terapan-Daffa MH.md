# Laporan Proyek Machine Learning - Daffa Maulana Haekal

# Prediksi Harga Rumah di Kawasan Menteng

## Latar Belakang
Kawasan Menteng di Jakarta Pusat merupakan area yang terkenal dengan nilai properti yang tinggi. Untuk mendukung pengambilan keputusan dalam jual-beli properti, proyek ini bertujuan untuk mengembangkan model prediksi harga rumah berdasarkan berbagai faktor seperti luas bangunan, luas tanah, jumlah kamar tidur, kamar mandi, dan kapasitas garasi.

## Business Understanding
Tujuan utama dari proyek ini adalah untuk menyediakan model prediksi harga rumah yang akurat bagi berbagai pemangku kepentingan, termasuk pengembang properti, agen real estate, dan calon pembeli. Model ini akan membantu dalam menentukan harga yang wajar berdasarkan karakteristik rumah.

## Problem Statement
Bagaimana cara memprediksi harga rumah di kawasan Menteng berdasarkan atribut-atribut seperti luas bangunan, luas tanah, jumlah kamar tidur, jumlah kamar mandi, dan kapasitas garasi?

## Goals
- Mengembangkan model prediktif yang akurat untuk memprediksi harga rumah di Menteng.
- Mengidentifikasi faktor-faktor kunci yang mempengaruhi harga rumah.
- Menyediakan wawasan untuk pengambilan keputusan terkait properti.

## Solution Statements
- Eksplorasi Data: Analisis eksplorasi untuk memahami distribusi harga dan hubungan antar-variabel.
- Data Preparation: Preprocessing data, termasuk penanganan missing values dan scaling.
- Modelling: Pengembangan dan evaluasi beberapa model machine learning.
- Evaluation: Mengevaluasi kinerja model menggunakan metrik seperti MAE, RMSE, dan R².

## Data Preparation
### Dataset
Dataset diambil dari Kaggle dan memiliki atribut berikut:

1. NO: Nomor data.
2. NAMA RUMAH: Nama atau title rumah.
3. HARGA: Harga rumah (dalam rupiah).
4. LB: Luas bangunan (m²).
5. LT: Luas tanah (m²).
6. KT: Jumlah kamar tidur.
7. KM: Jumlah kamar mandi.
8. GRS: Kapasitas garasi (jumlah mobil).

## Explaratory Data Analysis

### Univariate Data Analysis

![download](https://github.com/user-attachments/assets/9ed21535-b833-4e70-8496-6422ad91c3c5)


### Multivariate Data Analysis

![download](https://github.com/user-attachments/assets/b461cb1c-f172-47da-9390-9a92c91e0533)

## Preprocessing
- Missing Values: Penanganan data yang hilang dengan dengan menghilangkan data.
  Berdasarkan dataset tersebut 
- Scaling: Normalisasi atau standarisasi fitur numerik.
- Duplicate Values : Penanganan data yang duplikat dengan menghilangkan data.

## Modelling

Model yang Digunakan:
- Linear Regression: Untuk memprediksi harga berdasarkan hubungan linier.
- Random Forest: Untuk meningkatkan akurasi dengan mengurangi overfitting.
- Boosting Regressor:
- KNN :

## Evaluasi Model
Model dievaluasi menggunakan cross-validation dan metrik evaluasi seperti:

- Mean Absolute Error (MAE) : Mengukur rata-rata kesalahan absolut dari prediksi.
- Mean Squared Error (MSE) : Mengukur rata-rata kuadrat kesalahan dari prediksi.
- Root Mean Squared Error (RMSE) : Mengukur akar kuadrat dari rata-rata kesalahan kuadrat.
- R² Score : Mengukur seberapa baik model menjelaskan variabilitas dari data.

## Evaluations
Hasil dari model yang dipilih akan dibandingkan untuk menentukan model dengan performa terbaik. Analisis lebih lanjut akan dilakukan untuk memahami pengaruh masing-masing fitur terhadap harga rumah.


