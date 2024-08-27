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
- Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
- Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

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
