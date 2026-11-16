# Segmentasi Perilaku Transaksi Nasabah Menggunakan Machine Learning

Project portfolio Data Science dan Unsupervised Machine Learning ini mengeksplorasi pola transaksi pada tingkat akun untuk membentuk segmentasi perilaku pelanggan dan menerjemahkannya menjadi hipotesis strategi bisnis yang dapat diuji.

> **Catatan:** Hasil clustering bersifat eksploratif. Model bukan alat penilaian kredit, deteksi fraud, prediksi churn, atau dasar keputusan individual terhadap pelanggan.

## Ringkasan hasil

- 495 akun pelanggan digunakan dalam model terpilih.
- 2.513 baris transaksi tersedia; 2.493 baris memiliki `AccountID` dan 20 baris tidak dapat dipasangkan ke akun.
- K-Means dengan `C_Reduced18_Robust` dan `k=2` dipilih untuk profiling.
- Silhouette Score: **0,2048**; coverage: **100%**; noise: **0**.
- Mean sampling ARI: **0,9950** dari 30 pengulangan subsampling 80%; mean random-seed ARI: **1,0000** dari 30 percobaan.
- Cluster 0: 83 akun (16,77%); Cluster 1: 412 akun (83,23%).

## Temuan utama

Cluster 0 memiliki median 6 transaksi, 5 bulan aktif, dan 4 maksimum percobaan login. Cluster 1 memiliki median 5 transaksi, 4 bulan aktif, dan 1 maksimum percobaan login. Rata-rata nominal transaksi dan rata-rata saldo relatif serupa. Komposisi kanal ATM, Branch, dan Online juga cukup mirip.

## Tahapan penelitian

1. Exploratory Data Analysis
2. Data Cleaning & Preprocessing
3. Model Experimentation
4. Model Evaluation & Comparison
5. Cluster Profiling
6. Business Interpretation & Recommendations

## Menjalankan project

- Buka `notebooks/01_Data_Exploration_and_Preprocessing.ipynb` di Google Colab, lalu upload dataset transaksi sumber yang berhak digunakan.
- Jalankan notebook sampai selesai untuk menghasilkan tiga file preprocessing.
- Buka `notebooks/02_Machine_Learning_and_Business_Insights.ipynb` dan upload `customer_features_for_clustering_unscaled.csv`, `customer_level_features_audit.csv`, serta `cleaned_transaction_dataset.csv` saat sesi Colab dimulai. Jalankan semua sel berurutan.
- Detail dependencies ada di `requirements.txt`.

## Privasi data

Dataset mentah, AccountID, tabel per-pelanggan, dan label cluster per-pelanggan tidak disertakan dalam repositori publik. Hanya tabel agregat dan visualisasi yang disediakan. Pastikan hak penggunaan dataset sebelum mengunggah data apa pun.

Lihat [README utama (English)](README.md) untuk dokumentasi portfolio lengkap.
