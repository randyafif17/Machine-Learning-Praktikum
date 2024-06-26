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

## Preprocessing Data.ipynb
Repositori ini berisi kumpulan skrip Python untuk preprocessing, analisis, dan visualisasi data pada berbagai dataset. Skrip ini menunjukkan berbagai teknik seperti pembersihan data, analisis statistik, normalisasi, regresi, dan lain-lain.
### Isi
1. Analisis Teks Pidato
   - Direktori: Preprocessing/pidato
   - Deskripsi: Membaca file teks pidato dari direktori yang ditentukan dan menyimpan nama file serta konten dalam sebuah DataFrame. Selain itu, skrip ini mengekstrak nama kota dan tanggal dari nama file serta menghitung rasio kemunculan kata untuk beberapa kata kunci tertentu.
2. Analisis Dataset Auto MPG
   - Deskripsi: Melakukan analisis statistik deskriptif, mendeteksi nilai yang hilang, dan membuat visualisasi boxplot untuk atribut dalam dataset Auto MPG yang diambil dari UCI Machine Learning Repository. Juga melakukan regresi linier untuk memprediksi MPG berdasarkan jumlah silinder.
   - URL Dataset: http://archive.ics.uci.edu/ml/machine-learning-databases/auto-mpg/auto-mpg.data
3. Preprocessing Data Pelanggan
   - Deskripsi: Membaca data pelanggan, mengubah nama kolom, menghapus nilai yang hilang, mendeteksi duplikat, dan melakukan berbagai teknik preprocessing seperti normalisasi dan binarisasi.
   - File Data: Preprocessing/Customer Churn.csv
4. Analisis Data Respon Survei
   - Deskripsi: Membaca data respon survei, mendeteksi outlier dalam atribut numerik, dan melakukan preprocessing lanjutan seperti pengisian nilai yang hilang dan standardisasi.
   - File Data: Preprocessing/OSMI Mental Health in Tech Survey 2019.csv
5. Penggunaan Teknik Scaling dan Binarization
   - Deskripsi: Menerapkan teknik scaling (Min-Max Scaling, Standard Scaling) dan binarisasi pada atribut numerik dalam dataset.
   - File Data: Preprocessing/data.csv
6. Manipulasi dan Visualisasi Data Produksi Listrik
   - Deskripsi: Membaca dan memanipulasi data produksi listrik bulanan, serta membuat visualisasi untuk memahami distribusi dan tren data.
   - File Data: Preprocessing/Electric_Production.csv

## Decision Tree.ipynb
Kode ini merupakan implementasi dari algoritma decision tree untuk klasifikasi pada data BMI (Body Mass Index). Tujuan dari kode ini adalah sebagai berikut:
1. Preprocessing Data: Data BMI dibaca dari file CSV dan kemudian diproses. Variabel obese ditambahkan berdasarkan indeks BMI untuk menandai apakah seseorang termasuk dalam kategori obes atau tidak. Selanjutnya, variabel indeks BMI dihapus karena tidak akan digunakan dalam pembangunan model.
2. Perhitungan Metrik: Dilakukan perhitungan jumlah data yang salah diklasifikasikan (misclassified) ketika menggunakan batas pemotongan pada 100 kg dan 80 kg.
3. Pembangunan Decision Tree: Didefinisikan beberapa fungsi untuk menghitung metrik-metrik seperti entropy, gini impurity, information gain, dan pemilihan pembelahan terbaik untuk membangun decision tree. Decision tree tersebut akan digunakan untuk melakukan klasifikasi pada data BMI.
4. Prediksi dan Evaluasi: Dilakukan prediksi kategori obesitas berdasarkan decision tree yang telah dibangun. Selanjutnya, dilakukan evaluasi klasifikasi menggunakan metrik-metrik seperti akurasi, presisi, sensitivitas, spesifisitas, dan F1-score.
5. Confusion Matrix: Dihitung matriks kebingungan (confusion matrix) untuk mengevaluasi kinerja model klasifikasi.

Jadi, secara keseluruhan, tujuan dari kode ini adalah untuk membangun model decision tree yang dapat digunakan untuk mengklasifikasikan data BMI ke dalam kategori obes atau tidak obes, serta melakukan evaluasi kinerja model menggunakan berbagai metrik evaluasi klasifikasi.

## K-Means Clustering #1
Deskripsi:
Bagian pertama dari proyek ini melibatkan pembuatan kelas KMeansMod, yang merupakan modifikasi dari algoritma K-Means standar. Modifikasi termasuk dalam proses inisialisasi sentroid awal, perhitungan inertia, dan beberapa metode lainnya untuk mengoptimalkan kinerja algoritma.

Fungsi Utama:
1. fit(X: np.array) -> None: Metode ini digunakan untuk melatih model K-Means menggunakan data input X.
2. predict(X: np.array) -> np.array: Metode ini digunakan untuk memprediksi label klaster untuk setiap sampel dalam data input X.
3. return_wcss() -> Tuple[float, np.array]: Metode ini mengembalikan nilai total within-cluster sum of squares (WCSS) dan array WCSS untuk setiap klaster.
4. return_centroids() -> np.array: Metode ini mengembalikan array sentroid yang dihasilkan oleh model setelah proses pelatihan.

Penggunaan:
Bagian ini menunjukkan bagaimana kelas KMeansMod dapat digunakan untuk melakukan clustering pada data yang dimuat dari file Excel. Hasil clustering juga dibandingkan dengan hasil dari KMeans standar dari scikit-learn.

## K-Means Clustering #2
Deskripsi:
Bagian kedua dari proyek ini melibatkan eksplorasi jumlah klaster yang optimal menggunakan metode "Elbow" dan Silhouette Score untuk dataset iris. Tujuannya adalah untuk memilih jumlah klaster terbaik yang dapat mewakili struktur data dengan baik.

Fungsi Utama:
1. load_iris(): Fungsi ini digunakan untuk memuat dataset iris sebagai contoh.
2. StandardScaler(): Digunakan untuk melakukan penskalaan data sebelum diterapkan pada algoritma clustering.
3. KMeans(n_clusters=i, max_iter=300, random_state=0): Menginisialisasi model KMeans dengan jumlah klaster yang bervariasi dari 2 hingga 10 untuk mengevaluasi inersia dan Silhouette Score.
4. silhouette_score(data_scaled, kmeans.labels_): Menghitung Silhouette Score untuk setiap jumlah klaster yang diuji.

Penggunaan:
Bagian ini menjelaskan bagaimana menggunakan metode "Elbow" dan Silhouette Score untuk menentukan jumlah klaster optimal pada dataset iris, dan menampilkan grafik untuk masing-masing metode untuk memudahkan interpretasi.
