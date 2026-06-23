# Segmentasi & Analisis Perilaku Digital Gen Z menggunakan K-Means Clustering: Pengaruh Intensitas Penggunaan Media Sosial terhadap Kesehatan Mental

Proyek ini merupakan tugas akhir (UAS) untuk mata kuliah **Data Mining & Data Warehousing (DMDW)**. Penelitian ini berfokus pada analisis data mining untuk mengidentifikasi segmentasi perilaku pengguna dari generasi Gen Z berdasarkan pola intensitas penggunaan media sosial mereka, serta menganalisis hubungannya dengan skor kesehatan mental.

---

## 📌 Anggota Tim / Peneliti
* **Nama:** Maulana Hafidz Wibowo  
* **NIM:** 2410501031  
* **Kelas:** S1 Sistem Informasi - A (Semester 4)  
* **Institusi:** Universitas Pembangunan Nasional "Veteran" Jakarta  

---

## 🎯 Pertanyaan Penelitian (Research Questions)
1. Apakah pengguna Gen Z dapat disegmentasikan ke dalam kelompok-kelompok yang berbeda berdasarkan pola perilaku digital mereka menggunakan *K-Means Clustering*?
2. Apakah terdapat hubungan signifikan antara intensitas penggunaan media sosial dan kesehatan mental di setiap segmen pengguna?
3. Apakah tingkat kesehatan mental berbeda secara signifikan antar segmen pengguna berdasarkan intensitas penggunaan media sosial?

---

## ⚙️ Tahapan Penelitian & Metodologi
Proyek ini dikembangkan melalui 9 tahapan utama yang sistematis:
1. **Data Loading & Inspection:** Memuat dataset `social_media_user_behavior.csv` dan memeriksa kualitas fisik data (missing values, duplikat, dan *outliers*).
2. **Data Preparation (Filtering Gen Z):** Menyaring subset data spesifik untuk populasi Gen Z (rentang usia 12–27 tahun). Teridentifikasi sebanyak **1.072 baris** (53.60% dari total data umum).
3. **Data Cleaning:** Menghapus pencilan (*outliers*) menggunakan metode IQR secara selektif pada fitur utama clustering untuk menjaga stabilitas model, menyisakan **951 baris** data bersih.
4. **EDA (Exploratory Data Analysis):** Menemukan pola awal dan distribusi variabel.
5. **Feature Selection & Scaling:** Memilih fitur paling relevan dan melakukan standarisasi skala menggunakan `StandardScaler`.
6. **K-Means Clustering:** Mengelompokkan pengguna ke dalam 3 segmen unik.
7. **Cluster Profiling:** Menganalisis karakteristik spesifik dari setiap cluster yang terbentuk.
8. **Within-Cluster Correlation Analysis:** Menguji konsistensi hubungan antara intensitas media sosial dan *mental health score* di tiap cluster.
9. **Cross-Cluster Statistical Comparison & Visualization:** Membuktikan signifikansi perbedaan antar cluster dan menyajikannya dalam bentuk *insight* yang *actionable*.

---

## 🛠️ Tech Stack & Library yang Digunakan
* **Bahasa Pemrograman:** Python 3
* **Environment:** Google Colab
* **Libraries:**
  * `pandas` & `numpy` (Manipulasi & Pembersihan Data)
  * `matplotlib` & `seaborn` (Visualisasi Data)
  * `scikit-learn` (`KMeans`, `StandardScaler` untuk Modeling)

---

## 📊 Ringkasan Fitur yang Dianalisis
* **Fitur Intensitas Penggunaan (Fitur Utama Clustering):**
  * `daily_usage_hours`
  * `avg_session_duration_min`
  * `sessions_per_day`
  * `posts_per_week`
  * `likes_given_per_day`
* **Fitur Kesehatan Mental & Validasi:**
  * `self_reported_mental_health_score`
  * `sleep_disruption`
  * `mood_while_scrolling`
  * `takes_social_media_breaks`
