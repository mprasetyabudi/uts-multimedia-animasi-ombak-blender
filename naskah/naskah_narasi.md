# Naskah dan Storyboard: Cara Membuat Animasi Gelombang Ombak Air di Blender

M. PRASETYABUDI · NIM 1412240044 · Proyek UTS Multimedia (Opsi 4)

Naskah ini menjadi acuan saat mengisi suara dan menyusun caption. Narasi di video final ditulis ulang dan dibacakan sendiri dengan gaya bahasa sendiri, jadi kalimatnya tidak sama persis dengan naskah ini.

Waktu di tabel mengikuti rekaman layar asli (4 menit 11 detik, 1920 x 1080, 60 fps, tanpa suara). Pada video final, rekaman ini sudah dipotong, dizoom, dan diberi pembuka serta penutup, sehingga durasinya menjadi 4 menit 25 detik.

## Tujuan belajar

Setelah menonton, penonton bisa:

1. Membuat permukaan laut dengan Ocean modifier.
2. Menggerakkan ombak dengan keyframe pada nilai Time.
3. Membuat material air yang mengilap dan tembus pandang, lengkap dengan buih putih di puncak ombak.

## Pembuka

| Waktu | Di layar | Narasi |
| --- | --- | --- |
| Pembuka | Judul video | Halo semuanya! Di video ini kita belajar membuat animasi ombak laut di Blender. Kita mulai dari membuat permukaan laut, menggerakkan ombaknya, sampai memberi material air lengkap dengan buihnya. |

## Bagian 1: Membuat permukaan laut

| Waktu | Di layar | Narasi |
| --- | --- | --- |
| 0:02 – 0:10 | Blender terbuka, kubus dihapus | Buka Blender. Di sini saya memakai Blender versi 4.2. Pertama, hapus kubus bawaan dengan memilihnya lalu tekan Delete. |
| 0:10 – 0:14 | Menu Add, Mesh, Plane | Tekan Shift A, lalu pilih Mesh, Plane. |
| 0:14 – 0:20 | Plane diperbesar | Perbesar plane dengan menekan S lalu geser mouse. Plane inilah yang nanti menjadi lautnya. |
| 0:20 – 0:26 | Add Modifier, cari Ocean | Buka tab Modifier yang berlogo kunci pas. Klik Add Modifier, lalu ketik Ocean di kolom pencarian. |
| 0:26 – 0:36 | Resolution dan Render diubah ke 12 | Plane langsung berubah menjadi permukaan laut. Naikkan nilai Resolution dan Render menjadi 12 supaya detail ombaknya lebih halus. |
| 0:36 – 0:44 | Waves, Scale diubah ke 3 | Buka bagian Waves, lalu ubah Scale menjadi 3. Hasilnya, ombak menjadi lebih tinggi dan besar. |
| 0:44 – 0:54 | Foam dicentang, Data Layer diisi Ocean | Selanjutnya centang Foam untuk membuat buih. Di kolom Data Layer, ketik Ocean. Nama ini nanti kita pakai lagi di material. |
| 0:54 – 1:04 | Tampilan diputar | Putar tampilan untuk melihat ombak dari berbagai sisi. Ingat, Resolution yang terlalu tinggi membuat Blender berat, jadi sesuaikan dengan kemampuan laptop. |

## Bagian 2: Menggerakkan ombak

| Waktu | Di layar | Narasi |
| --- | --- | --- |
| 1:04 – 1:12 | Timeline diperbesar, End diubah ke 100 | Sekarang kita buat ombaknya bergerak. Perbesar panel Timeline, lalu ubah End menjadi 100 frame, atau sekitar 4 detik. |
| 1:12 – 1:20 | Klik kanan Time, Insert Keyframe | Di frame 1, klik kanan pada kolom Time, lalu pilih Insert Keyframe. Kolomnya akan berubah kuning. |
| 1:20 – 1:30 | Frame 100, Time diubah ke 3, klik ikon keyframe | Pindah ke frame 100. Ubah Time menjadi 3, lalu klik ikon belah ketupat di sampingnya untuk membuat keyframe kedua. |
| 1:30 – 1:40 | Dope Sheet, Interpolation Mode, Linear | Secara bawaan, gerakan melambat di awal dan akhir. Pilih kedua keyframe, klik kanan, Interpolation Mode, lalu Linear, supaya kecepatan ombak stabil. |
| 1:40 – 1:48 | Random Seed diubah ke 1 | Ubah juga Random Seed menjadi 1 untuk mendapatkan pola ombak yang berbeda. Sekarang kita beri material supaya terlihat seperti air sungguhan. |

