# SnapLedger - Photobooth Accounting System

Sistem Informasi Akuntansi berbasis web untuk bisnis photobooth. Kasir cukup input penjualan/pengeluaran; jurnal, buku besar, neraca saldo, penyesuaian, dan laporan keuangan terbentuk otomatis.

## Menjalankan
Buka `index.html` di browser (atau aktifkan GitHub Pages: Settings > Pages > branch `main`). Tidak perlu build/server.

## Struktur
- `index.html` - kerangka halaman (Tailwind CDN, Chart.js)
- `style.css` - tema Deep Violet/Indigo, glassmorphism, gaya print
- `app.js` - mesin akuntansi, modul, grafik, penyimpanan LocalStorage
- `assets/` - logo/gambar tambahan

## Alur akuntansi
Transaksi (POS/Pengeluaran) -> Jurnal Umum -> Buku Besar -> Neraca Saldo -> Jurnal Penyesuaian -> Laporan Laba Rugi & Neraca -> Close Book (jurnal penutup ke Laba Ditahan).

## Catatan
- Data disimpan di LocalStorage browser; tombol "Reset data demo" mengembalikan data awal.
- Setiap jurnal divalidasi: debit harus sama dengan kredit.
- Untuk backend Node.js/Express atau Supabase, ganti fungsi `load()` dan `save()` di `app.js` dengan pemanggilan API.
