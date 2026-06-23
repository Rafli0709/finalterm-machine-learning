# UAS Machine Learning & Deep Learning - End-to-End Hands-On Models

---

## 👤 Identifikasi Mahasiswa

- **Nama** :Muhammad Rafli Maulana
- **NIM** : 1103220034
- **Kelas** : TK-46-GAB
- **Mata Kuliah**: Machine Learning

---

## 📌 Purpose of the Repository

Repositori ini dibuat untuk memenuhi komponen penilaian **UAS Mandiri (Individual Task)** pada kelas _Machine Learning & Deep Learning_. Repositori ini memuat implementasi _pipeline_ kecerdasan buatan ujung-ke-ujung (_end-to-end_) untuk menyelesaikan dua buah studi kasus utama: **Klasifikasi Fraud Transaksi Elektronik** dan **Regresi Prediksi Tahun Rilis Lagu** dengan menerapkan otomatisasi optimasi parameter (_Optuna_) dan pelacakan eksperimen (_MLflow_).

---

## 📊 Overview of the Projects & Models Used

### Soal 1: Fraud Detection (Classification Case)

- **Deskripsi:** Memprediksi probabilitas sebuah transaksi _online_ terindikasi penipuan (`isFraud`) berdasarkan karakteristik data transaksi numerik.
- **Arsitektur Model:** Deep Learning Multi-Layer Perceptron (MLP) yang dibangun di atas framework **TensorFlow/Keras** dengan optimasi _Dropout layer_ untuk menangani data yang mengalami ketidakseimbangan kelas (_class imbalance_).
- **Hyperparameter Tuning:** Otomatis menggunakan **Optuna** untuk mencari kombinasi _learning rate_, jumlah unit neuron, dan _dropout rate_ terbaik.
- **Eksperimen Tracking:** Seluruh parameter dan performa dicatat menggunakan **MLflow Tracking**.

### Soal 2: Song Release Year Prediction (Regression Case)

- **Deskripsi:** Memprediksi nilai kontinu berupa tahun rilis sebuah lagu berdasarkan fitur audio numerik (timbre, karakteristik audio, dll.).
- **Arsitektur Model:** Deep Learning Regression Model (MLP) menggunakan **TensorFlow/Keras** dengan output _Dense layer_ tunggal linear.
- **Interpretability:** Menggunakan **LIME (Local Interpretable Model-agnostic Explanations)** untuk membedah kontribusi setiap fitur audio terhadap hasil prediksi prediksi model secara lokal.

---

## 🏆 Matrix Results Summary

Berikut adalah indikator metrik yang dievaluasi dan dicatat pada sistem log:

| Kasus Proyek                     | Algoritma / Framework | Metrik Evaluasi Utama                          | Status Log         |
| :------------------------------- | :-------------------- | :--------------------------------------------- | :----------------- |
| **Soal 1: Fraud Classification** | TensorFlow + Optuna   | **ROC-AUC Score**, Precision, Recall, F1-Score | Terlacak di MLflow |
| **Soal 2: Song Regression**      | TensorFlow + LIME     | **MSE, RMSE, MAE, $R^2$ Score**                | Terlacak di MLflow |

---

## 🗺️ How to Navigate Through the Repository

Untuk memeriksa kode program dan menjalankan ulang eksperimen ini, ikuti peta navigasi berikut:

- **`/README.md`** : Dokumen utama panduan repositori dan identitas mahasiswa.
- **`/Soal_1_Fraud_Detection.ipynb`** : Notebook Jupyter berisi pipeline data preprocessing, pencarian arsitektur dengan Optuna, dan tracking klasifikasi fraud dengan MLflow.
- **`/Soal_2_Song_Regression.ipynb`** : Notebook Jupyter berisi pipeline regresi tahun lagu, evaluasi metrik MSE/RMSE/MAE/$R^2$, serta visualisasi kontribusi fitur menggunakan LIME.

---

## 🚀 Cara Menjalankan Project Secara Lokal

1. Klon repositori ini ke komputer lokal Anda:
   ```bash
   git clone [https://github.com/Rafli0709/finalterm-machine-learning.git](https://github.com/Rafli0709/finalterm-machine-learning.git)
   ```
