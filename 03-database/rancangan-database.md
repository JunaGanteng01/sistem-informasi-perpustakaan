# Rancangan Database Sistem Informasi Perpustakaan

Database ini rencananya disimpan di layanan **managed relational database** di cloud,
jadi backup dan perawatannya sebagian besar diurus penyedia cloud.

## 1. Tabel `buku`
| Kolom | Tipe Data | Keterangan |
|-------|-----------|------------|
| id_buku | INT (PK) | Kode unik buku |
| judul | VARCHAR(150) | Judul buku |
| penulis | VARCHAR(100) | Nama penulis |
| penerbit | VARCHAR(100) | Nama penerbit |
| tahun_terbit | YEAR | Tahun terbit |
| kategori | VARCHAR(50) | Contoh: Pemrograman, Jaringan, Umum |
| stok | INT | Jumlah buku yang tersedia |

## 2. Tabel `anggota`
| Kolom | Tipe Data | Keterangan |
|-------|-----------|------------|
| id_anggota | INT (PK) | Kode unik anggota |
| nim_nip | VARCHAR(20) | NIM mahasiswa atau NIP dosen |
| nama | VARCHAR(100) | Nama lengkap |
| no_hp | VARCHAR(15) | Nomor HP |
| status | VARCHAR(10) | Aktif / Nonaktif |

## 3. Tabel `peminjaman`
| Kolom | Tipe Data | Keterangan |
|-------|-----------|------------|
| id_pinjam | INT (PK) | Kode transaksi |
| id_anggota | INT (FK) | Anggota yang meminjam |
| id_buku | INT (FK) | Buku yang dipinjam |
| tgl_pinjam | DATE | Tanggal pinjam |
| batas_kembali | DATE | Batas pengembalian |
| tgl_kembali | DATE | Tanggal dikembalikan (kosong kalau belum) |

## 4. Relasi Antar Tabel
- Satu **anggota** bisa punya banyak **peminjaman**.
- Satu **buku** bisa dipinjam berkali-kali (banyak **peminjaman**).

## 5. Tabel `denda`
| Kolom | Tipe Data | Keterangan |
|-------|-----------|------------|
| id_denda | INT (PK) | Kode unik denda |
| id_pinjam | INT (FK) | Transaksi peminjaman yang terlambat |
| jumlah_hari | INT | Jumlah hari keterlambatan |
| total_denda | INT | Rp1.000 x jumlah hari terlambat |
| status_bayar | VARCHAR(15) | Lunas / Belum Lunas |

- Satu **peminjaman** maksimal punya satu **denda**.
