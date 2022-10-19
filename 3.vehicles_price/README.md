

# Faktor Apakah yang Menjual Sebuah Mobil?

Sebagai seorang analis di Crankshaft List. Ratusan iklan kendaraan gratis ditayangkan di situs web Perusahaan setiap hari. Tim kami perlu mempelajari kumpulan data selama beberapa tahun terakhir dan menentukan faktor-faktor yang memengaruhi harga sebuah kendaraan.

## Goals

Dalam project ini kita akan befokus pada Exploratory Data Analysis dan Data Visualization yang akan dapat membantu kita dalam mengidentifikasi outlier dalam data, menemukan pola dalam data, dan memberikan insight baru. Visualisasi data juga membantu menyampaikan cerita dengan menggambarkan data ke dalam bentuk visual yang lebih mudah dipahami, dan menyoroti tren.

Studi ini untuk menjawab 5 hipostesis :
1. Apakah terdapat korelasi antara harga dengan usia kendaraan
2. Apakah terdapat korelasi antara harga dengan jarak tempuh kendaraan
3. Apakah terdapat korelasi antara harga dengan kondisi kendaraan
4. Apakah terdapat korelasi antara harga dengan warna kendaraan
5. Apakah terdapat korelasi antara harga dengan tipe transmisi kendaraan

## Kesimpulan Umum

Kita telah melakukan beberapa tahap dalam memproses data mobil untuk mendapatkan kesimpulan.

**A. Tahap Praproses**

Dari eksplorasi yang kita lakukan kita mendapatkan beberapa konsklusi:
1. Kita memulai dengan ukuran dataset sebanyak 51525 baris dan 13 kolom, ada 5 kolom yang terdapat missing value yaitu model_year, cylinders, odometer, paint_color, dan is_4wd.
2. Langkah-langkah yang kita lakukan berikutnya adalah mengisi nilai dari kolom-kolom yang terdapat missing value, memperbaiki tipe data, memperbaiki kualitas data, dan menambahkan beberapa kolom.

Penyebab nilai yang hilang, bisa diakibatkan karena human error atau memang tidak memiliki akses data yang cukup dengan kendaraan tersebut megingat beberapa kendaraan memiliki usia yang sangat tua bisa lebih dari seratus tahun

**B. Tahap Esksplorasi**

Setelah tahap prapemrosesan data kita melakukan beberapa ekplorasi:
1. Menetapkan batas outliers dari kolom harga, usia, dan odometer, dan membuat dataset baru dengan jumlah baris sebanyak 46169.
2. Kita juga memfilter untuk mendapatkan waktu iklan dengan rentang 1 - 150 hari.
3. Kita mendapati bahwa tipe mobil yang paling populer adalah sedan dan SUV.

**C. Konsklusi**

Dari eksplorasi yang kita lakukan kita mendapatkan beberapa konsklusi:
1. Harga mobil terhadap usia memiliki koneksi negatif meskipun nilainya tidak terlalu tinggi, artinya mobil yang lebih baru akan memiliki harga yang lebih tinggi.
2. Harga mobil dan rata-rata jarak memiliki korelasi yang sangat lemah.
3. Harga dan kondisi menunjukan korelasi yang rendah.
4. Mobil dengan warna hitam dan putih memiliki harga yang lebih tinggi dari warna lainnya.
5. Sedangkan tipe transmisi tidak selalu menunjukan bahwa mobil matic akan lebih mahal dari mobil manual.
