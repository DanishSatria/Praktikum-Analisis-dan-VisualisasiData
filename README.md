# Praktikum-Analisis-dan-VisualisasiData
Analisis Performa Penjualan E-Commerce
Anggota
Danish Satria
Business Question

Praktikum ini bertujuan menjawab beberapa pertanyaan bisnis berikut:

Produk apa yang memiliki harga tinggi tetapi volume penjualan rendah (underperformer)?
Siapa pelanggan terbaik berdasarkan metode RFM (Recency, Frequency, Monetary)?
Kategori produk mana yang paling efisien terhadap biaya iklan?
Apakah peningkatan anggaran iklan berpengaruh terhadap peningkatan penjualan?
Data Wrangling

Tahapan pembersihan data yang dilakukan:

Memeriksa struktur data menggunakan df.info().
Memeriksa missing value menggunakan df.isnull().sum().
Mengubah kolom Order_Date menjadi format datetime.
Menghapus atau menangani data kosong pada kolom Total_Sales.
Hasil Pemeriksaan Missing Value
Kolom	Missing Value
Total_Sales	7

Data terdiri dari 150 transaksi dengan 8 kolom utama.

Analisis 1 - Produk Underperformer
Tujuan

Mencari produk dengan harga tinggi namun memiliki jumlah penjualan rendah.

Hasil

Rata-rata harga produk:

Price_Per_Unit = Rp1.024.640

Contoh produk yang termasuk kategori underperformer:

Kategori	Harga	Quantity
Gadget	1.431.000	1
Books	1.654.000	1
Gadget	1.992.000	1
Home Decor	1.853.000	1
Fashion	1.399.000	1
Insight

Beberapa produk memiliki harga jauh di atas rata-rata tetapi hanya terjual satu kali. Produk-produk tersebut berpotensi memperlambat perputaran stok dan perlu dievaluasi kembali strategi pemasarannya.

Analisis 2 - Segmentasi Pelanggan (RFM Analysis)
Tujuan

Mengidentifikasi pelanggan yang memberikan kontribusi terbesar terhadap penjualan.

Top Customer
CustomerID	Frequency	Monetary
5015	6	Rp26.309.000
5008	6	Rp22.350.000
5035	6	Rp22.066.000
5014	6	Rp20.797.000
5044	7	Rp20.631.000
Insight

Customer 5015 merupakan pelanggan dengan total transaksi terbesar sehingga dapat dimasukkan ke dalam kategori pelanggan loyal dan layak mendapatkan program promosi khusus.

Analisis 3 - Efisiensi Kategori Produk
Tujuan

Mengukur efektivitas biaya iklan terhadap pendapatan yang dihasilkan.

Hasil
Kategori	Efficiency Ratio
Gadget	0.92
Home Decor	1.07
Fashion	1.17
Books	1.20
Electronics	1.44
Insight

Kategori Electronics merupakan kategori paling efisien karena menghasilkan pendapatan paling besar dibandingkan biaya iklan yang dikeluarkan.

Sebaliknya, kategori Gadget memiliki efisiensi paling rendah sehingga perlu evaluasi strategi pemasaran.

Analisis 4 - Pengaruh Iklan terhadap Penjualan
Regresi Linear

Output program:

Koefisien Iklan : 0.1842
R² Score : -0.1956
Insight
Nilai koefisien positif menunjukkan bahwa peningkatan anggaran iklan masih memiliki hubungan positif terhadap penjualan.
Namun nilai R² yang negatif menunjukkan bahwa model regresi sederhana belum mampu menjelaskan variasi penjualan dengan baik.
Hal ini mengindikasikan bahwa faktor lain selain iklan kemungkinan memiliki pengaruh yang lebih besar terhadap penjualan.
Kesimpulan

Berdasarkan analisis yang dilakukan:

Ditemukan beberapa produk dengan harga tinggi namun penjualan rendah.
CustomerID 5015 merupakan pelanggan dengan kontribusi penjualan terbesar.
Kategori Electronics memiliki efisiensi iklan terbaik.
Anggaran iklan memiliki hubungan positif terhadap penjualan, namun bukan satu-satunya faktor yang memengaruhi performa penjualan.
Rekomendasi
Evaluasi harga produk underperformer.
Berikan program loyalitas kepada pelanggan terbaik.
Tingkatkan fokus promosi pada kategori Electronics.
Tambahkan variabel lain seperti diskon, musim penjualan, dan kategori produk untuk meningkatkan akurasi model prediksi penjualan.
