---
layout: post
title: Evaluasi Model
date: 2024-06-03 00:00 +0700
categories: [Blog, "Data Science"]
tags: [blog, data-science]
---

<!--
Artikel : https://xrce.github.io/posts/evaluasi-model/
-->

Evaluasi model adalah langkah penting dalam siklus data science yang bertujuan untuk menilai kinerja model yang telah dibangun. Proses ini memastikan bahwa model yang dibuat dapat memberikan prediksi atau klasifikasi yang akurat dan andal ketika diterapkan pada data baru. Berikut adalah penjelasan lengkap dan merinci tentang evaluasi model dalam data science.

## Metode Evaluasi Model

### 1. **Train-Test Split**
Train-test split adalah metode dasar untuk mengevaluasi model di mana dataset dibagi menjadi dua bagian: satu untuk melatih model (train set) dan satu lagi untuk menguji model (test set). Pembagian yang umum digunakan adalah 80/20 atau 70/30.

### 2. **Cross-Validation**
Cross-validation adalah teknik yang lebih canggih di mana dataset dibagi menjadi beberapa bagian (folds). Model dilatih dan diuji pada bagian yang berbeda secara bergantian, yang membantu dalam mengurangi overfitting dan memberikan estimasi kinerja model yang lebih akurat. Teknik yang umum digunakan adalah k-fold cross-validation.

### 3. **Stratified Sampling**
Stratified sampling memastikan bahwa pembagian dataset ke dalam train dan test set mempertahankan distribusi proporsional dari kelas target. Ini sangat penting untuk dataset yang tidak seimbang.

## Metrik Evaluasi

### 1. **Akurasi**
Akurasi adalah proporsi prediksi yang benar dari keseluruhan prediksi. Metrik ini sangat intuitif namun bisa menyesatkan jika data tidak seimbang.

\[ \text{Akurasi} = \frac{\text{Jumlah Prediksi Benar}}{\text{Total Prediksi}} \]

### 2. **Precision, Recall, dan F1-Score**
- **Precision** adalah proporsi prediksi positif yang benar dari semua prediksi positif.

\[ \text{Precision} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Positives}} \]

- **Recall** (Sensitivity) adalah proporsi prediksi positif yang benar dari semua kasus sebenarnya positif.

\[ \text{Recall} = \frac{\text{True Positives}}{\text{True Positives} + \text{False Negatives}} \]

- **F1-Score** adalah rata-rata harmonis dari precision dan recall, memberikan keseimbangan antara keduanya.

\[ \text{F1-Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \]

### 3. **Area Under the Curve (AUC) - ROC Curve**
ROC Curve adalah grafik yang menunjukkan trade-off antara true positive rate (TPR) dan false positive rate (FPR). AUC memberikan satu nilai yang merangkum kinerja model, di mana nilai yang lebih dekat ke 1 menunjukkan kinerja yang lebih baik.

### 4. **Mean Absolute Error (MAE) dan Mean Squared Error (MSE)**
Untuk model regresi, MAE dan MSE adalah metrik umum yang digunakan untuk mengukur seberapa besar rata-rata kesalahan prediksi model.

\[ \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i| \]

\[ \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 \]

## Teknik Evaluasi Tambahan

### 1. **Confusion Matrix**
Confusion matrix adalah tabel yang digunakan untuk mengevaluasi kinerja model klasifikasi dengan menunjukkan jumlah true positives (TP), true negatives (TN), false positives (FP), dan false negatives (FN).

### 2. **Kappa Statistic**
Kappa statistic mengukur konsistensi antara prediksi model dan kelas sebenarnya, mempertimbangkan kemungkinan prediksi yang terjadi secara acak.

### 3. **Gain and Lift Charts**
Gain and lift charts digunakan dalam model pemasaran untuk mengukur efektivitas model prediksi dalam mengidentifikasi kelompok target yang berpotensi tinggi.

## Proses Evaluasi Model

1. **Pemisahan Dataset**: Pisahkan dataset menjadi train dan test set, atau gunakan cross-validation.
2. **Pelatihan Model**: Latih model menggunakan train set.
3. **Prediksi**: Gunakan model untuk membuat prediksi pada test set.
4. **Pengukuran Kinerja**: Gunakan metrik evaluasi untuk menilai kinerja model.
5. **Perbaikan Model**: Berdasarkan hasil evaluasi, lakukan tuning parameter atau pilih algoritma yang berbeda untuk meningkatkan kinerja.

## Kesimpulan

Evaluasi model adalah langkah krusial dalam data science yang memastikan model yang dibangun dapat diandalkan dan memberikan hasil yang akurat. Memahami dan menggunakan berbagai metode dan metrik evaluasi membantu dalam mengembangkan model yang lebih baik dan lebih tepat guna.

Evaluasi yang tepat memungkinkan pengambilan keputusan yang lebih baik dan memastikan model memberikan nilai tambah nyata dalam aplikasi dunia nyata.

