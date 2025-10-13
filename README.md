Proyek: Klasifikasi Ulasan Produk E-Commerce Indonesia
-----------------------------------------------------------------------------------------------
**1. Elevator Pitch**

Sebuah sistem klasifikasi teks otomatis yang mengelompokkan ulasan pelanggan e-commerce berbahasa Indonesia ke dalam tiga kategori utama berdasarkan isi pesannya:
(1) PUJIAN / ORDER, 
(2) KELUHAN / TANYA MASALAH PRODUK, dan 
(3) KOMENTAR UMUM.

Sistem ini dikembangkan menggunakan dataset PRDECT-ID, kumpulan ribuan review produk Indonesia dari berbagai kategori (elektronik, fashion, alat rumah tangga, dll).
Dengan memanfaatkan model machine learning ringan seperti Logistic Regression dan Naive Bayes, sistem ini membantu penjual online untuk memahami pola komunikasi pelanggan, memprioritaskan tanggapan yang penting, dan meningkatkan kepuasan pelanggan secara efisien.

Targetnya: akurasi ≥85% dan waktu klasifikasi <2 detik per ulasan, jauh lebih cepat dibanding memilah ulasan manual satu per satu.

**2. Problem Statement**

Marketplace seperti Tokopedia dan Shopee menampung ribuan ulasan pelanggan setiap hari.
Penjual sering kewalahan membedakan mana ulasan yang berisi pujian (positif), keluhan atau pertanyaan produk, dan komentar umum.

Tanpa sistem otomatis, proses ini memakan waktu lama dan sering membuat keluhan pelanggan terabaikan.

Dengan sistem klasifikasi otomatis berbasis teks, penjual dapat:
- Mengenali ulasan yang mengandung masalah atau pertanyaan produk,
- Memprioritaskan respons terhadap keluhan penting,
- Menganalisis persepsi pelanggan terhadap produk secara cepat.
---------------------------------------------------------------------------
**3. Scope Awal**

**In-Scope:**
- Klasifikasi teks Bahasa Indonesia menjadi tiga kategori utama:
1. PUJIAN / ORDER
2. KELUHAN / TANYA PRODUK
3. KOMENTAR UMUM

- Implementasi model machine learning ringan (Logistic Regression, Naive Bayes).
- Pemanfaatan dataset PRDECT-ID (review produk Indonesia) untuk pelatihan model.

**Out-of-Scope:**
- Analisis sentimen mendalam (positif/negatif).
- Integrasi real-time ke sistem marketplace.
- Penggunaan model bahasa besar (BERT, GPT).

---------------------------------------------------------------------------
**4. Metrik**

**Baseline (manual):**
- 10 menit untuk memilah 20 ulasan pelanggan.
- Akurasi manusia ±95%.

**Target sistem:**
- Waktu klasifikasi otomatis <2 detik per ulasan.
- Macro F1-Score ≥85%.

**Evaluasi:**
- Macro F1-Score → untuk keseimbangan antar kelas.
- Confusion Matrix → untuk analisis kesalahan antar kategori.

----------------------------------------------------------------------------
**5. Struktur Repository**
README.md         → Dokumentasi utama proyek  
data/             → Dataset PRDECT-ID (PRDECT-ID Dataset.csv)  
notebooks/        → Notebook EDA & Preprocessing  
src/              → Script preprocessing & model baseline  
docs/             → Dokumentasi Etika, Privasi, dan Design Notes  
issues board      → To Do / In Progress / Done (≥5 issue)

**6. Roadmap**
- M1: Definisi masalah & setup repo (selesai).
- M2: EDA + preprocessing dataset PRDECT-ID (hapus noise, tokenisasi, dll).
- M3: Implementasi model baseline (Logistic Regression / Naive Bayes).
- M4: Fine-tuning model (mis. SVM / TF-IDF tuning).
- M5: Evaluasi performa (F1-Score, confusion matrix).
- M6: Dokumentasi akhir & demo CLI sederhana.
---------------------------------------------------------------------------
**7. Etika & Privasi**

**Risiko:**
Model bisa salah mengklasifikasikan ulasan negatif sebagai positif, yang dapat menyebabkan miss-feedback dalam analisis pelanggan.

**Mitigasi:**
Dataset PRDECT-ID bersifat publik dan tidak memuat data pribadi (PII), sehingga aman untuk digunakan.
Untuk mengurangi kesalahan interpretasi, sistem akan menitikberatkan pada akurasi kelas keluhan, agar respons penjual terhadap masalah pelanggan tetap cepat dan tepat.

-----------------------------------------------------------------------------
**8. Link GitHub**

🔗 https://github.com/shopia-sal/trpl-ai-capstone.git

