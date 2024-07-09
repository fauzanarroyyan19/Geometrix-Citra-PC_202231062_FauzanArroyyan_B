# Geometrix_Citra-PC_202231062_FauzanArroyyan_B
# TEORI 
## GEOMETRI CITRA
Geometri citra dalam pengolahan citra digital merujuk pada berbagai teknik dan operasi yang digunakan untuk memanipulasi struktur geometris citra. Tujuan dari operasi ini adalah untuk mengubah bentuk, ukuran, posisi, atau orientasi citra sesuai dengan kebutuhan. Beberapa operasi geometri citra yang umum digunakan dalam pengolahan citra digital meliputi:

1. **Translasi (Translation)**: Memindahkan citra dari satu posisi ke posisi lain tanpa mengubah bentuk atau ukurannya.
2. **Rotasi (Rotation)**: Memutar citra dengan sudut tertentu di sekitar titik pusatnya.
3. **Skalasi (Scaling)**: Mengubah ukuran citra dengan faktor skala tertentu, baik memperbesar maupun memperkecil.
4. **Shearing (Geser)**: Menggeser citra dalam satu arah sehingga bentuknya berubah, tetapi area tetap sama.
5. **Refleksi (Reflection)**: Membalik citra terhadap sumbu tertentu, seperti sumbu x atau sumbu y.
6. **Interpolasi (Interpolation)**: Menggunakan metode interpolasi untuk menentukan nilai piksel baru saat citra diubah ukurannya atau diputar.

Operasi-operasi ini penting dalam berbagai aplikasi pengolahan citra, seperti pemrosesan citra medis, pengenalan pola, visi komputer, dan banyak lagi. Penggunaan teknik-teknik ini memungkinkan analisis dan manipulasi citra secara efektif untuk mendapatkan informasi atau hasil yang diinginkan. 

## Numpy
**NumPy** (Numerical Python) adalah library fundamental untuk komputasi ilmiah dalam bahasa Python. NumPy menyediakan dukungan untuk array multidimensi objek besar dan matriks matematika yang memiliki fungsi-fungsi tingkat tinggi untuk operasi matematika di atas array tersebut.

**Fitur utama NumPy:**
- **Array multidimensi**: Struktur data utama dalam NumPy adalah array N-dimensi (ndarray), yang memungkinkan penyimpanan data dalam tabel yang efisien dan manipulasi matematika.
- **Operasi vektor**: NumPy memungkinkan operasi aritmetika dan logika pada array dengan kecepatan yang sangat tinggi dibandingkan dengan perulangan tradisional dalam Python.
- **Fungsi matematika**: Menyediakan berbagai fungsi matematika seperti aljabar linier, transformasi Fourier, dan statistik.
- **Integrasi**: NumPy dapat dengan mudah diintegrasikan dengan bahasa lain seperti C, C++, dan Fortran untuk mempercepat proses komputasi.

## OpenCV (cv2)
**OpenCV** (Open Source Computer Vision Library) adalah library sumber terbuka yang digunakan untuk pengolahan citra dan visi komputer. Library ini awalnya dikembangkan oleh Intel dan sekarang dikelola oleh organisasi OpenCV.

**Fitur utama OpenCV:**
- **Pengolahan Citra**: Menyediakan berbagai fungsi untuk membaca, menulis, dan memproses citra, seperti deteksi tepi, segmentasi, dan pengenalan pola.
- **Visi Komputer**: Mendukung berbagai algoritma untuk visi komputer seperti deteksi objek, pengenalan wajah, dan analisis video.
- **Efisiensi dan Kecepatan**: Ditulis sebagian besar dalam C/C++ untuk efisiensi, tetapi menyediakan binding Python untuk kemudahan penggunaan.
- **Platform Multiplatform**: Dapat digunakan di berbagai platform seperti Windows, Linux, macOS, Android, dan iOS.

