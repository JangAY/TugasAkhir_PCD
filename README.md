# **Analisis Perbandingan Metode Noise Salt & Pepper dengan Median Filter dan Adaptive Regularization**

**Moch Nazham Ismul Azham** , **Zamzam Mubarok**
[Institut Teknologi Garut]  
Email: 2206096@itg.ac.id , 2206088@itg.ac.id  

---

## **1. Pendahuluan**
### 1.1 **Latar Belakang**
Suatu data atau informasi disajikan tidak hanya berupa data teks tetapi juga dapat berupa audio, video, dan gambar. Pada zaman sekarang informasi sangatlah penting dan diperlukan, begitu juga informasi yang terdapat pada citra (Maulana & Andono, 2016).

Citra digital merupakan bagian penting dalam berbagai aplikasi teknologi, termasuk dalam bidang medis, pengenalan wajah, sistem keamanan, dan penginderaan jauh. Dalam proses akuisisi, penyimpanan, dan transmisi citra, sering kali terjadi gangguan berupa noise yang mengakibatkan penurunan kualitas citra.

Sebuah citra harus memiliki kualitas yang cukup baik untuk pemrosesan lebih lanjut. Apabila kualitas citra yang akan diproses tidak baik, maka akan berakibat pada kesalahan pemrosesan citra tersebut. Kualitas citra ditentukan dari berapa nilai rasio gangguan terhadap citra aslinya. Oleh sebab itu, citra harus ditingkatkan kualitasnya terlebih dahulu sebelum citra akan diolah (Sajati, 2016).

Perbaikan kualitas diperlukan karena seringkali citra yang dijadikan objek pembahasan mempunyai kualitas yang buruk, misalnya citra mengalami derau (noise) pada saat pengiriman melalui saluran transmisi, citra terlalu terang/gelap, citra kurang tajam, kabur, dan sebagainya (Fauzi, 2022).

Keberadaan noise salt and pepper dapat mengganggu analisis citra karena menyebabkan distorsi yang signifikan, terutama pada citra yang memiliki detail halus dan tekstur kompleks. Oleh karena itu, diperlukan metode pemrosesan citra yang efektif untuk menghilangkan noise tanpa mengorbankan kualitas visual dan informasi penting dalam citra.

### 1.2 **Penelitian atau Teori Terkait**
Metode median filter merupakan filter non-linear. Dikatakan non-linear karena cara bekerja metode ini tidak termasuk dalam kategori operasi konvolusi.

Dalam berbagai penelitian, median filter telah terbukti efektif dalam menghilangkan noise salt and pepper pada tingkat noise yang rendah hingga menengah. Namun, metode ini memiliki keterbatasan dalam menangani noise dengan tingkat yang lebih tinggi, di mana detail gambar cenderung ikut terhapus dan menghasilkan citra yang buram. Untuk mengatasi keterbatasan ini, beberapa metode baru dikembangkan, seperti adaptive median filter, yang dapat menyesuaikan ukuran jendela filtering berdasarkan tingkat keparahan noise.

Metode Adaptive Median Filter adalah metode pengembangan dari median filter biasa. Perbedaan yang menonjol antara dua metode ini adalah bahwa besarnya window (jendela) yang ada pada adaptive median filter setiap piksel adalah variabel. Variasi ini tergantung pada nilai median dari piksel dalam window saat ini. Ukuran jendela akan diperluas jika nilai rata-rata adalah impuls (Aripin & Hasibuan, 2019).

Selain itu, metode *edge-preserving regularization* diperkenalkan sebagai teknik tambahan yang memungkinkan pemulihan citra dengan mempertahankan tepi dan detail yang penting. Teknik ini bekerja dengan mempertahankan perubahan intensitas piksel yang signifikan (seperti tepi objek) sambil menghaluskan daerah yang homogen. Kombinasi *adaptive median filter* dan *edge-preserving regularization* diyakini dapat memberikan hasil yang lebih baik dibandingkan metode median filter konvensional.

### 1.3 **Tujuan Tugas**
Penelitian ini bertujuan untuk membandingkan efektivitas metode *median filter* dengan metode kombinasi *adaptive median filter* dan *edge-preserving regularization* dalam menghilangkan noise salt and pepper. Evaluasi dilakukan berdasarkan metrik *Mean Square Error* (MSE) dan *Peak Signal-to-Noise Ratio* (PSNR), yang digunakan untuk menilai kualitas citra yang telah difilter.

