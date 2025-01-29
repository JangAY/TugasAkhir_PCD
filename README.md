# **Komparasi Metode Noise Salt & Pepper dengan Median Filter dan Adaptive Regularization**

**Moch Nazham Ismul Azham , Zamzam Mubarok**
[Institut Teknologi Garut]  
Email: 2206096@itg.ac.id , 2206088@itg.ac.id  

---

## **Abstrak**  
Noise salt and pepper merupakan salah satu bentuk gangguan dalam pemrosesan citra digital yang sering terjadi akibat kesalahan dalam proses akuisisi, transmisi, atau penyimpanan data gambar. Gangguan ini dapat menyebabkan distorsi signifikan pada citra, sehingga diperlukan teknik pemrosesan citra yang mampu menghilangkan noise tanpa mengorbankan detail penting dalam gambar. Penelitian ini membandingkan efektivitas dua pendekatan dalam mengatasi noise salt and pepper, yaitu metode *median filter* konvensional dan metode kombinasi *adaptive median filter* dengan *edge-preserving regularization*.  

Pendekatan pertama menggunakan *median filter*, yang telah lama digunakan dalam pengolahan citra karena kesederhanaannya dan kemampuannya dalam menghilangkan noise dengan cepat. Namun, metode ini memiliki kelemahan dalam menangani noise dengan tingkat yang tinggi, di mana detail gambar sering ikut terhapus. Sebagai alternatif, pendekatan kedua menggunakan *adaptive median filter* untuk mendeteksi dan mengisolasi pixel yang terkena noise, kemudian menerapkan *edge-preserving regularization* untuk mempertahankan detail dan tepi citra.  

Hasil eksperimen menunjukkan bahwa metode kombinasi mampu menghilangkan noise hingga 90% tanpa mengurangi ketajaman gambar secara signifikan. Evaluasi dilakukan menggunakan metrik *Mean Square Error (MSE)* dan *Peak Signal-to-Noise Ratio (PSNR)*, yang menunjukkan bahwa metode kombinasi memiliki performa yang lebih baik dibandingkan *median filter* konvensional. Oleh karena itu, metode ini direkomendasikan untuk aplikasi pemrosesan citra yang membutuhkan kualitas gambar yang tinggi, seperti pemrosesan citra medis dan citra satelit.  

**Kata Kunci**: *Noise Salt and Pepper, Median Filter, Adaptive Median Filter, Edge-Preserving Regularization, PSNR, MSE*  

---

## **1. Pendahuluan**  
Dalam era digital, citra digital digunakan secara luas dalam berbagai bidang, termasuk pemrosesan citra medis, pengenalan wajah, penginderaan jauh, dan pengawasan keamanan. Namun, dalam banyak kasus, kualitas citra dapat menurun akibat gangguan noise yang muncul selama proses akuisisi, transmisi, atau penyimpanan. Salah satu jenis noise yang paling umum adalah *salt and pepper noise*, yang ditandai dengan munculnya piksel berwarna putih atau hitam secara acak pada citra (Gonzalez & Woods, 2018).  

Untuk mengatasi masalah ini, berbagai teknik pengolahan citra telah dikembangkan, salah satunya adalah *median filter*. Filter ini merupakan teknik non-linear yang bekerja dengan mengganti nilai piksel berdasarkan median dari sekelompok piksel di sekitarnya. Metode ini cukup efektif dalam menghilangkan noise tingkat rendah, tetapi memiliki kelemahan dalam menangani noise dengan tingkat yang lebih tinggi karena dapat menyebabkan hilangnya detail penting dalam gambar (Hwang & Haddad, 1995).  

Sebagai solusi alternatif, metode *adaptive median filter* dikembangkan untuk mengatasi keterbatasan *median filter* konvensional dengan memperluas ukuran jendela filter secara adaptif berdasarkan tingkat keparahan noise. Selain itu, metode *edge-preserving regularization* digunakan untuk mempertahankan detail gambar selama proses denoising (Chan et al., 2005). Penelitian ini bertujuan untuk membandingkan efektivitas kedua metode dalam mereduksi noise salt and pepper serta mengevaluasi kinerja masing-masing pendekatan menggunakan metrik PSNR dan MSE.  

---

## **2. Metode Penelitian**  

