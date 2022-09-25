# Menganalisis risiko peminjam gagal membayar

Sebagai kredit analyst proyek kami ialah menyiapkan laporan untuk bank bagian kredit. Kami mencari tahu pengaruh status perkawinan seorang nasabah dan jumlah anak terhadap probabilitas ketepatan waktu dalam melunasi pinjaman. Bank sudah memiliki beberapa data mengenai kelayakan kredit nasabah.

Laporan ini akan dipertimbangkan pada saat membuat penilaian kredit untuk calon nasabah. Penilaian kredit digunakan untuk mengevaluasi kemampuan calon peminjam untuk melunasi pinjaman mereka.

Tujuan utama dari poject ini adalah untuk mengetahui kelayakan seorang klien untuk mendapatkan kredit berdasarkan status dan keadaan mereka yang tersimpan dalam data kita. Kita juga menguji kapasitas nasabah berdasarkan karakteristik mereka yang kita rangkum berdasarkan kategori-kategori sehingga diperoleh pattern untuk memberikan lampu kuning kepada nasabah yang masuk ke dalam kategori tertentu.

Hipotesis project :

1. Apakah terdapat korelasi antara jumlah anak dengan kemampuan melunasi pinjaman tepat waktu?
2. Apakah terdapat korelasi antara status keluarga dengan kemampuan melunasi pinjaman tepat waktu?
3. Apakah terdapat korelasi antara kelas ekonomi dengan kemampuan melunasi pinjaman tepat waktu?
4. Apakah terdapat korelasi antara tujuan kredit dengan kemampuan melunasi pinjaman tepat waktu?

## Tahapan dalam project

### A. Ekplorasi data

1. Menampilkan sampel
2. Menghitung jumlah baris dan kolom
3. Memeriksa missing value
4. Memeriksa register
5. Memeriksa duplikat

### B. Transformasi Data

1. Memperbaiki register 
2. Memperbaiki value yang tidak wajar dari kolom-kolom
3. Menghapus duplikat

### C. Mengisi missing value

1. Membuat kategori berdasarkan rentang
2. Mengisi kolom-kolom dengan missing value dengan rata-rata berdasarkan range

### D. Mengkategorikan data

1. Mengkategorikan data kategorikal menjadi lebih umum
2. Mengkategorikan data numerikal menjadi range

### E. Memeriksa hipostesis

Memeriksa hipotesis yang telah kita tentukan

### 1. Korelasi antara jumlah anak dengan kemampuan melunasi pinjaman tepat waktu

1. Klien yang memliki 1 sampai 4 anak memiliki persentase yang hampir sama di angka 8% sampai 9%.
2. Klien yang memiliki 5 anak tidak memiliki hutang pembayaran pinjaman tatapi tidak bisa kita jadikan acuan karena jumlah data terlalu sedikit.
3. Klien yang tidak memilki anak memiliki rasio yang paling kecil untuk hutang pembayaran pinjaman sebesar 7% hal ini mungkin terjadi karena mereka memiliki tanggungan yang lebih sedikit dibandingkan dengan klien yang telah memilki anak.

Hal ini tentu akan memudahkan dalam pengambilan keputusan kita dalam memberikan kredit kepada klien yang belum memiliki anak karena kemampuan mereka dalam melunasi kredit mereka.

### 2. Korelasi antara status keluarga dengan kemampuan melunasi pinjaman tepat waktu

Ada beberapa hal menarik yang kita temukan disini:
1. Klien yang unmarried dan civil partnership memiliki persentase yang cukup tinggi sebesar 9%.
2. Klien yang divorced dan married memiliki rasio sebesar 7% yang artinya lebih kecil daripada klien yang belum menikah apakah karena mereka dapat menggabungkan penghasilan dengan pasangan mereka, hal ini tentu berbanding terbalik dengan pengujian sebelumnya bahwa klien yang belum memiliki anak memiliki persentase hutang lebih kecil mengingat seseorang yang telah menikah punya kecenderungan untuk memiliki anak.
3. Klien dengan status widow / widower memiliki pensentase hutang paling kecil sebesar 6%. Apakah kita akan mempertimbangkan status sebagai dasar dalam pengambilan keputusan?

### 3. Korelasi antara kelas ekonomi dengan kemampuan melunasi pinjaman tepat waktu

Beberapa hal yang kita temukan dari manipulasi data di atas diantaranya:
1. Klien dengan tingkat ekonomi lower middle class dan middle class memilki persentase yang seimbang yaitu sebesar 7% untuk klien yang memiliki hutang pembayaran kredit.
2. Klien dengan tingkat ekonomi poor memiliki kemungkinan untuk menunggak lebih besar yaitu 8%. Apakah ini dapat memengaruhi keputusan kita untuk tidak memberikan kredit mengingat jumlah mereka yang paling banyak.
3. Klien dengan pendapatan upper middle class yang memiliki risiko paling kecil sebesar 6%.

### 4. Korelasi antara tujuan kredit dengan kemampuan melunasi pinjaman tepat waktu

Berdasarkan penganganan yang kita lakukan hal-hal yang bisa kita dapatkan:
1. Klien yang melakukan pinjaman untuk keperluan car dan education memiliki risiko gagal bayar paling tinggi sebesar 9%.
2. Klien yang menggunakan pinjamannya untuk wedding memiliki persentase hutang pinjaman yang lebih rendah dibandigkan kriteria sebelumnya.
3. Klien yang membayar tepat waktu yaitu untuk kegunaan property dengan risiko hutang tak lancar sebesar 7%.

## Kesimpulan Umum

Kita telah melakukan proses cleansing data untuk memperbaiki data-data yang bermasalah dalam dataset kita. Pembersihan yang kita lakukan meliputi mengisi value yang hilang, menghapus nilai duplikat, memperbaiki register yang tak beraturan, nilai yang terlalu besar, hingga mengganti nilai yang tidak wajar, sehingga kita mendapati dataset yang dapat kita olah untuk proses analisa kredit.

Temuan yang kita dapatkan setelah melakukan beberapa eksplorasi kita mendapati bahwa terdapat korelasi antara jumlah anak dan status perkawinan dalam risiko pemayaran kredit, klien yang tidak memiliki anak akan lebih mudah dalam melunasi hutangnya dibandingkan dengan klien yang memiliki anak. Klien yang menikah atau pernah memiliki pasangan memiliki risiko lebih rendah gagal bayar daripada klien dengan status single maupun tinggal bersama. Klien yang memiliki penghasilan lebih rendah akan lebih tinggi untuk memiliki hutang pinjaman, dan klien yang menggunakan uangnya untuk keperluan rumah akan lebih besar persentase mereka untuk dapat melunasi hutangnya.

Tetapi apakah semua manipulasi data yang kita lakukan dapat kita gunakan dalam proses decision making sehingga akan meminimalisir risiko yang akan terjadi di kemudian hari?