*Peak Signal to Noise Ratio* (PSNR) sering digunakan sebagai parameter pembanding antara citra yang telah dikonstruksi (diberi noise atau diberi filter) dengan citra aslinya. PSNR merupakan nilai perbandingan antara nilai maksimum warna pada hasil citra filtering dengan kuantitas gangguan (*noise*) yang merupakan akar rata-rata kuadrat nilai kesalahan (√MSE). PSNR dinyatakan dengan satuan desibel (dB) (Restima, 2021).

Dengan penelitian ini, diharapkan dapat ditemukan metode yang lebih optimal untuk menangani noise salt and pepper tanpa mengurangi kualitas detail citra.

---

## **2. Metode Penelitian**

### 2.1 **Penjelasan Langkah-Langkah**

 1. **Persiapan Data**
    - Pemilihan gambar *Lena* dan gambar *Bridge* dengan citra grayscale yang digunakan dalam eksperimen.
    - Penambahan noise *salt and pepper* pada citra.

 2. **Penerapan Filtering**
    - **Metode Median Filter**
     - Citra yang telah terkontaminasi noise diproses menggunakan *median filter* dengan ukuran jendela tetap (3x3 dan 5x5).
    - **Metode Adaptive Median Filter dan Edge-Preserving Regularization**
     - Citra diproses dengan *adaptive median filter* untuk mendeteksi dan menghilangkan noise.
     - Diterapkan *edge-preserving regularization* untuk mempertahankan detail gambar.

 3. **Evaluasi Hasil**
    - Pengukuran kualitas citra dilakukan menggunakan metrik *PSNR* dan *MSE*.
    - Analisis visual dilakukan untuk melihat perbedaan hasil filtering noise dengan metode yang berbeda: *Median Filter, Adaptive Median Filter,* dan *Edge-Preserving Regularization*.
    - Menghitung *PSNR* dan *MAE* untuk mengevaluasi kualitas citra yang dipulihkan oleh *AMF* dan *EPR*.
    - *PSNR* mengukur rasio antara daya sinyal maksimum dan daya noise, dengan nilai yang lebih tinggi menunjukkan kualitas citra yang lebih baik.
    - *MAE* mengukur rata-rata perbedaan absolut antara piksel-piksel dalam citra asli dan citra yang dipulihkan, dengan nilai yang lebih rendah menunjukkan kualitas citra yang lebih baik.
    - Membandingkan nilai *PSNR* dan *MAE* dari *Median Filter, AMF,* dan *EPR* untuk menentukan metode yang lebih efektif.

---

## **3. Hasil dan Pembahasan**

### 3.1 **Hasil Eksperimen**

**Hasil Metode Median Filter**
Pada metode *Median Filter* terdapat hasil dengan nilai **PSNR** 34,49 dan **MSE** 23,09 serta nilai **MAE** mencapai 91,06.

**Hasil Metode Adaptive Median Filter**
Pada metode *Adaptive Median Filter* terdapat hasil dengan nilai **PSNR** 15,40 dan nilai **MAE** sebesar 31,73.

| **Metode**               | **PSNR (db)** | **MAE**  |
|--------------------------|--------------|---------|
| Median Filter           | 34,49        | 91,06   |
| Adaptive Median Filter  | 15,40        | 31,73   |

Hasil eksperimen menunjukkan bahwa metode *Median Filter* mendapatkan nilai **PSNR** lebih tinggi dibanding *Adaptive Median Filter*, tetapi nilai **Mean Absolute Error (MAE)** metode *Adaptive Median Filter* lebih kecil, yaitu 31,73 dibandingkan dengan *Median Filter* yang memiliki nilai **MAE** sebesar 91,06.