## Matplotlib.pyplot
**Matplotlib** adalah library plotting komprehensif untuk visualisasi data dalam bahasa Python. `matplotlib.pyplot` adalah modul dalam Matplotlib yang menyediakan antarmuka seperti MATLAB untuk pembuatan grafik.

**Fitur utama Matplotlib.pyplot:**
- **Pembuatan Grafik**: Dapat membuat berbagai jenis grafik seperti garis, scatter, bar, histogram, dan pie chart.
- **Antarmuka Mudah**: `pyplot` menyediakan antarmuka yang sederhana dan mudah digunakan untuk membuat dan menyesuaikan grafik.
- **Kontrol Lengkap**: Memungkinkan kontrol penuh atas elemen-elemen grafik seperti sumbu, label, legenda, dan anotasi.
- **Kompatibilitas**: Dapat digunakan bersama dengan library lain seperti NumPy dan Pandas untuk visualisasi data yang diolah.



## Rotated Image (Citra yang Diputar)

Definisi: Citra yang diputar adalah citra yang telah diubah orientasinya dengan memutar seluruh citra pada sudut tertentu di sekitar titik pusat atau titik lain yang ditentukan. 

Contoh Penggunaan: Memutar gambar sebesar 90 derajat untuk mengubah orientasi dari potret ke lanskap.

## Resized Image (Citra yang Diubah Ukurannya)
Definisi: Citra yang diubah ukurannya adalah citra yang telah diperbesar atau diperkecil dengan mengubah jumlah piksel dalam dimensi horizontal dan vertikal. 

Contoh Penggunaan: Mengurangi ukuran gambar untuk menghemat ruang penyimpanan atau memperbesar gambar untuk memperjelas detail.

## Cropped Image (Citra yang Dipotong)
Definisi: Citra yang dipotong adalah citra yang telah diambil sebagian dari keseluruhan citra asli berdasarkan koordinat batas yang ditentukan. 

Contoh Penggunaan: Memotong bagian yang tidak diinginkan dari sebuah foto untuk fokus pada objek utama.

## Flipped Image (Citra yang Dibalik)
Definisi: Citra yang dibalik adalah citra yang telah dipantulkan terhadap sumbu vertikal atau horizontal sehingga menghasilkan efek cermin. 

Contoh Penggunaan: Membalik gambar secara horizontal untuk mendapatkan cermin dari gambar asli.

## Translated Image (Citra yang Ditranslasi)
Definisi: Citra yang ditranslasi adalah citra yang telah dipindahkan dari satu posisi ke posisi lain tanpa mengubah bentuk atau orientasinya. 

Contoh Penggunaan: Memindahkan gambar ke kanan atau ke bawah untuk mengubah lokasi objek dalam kanvas.

### TAHAPAN PROJEK 
Berikut adalah penjelasan tentang fungsi dari program yang telah Anda tulis untuk mengoperasikan berbagai transformasi geometri pada citra menggunakan library OpenCV (`cv2`), NumPy, dan Matplotlib:

### Penjelasan Program

1. **Import Library**
   ```python
   import cv2
   import numpy as np
   import matplotlib.pyplot as plt
   ```
   - Mengimpor library yang diperlukan: `cv2` untuk pengolahan citra, `numpy` untuk operasi matematika pada array, dan `matplotlib.pyplot` untuk visualisasi citra.

2. **Membaca Citra Asli**
   ```python
   img = cv2.imread('royyan.jpg')
   ```
   - Membaca citra asli dari file `royyan.jpg` dan menyimpannya dalam variabel `img`.

3. **Menampilkan Citra Asli**
   ```python
   plt.subplot(2, 3, 1)
   plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
   plt.title('Original Image')
   plt.axis('off')
   ```
   - Menampilkan citra asli dalam subplot pertama (posisi 1 dari grid 2x3) setelah mengonversi format warna dari BGR (format default OpenCV) ke RGB (format yang digunakan Matplotlib).

