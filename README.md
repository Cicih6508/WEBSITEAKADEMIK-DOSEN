# JAD — Panduan Jabatan Akademik Dosen

Website statis (HTML, CSS, JavaScript murni, tanpa framework) berisi panduan interaktif jabatan akademik dosen di Indonesia.

## Cara menjalankan

Buka `index.html` langsung di peramban, atau jalankan server lokal:

```bash
# Python
python -m http.server 8000
# lalu buka http://localhost:8000
```

Tidak perlu instalasi atau build. Font (Plus Jakarta Sans dan Source Serif 4) dimuat dari Google Fonts; bila offline, halaman memakai font cadangan sistem.

## Struktur

```
jad-website/
├── index.html              Kerangka halaman dan semua seksi
├── assets/
│   ├── css/style.css       Token warna, tipografi, tata letak, mode gelap, responsif
│   ├── js/data.js          SEMUA isi regulasi (jenjang, AK, syarat, alur, FAQ)
│   ├── js/main.js          Interaksi: penggaris AK, tangga, kalkulator, checklist, FAQ
│   └── img/favicon.svg
└── README.md
```

## Fitur

- **Penggaris angka kredit** di hero: geser penanda untuk melihat rentang jabatan, jenjang berikutnya, kekurangan AK, dan perkiraan waktu.
- **Tangga jenjang**: tinggi batang sebanding dengan AK tertinggi tiap jenjang; klik untuk membaca syarat, publikasi, uji kompetensi, dan tunjangan.
- **Angka kredit**: empat komponen AK Kumulatif, tabel AK per tahun, dan proporsi AK penelitian.
- **Kalkulator kesiapan usulan**: menghitung kekurangan AK, kebutuhan AK penelitian (proporsi × selisih AK tujuan dan AK jabatan terakhir), daftar syarat, dan perkiraan waktu.
- **Alur pengusulan** lewat SISTER, **loncat jabatan**, **daftar periksa berkas** (tersimpan di localStorage), dan **FAQ** dengan pencarian.
- Mode terang/gelap, menu ponsel, navigasi aktif saat menggulir, dukungan keyboard, dan `prefers-reduced-motion`.

## Memperbarui isi

Semua angka dan teks regulasi ada di `assets/js/data.js`. Ubah nilainya di sana bila ada aturan baru, misalnya AK kumulatif (`ak`), koefisien SKP (`konversiBaik`, `konversiSangatBaik`), batas AK per tahun (`maksPerTahun`), atau proporsi penelitian (`proporsiPenelitian`). Halaman otomatis menyesuaikan.

## Dasar regulasi

- Permendiktisaintek No. 52 Tahun 2025 tentang Profesi, Karier, dan Penghasilan Dosen (diundangkan 24 Desember 2025).
- Kepmendiktisaintek No. 39/M/KEP/2026 tentang Petunjuk Teknis Layanan Pengembangan Profesi dan Karier Dosen (ditetapkan 26 Januari 2026).

Isi website adalah ringkasan untuk perencanaan, bukan dokumen resmi. Selalu cocokkan dengan salinan resmi regulasi dan ketentuan Tim PAK perguruan tinggi.
