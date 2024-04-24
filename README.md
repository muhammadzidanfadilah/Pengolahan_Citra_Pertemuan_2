# Tugas Pengolahan Citra 2


| NIM | 312210277 |
| --- | --- |
| NAMA |  MUHAMMAD ZIDAN FADILLAH |
| KELAS | TI.22.A.2 |





# Tugas Pada Pertemuan 2

# Link video penjelasan mengenai tugas di bawah ini 

| Link YouTube: | https://youtu.be/QVzNJ2SZ34g  |
| --- | --- |

| Link Tiktok: | https://www.tiktok.com/@muhammadzidanfadillah08/video/7361486244234218768?is_from_webapp=1&sender_device=pc&web_id=7345347257934480898 |
| --- | --- |



# Tugas 

Impor pustaka yang diperlukan:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

Baca gambar masukan menggunakan OpenCV:


```
img = cv2.imread("upb.jpg")
```

Tampilkan gambar asli menggunakan Matplotlib:

[:,:,::-1] digunakan untuk mengonversi format BGR (digunakan oleh OpenCV) menjadi format RGB (digunakan oleh Matplotlib).

```
plt.imshow(img[:,:,::-1])
plt.show()
```



Tentukan empat titik masukan (inputPts) dan titik destinasi yang sesuai (outputPts) untuk transformasi perspektif:

```
inputPts = np.float32([[4,381],
                      [266,429],
                      [329,68],
                      [68,20]])

outputPts = np.float32([[0,300],
                       [300,300],
                       [300,0],
                       [0,0]])
```
                       
Hitung matriks transformasi perspektif (M) menggunakan cv2.getPerspectiveTransform():

```
M = cv2.getPerspectiveTransform(inputPts, outputPts)

```

Terapkan transformasi perspektif pada gambar masukan menggunakan cv2.warpPerspective():

```
dst = cv2.warpPerspective(img, M, (300,300))
  
```
Gambar hasil (dst) akan menjadi versi gambar yang telah mengalami transformasi perspektif.


Kembali, [:,:,::-1] digunakan untuk mengonversi format BGR menjadi RGB sebelum menyimpan gambar.

```
plt.imshow(dst[:,:,::-1])
plt.show()

```

# Hasil 
![LL](https://github.com/muhammadzidanfadilah/Pengolahan_Citra_Pertemuan_2/assets/115553474/113500dc-9ebc-4d8f-8105-9d3745924b56)
![LL1](https://github.com/muhammadzidanfadilah/Pengolahan_Citra_Pertemuan_2/assets/115553474/243df02c-583a-4ba9-a4c8-40e1cd206f63)