### 3.2 **Analisis Hasil**

 1. **PSNR (*Peak Signal-to-Noise Ratio*)**
   - *Median Filter* menghasilkan **PSNR** yang lebih tinggi dibandingkan dengan *Adaptive Median Filter*.
   - **PSNR** merupakan metrik yang mengukur rasio antara daya sinyal maksimum dan daya noise. Nilai **PSNR** yang lebih tinggi menunjukkan kualitas citra yang lebih baik, khususnya dalam mengurangi noise.
   - Hal ini menunjukkan bahwa *Median Filter* lebih efektif dalam mengurangi noise secara keseluruhan dan mempertahankan informasi sinyal asli.

 2. **MAE (*Mean Absolute Error*)**
   - *Adaptive Median Filter* memiliki nilai **MAE** yang lebih rendah dibandingkan dengan *Median Filter*.
   - **MAE** mengukur rata-rata perbedaan absolut antara piksel-piksel dalam citra asli dan citra yang dipulihkan. Nilai **MAE** yang lebih rendah menunjukkan bahwa citra yang dipulihkan lebih mirip dengan citra asli secara visual.
   - Hal ini menunjukkan bahwa *Adaptive Median Filter* lebih baik dalam mempertahankan detail halus dan tekstur citra, meskipun mungkin tidak seefektif *Median Filter* dalam mengurangi noise secara keseluruhan.

---

## **4. Kesimpulan**

### 4.1	**Ringkasan Temuan**
Median Filter dan Adaptive Median Filter menawarkan pendekatan yang berbeda untuk pengurangan noise pada citra, masing-masing dengan kelebihan dan kekurangannya sendiri. Median Filter, dengan sifatnya yang non-adaptif, lebih agresif dalam mengurangi noise, menghasilkan PSNR yang lebih tinggi. Namun, hal ini dapat mengakibatkan hilangnya detail halus dan efek "blocky" pada citra, yang tercermin dalam MAE yang lebih tinggi.

Adaptive Median Filter, dengan pendekatan adaptifnya, lebih selektif dalam mengurangi noise, menyesuaikan ukuran kernel berdasarkan karakteristik lokal citra. Hal ini membantu dalam mempertahankan detail halus dan tekstur, menghasilkan MAE yang lebih rendah. Namun, pendekatan ini mungkin kurang efektif dalam mengurangi noise secara keseluruhan dibandingkan dengan Median Filter standar, menghasilkan PSNR yang lebih rendah.

### 4.2	**Batasan Pekerjaan**
 1.	Waktu pemrosesan metode kombinasi lebih lama dibandingkan dengan median filter
 2.	Efektivitas metode kombinasi dapat bervariasi tergantung pada parameter yang digunakan.

### **4.3	Rekomendasi untuk Pekerjaan di Masa Depan**
 1.	Pengembangan algoritma yang lebih efisien untuk mempercepat waktu komputasi.
 2.	Eksplorasi metode berbasis pembelajaran mesin untuk penghapusan noise yang lebih adaptif.
 
---
## **5. Referensi**
Aripin, S., & Hasibuan, N. A. (2019). Penerapan Metode Interpolasi Linier dan Metode Adaptive Median Filter untuk Perbaikan Kualitas Citra pada Hasil CCTV. Prosiding Seminar Nasional Riset Information Science (SENARIS), 1(September), 854. https://doi.org/10.30645/senaris.v1i0.92 

Fauzi, A. (2022). Pengurangan Derau (Noise) pada Citra Paper Dokumen menggunakan Metode Gaussian Filter dan Median Filter. KAKIFIKOM (Kumpulan Artikel Karya Ilmiah Fakultas Ilmu Komputer), 04(01), 7–15. https://doi.org/10.54367/kakifikom.v4i1.1871 

Maulana, I., & Andono, P. N. (2016). Analisa Perbandingan Adaptif Median Filter Dan Median Filter Dalam Reduksi Noise Salt & Pepper. CogITo Smart Journal, 2(2), 157–166. https://doi.org/10.31154/cogito.v2i2.26.157-166 

Restima. (2021). Implementasi Metode Alpha-Trimmed Mean Filter dan Adaptive Median Filter Untuk Mereduksi Noise Poisson Pada Citra Digital. Terapan Informatika Nusantara, 1(10), 527–535. https://ejurnal.seminar-id.com/index.php/tin 

Sajati, H. (2016). Analisis kualitas perbaikan citra m enggunakan m etode m edian f il t e r dengan penyeleksian n ila i. 41–48.

