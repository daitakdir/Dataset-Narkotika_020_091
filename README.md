# Dataset Narkotika 020-029 — Putusan Pengadilan Negeri Tangerang

**Repository:** `Dataset-Narkotika_020_091`  
**Mata kuliah:** Temu Kembali Informasi (*Information Retrieval*)  
**Penugasan:** UTS — SUBCPMK 2: Akuisisi dan Pengelolaan Dokumen Putusan Pengadilan  
**Program studi:** Informatika, Universitas Muhammadiyah Malang  
**Tahun akademik:** 2026/2027

---

## 📖 Deskripsi

Repository ini disusun untuk mendokumentasikan **dataset 50 dokumen putusan pengadilan dalam format PDF** beserta ringkasan informasinya dalam format Excel. Dataset berfokus pada perkara **Pidana Khusus — Narkotika dan Psikotropika** di **Pengadilan Negeri Tangerang (PN Tng)**, dengan sumber dokumen dari [Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/direktori.html).

Dokumentasi ini merupakan bagian dari tugas UTS SUBCPMK 2, yaitu proses **akuisisi dokumen secara manual**, pengelolaan arsip, dan penyajian metadata putusan. Dataset dapat menjadi landasan untuk latihan *Information Retrieval* dan analisis dokumen hukum pada tahapan pembelajaran berikutnya.

> **Catatan:** Repository ini merupakan tugas akademik mahasiswa, bukan produk atau dataset resmi yang diterbitkan oleh Mahkamah Agung RI.

## 🎯 Tujuan

1. Mengumpulkan dokumen putusan pengadilan dari sumber resmi secara terstruktur.
2. Mengorganisasikan 50 PDF putusan ke dalam satu arsip yang mudah diakses.
3. Membuat tabel ringkasan informasi putusan dalam `Overview.xlsx`.
4. Menyediakan dokumentasi asal data, struktur dataset, dan batasan penggunaan.
5. Menyiapkan korpus dokumen hukum untuk pembelajaran temu kembali informasi.

## 🗂️ Struktur Repository

Susunan yang mengikuti format pengumpulan SUBCPMK 2:

```text
Dataset-Narkotika_020_091/
├── Dataset/
│   └── Narkotika.zip          # Arsip 50 dokumen putusan PDF
├── Overview/
│   └── Overview.xlsx          # Ringkasan 50 dokumen putusan
└── README.md                  # Dokumentasi dataset
```

**Akses berkas setelah struktur di atas diterapkan:**

- [Arsip putusan PDF — Narkotika.zip](Dataset/Narkotika.zip)
- [Ringkasan dataset — Overview.xlsx](Overview/Overview.xlsx)

## 📊 Spesifikasi Dataset

| Aspek | Keterangan |
|---|---|
| Sumber | Direktori Putusan Mahkamah Agung RI |
| Peradilan | Pengadilan Negeri Tangerang (PN Tng) |
| Kategori | Pidana Khusus |
| Klasifikasi | Narkotika dan Psikotropika |
| Jumlah target dokumen | 50 putusan |
| Format dokumen asli | `.pdf` |
| Format metadata/ringkasan | `.xlsx` |
| Rentang tahun yang digunakan | 2023–2025 |
| Metode akuisisi SUBCPMK 2 | Unduh dokumen secara manual dari direktori resmi |
| Bahasa dokumen | Bahasa Indonesia |

## 🧾 Struktur `Overview.xlsx`

Setiap baris mewakili satu putusan pengadilan. Kolom yang digunakan adalah:

| Kolom | Deskripsi |
|---|---|
| `No` | Nomor urut dokumen dalam daftar |
| `No Putusan` | Identitas atau nomor perkara sesuai dokumen putusan |
| `Lembaga Peradilan` | Nama/kode pengadilan yang memutus perkara |
| `Barang Bukti` | Ringkasan daftar barang bukti yang disebutkan dalam putusan |
| `Amar Putusan` | Isi atau ringkasan amar putusan sesuai dokumen sumber |

Informasi dalam `Overview.xlsx` harus selalu dapat ditelusuri kembali ke dokumen PDF yang bersangkutan.

## 🔎 Prosedur Pengumpulan Data

1. Akses [Direktori Putusan Mahkamah Agung RI](https://putusan3.mahkamahagung.go.id/direktori.html).
2. Pilih **Pidana Khusus → Narkotika dan Psikotropika**.
3. Batasi pencarian pada **Pengadilan Negeri Tangerang** dan tahun putusan yang dipilih.
4. Terapkan ketentuan penugasan: hindari putusan dengan status **Berkekuatan Hukum Tetap**. Status masing-masing putusan perlu diperiksa pada sumber resminya.
5. Unduh putusan dalam format PDF secara **manual**.
6. Periksa nama/nomor putusan agar tidak ada duplikasi yang tidak disengaja.
7. Kumpulkan PDF ke dalam satu folder, kemudian kompres sebagai `Narkotika.zip`.
8. Susun metadata 50 dokumen dalam `Overview.xlsx`.
9. Cocokkan informasi ringkasan dengan PDF asli sebelum publikasi.


## 💻 Cara Menggunakan Dataset

1. Buka direktori `Dataset/` dan unduh `Narkotika.zip`.
2. Ekstrak arsip untuk mengakses dokumen putusan dalam format PDF.
3. Buka `Overview/Overview.xlsx` dengan Microsoft Excel, LibreOffice Calc, atau aplikasi spreadsheet yang kompatibel.
4. Gunakan kolom `No Putusan` untuk mencocokkan ringkasan dengan PDF sumber.
5. Jika digunakan pada Python/Google Colab, PDF dapat diproses dengan PyMuPDF dan file Excel dapat dibaca menggunakan `pandas`.

Contoh membaca ringkasan Excel dengan Python:

```python
import pandas as pd

df = pd.read_excel("Overview/Overview.xlsx")
print("Jumlah putusan:", len(df))
print(df.columns.tolist())
print(df.head())
```

## ⚠️ Batasan dan Etika Penggunaan

- Isi putusan merupakan dokumen hukum yang **harus dirujuk ke sumber resminya** jika digunakan dalam penelitian atau publikasi.
- Metadata dan ringkasan dapat mengandung kekeliruan penyalinan; lakukan pengecekan silang dengan PDF asli.
- Putusan dapat memuat informasi pribadi atau informasi sensitif terkait perkara. Hindari penyalahgunaan, pengungkapan berlebihan, atau penggunaan data untuk merugikan pihak tertentu.
- Repository ini **tidak memberikan nasihat hukum** dan tidak berafiliasi dengan Mahkamah Agung RI.
- Ketersediaan dokumen publik tidak berarti seluruh bentuk penggunaan ulang bebas dari ketentuan hukum atau kebijakan sumber.

## 📚 Sumber dan Rujukan

- [Direktori Putusan Mahkamah Agung Republik Indonesia](https://putusan3.mahkamahagung.go.id/direktori.html)
- [GitHub — Panduan dasar penulisan README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)

## 👥 Anggota Kelompok

| Anggota |         Nama           |      NIM       |
|---      |         ---            |      ---       |
| 1       | Muhammad Rezky Maulana | 202310370311020 
| 2       | Muhammad Dai Takdir    | 202310370311091

**Identitas repository:** `Dataset-Narkotika_020_091`, berdasarkan tiga digit terakhir NIM kedua anggota.

---

*Dibuat untuk keperluan akademik UTS Temu Kembali Informasi, Universitas Muhammadiyah Malang — Tahun Akademik 2026/2027.*
