# Chat Sentiment Analysis

Nama: Annisa Mufidatun Sholihah

Username dicoding: annisams11

| | Deskripsi |
| ----------- | ----------- |
| **Dataset** | [Chat Sentiment Dataset](https://www.kaggle.com/datasets/nursyahrina/chat-sentiment-dataset) |
| **Masalah** | Masalah yang diangkat adalah analisis sentimen dari pesan chat untuk mengklasifikasikan pesan menjadi dua kelas sentimen: positif dan negatif. Pesan-pesan dalam dataset ini beragam, mengandung teks sederhana, karakter khusus, angka, emoji/emotikon, dan URL, yang membuat analisis sentimen lebih menantang. |
| **Solusi machine learning** | Solusi machine learning yang akan dibuat adalah model klasifikasi yang dapat memprediksi sentimen dari pesan chat. Model ini akan dilatih menggunakan dataset yang tersedia untuk mengenali pola-pola dalam teks yang menunjukkan sentimen positif atau negatif. |
| **Metode pengolahan** | Metode pengolahan data yang digunakan meliputi: <ul><li>Preprocessing teks seperti menghapus karakter khusus, URL, dan angka.</li><li>Tokenisasi teks untuk memecah pesan menjadi kata-kata atau token.</li><li>Penggunaan teknik Natural Language Processing (NLP) seperti stemming atau lemmatization untuk menyederhanakan kata.</li><li>Konversi teks menjadi vektor menggunakan teknik seperti TF-IDF atau word embeddings (contohnya, Word2Vec atau GloVe).</li></ul> |
| **Arsitektur model** | Arsitektur model yang digunakan adalah sebagai berikut: <ul><li>**Text Vectorization**: Mengubah teks menjadi urutan token menggunakan `TextVectorization` layer dari Keras.</li><li>**Embedding Layer**: Menggunakan embedding layer untuk memetakan token ke vektor dengan dimensi tertentu.</li><li>**Global Average Pooling**: Mengurangi dimensi dari embedding dengan mengambil rata-rata dari semua vektor dalam satu urutan.</li><li>**Dense Layers**: Dua layer Dense dengan aktivasi ReLU untuk mengekstraksi fitur penting.</li><li>**Output Layer**: Layer Dense dengan aktivasi sigmoid untuk menghasilkan probabilitas dari kelas positif.</li></ul> | 
| **Transformasi Data** | <ul><li>**Lowercasing**: Mengubah semua teks menjadi huruf kecil menggunakan `tf.strings.lower`.</li><li>**Casting Label**: Mengubah label menjadi tipe integer (`tf.int64`).</li></ul> |
| **Evaluasi Model** | <ul><li>**Model Specs**: Menggunakan `tfma.ModelSpec` untuk menentukan label dari data.</li><li>**Slicing Specs**: Menggunakan `tfma.SlicingSpec` untuk menentukan pengelompokan data saat evaluasi.</li><li>**Metrics Specs**: Menggunakan `tfma.MetricsSpec` untuk menentukan metrik yang akan dievaluasi seperti AUC, Binary Accuracy, False Positives, True Positives, False Negatives, True Negatives, dan Example Count.</li></ul> |
| **Metrik Evaluasi** | Metrik yang digunakan untuk mengevaluasi performa model mencakup: <ul><li>AUC (Area Under Curve): 0.822</li><li>Example Count: 127</li><li>Binary Accuracy dengan threshold 0.5</li></ul> |
| **Performa Model** | Model menunjukkan performa yang baik dengan AUC sebesar 0.822 dan jumlah contoh (example count) sebesar 127. Model ini mampu mengklasifikasikan sentimen dengan tingkat akurasi yang tinggi, menunjukkan bahwa model dapat membedakan antara sentimen positif dan negatif dengan cukup baik. |
