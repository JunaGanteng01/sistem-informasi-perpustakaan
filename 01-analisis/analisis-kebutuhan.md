# Analisis Kebutuhan Sistem Informasi Perpustakaan

## 1. Nama Sistem
Sistem Informasi Perpustakaan (SIPUS)

## 2. Latar Belakang
Selama ini pencatatan di perpustakaan masih banyak yang manual, misalnya pakai buku besar
atau file Excel di satu komputer. Cara ini bikin petugas repot, data gampang hilang, dan
anggota harus datang langsung cuma buat ngecek buku yang mau dipinjam ada atau nggak.

## 3. Tujuan Sistem
- Mempermudah pustakawan dalam mengelola data buku dan anggota.
- Mempercepat proses peminjaman dan pengembalian buku.
- Membantu anggota mencari buku dan cek ketersediaannya secara online.
- Menyediakan laporan perpustakaan dengan cepat untuk kepala perpustakaan.

## 4. Pengguna Sistem
| Pengguna | Peran |
|----------|-------|
| Admin / Pustakawan | Mengelola data buku, anggota, transaksi, dan denda |
| Anggota | Mencari buku, melihat status dan riwayat peminjaman |
| Kepala Perpustakaan | Melihat laporan dan rekap aktivitas perpustakaan |

## 5. Jenis Informasi yang Dikelola
- Data buku (judul, penulis, penerbit, tahun terbit, kategori, stok)
- Data anggota (nama, NIM/NIP, kontak, status keanggotaan)
- Data peminjaman dan pengembalian
- Data denda keterlambatan
- Laporan perpustakaan
- File digital (e-book, jurnal, cover buku)

## 6. Kebutuhan Fungsional
1. Admin bisa menambah, mengubah, dan menghapus data buku.
2. Admin bisa mengelola data anggota.
3. Admin bisa mencatat peminjaman dan pengembalian buku.
4. Sistem bisa menghitung denda otomatis kalau terlambat mengembalikan.
5. Anggota bisa mencari buku berdasarkan judul, penulis, atau kategori.
6. Anggota bisa melihat riwayat peminjaman.
7. Kepala perpustakaan bisa melihat laporan bulanan.

## 7. Kebutuhan Non-Fungsional
1. Sistem bisa diakses lewat browser di laptop maupun HP.
2. Ada login dan hak akses yang berbeda untuk tiap pengguna.
3. Data dibackup secara rutin.
4. Sistem tetap lancar walaupun banyak yang akses bersamaan (misalnya musim ujian).

## 8. Kebutuhan terhadap Layanan Cloud
| Kebutuhan | Layanan Cloud |
|-----------|---------------|
| Menyimpan data buku, anggota, transaksi | Managed database |
| Menyimpan e-book dan cover buku | Object storage |
| Menjalankan aplikasi web | Hosting / PaaS |
| Menambah kapasitas saat ramai | Autoscaling |
| Mencegah data hilang | Backup otomatis |
| Menyimpan dokumentasi sistem | GitHub (SaaS) |
