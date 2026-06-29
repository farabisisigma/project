# 🛍️ TokoKu — Web Penjualan Sederhana

Aplikasi web penjualan barang berbasis HTML, CSS, dan JavaScript murni. Tidak memerlukan framework, library eksternal, atau server backend. Cukup buka file di browser.

---

## 🚀 Cara Menjalankan

1. Download file `toko-online.html`
2. Buka file tersebut di browser (Chrome, Firefox, Edge, dll.)
3. Aplikasi langsung berjalan — tidak perlu instalasi apapun

---

## ✨ Fitur

### 🔍 Pencarian & Filter
- **Pencarian real-time** — ketik nama atau kategori produk, hasil langsung muncul
- **Filter kategori** — Elektronik, Fashion, Makanan, Olahraga, Rumah
- **Sortir harga** — dari termurah ke termahal, atau sebaliknya
- **Sortir rating** — produk dengan rating tertinggi tampil duluan
- **Sortir terlaris** — berdasarkan jumlah produk terjual
- **Slider harga** — filter produk berdasarkan harga maksimal

### 🛒 Keranjang Belanja
- Tambah produk tanpa batas ke keranjang
- Ubah jumlah item dengan tombol `+` dan `−`
- Hapus item dari keranjang
- Total harga terupdate otomatis

### 💳 Pembayaran
- Pilih metode pembayaran: **Transfer Bank**, **QRIS**, **COD**, **Dompet Digital**
- Konfirmasi pembayaran dengan notifikasi sukses

### 📦 Detail Produk
- Klik produk untuk membuka halaman detail
- Menampilkan deskripsi lengkap, rating, jumlah terjual
- Menampilkan ulasan dari pembeli

### 📤 Jual Produk (Seller)
- Upload foto produk langsung dari perangkat
- Isi nama, kategori, harga, dan deskripsi
- Produk langsung muncul di halaman utama setelah dipublikasikan

---

## 📁 Struktur File

```
toko-online.html
│
├── <style>          → Semua styling CSS (layout, komponen, responsif)
│
├── <body>           → Struktur HTML
│   ├── navbar       → Logo, search bar, tombol keranjang & jual
│   ├── sidebar      → Filter kategori, sortir, slider harga
│   ├── content      → Grid produk & form seller
│   ├── cart panel   → Panel keranjang (slide dari kanan)
│   └── modal        → Detail produk & ulasan
│
└── <script>         → Semua logika JavaScript
    ├── Data produk  → Array produk awal
    ├── renderGrid() → Render kartu produk ke grid
    ├── filterProducts() → Filter + sort produk
    ├── addToCart()  → Tambah produk ke keranjang
    ├── updateCartUI() → Update tampilan keranjang
    ├── openModal()  → Buka detail produk
    ├── checkout()   → Proses pembayaran
    └── submitProduct() → Publikasikan produk baru
```

---

## 🧩 Teknologi

| Teknologi | Keterangan |
|-----------|------------|
| HTML5 | Struktur halaman |
| CSS3 | Styling & animasi |
| JavaScript (Vanilla) | Semua logika aplikasi |
| FileReader API | Upload & preview foto produk |

> Tidak menggunakan framework (React, Vue, dll.) maupun library eksternal.

---

## 📝 Cara Menambah Produk Secara Manual (di Kode)

Buka file `toko-online.html`, cari bagian `let products = [...]`, lalu tambahkan objek produk baru:

```js
{
  id: 9,                          // ID unik (angka)
  name: 'Nama Produk',            // Nama produk
  cat: 'Elektronik',              // Kategori (lihat daftar di bawah)
  price: 250000,                  // Harga dalam Rupiah
  rating: 4.5,                    // Rating (0.0 - 5.0)
  sold: 100,                      // Jumlah terjual
  desc: 'Deskripsi produk...',    // Deskripsi lengkap
  reviews: [
    { author: 'Nama Pembeli', rating: 5, text: 'Isi ulasan...' }
  ]
}
```

**Kategori yang tersedia:** `Elektronik` · `Fashion` · `Makanan` · `Olahraga` · `Rumah`

---

## 🔧 Pengembangan Lanjutan

Beberapa ide untuk mengembangkan proyek ini lebih jauh:

- **Backend** — hubungkan ke Node.js / PHP untuk menyimpan data produk secara permanen
- **Database** — simpan produk dan transaksi ke MySQL / MongoDB
- **Autentikasi** — sistem login untuk pembeli dan seller
- **Pagination** — tampilkan produk per halaman jika jumlahnya banyak
- **Wishlist** — fitur simpan produk favorit
- **Riwayat transaksi** — tampilkan history pembelian
- **Responsif mobile** — optimasi tampilan untuk layar kecil

---

## 👤 Dibuat Dengan

HTML · CSS · JavaScript — tanpa dependency apapun.
