# BSBL MMI 2026 — Aplikasi Web + Data GitHub

Aplikasi web untuk **Borang Semakan Buku Latihan Pelajar** berdasarkan fail:

`BORANG SEMAK BUKU LATIHAN MMI 2026.xlsx`

## Prinsip data
- Fail Excel asal disimpan **tanpa diubah** sebagai `BORANG SEMAK BUKU LATIHAN MMI 2026.xlsx`.
- Data rujukan aplikasi diekstrak ke `data/data.json`.
- Nilai teks asal dikekalkan termasuk nama guru, mata pelajaran, tingkatan dan nama murid.
- Rekod semakan baharu disimpan pada pelayar pengguna (`localStorage`), bukan ditulis balik ke Excel.
- Hash SHA-256 fail Excel asal: `888263b6e1028e277b3c729aff9081ce7545c4161dea2adb9a6cdf0bf2956982`

## Fungsi
1. Borang semakan digital.
2. Pilihan tingkatan, guru, mata pelajaran dan pencerapan daripada data asal.
3. Senarai murid lelaki/perempuan mengikut tingkatan.
4. Maksimum 10 murid setiap borang, selaras dengan struktur borang asal.
5. Skor 1–4 menggunakan petunjuk skala asal.
6. Lima pernyataan skala asal.
7. Simpan, cari dan padam rekod.
8. Eksport/import JSON dan CSV.
9. Cetak borang.
10. Paparan data asal secara read-only.
11. Sesuai untuk GitHub Pages — tiada server diperlukan.

## Cara letak di GitHub
1. Buat repository baharu di GitHub, contoh `bsbl-mmi-2026`.
2. Upload semua fail/folder dalam projek ini ke repository.
3. Pastikan `index.html` berada di root repository.
4. Buka **Settings → Pages**.
5. Pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
6. Simpan. GitHub akan menyediakan alamat GitHub Pages.

### Jika data hendak dikemas kini
Ubah **hanya** `data/data.json` menggunakan data yang sah. Jangan ubah fail Excel asal jika objektifnya ialah mengekalkan sumber asal.

## Nota penting tentang GitHub
Versi ini ialah aplikasi statik yang mengambil data daripada fail `data/data.json` dalam repository GitHub semasa aplikasi dimuatkan. Ia tidak memerlukan API key.

Jika anda mahu **rekod semua guru disimpan terus ke pangkalan data/cloud melalui GitHub atau backend**, projek ini boleh dinaik taraf kepada Supabase/Firebase/API. GitHub Pages sendiri bukan pangkalan data transaksi.

## Struktur
```
/
├─ index.html
├─ data/
│  └─ data.json
├─ assets/
│  └─ style.css
├─ BORANG SEMAK BUKU LATIHAN MMI 2026.xlsx
└─ README.md
```
