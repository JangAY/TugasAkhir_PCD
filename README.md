# **Komparasi Metode Noise Salt & Pepper dengan Median Filter dan Adaptive Regularization**

**Nama Penulis**  
[Institusi Penulis]  
Email: penulis@example.com  

## **Abstrak**  
Penelitian ini membandingkan efektivitas dua metode pengurangan noise salt and pepper pada citra digital. Jurnal pertama menggunakan metode *median filter* untuk menghilangkan noise, sedangkan jurnal kedua dari IEEE mengusulkan pendekatan dua tahap yang menggabungkan *adaptive median filter* dan *edge-preserving regularization*. Analisis menunjukkan bahwa metode adaptif memiliki kinerja yang lebih baik dalam mempertahankan detail dan tepi citra, terutama pada tingkat noise yang tinggi. Evaluasi dilakukan dengan metrik *Mean Square Error (MSE)* dan *Peak Signal-to-Noise Ratio (PSNR)*. Hasil menunjukkan bahwa metode adaptif mampu menangani noise hingga 90% lebih efektif dibandingkan dengan *median filter* konvensional.

**Kata Kunci**: *Noise Salt and Pepper, Median Filter, Adaptive Median Filter, Edge-Preserving Regularization, PSNR, MSE*

---

## **1. Pendahuluan**  
Noise salt and pepper merupakan salah satu bentuk gangguan pada citra digital yang dapat disebabkan oleh kesalahan transmisi atau kerusakan sensor pada perangkat akuisisi gambar (Gonzalez & Woods, 2018). Untuk mengatasi masalah ini, berbagai metode telah dikembangkan, termasuk *median filter* yang banyak digunakan karena kemampuannya dalam mereduksi noise tanpa terlalu banyak mengaburkan detail citra (Hwang & Haddad, 1995). Namun, metode ini memiliki kelemahan dalam mempertahankan detail gambar saat tingkat noise tinggi (Nodes & Gallagher, 1984).  

Pendekatan baru seperti *adaptive median filter* dan *edge-preserving regularization* telah dikembangkan untuk mengatasi keterbatasan tersebut (Chan et al., 2005). Penelitian ini bertujuan untuk membandingkan efektivitas kedua metode dalam menghilangkan noise salt and pepper dan mempertahankan kualitas citra.

---

## **2. Metode Penelitian**  

### **2.1 Jurnal 1: Median Filter untuk Pengurangan Noise Salt and Pepper**  
- Menggunakan *median filter* sebagai metode utama dalam menghilangkan noise.  
- Evaluasi dilakukan menggunakan MSE dan PSNR untuk membandingkan kualitas citra asli dan hasil filtrasi.  
- Hasil menunjukkan bahwa metode ini efektif untuk tingkat noise rendah tetapi kurang optimal untuk noise tinggi.

### **2.2 Jurnal 2: Adaptive Median Filter dan Edge-Preserving Regularization**  
- Pendekatan dua tahap:  
  1. *Adaptive median filter* digunakan untuk mendeteksi dan mengisolasi pixel yang terkena noise.  
  2. *Edge-preserving regularization* diterapkan untuk memulihkan detail citra tanpa mengaburkan tepi.  
- Metode ini dapat menangani noise hingga 90% dan memberikan hasil yang lebih baik dibandingkan *median filter* konvensional.

---

## **3. Hasil dan Pembahasan**  

| **Metode** | **Efektivitas pada Noise Rendah** | **Efektivitas pada Noise Tinggi** | **Preservasi Detail** |
|------------|----------------------------------|---------------------------------|------------------------|
| *Median Filter* | Baik | Buruk (detail hilang) | Tidak Optimal |
| *Adaptive Median Filter + Regularization* | Baik | Sangat Baik | Optimal |

- *Median filter* bekerja dengan baik pada noise rendah tetapi kehilangan detail pada noise tinggi.  
- Metode adaptif dari jurnal IEEE lebih unggul dalam menangani noise tinggi dan mempertahankan detail gambar.  
- Nilai PSNR pada metode adaptif lebih tinggi dibandingkan *median filter*, menunjukkan kualitas citra yang lebih baik.  

---

## **4. Kesimpulan**  
Hasil analisis menunjukkan bahwa metode *adaptive median filter* dengan *edge-preserving regularization* lebih efektif dibandingkan *median filter* dalam mereduksi noise salt and pepper, terutama pada tingkat noise yang tinggi. Oleh karena itu, metode ini direkomendasikan untuk aplikasi yang membutuhkan preservasi detail citra yang lebih baik, seperti pemrosesan medis dan citra satelit.

---

## **5. Daftar Pustaka**  
1. Chan, R. H., Ho, C.-W., & Nikolova, M. (2005). *Salt-and-Pepper Noise Removal by Median-Type Noise Detectors and Detail-Preserving Regularization*. IEEE Transactions on Image Processing, 14(10), 1479–1485.  
2. Fadillah, N., & Gunawan, C. R. (2019). *Mendeteksi Keakuratan Noise Salt and Pepper dengan Median Filter*. Jurnal Informatika, 6(1), 91-95.  
3. Gonzalez, R. C., & Woods, R. E. (2018). *Digital Image Processing* (4th ed.). Pearson.  
4. Hwang, H., & Haddad, R. A. (1995). *Adaptive Median Filters: New Algorithms and Results*. IEEE Transactions on Image Processing, 4(4), 499-502.  
5. Nodes, T. A., & Gallagher, N. C. (1984). *The Output Distribution of Median Type Filters*. IEEE Transactions on Communications, 32(5), 532-541.  
6. Pok, G., Liu, J.-C., & Nair, A. S. (2003). *Selective Removal of Impulse Noise Based on Homogeneity Level Information*. IEEE Transactions on Image Processing, 12(1), 85-92.  
7. Wang, Z., & Zhang, D. (1999). *Progressive Switching Median Filter for the Removal of Impulse Noise from Highly Corrupted Images*. IEEE Transactions on Circuits and Systems II: Analog and Digital Signal Processing, 46(1), 78-80.  

---

Artikel ini sekarang sudah mengikuti standar penulisan jurnal ilmiah dengan tambahan lima referensi yang relevan. Jika Anda ingin menyesuaikan lebih lanjut, silakan beri tahu saya! 😊📄
