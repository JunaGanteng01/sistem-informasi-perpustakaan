# Use Case Sistem Informasi Perpustakaan

Use case itu gambaran apa saja yang bisa dilakukan setiap pengguna di dalam sistem.

## 1. Aktor
- **Admin / Pustakawan**
- **Anggota** (mahasiswa dan dosen)
- **Kepala Perpustakaan**

## 2. Daftar Use Case

### Admin / Pustakawan
| No | Use Case | Keterangan |
|----|----------|------------|
| 1 | Login | Masuk ke sistem pakai username dan password |
| 2 | Kelola data buku | Tambah, ubah, hapus, dan lihat data buku |
| 3 | Kelola data anggota | Daftarkan anggota baru dan ubah data anggota |
| 4 | Catat peminjaman | Input buku yang dipinjam anggota |
| 5 | Catat pengembalian | Input buku yang dikembalikan, sistem cek terlambat atau nggak |
| 6 | Kelola denda | Melihat dan mencatat pembayaran denda |

### Anggota
| No | Use Case | Keterangan |
|----|----------|------------|
| 1 | Login | Masuk pakai NIM/NIP dan password |
| 2 | Cari buku | Cari berdasarkan judul, penulis, atau kategori |
| 3 | Lihat ketersediaan buku | Cek stok buku yang masih bisa dipinjam |
| 4 | Lihat riwayat peminjaman | Melihat buku yang pernah dan sedang dipinjam |
| 5 | Lihat denda | Cek apakah ada denda yang belum dibayar |

### Kepala Perpustakaan
| No | Use Case | Keterangan |
|----|----------|------------|
| 1 | Login | Masuk ke sistem |
| 2 | Lihat laporan | Rekap peminjaman, buku populer, dan anggota aktif |

## 3. Alur Peminjaman Buku
1. Anggota cari buku di sistem dan cek apakah stoknya ada.
2. Anggota datang ke perpustakaan bawa kartu anggota / KTM.
3. Pustakawan input data peminjaman (anggota, buku, tanggal pinjam).
4. Sistem otomatis mengurangi stok buku dan menentukan batas kembali (7 hari).
5. Data peminjaman tersimpan di database cloud.

## 4. Alur Pengembalian Buku
1. Anggota mengembalikan buku ke pustakawan.
2. Pustakawan input pengembalian di sistem.
3. Sistem cek tanggal kembali. Kalau lewat dari batas, denda dihitung otomatis.
4. Stok buku bertambah lagi.
