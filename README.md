
No. 4

Teori yang mendukung mengenai projek terkait
1.	Perubahan intensitas, yaitu menggunakan kontur untuk memanfaatkan perubahan intensitas citra yang terkait dengan batas objek. Ketika ada perbedaan intensitas yang signifikan antara dua daerah citra yang berdekatan, maka akan terbentuklah kontur yang dapat digunakan untuk mengidentifikasi objek. Dan akan didasarkan pada perbedaan intensitas yang terjadi di sepanjang kontur objek dalam citra.
2.	Ekstraksi fitur, yaitu menggunakan kontur sebagai fitur yang relevan untuk membedakan objek dalam citra. Dalam analisis citra, ekstraksi fitur adalah proses mengidentifikasi dan memisahkan informasi yang penting dari citra. Dengan menggunakan deteksi menggunakan kontur, teknik pemrosesan citra, seperti deteksi tepi kita dapat mengambil fitur-fitur ini untuk mengidentifikasi objek.
3.	Pengolahan citra digital, dengan mendeteksi menggunakan kontur juga didukung oleh teori pengolahan citra digital. Maka deteksi kontur seperti canny edge detection atau metode berbasis gradient memanfaatkan konsep matematika seperti turunan dan konvolusi untuk mengungkapkan kontur dalam citra secara efisien dan dalam mendeteksi kontur yang relevan serta mengisolasi objek dalam citra.
4.	Segmentasi objek, yaitu mendeteksi menggunakan kontur dapat digunakan sebagai langkah awal dalam proses segmentasi objek. Dengan mengidentifikasi kontur yang signifikan dalam citra, kita dapat memisahkan objek dari latar belakang atau objek lain yang saling tumpang tindih. Maka dilakukan dengan menggunakan metode deteksi kontur, seperti deteksi tepi anny, transformasi hough, atau segmentasi berbasis perbedaan intensitas.
5.	Pengenalan objek, yaitu mendeteksi menggunakan kontur juga berhubungan erat dengan teori pengenalan objek. Dengan mengenali fitur-fitur kontur yang signifikan, seperti bentuk, tekstur, atau properti statistik lainnya, kita dapat mengklasifikasikan objek ke dalam kategori tertentu atau mengenali objek.

Menjelaskan Tahapan Cara Menyelesaikan projek secara detail 
1.	Import cv2 as cv, untuk mengimpor modul “CV2” yang merupakan open cv (open source computer vision library) kedalam program.
2.	Fungsi numpy as np, untuk mengimpor “numpy” dengan disingkat “np”.
3.	Fungsi matplotlib.pyplot as plt, untuk visualisai data dan pembuatan grafik.
4.	Baris pertama membaca file gambar bernama 'gambar.jpg' dan menyimpan didalam variabel gambar.
5.	Lalu fungsi cv2.cvtColor() digunakan untuk mengkonversi warna. Ini diperlukan karena OpenCV menggunakan urutan warna BGR secara default, sementara Matplotlib (yang akan digunakan untuk menampilkan gambar) mengharapkan urutan RGB.
6.	Lalu baris keenam sampai kedelapan ini mengatur grid subplot dengan 2 baris dan 2 kolom dan memilih subplot pertama. Kemudian menetapkan judul subplot ke gambar asli dan menampilkan gambar menggunakan plt.imshow().
7.	Baris kesebelas dan empat belas ini fungsinya cv2.cvtColor() digunakan lagi untuk mengkonversi gambar menjadi skala abu-abu. Kemudian, cv2, fungsi canny() menerapkan algoritma deteksi tepi canny ke gambar skala abu-abu, yang mengidentifikasi wilayah dengan perubahan intensitas yang signifikan. Lalu hasilnya disimpan dalam variabel.
8.	Lalu baris keenam belas sampai kedelapan belas ini mengatur subplot kedua, menetapkan judulnya menjadi kontur warna dan menampilkan gambarnya.
9.	Lalu baris keduapuluh satu fungsinya cv2.findContours() yang mendeteksi kontur pada gambar. Kemudian dibutuhkan gambar, mode pengambilan (cv2. RETR_EXTERNAL maka untuk mengambil hanya kontur eksternal), dan metode perkiraan kontur (CV2. CHAIN_APPROX_NONE untuk menyimpan semua titik batas) sebagai input. Jadi kontur yang dihasilkan masing-masing disimpan dalam variabel kontur.
10.	Lalu baris keduapuluh tiga sampai keduapuluh lima kode ini mengatur subplot ketiga, menetapkan judulnya menjadi color contours after contouring dan menampilkan gambar. Maka gambar tersebut tidak dimodifikasi, sehingga akan tampak sama dengan subplot sebelumnya.
11.	Lalu baris keduapuluh tujuh baris ini mencetak jumlah kontur yang ditemukan pada gambar dengan mengambil panjang daftar kontur.
12.	Kemudian baris keduapuluh sembilan Fungsi cv2.drawContours() digunakan untuk menggambar kontur yang terdeteksi pada gambar. Kemudian gambar, kontur, indeks kontur (-1 untuk menggambar semua kontur), warna (dalam format BGR, hijau), dan ketebalan (3 piksel) sebagai argumen. Maka gambar yang dimodifikasi disimpan kembali dalam variabel gambar.
13.	Selanjutnya baris ketigapuluh satu sampai ketigapuluh empat kode ini mengatur subplot keempat, menetapkan judulnya menjadi gambar dengan kontur dan menampilkan gambar yang dimodifikasi dengan kontur yang digambar.