4. **Rotasi Citra**
   ```python
   (h, w) = img.shape[:2]
   center = (w // 2, h // 2)
   M = cv2.getRotationMatrix2D(center, 45, 1.0)
   img_rotated = cv2.warpAffine(img, M, (w, h))
   plt.subplot(2, 3, 2)
   plt.imshow(cv2.cvtColor(img_rotated, cv2.COLOR_BGR2RGB))
   plt.title('Rotated Image')
   plt.axis('off')
   ```
   - Menghitung pusat citra.
   - Membuat matriks rotasi untuk memutar citra sebesar 45 derajat di sekitar pusat citra.
   - Menerapkan rotasi menggunakan fungsi `cv2.warpAffine` dan menampilkan hasilnya pada subplot kedua.

5. **Mengubah Ukuran Citra (Resizing)**
   ```python
   img_resized = cv2.resize(img, (img.shape[1]//3, img.shape[0]//2))
   plt.subplot(2, 3, 3)
   plt.imshow(cv2.cvtColor(img_resized, cv2.COLOR_BGR2RGB))
   plt.title('Resized Image')
   plt.axis('off')
   ```
   - Mengubah ukuran citra menjadi sepertiga lebar asli dan setengah tinggi asli menggunakan fungsi `cv2.resize`.
   - Menampilkan hasil perubahan ukuran pada subplot ketiga.

6. **Memotong Citra (Cropping)**
   ```python
   img_cropped = img[0:img.shape[0]//2, 0:img.shape[1]//2]
   plt.subplot(2, 3, 4)
   plt.imshow(cv2.cvtColor(img_cropped, cv2.COLOR_BGR2RGB))
   plt.title('Cropped Image')
   plt.axis('off')
   ```
   - Memotong citra untuk mendapatkan bagian seperempat dari citra asli (kuartal kiri atas).
   - Menampilkan hasil pemotongan pada subplot keempat.

7. **Membalik Citra (Flipping)**
   ```python
   img_flipped = cv2.flip(img, 1)
   plt.subplot(2, 3, 5)
   plt.imshow(cv2.cvtColor(img_flipped, cv2.COLOR_BGR2RGB))
   plt.title('Flipped Image')
   plt.axis('off')
   ```
   - Membalik citra secara horizontal menggunakan fungsi `cv2.flip` dengan parameter `1` yang menunjukkan flip horizontal.
   - Menampilkan hasil pembalikan pada subplot kelima.

8. **Translasi Citra**
   ```python
   rows, cols = img.shape[:2]
   M_translate = np.float32([[1, 0, 250], [0, 1, 180]])
   img_translated = cv2.warpAffine(img, M_translate, (cols, rows))
   plt.subplot(2, 3, 6)
   plt.imshow(cv2.cvtColor(img_translated, cv2.COLOR_BGR2RGB))
   plt.title('Translated Image')
   plt.axis('off')
   ```
   - Membuat matriks translasi untuk menggeser citra sebesar 250 piksel ke kanan dan 180 piksel ke bawah.
   - Menerapkan translasi menggunakan fungsi `cv2.warpAffine` dan menampilkan hasilnya pada subplot keenam.

9. **Mengatur dan Menampilkan Layout**
   ```python
   plt.tight_layout()
   plt.show()
   ```
   - Menyusun layout agar subplot tidak saling bertabrakan.
   - Menampilkan semua subplot pada satu figur.

### Fungsi dari Program
Program di atas membaca citra asli dan kemudian menerapkan berbagai transformasi geometri pada citra tersebut, seperti rotasi, perubahan ukuran, pemotongan, pembalikan, dan translasi. Setiap hasil transformasi ditampilkan dalam subplot yang berbeda menggunakan Matplotlib untuk visualisasi. Program ini berguna untuk demonstrasi dan pemahaman operasi geometri dasar pada citra digital.

