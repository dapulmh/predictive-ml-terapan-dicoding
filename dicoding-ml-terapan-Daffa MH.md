# Laporan Proyek Machine Learning - Daffa Maulana Haekal

# Prediksi Harga Rumah di Kawasan Menteng

## Domain
Kawasan Menteng di Jakarta Pusat merupakan area yang terkenal dengan nilai properti yang tinggi. Untuk mendukung pengambilan keputusan dalam jual-beli properti, proyek ini bertujuan untuk mengembangkan model prediksi harga rumah berdasarkan berbagai faktor seperti luas bangunan, luas tanah, jumlah kamar tidur, kamar mandi, dan kapasitas garasi.

## Business Understanding
Tujuan utama dari proyek ini adalah untuk menyediakan model prediksi harga rumah yang akurat bagi berbagai pemangku kepentingan, termasuk pengembang properti, agen real estate, dan calon pembeli. Model ini akan membantu dalam menentukan harga yang wajar berdasarkan karakteristik rumah.

## Problem Statement
1. Bagaimana cara memprediksi harga rumah di kawasan Menteng berdasarkan atribut-atribut seperti luas bangunan, luas tanah, jumlah kamar tidur, jumlah kamar mandi, dan kapasitas garasi?
2. Apa hubungan tiap atribut dan pengaruhnya terhadap harga properti di kawasan menteng ?
   
## Goals
- Mengembangkan model prediktif yang akurat untuk memprediksi harga rumah di Menteng.
- Mengidentifikasi faktor-faktor kunci yang mempengaruhi harga rumah.

## Solution Statements
- Eksplorasi Data: Analisis eksplorasi untuk memahami distribusi harga dan hubungan antar-variabel.
- Data Preparation: Preprocessing data, termasuk penanganan missing values dan scaling.
- Model Development: Pengembangan dan evaluasi beberapa model machine learning. Model Machine Learning yang digunakan dalam proyek ini yaitu Linear Regression, Boosting Algorithm, Random Forest Algorithm, dan KNN. Keempat model tersebut dicari nilai evaluasi yang paling baik untuk memprediksi harga rumah di menteng.
- Evaluation: Mengevaluasi kinerja model menggunakan metrik seperti MAE, RMSE, dan R².

## Data Understanding
Dataset diambil dari Kaggle dan memiliki atribut berikut:

1. NO: Nomor data.
2. NAMA RUMAH: Nama atau title rumah.
3. HARGA: Harga rumah (dalam rupiah).
4. LB: Luas bangunan (m²).
5. LT: Luas tanah (m²).
6. KT: Jumlah kamar tidur.
8. KM: Jumlah kamar mandi.
9. GRS: Kapasitas garasi (jumlah mobil).

Link Dataset : https://www.kaggle.com/datasets/wisnuanggara/daftar-harga-rumah

Kondisi Dataset:
- Kondisi dataset tidak memilki Null Value
- Kondisi dataset Memiliki outlier akan tetapi penghilangan outlier mempengaruhi hasil evaluasi model sehingga tidak dihilangkan
- Kondisi dataset tidak memilki duplicate Value
- Terdapat atribut yang unik sehingga mengurangi hasil evaluasi model sehingga lebih baik dihilangkan seperti atribut NO dan NAMA RUMAH

Hal ini yang membuat fitur-fitur dalam dataset menjadi:
1. HARGA: Harga rumah (dalam rupiah).
2. LB: Luas bangunan (m²).
3. LT: Luas tanah (m²).
4. KT: Jumlah kamar tidur.
5. KM: Jumlah kamar mandi.
6. GRS: Kapasitas garasi (jumlah mobil).

Setelah dilakukan cleaning dan feature engineering maka dataset memiliki 1010 baris data dan 6 kolom atribut yang digunakan

## Explaratory Data Analysis

### Univariate Data Analysis

