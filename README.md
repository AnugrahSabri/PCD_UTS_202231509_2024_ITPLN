# PCD_UTS_202231509_2024_ITPLN
PROJECT UTS PENGOLAHAN CITRA 2024

Pada project UTS pengolahan citra kali ini akan dibahas deteksi warna pada citra, urutkan ambang batas terkecil sampai dengan terbesar.
1. DETEKSI WARNA PADA CITRA
Pertama kita import library seperti code dibawah ini :
import cv2 import numpy as np import matplotlib.pyplot as plt

Kode tersebut mengimpor tiga pustaka yang berbeda:
cv2: OpenCV untuk pemrosesan citra.
matplotlib.pyplot as plt: Matplotlib untuk membuat plot dan grafik.
numpy as np: NumPy untuk komputasi numerik.
Kemudian membaca data gambar dengan code dibawa ini : img = cv2.imread('gambar_nama.jpg') img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB) hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)

Coding tersebut bertujuan untuk membaca file gambar "parking_lot.jpeg" dan menyimpannya dalam variabel img menggunakan OpenCV.

sedangkan cv2.cvtColor(img, cv2.COLOR_BGR2RGB): Ini adalah fungsi yang digunakan untuk mengubah ruang warna gambar. Dalam hal ini, gambar yang dibaca sebelumnya (img) dikonversi dari format BGR (Blue-Green-Red) ke format RGB (Red-Green-Blue). Karena OpenCV membaca gambar dalam format BGR secara default, tetapi dalam banyak kasus, kita lebih suka menggunakan format RGB.

sedangkan cv2.cvtColor(img, cv2.COLOR_BGR2HSV): Ini adalah fungsi yang sama untuk mengubah ruang warna, tetapi kali ini mengonversi dari BGR ke HSV (Hue-Saturation-Value). HSV adalah model warna yang sangat berguna dalam pengolahan citra, terutama untuk deteksi warna, karena memisahkan informasi warna (hue), kejenuhan (saturation), dan nilai (value/brightness).

Kemudian mendefinisikan warna dari semua warna

