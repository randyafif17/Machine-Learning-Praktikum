## Machine Learning Algorithms.ipynb
Deskripsi:
File ini berisi implementasi kustom dari algoritma RandomForest untuk tugas regresi dan klasifikasi,
serta contoh penggunaan Naive Bayes untuk klasifikasi. Algoritma RandomForest diimplementasikan dengan
penggunaan bootstrapping dan pelatihan beberapa model pohon keputusan (DecisionTree).

Implementasi mencakup:
1. Kelas abstrak `RandomForest` untuk mendefinisikan struktur dasar RandomForest.
2. Kelas `CustomRandomForestRegressor` untuk regresi menggunakan RandomForest.
3. Kelas `CustomRandomForestClassifier` untuk klasifikasi menggunakan RandomForest dengan opsi untuk
   menyesuaikan kedalaman maksimum pohon, kriteria pemisahan, dan penanganan bobot kelas.
4. Contoh penggunaan Naive Bayes dengan dataset iris menggunakan perpustakaan scikit-learn.

Dataset:
1. Boston Housing Dataset - digunakan untuk regresi.
2. Wine Dataset - digunakan untuk klasifikasi.
3. Iris Dataset - digunakan untuk klasifikasi dengan Naive Bayes.

Fitur-fitur utama:
- Pembuatan bootstrap sample untuk pelatihan model.
- Evaluasi performa model dengan cross-validation.
- Penghitungan dan penampilan metrik kinerja seperti akurasi, presisi, dan recall.
- Visualisasi distribusi data dan korelasi fitur.

Cara Penggunaan:
- Jalankan skrip untuk melatih model RandomForest dan Naive Bayes pada dataset yang diberikan.
- Lihat hasil prediksi dan evaluasi kinerja model.

Perpustakaan yang diperlukan:
- numpy
- pandas
- seaborn
- matplotlib
- scikit-learn