Penelitian ini dilakukan dengan menggunakan dataset citra grayscale yang diberikan noise salt and pepper dengan berbagai tingkat intensitas (10% - 90%). Analisis dilakukan dengan dua metode utama, yaitu:  

### **2.1 Metode Median Filter**  
Metode ini bekerja dengan menggantikan setiap piksel dengan nilai median dari sekelompok piksel di sekitarnya. Langkah-langkah utama dalam metode ini adalah:  
1. Konversi citra berwarna menjadi grayscale (jika diperlukan).  
2. Penambahan noise salt and pepper pada citra grayscale.  
3. Penerapan *median filter* dengan ukuran jendela tetap (3×3 atau 5×5).  
4. Evaluasi hasil filtering menggunakan PSNR dan MSE untuk mengukur efektivitas reduksi noise.  

### **2.2 Metode Adaptive Median Filter dan Edge-Preserving Regularization**  
Metode ini dilakukan dalam dua tahap:  
1. **Adaptive Median Filter**  
   - Mendeteksi dan mengisolasi piksel yang terkena noise dengan menyesuaikan ukuran jendela filter.  
   - Menggunakan median dari jendela yang diperbesar jika noise tetap terdeteksi pada ukuran jendela awal.  
2. **Edge-Preserving Regularization**  
   - Menggunakan fungsi regularisasi untuk mempertahankan detail gambar, terutama pada tepi dan tekstur citra.  
   - Mengoptimalkan nilai piksel yang telah difilter dengan pendekatan matematis berbasis *variational methods*.  
3. Evaluasi hasil dengan metrik PSNR dan MSE untuk membandingkan kualitas citra hasil filtering dengan citra asli.  

---

## **3. Hasil dan Pembahasan**  

| **Metode** | **Efektivitas pada Noise Rendah** | **Efektivitas pada Noise Tinggi** | **Preservasi Detail** |
|------------|----------------------------------|---------------------------------|------------------------|
| *Median Filter* | Baik | Buruk (detail hilang) | Tidak Optimal |
| *Adaptive Median Filter + Regularization* | Baik | Sangat Baik | Optimal |

- Dari hasil eksperimen, metode *adaptive median filter* dengan *edge-preserving regularization* terbukti lebih efektif dalam menangani noise dengan tingkat tinggi.  
- Metode ini memiliki nilai PSNR yang lebih tinggi dibandingkan dengan *median filter*, menandakan kualitas citra yang lebih baik.  
- *Median filter* bekerja dengan baik untuk noise rendah tetapi kehilangan banyak detail pada noise tinggi.  

---

## **4. Kesimpulan**  
Berdasarkan hasil penelitian, dapat disimpulkan bahwa metode *adaptive median filter* dengan *edge-preserving regularization* memiliki keunggulan dalam mereduksi noise salt and pepper tanpa mengurangi detail citra secara signifikan. Sementara itu, metode *median filter* konvensional hanya efektif pada noise dengan tingkat rendah, tetapi cenderung menghilangkan detail citra pada tingkat noise yang lebih tinggi.  

Metode kombinasi ini sangat cocok untuk aplikasi yang memerlukan pemrosesan citra dengan kualitas tinggi, seperti dalam bidang medis, pengawasan, dan penginderaan jauh. Oleh karena itu, penelitian lebih lanjut disarankan untuk mengembangkan metode yang lebih efisien dalam hal waktu komputasi tanpa mengorbankan kualitas citra.  

---

## **5. Daftar Pustaka**  
1. Chan, R. H., Ho, C.-W., & Nikolova, M. (2005). *Salt-and-Pepper Noise Removal by Median-Type Noise Detectors and Detail-Preserving Regularization*. IEEE Transactions on Image Processing, 14(10), 1479–1485.  
2. Fadillah, N., & Gunawan, C. R. (2019). *Mendeteksi Keakuratan Noise Salt and Pepper dengan Median Filter*. Jurnal Informatika, 6(1), 91-95.  
3. Gonzalez, R. C., & Woods, R. E. (2018). *Digital Image Processing* (4th ed.). Pearson.  
4. Hwang, H., & Haddad, R. A. (1995). *Adaptive Median Filters: New Algorithms and Results*. IEEE Transactions on Image Processing, 4(4), 499-502.  
5. Nodes, T. A., & Gallagher, N. C. (1984). *The Output Distribution of Median Type Filters*. IEEE Transactions on Communications, 32(5), 532-541.  

