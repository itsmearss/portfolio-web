---
title: "Build and test a real time human pose classification model using mediapipe and random forest algorithm."
description: "Dunia computer vision terus berkembang pesat, salah satu aplikasinya yang menarik adalah klasifikasi pose manusia secara real-time.... "
pubDate: "May 11 2024"
heroImage: "/post_img.webp"
---

Dunia computer vision terus berkembang pesat, salah satu aplikasinya yang menarik adalah klasifikasi pose manusia secara real-time. Artikel ini akan membahas cara membangun dan menguji model klasifikasi pose manusia menggunakan kombinasi MediaPipe dan algoritma Random Forest.

Mengenal Komponen:

MediaPipe: Framework open-source dari Google yang menyediakan pipeline machine learning untuk berbagai tugas computer vision, termasuk pose estimation (estimasi pose). MediaPipe memudahkan kita untuk mendeteksi landmark (titik keypoint) pada tubuh manusia dari video atau gambar.
Random Forest: Algoritma machine learning yang termasuk dalam kategori ensemble learning. Random Forest bekerja dengan menggabungkan prediksi dari multiple decision tree, menghasilkan klasifikasi yang lebih akurat dan robust.
Langkah-langkah Membangun Model:

Pengumpulan Data:

Kumpulkan dataset video atau gambar yang berisi berbagai pose manusia yang ingin diklasifikasikan (misalnya, berdiri, jongkok, melamba tangan).
Dataset ini nantinya akan digunakan untuk melatih model Random Forest.
Pre-processing Data:

Gunakan MediaPipe untuk memproses data video atau gambar.
Ekstrak landmark (titik keypoint) pose manusia dari setiap frame video atau gambar.
Selain landmark, Anda mungkin perlu mengekstrak fitur tambahan seperti jarak antar landmark atau sudut antar tulang.
Pelatihan Model:

Siapkan data landmark yang telah diekstrak beserta label pose yang sesuai (misalnya, label "berdiri" untuk frame dengan pose berdiri).
Gunakan library machine learning seperti Scikit-learn untuk melatih model Random Forest dengan data tersebut.
Random Forest akan belajar mengidentifikasi pola dan hubungan antar landmark untuk memprediksi pose baru.
Pengujian Model:

Setelah proses pelatihan selesai, uji model Random Forest dengan data yang belum pernah dilihat sebelumnya.
Evaluasi performa model dengan menghitung akurasi klasifikasi, precision, dan recall untuk setiap pose.
Sesuaikan parameter model (misalnya, jumlah pohon keputusan) berdasarkan hasil evaluasi untuk meningkatkan akurasi.
Implementasi Real-Time:

Setelah memiliki model terlatih, gunakan MediaPipe untuk memproses video secara real-time dari webcam atau sumber lainnya.
Ekstrak landmark pose dari setiap frame video.
Gunakan model Random Forest yang telah dilatih untuk memprediksi pose manusia secara real-time berdasarkan landmark yang diekstrak.
Visualisasikan hasil klasifikasi pose pada frame video (misalnya, menampilkan label pose di overlay).
Keuntungan Menggunakan Random Forest:

Mudah dipahami dan diinterpretasikan.
Berperforma baik dengan dataset berukuran sedang.
Tidak terlalu rentan terhadap overfitting.
Kelemahan Menggunakan Random Forest:

Mungkin membutuhkan waktu pelatihan yang lebih lama dibandingkan algoritma lain.
Bisa jadi kurang akurat dibandingkan algoritma lain untuk dataset yang sangat besar.
Kesimpulan:

Kombinasi MediaPipe dan Random Forest menawarkan cara yang efisien untuk membangun model klasifikasi pose manusia real-time. Dengan mengikuti langkah-langkah yang diberikan dan bereksperimen dengan parameter, Anda dapat membangun model yang mampu mengenali berbagai pose manusia secara akurat.