![download](https://github.com/user-attachments/assets/9ed21535-b833-4e70-8496-6422ad91c3c5)


### Multivariate Data Analysis

![download](https://github.com/user-attachments/assets/b461cb1c-f172-47da-9390-9a92c91e0533)

![download](https://github.com/user-attachments/assets/1325ce56-5b8c-4fa7-9acc-3a5827be26c1)

Bisa dilihat berdasarkan gambar atribut yang paling mempengaruhi tinggi rendahnya harga adalah LT (luas tanah)

## Data Preparation
- Missing Values: Penanganan data yang hilang dengan dengan menghilangkan data.

Berdasarkan data yang diperoleh tidak terdapat missing value sehingga tidak perlu diatasi

- Scaling: Normalisasi atau standarisasi fitur numerik.

Standarisasi digunakan untuk menormalisasi data sehingga meningkatkan akurasi model
- Duplicate Values : Penanganan data yang duplikat dengan menghilangkan data.
  
Berdasarkan data yang diperoleh tidak terdapat duplicate value sehingga tidak perlu diatasi
- Penanganan Outlier : Penanganan data yang terlalu ekstrem.
  
Berdasarkan evaluasi data, penghilangan outlier malah mengurangi akurasi data sehingga tidak saya hilangkan

- Melakukan train test split dimana memisahkan data yang akan digunakan untuk training dengan data yang akan digunakan untuk test
  
## Model Development

Model yang Digunakan:
- Linear Regression: model machine learning statistik yang digunakan untuk memprediksi nilai dari variabel dependen (target) berdasarkan satu atau lebih variabel independen (fitur)

### Cara Kerja
1. **Model Linear**: 
   - Asumsi bahwa ada hubungan linear antara input (X) dan output (Y), dalam bentuk persamaan:
     \[
     Y = b_0 + b_1X_1 + b_2X_2 + ... + b_nX_n
     \]
2. **Fitting Model**:
   - Menyesuaikan parameter (koefisien) \( b_0, b_1, \dots, b_n \) menggunakan metode **Least Squares**, yang meminimalkan jumlah kuadrat dari perbedaan antara nilai aktual dan nilai yang diprediksi.
3. **Prediksi**:
   - Prediksi dilakukan dengan memasukkan nilai input ke dalam persamaan linear yang telah dibentuk.

- Random Forest: model ensemble yang menggabungkan banyak decision tree untuk meningkatkan akurasi dan mengurangi overfitting.

### Cara Kerja
1. **Pembuatan Forest**:
   - Membangun banyak decision tree selama pelatihan, di mana setiap tree dilatih menggunakan subset acak dari data dan subset acak dari fitur.
2. **Bagging**:
   - Menggunakan teknik **bagging** (Bootstrap Aggregating) untuk membuat dataset acak dari data asli dengan pengambilan sampel acak dengan penggantian.
3. **Voting atau Rata-rata**:
   - Untuk klasifikasi, Random Forest melakukan voting mayoritas dari semua decision tree. Untuk regresi, diambil rata-rata dari semua prediksi.

Dalam pengembangannya model random forest dikonfigurasikan parameternya menggunakan gridsearch cv sehingga model random forest dikonfigurasikan dengan parameter yang menghasilkan hasil evaluasi terbaik. Parameter tersebut yaitu:

{'bootstrap': True, 'max_depth': 10, 'n_estimators': 100}

- Boosting Regressor: Teknik ensemble yang menggabungkan beberapa model lemah (biasanya decision tree kecil) secara bertahap untuk membentuk model yang kuat.

### Cara Kerja
1. **Training Iteratif**:
   - Melatih model secara bertahap, di mana setiap model baru mencoba untuk memperbaiki kesalahan dari model sebelumnya.
2. **Pemberian Bobot**:
   - Data yang sulit diprediksi diberi bobot lebih tinggi sehingga model berikutnya lebih fokus pada data tersebut.
3. **Agregasi**:
   - Model akhir adalah kombinasi dari semua model yang dilatih, di mana prediksi diambil dengan menggabungkan prediksi dari masing-masing model.
  
Dalam pengembangannya model Boosting regression dikonfigurasikan parameternya menggunakan gridsearch cv sehingga model Boosting regression dikonfigurasikan dengan parameter yang menghasilkan hasil evaluasi terbaik. Parameter tersebut yaitu:

{'learning_rate': 0.1, 'max_depth': 3, 'n_estimators': 200, 'subsample': 0.8}
   
- KNN : algoritma non-parametrik yang digunakan untuk klasifikasi dan regresi. Dalam KNN, prediksi dibuat berdasarkan rata-rata atau mayoritas suara dari k tetangga terdekat dalam ruang fitur.

### Cara Kerja
1. **Jarak **:
   - Menghitung jarak antara data baru dan semua data dalam dataset pelatihan menggunakan suatu metode jarak.
2. **Pemilihan Tetangga Terdekat**:
   - Memilih K data terdekat dari dataset pelatihan.
3. **Voting atau Rata-rata**:
   - Untuk klasifikasi, data baru diklasifikasikan ke dalam kelas yang paling umum di antara K tetangga terdekat (voting mayoritas). Untuk regresi, nilai prediksi dihitung sebagai rata-rata dari nilai-nilai tetangga terdekat.

Dalam pengembangannya model KNN dikonfigurasikan parameternya menggunakan gridsearch cv sehingga model KNN dikonfigurasikan dengan parameter yang menghasilkan hasil evaluasi terbaik. Parameter tersebut yaitu:

{'metric': 'manhattan', 'n_neighbors': 7}
     
Keempat model tersebut dieksperimenkan untuk dilakukan training dan dilihat evaluasi model mana yang memiliki hasil terbaik, baik untuk hasil training maupun validation. Saya juga melakukan gridsearch untuk menemukan parameter terbaik untuk setiap model sehingga mendapatkan akurasi yang maksimal untuk setiap modelnya.

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

![download](https://github.com/user-attachments/assets/42154ce3-0ec6-47bf-874e-fa6321aad419)

 Jawaban dari Problem Statement: 
1. Bisa dilihat secara umum model Boosting Regressor lebih menghasilkan prediksi yang lebih baik dibandingkan model lainnya. Hal ini yang membuat kita dapat memakai model boosting regression untuk memprediksi harga properti di menteng. Akan tetapi hasil evaluasi model masih dapat ditingkatkan.
2. Lalu untuk atribut-atribut yang sangat mempengaruhi harga properti di kawasan menteng adalah LT (luas tan nah) dan LB (luas bangunan)  




