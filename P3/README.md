# Tugas Pemrograman Web - Tampilan Instagram

## Versi Bootstrap
# Tugas Pemrograman Web - Tampilan Instagram

## 📖 Deskripsi Project
Aku bikin tampilan mirip Instagram pakai Bootstrap 5 dari CDN, jadi nggak perlu install apa-apa lagi.  
Struktur halaman yang aku buat:  
- *Header: foto profil, username, tombol *Edit Profile / Follow, info jumlah post, followers, dan following.  
- *Bio singkat* pengguna.  
- *Feed*: ada 12 foto postingan dengan ukuran sama. Susunan foto dibuat responsif:  
  - Mobile (≤576px): 1 kolom  
  - Tablet (≥768px): 2–3 kolom  
  - Desktop (≥992px): 4–6 kolom  
- *Footer* sederhana di bagian bawah.  

Tambahan: saat hover di postingan muncul icon like, komen, dan share beserta jumlahnya.  

File utama yang dipakai: *index.html*  

---

## 📂 Struktur File Project
- *index.html* → halaman utama (isi header profil, bio, feed foto, footer).  
- *assets/css/custom.css* → styling tambahan di luar bawaan Bootstrap.  
- *assets/img/* → folder khusus untuk gambar feed dan foto profil.  

---

## 🚀 Cara Jalanin Project
1. Buka file *index.html* langsung di browser (Chrome, Edge, dll).  
2. Pastikan folder *assets/* (img + css) ada di tempat yang sama dengan index.html.  
3. Nggak perlu build atau install apa-apa karena ini full HTML + Bootstrap CDN.  

---

## 📦 Dependensi
- *Bootstrap 5* (via CDN) → dipakai buat grid system, komponen tombol, navbar, dll.  
- *Custom CSS* (opsional) → buat tambahan styling biar tampilannya lebih rapi.  

---

## ❓ Jawaban Pertanyaan README  

*1. Kenapa milih konfigurasi col tertentu untuk tiap breakpoint?*  
Karena ukuran layar beda-beda, jadi biar layout tetap enak dilihat di semua device. Kalau di HP layar kecil, cukup 1 kolom supaya foto feed nggak terlalu kecil. Di tablet agak lebar, jadi aku pakai 2–3 kolom. Nah di desktop lebih lega lagi, bisa 4 sampai 6 kolom biar tampilannya mirip Instagram beneran dan lebih efisien.  

*2. Gimana memastikan tombol Follow/Edit Profile tetap mudah dijangkau di mobile?*  
Aku taruh tombolnya pakai grid dan utilities Bootstrap biar posisinya responsif. Jadi kalau di desktop bisa sejajar dengan bio, tapi di mobile otomatis pindah ke bawah bio biar gampang di-klik pakai jempol. Intinya pakai class order dan spacing bawaan Bootstrap.  

*3. Kalau postingan nambah jadi 50, potensi masalah apa dan gimana solusinya?*  
Kalau jumlahnya banyak banget, masalahnya grid bisa kelihatan terlalu panjang ke bawah, jadi user mesti scroll jauh. Solusinya bisa bikin sistem pagination (halaman 1, 2, dst) atau pakai fitur "load more" biar nggak numpuk semua di satu halaman. Dari sisi grid nggak masalah sih, tinggal lanjut otomatis ke row berikutnya, tapi dari UX lebih enak kalau dipotong per bagian.

---

## Versi Tailwind
# Tugas Pemrograman Web - Tampilan Instagram (Tailwind CSS)

## 📖 Deskripsi Project
Kalau yang ini aku pakai *Tailwind CSS*.  
Tailwind aku ambil langsung dari CDN, jadi semua styling udah ada di dalam HTML.  
Nggak perlu bikin file CSS terpisah karena Tailwind emang pakai utility classes.  

Tampilannya hampir sama kayak versi Bootstrap yang sebelumnya:  
- Foto profil bulat dengan ukuran sesuai IG.  
- Username + tombol Edit Profile / Follow + info jumlah post, followers, following.  
- Feed foto ada 12 gambar dengan ukuran seragam.  
- Hover di foto muncul icon like, komen, dan share plus jumlahnya.  

Struktur yang aku buat:  
- *Header*: profil, username, tombol interaksi, info post/followers/following.  
- *Bio singkat* pengguna.  
- *Feed*: responsif sesuai device:  
  - Mobile (default): grid-cols-1  
  - Tablet (md): grid-cols-2 atau grid-cols-3  
  - Desktop (lg): grid-cols-4 atau lebih  
- *Footer* sederhana di bawah.  

File utama yang dipakai: *index.html* (sebelumnya aku simpan dengan nama index-tailwind.html).  

---

## 📂 Struktur File Project
- *index.html* → halaman utama (isi profil, bio, feed, footer).  
- *assets/img/* → folder gambar (foto profil + feed).  
- *README.md* → penjelasan desain + jawaban reflektif.  
- (Opsional) file config Tailwind kalau build manual.  

---

## 🚀 Cara Jalanin Project
1. Buka file *index.html* langsung di browser (Chrome/Edge).  
2. Pastikan folder *assets/img/* ada di tempat yang sama dengan index.html.  
3. Tailwind dipakai via CDN, jadi nggak perlu setup atau install NodeJS.  

---

## 📦 Dependensi
- *Tailwind CSS (CDN)* → dipakai buat semua styling (grid, flex, spacing, alignment, dll).  

---

## ❓ Jawaban Pertanyaan README

*1. Kenapa pilih grid-cols/gap tertentu buat tiap breakpoint?*  
Karena ukuran layar beda-beda. Kalau di HP, feed 1 kolom biar fotonya jelas. Di tablet bisa 2–3 kolom supaya lebih rapat. Nah di desktop lebih lebar, jadi aku pakai 4 kolom atau lebih biar mirip feed IG asli.  

*2. Gimana manfaatin utility responsive Tailwind buat masalah layout di mobile?*  
Aku pakai class bawaan kayak sm:, md:, lg: biar layout otomatis adaptif. Misalnya tombol Edit Profile kalau di desktop bisa sejajar sama bio, tapi di mobile aku atur biar pindah ke bawah bio supaya gampang di-klik jempol. Jadi nggak perlu bikin CSS custom tambahan.  

*3. Trade-off antara pakai banyak utility classes vs bikin component CSS sendiri?*  
Kalau pakai utility classes, enaknya lebih cepat dan fleksibel, tinggal tambahin class aja udah jadi. Kekurangannya, HTML bisa kelihatan rame banget. Kalau bikin CSS component sendiri lebih rapi dan reusable, tapi agak ribet karena harus nulis file CSS tambahan. Untuk project kecil kayak gini, pakai utility class langsung udah cukup.

---

## Catatan
Dari dua versi ini, sebenarnya hasilnya mirip, cuma cara pakai CSS frameworknya aja yang beda:
- Bootstrap lebih banyak pakai class bawaan (misalnya row, col-4, card, dll).
- Tailwind lebih fleksibel karena styling langsung ditulis di HTML pakai utility classes.

Jadi kesimpulannya, dua-duanya bisa dipakai buat bikin tampilan IG sederhana sesuai tugas.