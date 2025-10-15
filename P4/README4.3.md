# Penjelasan Praktikum 4.3

## Soal
Ubah baris 5 menjadi:
html link rel="stylesheet" type="text/css" href="#"

Jalankan di browser, lalu amati hasilnya.


# Analisis 
Awalnya baris 5 berisi:

link rel="stylesheet" type="text/css" href="style.css"

Kode ini berfungsi untuk menghubungkan file HTML dengan file CSS eksternal bernama style.css.
Jika file CSS tersebut ada dan benar, maka semua aturan gaya (warna, background, ukuran teks, dll) akan diterapkan ke halaman web.

Namun setelah diubah menjadi:

<link rel="stylesheet" type="text/css" href="#">

Browser tidak bisa menemukan file CSS yang valid, karena # bukanlah alamat file CSS, hanya placeholder link kosong.


# Hasil di Browser

Tampilan halaman web jadi polos, hanya mengikuti gaya bawaan HTML.

Semua style dari file style.css tidak dijalankan.

Dengan kata lain, desain (warna, background, ukuran teks) hilang.


# Kesimpulan 

Tampilannya berubah,Karena saat kita pakai href="#", sebenarnya kita nggak ngasih alamat file CSS yang bener. Browser bingung harus ambil style dari mana. Akhirnya, halaman ditampilkan pakai style default HTML aja, tanpa ada efek desain dari CSS yang sudah kita buat sebelumnya.