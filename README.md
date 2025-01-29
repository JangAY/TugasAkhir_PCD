# Komparasi Metode Noise Salt & Pepper dengan Median Filter

**Nama Penulis**  
[Institusi Penulis]  
Email: penulis@example.com  

## Abstrak
Penelitian ini membandingkan dua metode pengurangan noise salt and pepper yang diusulkan dalam dua jurnal berbeda. Jurnal pertama menggunakan metode *median filter* konvensional untuk mereduksi noise pada citra digital. Sementara itu, jurnal kedua dari IEEE mengusulkan pendekatan dua tahap yang menggabungkan *adaptive median filter* dan *edge-preserving regularization*. Hasil analisis menunjukkan bahwa metode adaptif lebih efektif dalam mempertahankan detail dan tepi citra pada tingkat noise yang tinggi.

## Kata Kunci
- Noise Salt and Pepper
- Median Filter
- Adaptive Median Filter
- Edge-Preserving Regularization

## Pendahuluan
Noise salt and pepper merupakan gangguan umum dalam pemrosesan citra digital. Artikel jurnal yang dianalisis memiliki pendekatan berbeda dalam mereduksi noise ini. Jurnal pertama meneliti efektivitas *median filter* dalam membersihkan noise salt and pepper, sedangkan jurnal kedua mengusulkan metode yang lebih kompleks dengan mempertahankan detail citra.

## Metode Penelitian
### Jurnal 1: Mendeteksi Keakuratan Noise Salt and Pepper dengan Median Filter
- Menggunakan metode *median filter* untuk menghilangkan noise.
- Mengukur efektivitas dengan Mean Square Error (MSE) dan Peak Signal-to-Noise Ratio (PSNR).
- Hasil menunjukkan bahwa metode *median filter* efektif untuk noise salt and pepper dengan tingkat noise rendah hingga menengah.

### Jurnal 2: Adaptive Median Filter dan Edge-Preserving Regularization
- Menggunakan pendekatan dua tahap:
  1. *Adaptive median filter* untuk mendeteksi pixel yang terkontaminasi noise.
  2. *Edge-preserving regularization* untuk memulihkan citra tanpa mengaburkan tepi.
- Dapat menangani noise hingga 90% dengan hasil yang lebih baik dibandingkan *median filter* konvensional.

## Hasil dan Pembahasan
| Metode | Efektivitas pada Noise Rendah | Efektivitas pada Noise Tinggi | Preservasi Detail |
|--------|-----------------------------|----------------------------|------------------|
| Median Filter | Baik | Buruk (detail hilang) | Tidak Optimal |
| Adaptive Median Filter + Regularization | Baik | Sangat Baik | Optimal |

- *Median filter* bekerja dengan baik untuk noise tingkat rendah tetapi menghilangkan detail pada noise tinggi.
- Metode adaptif yang diusulkan dalam jurnal IEEE lebih efektif dalam mempertahankan detail citra dan menangani noise dengan intensitas tinggi.

## Kesimpulan
Berdasarkan perbandingan, metode *adaptive median filter* dengan *edge-preserving regularization* lebih unggul dibandingkan dengan *median filter* biasa, terutama dalam menangani noise dengan tingkat yang lebih tinggi. Oleh karena itu, metode ini direkomendasikan untuk aplikasi yang membutuhkan pelestarian detail citra yang lebih baik.

## Daftar Pustaka
1. Nurul Fadillah, Chicha Rizka Gunawan. "Mendeteksi Keakuratan Noise Salt and Pepper dengan Median Filter". *Jurnal Informatika*, Vol.6 No.1, 2019.
2. Raymond H. Chan, Chung-Wa Ho, Mila Nikolova. "Salt-and-Pepper Noise Removal by Median-Type Noise Detectors and Detail-Preserving Regularization". *IEEE Transactions on Image Processing*, Vol.14 No.10, 2005.
