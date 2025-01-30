# Pendahuluan
## 1.1 Latar Belakang
Suatu data atau informasi disajikan tidak hanya berupa data teks tetapi juga dapat berupa audio, video, dan gambar. Pada zaman sekarang informasi sangatlah penting dan diperlukan, begitu juga informasi yang terdapat pada citra (Maulana & Andono, 2016).

Citra digital merupakan bagian penting dalam berbagai aplikasi teknologi, termasuk dalam bidang medis, pengenalan wajah, sistem keamanan, dan penginderaan jauh. Dalam proses akuisisi, penyimpanan, dan transmisi citra, sering kali terjadi gangguan berupa noise yang mengakibatkan penurunan kualitas citra.

Sebuah citra harus memiliki kualitas yang cukup baik untuk pemrosesan lebih lanjut. Apabila kualitas citra yang akan diproses tidak baik, maka akan berakibat pada kesalahan pemrosesan citra tersebut. Kualitas citra ditentukan dari berapa nilai rasio gangguan terhadap citra aslinya. Oleh sebab itu, citra harus ditingkatkan kualitasnya terlebih dahulu sebelum citra akan diolah (Sajati, 2016).

Perbaikan kualitas diperlukan karena seringkali citra yang dijadikan objek pembahasan mempunyai kualitas yang buruk, misalnya citra mengalami derau (noise) pada saat pengiriman melalui saluran transmisi, citra terlalu terang/gelap, citra kurang tajam, kabur, dan sebagainya (Fauzi, 2022).

Keberadaan noise salt and pepper dapat mengganggu analisis citra karena menyebabkan distorsi yang signifikan, terutama pada citra yang memiliki detail halus dan tekstur kompleks. Oleh karena itu, diperlukan metode pemrosesan citra yang efektif untuk menghilangkan noise tanpa mengorbankan kualitas visual dan informasi penting dalam citra.

## 1.2 Penelitian atau Teori Terkait
Metode median filter merupakan filter non-linear. Dikatakan non-linear karena cara bekerja metode ini tidak termasuk dalam kategori operasi konvolusi.

Dalam berbagai penelitian, median filter telah terbukti efektif dalam menghilangkan noise salt and pepper pada tingkat noise yang rendah hingga menengah. Namun, metode ini memiliki keterbatasan dalam menangani noise dengan tingkat yang lebih tinggi, di mana detail gambar cenderung ikut terhapus dan menghasilkan citra yang buram. Untuk mengatasi keterbatasan ini, beberapa metode baru dikembangkan, seperti adaptive median filter, yang dapat menyesuaikan ukuran jendela filtering berdasarkan tingkat keparahan noise.

Metode Adaptive Median Filter adalah metode pengembangan dari median filter biasa. Perbedaan yang menonjol antara dua metode ini adalah bahwa besarnya window (jendela) yang ada pada adaptive median filter setiap piksel adalah variabel. Variasi ini tergantung pada nilai median dari piksel dalam window saat ini. Ukuran jendela akan diperluas jika nilai rata-rata adalah impuls (Aripin & Hasibuan, 2019).

Selain itu, metode *edge-preserving regularization* diperkenalkan sebagai teknik tambahan yang memungkinkan pemulihan citra dengan mempertahankan tepi dan detail yang penting. Teknik ini bekerja dengan mempertahankan perubahan intensitas piksel yang signifikan (seperti tepi objek) sambil menghaluskan daerah yang homogen. Kombinasi *adaptive median filter* dan *edge-preserving regularization* diyakini dapat memberikan hasil yang lebih baik dibandingkan metode median filter konvensional.

## 1.3 Tujuan Tugas
Penelitian ini bertujuan untuk membandingkan efektivitas metode *median filter* dengan metode kombinasi *adaptive median filter* dan *edge-preserving regularization* dalam menghilangkan noise salt and pepper. Evaluasi dilakukan berdasarkan metrik *Mean Square Error* (MSE) dan *Peak Signal-to-Noise Ratio* (PSNR), yang digunakan untuk menilai kualitas citra yang telah difilter.

*Peak Signal to Noise Ratio* (PSNR) sering digunakan sebagai parameter pembanding antara citra yang telah dikonstruksi (diberi noise atau diberi filter) dengan citra aslinya. PSNR merupakan nilai perbandingan antara nilai maksimum warna pada hasil citra filtering dengan kuantitas gangguan (*noise*) yang merupakan akar rata-rata kuadrat nilai kesalahan (√MSE). PSNR dinyatakan dengan satuan desibel (dB) (Restima, 2021).

Dengan penelitian ini, diharapkan dapat ditemukan metode yang lebih optimal untuk menangani noise salt and pepper tanpa mengurangi kualitas detail citra.
