# 📊 Analisis dan Visualisasi Data Penjualan E-Commerce

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-black?style=for-the-badge&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical_Graphics-green?style=for-the-badge)

### Praktikum Analisis dan Visualisasi Data

Analisis performa penjualan e-commerce menggunakan Python untuk menghasilkan insight bisnis berbasis data.

</div>

---

# 📌 Deskripsi Praktikum

Praktikum ini bertujuan untuk melakukan proses analisis dan visualisasi data penjualan e-commerce menggunakan Python.

Tahapan yang dilakukan meliputi:

- Data Collection
- Data Cleaning
- Data Exploration
- Data Visualization
- Business Insight
- Recommendation

Dataset yang digunakan berisi informasi transaksi penjualan, kategori produk, pelanggan, anggaran iklan, dan total penjualan.

---

# 🎯 Business Question

Beberapa pertanyaan bisnis yang ingin dijawab pada praktikum ini adalah:

### 1. Produk Underperformer
Produk apa yang memiliki harga tinggi tetapi volume penjualannya rendah?

### 2. Segmentasi Pelanggan
Siapa pelanggan terbaik berdasarkan metode RFM (Recency, Frequency, Monetary)?

### 3. Efisiensi Kategori Produk
Kategori produk mana yang memberikan hasil terbaik dibandingkan biaya iklan yang dikeluarkan?

### 4. Pengaruh Iklan
Apakah peningkatan anggaran iklan berpengaruh terhadap peningkatan penjualan?

---

# 🧹 Data Wrangling

Tahapan pembersihan data yang dilakukan:

- Memeriksa struktur data (`df.info()`)
- Memeriksa missing value (`df.isnull().sum()`)
- Mengubah tipe data tanggal menjadi datetime
- Membersihkan data yang tidak valid
- Menyiapkan data untuk proses analisis

### Hasil Pemeriksaan Data

| Informasi | Nilai |
|------------|---------|
| Total Data | 150 |
| Total Kolom | 8 |
| Missing Value pada Total_Sales | 7 |

---

# 📈 Analisis 1: Produk Underperformer

## Tujuan

Mengidentifikasi produk dengan harga di atas rata-rata tetapi memiliki jumlah penjualan yang rendah.

### Rata-rata Harga Produk

```text
Rp1.024.640
```

### Contoh Produk Underperformer

| Kategori | Harga | Quantity |
|-----------|-----------:|-----------:|
| Gadget | Rp1.431.000 | 1 |
| Books | Rp1.654.000 | 1 |
| Gadget | Rp1.992.000 | 1 |
| Home Decor | Rp1.853.000 | 1 |
| Fashion | Rp1.399.000 | 1 |

### Insight

Produk-produk tersebut memiliki harga relatif tinggi namun hanya terjual satu kali.

Hal ini menunjukkan kemungkinan adanya:

- Harga yang kurang kompetitif
- Target pasar yang kurang tepat
- Kurangnya promosi terhadap produk tertentu

---

# 👥 Analisis 2: Segmentasi Pelanggan (RFM Analysis)

## Tujuan

Mengidentifikasi pelanggan yang memberikan kontribusi terbesar terhadap perusahaan.

### Top Customer

| CustomerID | Frequency | Monetary |
|------------|-----------:|-----------:|
| 5015 | 6 | Rp26.309.000 |
| 5008 | 6 | Rp22.350.000 |
| 5035 | 6 | Rp22.066.000 |
| 5014 | 6 | Rp20.797.000 |
| 5044 | 7 | Rp20.631.000 |

### Insight

Customer **5015** memiliki nilai transaksi tertinggi sehingga dapat dikategorikan sebagai pelanggan loyal dan bernilai tinggi.

Pelanggan seperti ini layak mendapatkan:

- Voucher loyalitas
- Program membership
- Promo eksklusif

---

# 📊 Analisis 3: Efisiensi Kategori Produk

## Tujuan

Menentukan kategori produk yang paling efisien berdasarkan perbandingan antara pendapatan dan biaya iklan.

### Hasil Analisis

| Kategori | Efficiency Ratio |
|-----------|-----------:|
| Gadget | 0.92 |
| Home Decor | 1.07 |
| Fashion | 1.17 |
| Books | 1.20 |
| Electronics | 1.44 |

### Insight

🏆 **Electronics** menjadi kategori paling efisien karena menghasilkan pendapatan tertinggi dibandingkan biaya iklan yang dikeluarkan.

⚠️ **Gadget** memiliki efisiensi terendah sehingga strategi pemasarannya perlu dievaluasi kembali.

---

# 📉 Analisis 4: Pengaruh Iklan terhadap Penjualan

## Regresi Linear

### Output Program

```python
Koefisien Iklan : 0.1842
R² Score : -0.1956
```

### Insight

- Koefisien bernilai positif.
- Peningkatan anggaran iklan masih menunjukkan hubungan positif terhadap penjualan.
- Nilai R² negatif menunjukkan bahwa model sederhana ini belum mampu menjelaskan variasi penjualan secara optimal.

Kemungkinan terdapat faktor lain yang lebih berpengaruh seperti:

- Diskon
- Kategori produk
- Musim penjualan
- Perilaku pelanggan

---

# 💡 Insight Utama

✅ Ditemukan beberapa produk mahal yang memiliki volume penjualan rendah.

✅ Customer 5015 merupakan pelanggan dengan nilai transaksi terbesar.

✅ Kategori Electronics memiliki efisiensi iklan terbaik.

✅ Anggaran iklan memiliki hubungan positif terhadap penjualan namun belum menjadi faktor dominan.

---

# 🚀 Recommendation

### Untuk Produk

- Evaluasi harga produk underperformer.
- Tingkatkan promosi pada produk dengan penjualan rendah.

### Untuk Pelanggan

- Berikan reward kepada pelanggan loyal.
- Terapkan program membership dan voucher khusus.

### Untuk Marketing

- Fokuskan anggaran iklan pada kategori Electronics.
- Evaluasi efektivitas iklan pada kategori Gadget.

### Untuk Analisis Selanjutnya

- Menambahkan variabel diskon.
- Menambahkan variabel kategori produk.
- Menggunakan model machine learning yang lebih kompleks.

---

# 🛠️ Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook / Google Colab

---

# 📚 Kesimpulan

Berdasarkan hasil analisis yang dilakukan, perusahaan dapat meningkatkan performa bisnis dengan mengoptimalkan strategi pemasaran, mempertahankan pelanggan loyal, serta mengevaluasi produk yang memiliki performa penjualan rendah.

Data menunjukkan bahwa keputusan bisnis yang didasarkan pada analisis data dapat membantu perusahaan mengalokasikan sumber daya secara lebih efektif dan efisien.

---

<div align="center">

### ⭐ Praktikum Analisis dan Visualisasi Data

Dibuat sebagai tugas praktikum mata kuliah Analisis dan Visualisasi Data

</div>
