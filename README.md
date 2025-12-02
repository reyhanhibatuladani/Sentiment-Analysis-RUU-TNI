# Sentiment-Analysis-RUU-TNI
# Analisis Komparasi Sentimen Revisi RUU TNI (Naïve Bayes vs SVM)

Penelitian ini berfokus pada analisis sentimen publik terhadap isu kontroversial Revisi Undang-Undang TNI (RUU TNI), khususnya terkait penolakan masyarakat di media sosial X (Twitter).

## Ringkasan Proyek
Penelitian ini bertujuan untuk membandingkan kinerja dua algoritma *machine learning*, yaitu **Naïve Bayes** dan **Support Vector Machine (SVM)**, dalam mengklasifikasikan opini publik menjadi 5 kategori sentimen: *Positif, Agak Positif, Netral, Agak Negatif,* dan *Negatif*.

Hasil penelitian menunjukkan bahwa **SVM** memiliki kinerja yang lebih unggul dibandingkan Naïve Bayes dalam hal akurasi dan F1-Score pada dataset ini.

## Data & Sumber
Data dikumpulkan pada periode puncak isu, yaitu **16–31 Maret 2025**.
* **Total Data:** 9.924 dokumen
    * **Twitter/X:** 9.827 tweet (menggunakan kata kunci `#TolakRUUTNI` dan lainnya).
    * **Portal Berita:** 97 artikel berita (sebagai pembanding diskursus media).

## Metodologi
Penelitian ini dilaksanakan menggunakan kerangka kerja standar **CRISP-DM** dengan tahapan teknis sebagai berikut:

1.  **Preprocessing:** Pembersihan teks, normalisasi, stemming, dan stopword removal.
2.  **Labeling:** Menggunakan kamus **InSet Lexicon**.
3.  **Expert Validation:** Validasi manual oleh pakar bahasa/domain terhadap **400 sampel tweet** untuk memastikan kualitas pelabelan.
4.  **Feature Extraction:** Term Frequency-Inverse Document Frequency (**TF-IDF**).
5.  **Handling Imbalance:** Penerapan **SMOTE** (Synthetic Minority Over-sampling Technique) untuk menangani ketidakseimbangan kelas data.
6.  **Evaluation:** Validasi model menggunakan **Stratified K-Fold Cross Validation** untuk hasil yang robust.

## Hasil Utama
* **Performa Algoritma:** SVM terbukti lebih akurat dalam mengklasifikasikan sentimen yang kompleks dibandingkan Naïve Bayes.
* **Analisis Opini:** Mayoritas sentimen publik bersifat **Negatif**.
* **Topik Sorotan:** Kemarahan dan kekhawatiran publik terpusat pada tiga isu utama:
    * Isu kembalinya **Dwifungsi ABRI**.
    * Perluasan **jabatan sipil** untuk prajurit aktif.
    * Usia **perpanjangan pensiun**.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Imbalanced-learn, Sastrawi, Matplotlib/Seaborn.
* **Tools:** Google Colab, Google Looker Studio (Dashboard).
