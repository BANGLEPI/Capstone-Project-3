# 🏎️ Capstone Project 3 – Prediksi Harga Mobil Bekas di Arab Saudi

## Deskripsi Proyek
Proyek ini merupakan bagian dari **Capstone Project Modul 3** yang berfokus pada penerapan **Machine Learning** untuk permasalahan bisnis nyata.  
Dataset yang digunakan adalah **Saudi Arabia Used Cars**, yang berisi data mobil bekas dari situs [syarah.com](https://syarah.com/).  
Tujuan utama proyek ini adalah **memprediksi harga mobil bekas** berdasarkan fitur-fitur yang tersedia, agar proses jual-beli mobil menjadi lebih **efisien, transparan, dan adil**.

---

## Tujuan Bisnis
- Membantu **penjual** menentukan harga mobil yang kompetitif dan realistis.  
- Membantu **pembeli** mengetahui apakah harga yang ditawarkan sesuai dengan kondisi mobil.  
- Memberikan **rekomendasi harga otomatis** bagi platform jual beli mobil seperti *syarah.com*.  

---

## 📊 Dataset
Dataset berisi **5.624 baris dan 11 fitur** utama yang merepresentasikan karakteristik mobil bekas.

| Kolom | Deskripsi |
|-------|------------|
| Type | Jenis mobil |
| Region | Wilayah tempat mobil dijual |
| Make | Merek mobil |
| Gear_Type | Jenis transmisi (Automatic / Manual) |
| Origin | Asal mobil |
| Options | Tingkat fitur (Standard / Semi Full / Full) |
| Year | Tahun pembuatan |
| Engine_Size | Kapasitas mesin (liter) |
| Mileage | Jarak tempuh (kilometer) |
| Negotiable | True jika harga masih bisa dinegosiasikan |
| Price | Harga mobil (dalam SAR) |

Fitur tambahan yang dibuat:
- **Car_Age** = 2025 - Year  

---

## Tahapan Pengerjaan

### 1. Data Understanding
- Memahami struktur dataset dan konteks bisnis.  
- Menentukan variabel target: `Price`.  

### 2. Data Cleaning & Preparation
- Menghapus data duplikat (4 baris).  
- Memastikan tidak ada missing values.  
- Melakukan encoding pada kolom kategorikal.  
- Menambahkan fitur baru `Car_Age`.

### 3. Exploratory Data Analysis (EDA)
- Menganalisis distribusi harga, jarak tempuh, dan ukuran mesin.  
- Melihat hubungan antara usia mobil dan harga.  
- Meneliti perbedaan harga rata-rata berdasarkan merek, wilayah, transmisi, dan opsi fitur.  

### 4. Modeling
Model yang digunakan:
- **Linear Regression**
- **Random Forest Regressor**

Data dibagi menjadi:
- **80%** data latih  
- **20%** data uji  

### 5. Evaluation
Metrik evaluasi yang digunakan:
- **MAE (Mean Absolute Error)**  
- **RMSE (Root Mean Squared Error)**  
- **R² (R-squared)**  

| Model | MAE | RMSE | R² |
|--------|------|------|----|
| Linear Regression | 27,005 | 44,083 | 0.578 |
| **Random Forest** | **11,393** | **30,223** | **0.802** |

Model terbaik: **Random Forest Regressor**

---

## Kesimpulan
- Model **Random Forest** mampu memprediksi harga mobil bekas dengan akurasi tinggi (**R² = 0.80**).  
- Fitur yang paling berpengaruh terhadap harga:  
  **Tahun (Year), Jarak Tempuh (Mileage), Ukuran Mesin (Engine_Size), dan Usia Mobil (Car_Age).**  
- Model ini dapat digunakan oleh platform jual beli mobil untuk memberikan **rekomendasi harga otomatis** kepada pengguna.

---

## Rekomendasi Bisnis
- **Penjual:** Gunakan model untuk menentukan harga jual kompetitif.  
- **Pembeli:** Jadikan prediksi model sebagai acuan sebelum membeli mobil.  
- **Platform:** Integrasikan model ke sistem listing untuk rekomendasi harga otomatis.  
- **Tim Pemasaran:** Fokus pada wilayah dan merek dengan harga jual rata-rata tinggi.

---

## Teknologi yang Digunakan
- **Python 3.11+**  
- **Pandas, NumPy, Matplotlib, Seaborn**  
- **Scikit-Learn (Linear Regression, Random Forest)**  
- **Jupyter Notebook**  
- **Pickle (untuk menyimpan model)**

---

## 💾 File dalam Repositori
