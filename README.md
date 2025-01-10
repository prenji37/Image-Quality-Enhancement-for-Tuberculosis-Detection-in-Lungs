# Peningkatan Kualitas Citra untuk Deteksi Tuberkulosis pada Paru-Paru

Proyek ini bertujuan untuk meningkatkan kualitas citra radiografi paru-paru guna mendukung deteksi tuberkulosis (TB) yang lebih efisien dan akurat. Dengan menggunakan teknik pengolahan citra seperti histogram equalization, koreksi gamma, dan sharpening, proyek ini berhasil mengoptimalkan citra X-ray untuk analisis lebih lanjut.

## Daftar Isi
- [Latar Belakang](#latar-belakang)
- [Tujuan dan Manfaat](#tujuan-dan-manfaat)
- [Metode](#metode)
  - [Histogram Equalization](#histogram-equalization)
  - [Koreksi Gamma](#koreksi-gamma)
  - [Sharpening](#sharpening)
- [Hasil dan Pembahasan](#hasil-dan-pembahasan)
- [Kesimpulan](#kesimpulan)
- [Cara Penggunaan](#cara-penggunaan)
- [Referensi](#referensi)

## Latar Belakang
Tuberkulosis adalah masalah kesehatan global yang memerlukan deteksi dini untuk mencegah penyebarannya. Radiografi paru-paru memiliki potensi besar untuk mendeteksi TB, namun interpretasi manual seringkali memerlukan keahlian khusus dan bersifat subjektif. Proyek ini bertujuan untuk mengatasi keterbatasan tersebut dengan meningkatkan kualitas citra radiografi paru-paru.

## Tujuan dan Manfaat
1. Meningkatkan kualitas citra X-ray paru-paru.
2. Menggunakan metode yang efisien untuk mendeteksi tuberkulosis.
3. Meningkatkan akurasi dan kecepatan diagnosis TB.

## Metode
### Histogram Equalization
Metode ini mendistribusikan tingkat abu-abu dalam citra untuk meningkatkan kontras, sehingga detail lebih mudah terlihat.

### Koreksi Gamma
Koreksi gamma digunakan untuk menyesuaikan kecerahan citra secara non-linear, meningkatkan kontras sesuai dengan persepsi visual manusia.

### Sharpening
Teknik ini menonjolkan detail citra dengan meningkatkan kontras lokal.

## Hasil dan Pembahasan
- **Histogram Equalization**: Kontras meningkat dari 42.7 menjadi 74.0, dengan distribusi intensitas piksel yang lebih merata.
- **Koreksi Gamma**: Akurasi terbaik (99.5%) dicapai dengan gamma 0.89 untuk dataset TB dan 1.1 untuk dataset normal.
- **Sharpening**: Menggunakan sharpening mengurangi akurasi sebesar 0.8%, dari 98.1% menjadi 97.3%.

Model Support Vector Machine (SVM) mencapai akurasi **99.5%** dengan preprocessing optimal.

## Kesimpulan
Peningkatan kualitas citra menggunakan histogram equalization dan koreksi gamma berhasil meningkatkan akurasi deteksi tuberkulosis. Nilai gamma yang berbeda untuk dataset TB dan normal memberikan hasil terbaik dengan rata-rata waktu proses sekitar 7 menit.

## Cara Penggunaan
1. **Persyaratan**:
   - Python 3.12
   - Library: `opencv-python`, `numpy`, `matplotlib`, `sklearn`, `seaborn`

2. **Langkah-Langkah**:
   - Jalankan preprocessing citra menggunakan `histogram_equalization` dan `gamma_correction`.
   - Gunakan model SVM untuk klasifikasi dataset yang telah diproses.
   - Evaluasi hasil menggunakan metrik akurasi, precision, recall, dan confusion matrix.

3. **Contoh Perintah**:
   ```python
   python preprocess.py
   python train_model.py
