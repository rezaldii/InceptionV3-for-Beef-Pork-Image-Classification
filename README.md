# Klasifikasi Citra Daging Sapi dan Daging Babi Menggunakan Metode Convolutional Neural Network (CNN) dengan Arsitektur Inception V3

## Deskripsi
Proyek ini menggunakan model **InceptionV3** untuk mengklasifikasikan gambar menjadi dua kategori: **Sapi (Beef)** dan **Babi (Pork)**. Dengan memanfaatkan teknik **transfer learning**, model yang sudah dilatih sebelumnya pada dataset ImageNet diadaptasi untuk tugas klasifikasi spesifik ini. Teknik data augmentation juga digunakan untuk meningkatkan variasi data dan mengurangi risiko overfitting.

## Fitur Utama
- **Transfer Learning:** Memanfaatkan model InceptionV3 yang telah dipelajari dari ImageNet dan melakukan fine-tuning untuk dataset daging sapi dan babi.
- **Data Augmentation:** Menerapkan teknik augmentasi (rotasi, zoom, flipping, dll.) untuk meningkatkan jumlah dan variasi data pelatihan.
- **Evaluasi Model:** Menggunakan metrik akurasi, confusion matrix, dan grafik visualisasi (akurasi & loss) untuk menganalisis performa model.
- **Implementasi Sederhana:** Kode disusun agar mudah dipahami dan dapat dijalankan untuk keperluan eksperimen maupun pengembangan lebih lanjut.

## Cara Kerja Proyek
1. **Persiapan Data:**  
   - Gambar daging sapi dan babi ditempatkan dalam folder `dataset/beef` dan `dataset/pork` masing-masing.
   - Data augmentation diterapkan untuk menambah variasi gambar.

2. **Pembuatan Model:**  
   - Model **InceptionV3** di-load dengan bobot dari ImageNet.
   - Layer akhir model dihapus dan diganti dengan layer baru untuk klasifikasi dua kelas (beef vs. pork).
   - Proses fine-tuning dilakukan untuk menyesuaikan model dengan dataset yang spesifik.

3. **Pelatihan:**  
   - Model dilatih dengan optimizer (misalnya, Adam) dan loss function (categorical crossentropy).
   - Selama pelatihan, metrik akurasi dan loss dicatat untuk analisis performa.

4. **Evaluasi:**  
   - Model diuji menggunakan data validasi/test.
   - Hasil evaluasi berupa akurasi, confusion matrix, dan grafik visualisasi disajikan untuk melihat performa model.

## Dependencies
- Python 3.x
- TensorFlow / Keras
- scikit-learn
- matplotlib
- numpy

## Hasil & Output
- **Akurasi:** Persentase akurasi model dalam mengklasifikasikan gambar.
- **Confusion Matrix:** Menunjukkan perbandingan antara prediksi dan label asli.
- **Grafik Training:** Visualisasi akurasi dan loss selama proses training.

## Kesimpulan
Proyek ini menunjukkan bagaimana model InceptionV3 dapat diadaptasi melalui transfer learning untuk tugas klasifikasi gambar khusus, yaitu membedakan antara daging sapi dan babi. Teknik data augmentation dan fine-tuning terbukti efektif meningkatkan performa model meskipun dataset yang tersedia relatif terbatas.