## Bagian 3: Membuat material air

| Waktu | Di layar | Narasi |
| --- | --- | --- |
| 1:48 – 1:58 | Tab Shading, Material, New | Pindah ke tab Shading di bagian atas. Buka tab Material, lalu klik New. Blender otomatis membuat node Principled BSDF. |
| 1:58 – 2:16 | Node Add Shader disisipkan | Di Shader Editor, geser node Material Output ke kanan supaya ada ruang. Tekan Shift A, ketik Add, lalu pilih Add Shader. Letakkan node ini di garis antara Principled BSDF dan Material Output, supaya dua shader bisa digabung. |
| 2:16 – 2:24 | Node Emission ditambahkan | Tambahkan node Emission, lalu sambungkan ke input Shader kedua pada Add Shader. Emission inilah yang membuat buih tampak putih terang. |
| 2:24 – 2:36 | Node Color Ramp ditambahkan | Berikutnya, tambahkan node Color Ramp. Sambungkan output Color-nya ke input Strength pada Emission. Jadi Color Ramp mengatur seberapa terang buihnya. |
| 2:36 – 2:50 | Node Attribute, Name diisi Ocean | Tambahkan node Attribute. Di kolom Name, ketik Ocean, sama dengan nama Data Layer pada Foam tadi. Sambungkan output Color dari Attribute ke input Fac pada Color Ramp. |
| 2:50 – 3:06 | Base Color diubah ke biru muda | Dengan begitu, bagian ombak yang berbuih akan bersinar putih. Sekarang klik Base Color pada Principled BSDF, lalu pilih warna biru muda sebagai warna dasar air. |
| 3:06 – 3:12 | Roughness diubah ke 0 | Turunkan Roughness menjadi 0 supaya permukaan air mengilap. |
| 3:12 – 3:20 | Transmission, Weight diubah ke 1 | Buka bagian Transmission dan ubah Weight menjadi 1. Air sekarang tembus pandang dan memantulkan lingkungan di sekitarnya. |
| 3:20 – 3:42 | Warna dasar disesuaikan, tampilan diputar | Warna dasarnya bisa disesuaikan. Geser ke biru kehijauan atau biru tua sampai mirip air laut. Perhatikan buih putih di puncak ombak. Itu hasil dari Foam, Attribute, dan Emission yang kita buat tadi. |

## Bagian 4: Hasil akhir dan penutup

| Waktu | Di layar | Narasi |
| --- | --- | --- |
| 3:42 – 3:48 | Kembali ke Layout, Material Preview | Kembali ke tab Layout, lalu aktifkan mode Material Preview. |
| 3:48 – 4:08 | Animasi diputar | Tekan Spasi untuk memutar animasi. Ombak sekarang bergerak dengan buih putih di puncaknya. Karena interpolasinya Linear, gerakannya stabil dari frame 1 sampai 100. Kalau ingin animasi lebih panjang, tambah saja nilai End dan nilai Time pada keyframe terakhir. |
| Penutup | Ringkasan dan ucapan terima kasih | Itulah cara membuat animasi gelombang ombak air di Blender. Intinya ada tiga: Ocean modifier untuk bentuk ombak, keyframe Time untuk gerakannya, dan node material untuk air serta buihnya. Terima kasih sudah menonton! |

## Teks keterangan di layar

| Waktu | Teks |
| --- | --- |
| 0:20 | Add Modifier → Ocean |
| 0:26 | Resolution: 12 · Render: 12 |
| 0:36 | Waves → Scale: 3 |
| 0:44 | Foam ✓ · Data Layer: Ocean |
| 1:06 | End: 100 frame |
| 1:12 | Frame 1 → Time: 1 |
| 1:20 | Frame 100 → Time: 3 |
| 1:30 | Interpolation Mode → Linear |
| 1:40 | Random Seed: 1 |
| 2:36 | Attribute (Name: Ocean) → Color Ramp → Emission Strength |
| 3:06 | Roughness: 0 |
| 3:12 | Transmission → Weight: 1 |
