# Klasifikasi_Submission_Akhir_BMLP_Briyan_Yehezkhiel

# Analisis Data dan Pembangunan Model Klasifikasi

Repositori ini berisi kode Python dalam format Google Colab notebook untuk melakukan analisis data dan membangun model klasifikasi berdasarkan dataset hasil clustering.

## Daftar Isi

1.  [Import Library](#1-import-library)
2.  [Memuat Dataset dari Hasil Clustering](#2-memuat-dataset-dari-hasil-clustering)
3.  [Data Splitting](#3-data-splitting)
4.  [Membangun Model Klasifikasi](#4-membangun-model-klasifikasi)
5.  [Memenuhi Kriteria Skilled dan Advanced dalam Membangun Model Klasifikasi](#5-memenuhi-kriteria-skilled-dan-advanced-dalam-membangun-model-klasifikasi)
    *   [Algoritma Klasifikasi Selain Decision Tree](#algoritma-klasifikasi-selain-decision-tree)
    *   [Evaluasi Model](#evaluasi-model)
    *   [Hyperparameter Tuning Model](#hyperparameter-tuning-model)

## 1. Import Library

Bagian ini mengimpor pustaka Python yang diperlukan untuk analisis data dan machine learning, termasuk `pandas`, `joblib`, `sklearn.ensemble`, `sklearn.model_selection`, `sklearn.tree`, dan `sklearn.metrics`.

## 2. Memuat Dataset dari Hasil Clustering

Dataset hasil clustering, `data_clustering_inverse.csv`, dimuat ke dalam DataFrame pandas untuk analisis lebih lanjut.

## 3. Data Splitting

Dataset dibagi menjadi data latih (training set) dan data uji (test set) menggunakan `train_test_split` dari `sklearn.model_selection` dengan `test_size=0.2` dan `random_state=42`.

## 4. Membangun Model Klasifikasi

Model klasifikasi Decision Tree dibangun dan dilatih menggunakan data latih yang telah diproses (mengubah kolom tanggal menjadi numerik dan one-hot encoding kolom kategorikal). Model yang dilatih disimpan sebagai `decision_tree_model.h5`.

## 5. Memenuhi Kriteria Skilled dan Advanced dalam Membangun Model Klasifikasi

### Algoritma Klasifikasi Selain Decision Tree

Selain Decision Tree, model Random Forest juga dilatih untuk perbandingan.

### Evaluasi Model

Model Decision Tree dan Random Forest dievaluasi menggunakan metrik akurasi, presisi, recall, dan F1-Score pada data uji. Hasil evaluasi kedua model ditampilkan.

### Hyperparameter Tuning Model

Hyperparameter tuning dilakukan pada model Random Forest menggunakan `GridSearchCV` untuk mencari kombinasi parameter terbaik (`n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`). Model Random Forest terbaik setelah tuning dilatih kembali dan dievaluasi. Model hasil tuning disimpan sebagai `tuning_classification.h5`.
