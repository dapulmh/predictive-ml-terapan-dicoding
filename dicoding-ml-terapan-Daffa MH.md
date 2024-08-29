# Laporan Proyek Machine Learning - Daffa Maulana Haekal

# Prediksi Harga Rumah di Kawasan Menteng

## Latar Belakang
Kawasan Menteng di Jakarta Pusat merupakan area yang terkenal dengan nilai properti yang tinggi. Untuk mendukung pengambilan keputusan dalam jual-beli properti, proyek ini bertujuan untuk mengembangkan model prediksi harga rumah berdasarkan berbagai faktor seperti luas bangunan, luas tanah, jumlah kamar tidur, kamar mandi, dan kapasitas garasi.

## Business Understanding
Tujuan utama dari proyek ini adalah untuk menyediakan model prediksi harga rumah yang akurat bagi berbagai pemangku kepentingan, termasuk pengembang properti, agen real estate, dan calon pembeli. Model ini akan membantu dalam menentukan harga yang wajar berdasarkan karakteristik rumah.

## Problem Statement
1. Bagaimana cara memprediksi harga rumah di kawasan Menteng berdasarkan atribut-atribut seperti luas bangunan, luas tanah, jumlah kamar tidur, jumlah kamar mandi, dan kapasitas garasi?
2. Apa hubungan tiap atribut dan pengaruhnya terhadap harga properti di kawasan menteng ?
   
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

![download](https://github.com/user-attachments/assets/1325ce56-5b8c-4fa7-9acc-3a5827be26c1)

## Preprocessing
- Missing Values: Penanganan data yang hilang dengan dengan menghilangkan data.

Berdasarkan data yang diperoleh tidak terdapat missing value sehingga tidak perlu diatasi

- Scaling: Normalisasi atau standarisasi fitur numerik.

Standarisasi digunakan untuk menormalisasi data sehingga meningkatkan akurasi model
- Duplicate Values : Penanganan data yang duplikat dengan menghilangkan data.
  
Berdasarkan data yang diperoleh tidak terdapat duplicate value sehingga tidak perlu diatasi
- Penanganan Outlier : Penanganan data yang terlalu ekstrem.
  
Berdasarkan evaluasi data, penghilangan outlier malah mengurangi akurasi data sehingga tidak saya hilangkan

## Modelling

Model yang Digunakan:
- Linear Regression: model machine learning statistik yang digunakan untuk memprediksi nilai dari variabel dependen (target) berdasarkan satu atau lebih variabel independen (fitur)
- Random Forest: model ensemble yang menggabungkan banyak decision tree untuk meningkatkan akurasi dan mengurangi overfitting.
- Boosting Regressor: Teknik ensemble yang menggabungkan beberapa model lemah (biasanya decision tree kecil) secara bertahap untuk membentuk model yang kuat. 
- KNN : algoritma non-parametrik yang digunakan untuk klasifikasi dan regresi. Dalam KNN, prediksi dibuat berdasarkan rata-rata atau mayoritas suara dari k tetangga terdekat dalam ruang fitur.

Keempat model tersebut dieksperimenkan untuk dilakukan training dan dilihat evaluasi model mana yang memiliki hasil terbaik, baik untuk hasil training maupun validation.

## Evaluasi Model
Model dievaluasi menggunakan cross-validation dan metrik evaluasi seperti:

- Mean Absolute Error (MAE) : Mengukur rata-rata kesalahan absolut dari prediksi.
- Mean Squared Error (MSE) : Mengukur rata-rata kuadrat kesalahan dari prediksi.
- Root Mean Squared Error (RMSE) : Mengukur akar kuadrat dari rata-rata kesalahan kuadrat.
- R² Score : Mengukur seberapa baik model menjelaskan variabilitas dari data.
  
1. Hasil Evaluasi Linear Regression

![Screenshot 2024-08-29 223608](https://github.com/user-attachments/assets/c97d7300-0ea6-4472-b127-caf0624d4607)

2. Hasil Evaluasi Random Forest
   
![Screenshot 2024-08-29 223435](https://github.com/user-attachments/assets/41582a3d-1a8d-4af6-b8c2-70c6e0ba1de5)

3. Hasil Evaluasi Boosting Regressor
   
![Screenshot 2024-08-29 223619](https://github.com/user-attachments/assets/3bffa54e-fb21-4183-bf7e-18b6249667ba)

4. Hasil Evaluasi KNN

![Screenshot 2024-08-29 223445](https://github.com/user-attachments/assets/7753bbe5-5041-41f0-b8ba-eda2db268dd7)

### Evaluasi Model Secara Umum
Hasil dari model yang dipilih akan dibandingkan untuk menentukan model dengan performa terbaik. Analisis lebih lanjut akan dilakukan untuk memahami pengaruh masing-masing fitur terhadap harga rumah.

![Screenshot 2024-08-29 223559](https://github.com/user-attachments/assets/1cfcdb13-f6f6-4e14-97e7-dd4497438bc9)

Bisa dilihat secara umum model Boosting Regressor lebih menghasilkan prediksi yang lebih baik dibandingkan model lainnya

![download](https://github.com/user-attachments/assets/42154ce3-0ec6-47bf-874e-fa6321aad419)


