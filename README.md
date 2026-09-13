# Retail Store Sales Analysis 📊

## 📌 Project Overview

Project ini merupakan analisis data penjualan retail yang bertujuan untuk menemukan insight mengenai performa penjualan, produk, customer, metode pembayaran, lokasi transaksi, discount, dan pola penjualan berdasarkan waktu.

Dataset yang digunakan merupakan dataset retail yang memiliki data kotor (*dirty data*), sehingga project ini mencakup proses **data cleaning, exploratory data analysis (EDA), dan business insight** menggunakan Python.

Project ini dibuat sebagai bagian dari portfolio untuk mengembangkan kemampuan **Data Analyst**.

---

## 🎯 Objectives

Tujuan dari project ini adalah:

- Membersihkan dataset yang memiliki missing values dan data yang perlu divalidasi.
- Melakukan Exploratory Data Analysis (EDA).
- Menganalisis performa penjualan berdasarkan kategori dan produk.
- Menganalisis customer dan pola transaksi.
- Menganalisis metode pembayaran dan lokasi transaksi.
- Menganalisis pola penjualan berdasarkan waktu.
- Mengidentifikasi outlier dan memastikan apakah data tersebut valid.
- Menghasilkan business insight yang dapat digunakan sebagai dasar pengambilan keputusan.

---

## 🗂️ Dataset

**Dataset:** Retail Store Sales: Dirty for Data Cleaning

Dataset berisi data transaksi retail dengan informasi seperti:

| Column | Description |
|---|---|
| Transaction ID | ID unik transaksi |
| Customer ID | ID customer |
| Category | Kategori produk |
| Item | Nama/kode produk |
| Price Per Unit | Harga produk per unit |
| Quantity | Jumlah produk yang dibeli |
| Total Spent | Total nilai transaksi |
| Payment Method | Metode pembayaran |
| Location | Lokasi transaksi |
| Transaction Date | Tanggal transaksi |
| Discount Applied | Informasi penggunaan discount |

### Data awal

- Rows: **12,575**
- Columns: **11**

Dataset memiliki beberapa missing values, terutama pada:
- Item
- Price Per Unit
- Quantity
- Total Spent
- Discount Applied

---

## 🧹 Data Cleaning

Tahapan cleaning yang dilakukan:

1. Mengecek struktur dan tipe data.
2. Mengecek missing values.
3. Mengecek duplicate rows.
4. Mengecek duplicate Transaction ID.
5. Menangani missing values pada kolom transaksi utama.
6. Mengubah `Transaction Date` menjadi format datetime.
7. Memvalidasi hubungan:
   `Total Spent = Price Per Unit × Quantity`
8. Mengecek nilai tidak valid pada harga dan quantity.
9. Menangani missing value pada `Discount Applied` sebagai **Unknown**, bukan `False`.
10. Melakukan feature engineering berdasarkan tanggal.

### Hasil Cleaning

Setelah proses cleaning:

- Rows awal: **12,575**
- Rows setelah cleaning: **11,362**
- Rows yang dihapus: **1,213**
- Columns setelah feature engineering: **17**

Data hasil cleaning disimpan di:

```text
data/cleaned/retail_store_sales_cleaned.csv
