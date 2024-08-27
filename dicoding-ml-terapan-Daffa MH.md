# Laporan Proyek Machine Learning - Daffa Maulana Haekal

## Domain Proyek

### Latar Belakang

Dalam dunia yang semakin kompetitif, baik perusahaan maupun karyawan sangat membutuhkan informasi yang akurat mengenai standar gaji. Bagi perusahaan, prediksi gaji yang akurat membantu mereka dalam merancang paket kompensasi yang kompetitif untuk menarik dan mempertahankan talenta terbaik. Bagi karyawan, pemahaman mengenai gaji yang sesuai dengan keahlian dan pengalaman mereka dapat membantu dalam negosiasi gaji dan perencanaan karier.

## Business Understanding

Dalam konteks bisnis, prediksi gaji memainkan peran penting dalam berbagai aspek operasional dan strategis. Perusahaan, khususnya dalam sektor perekrutan, sangat bergantung pada data gaji untuk menawarkan kompensasi yang kompetitif dan adil kepada calon karyawan. Sebuah prediksi gaji yang akurat membantu perusahaan dalam menetapkan anggaran gaji, merancang struktur kompensasi yang menarik, dan meminimalkan risiko kehilangan talenta potensial akibat penawaran yang kurang kompetitif.

Di sisi lain, karyawan dan pencari kerja juga sangat diuntungkan dengan adanya model prediksi gaji yang dapat diandalkan. Dengan mengetahui estimasi gaji berdasarkan profil mereka, mereka dapat lebih percaya diri dalam melakukan negosiasi gaji dan mengambil keputusan karier yang lebih baik.

### Problem Statements

Permasalahan utama yang ingin diselesaikan dalam proyek ini adalah:

- Bagaimana kita dapat memprediksi gaji seseorang secara akurat berdasarkan umur dari pelamar ?
- Seberapa efektif model machine learning dalam memprediksi gaji dibandingkan dengan metode tradisional?

### Goals

Tujuan dari diadakannya proyek ini diantara lain:
- Mengembangkan model prediksi gaji menggunakan algoritma machine learning.
- Menguji akurasi model dan membandingkan kinerjanya dengan berbagai metode.
- Menghasilkan wawasan yang dapat membantu perekrut dan karyawan dalam pengambilan keputusan terkait gaji.

Proyek ini akan memberikan kontribusi penting dalam pemahaman tentang bagaimana berbagai faktor mempengaruhi gaji, serta menyediakan alat yang berguna untuk prediksi gaji yang akurat dan berbasis data.

### Solution statements
Tujuan utama proyek ini adalah mengembangkan model prediktif yang akurat untuk memperkirakan gaji seseorang berdasarkan faktor-faktor seperti umur.

Solusi yang diusulkan mencakup:

1. Pengembangan Model Machine Learning:
- Menggunakan algoritma regresi (misalnya, Linear Regression, Random Forest, atau Gradient Boosting) untuk membangun model prediksi gaji.
- Melakukan eksperimen dengan berbagai algoritma dan teknik untuk menentukan model yang paling akurat.
  
2. Evaluasi Model:
- Menggunakan metrik evaluasi seperti Mean Absolute Error (MAE), Root Mean Square Error (RMSE), dan R-squared (R²) untuk mengukur kinerja model.
- Melakukan cross-validation untuk memastikan generalisasi model pada data yang tidak terlihat (unseen data).
  
3. Optimalisasi Model:

- Melakukan tuning hyperparameter menggunakan gridsearch untuk meningkatkan akurasi model.
- Menerapkan teknik feature engineering untuk menciptakan fitur-fitur baru yang mungkin lebih berkaitan dengan gaji.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- id : id dari data tersebut
- yearsExperience : Umur pengalaman kerja
- salary : Pendapatan yang didapat


## Data Preparation
Data preparation adalah langkah penting yang memastikan data yang digunakan dalam pembangunan model memiliki kualitas tinggi dan relevan. Beberapa langkah dalam data preparation meliputi:

1. Cleaning the Data:

- Mengatasi missing values: Mengisi atau menghapus data yang hilang (missing data) menggunakan teknik seperti imputasi rata-rata, median, atau metode lainnya.
- Menangani outliers: Mempertimbangkan strategi untuk menangani outliers yang dapat mencakup penghapusan atau transformasi data.

2. Feature Engineering:
Scaling and normalization: Menerapkan teknik scaling (misalnya, Standardization atau Min-Max Scaling) pada variabel numerik agar semua fitur berada dalam skala yang sama, sehingga model tidak bias terhadap fitur tertentu.

3. Splitting the Dataset:
- Membagi dataset menjadi set pelatihan (training set) dan set pengujian (testing set) untuk memastikan model yang dibangun dapat melakukan generalisasi pada data yang belum pernah dilihat sebelumnya.
- Memastikan distribusi variabel penting seperti gaji merata di kedua subset untuk mencegah bias.
- Dengan persiapan data yang matang dan pemilihan solusi yang tepat, proyek ini diharapkan dapat menghasilkan model prediksi gaji yang tidak hanya akurat tetapi juga dapat diandalkan dan aplikatif dalam berbagai konteks bisnis.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
