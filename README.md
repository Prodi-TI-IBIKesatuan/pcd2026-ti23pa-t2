# Penyelarasan Warna dan Perbaikan Citra Malam Hari

Proyek kelompok **Pengolahan Citra Digital 2026** · kelas `ti23pa` · topik **T2**

[![Cek proyek](https://github.com/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/actions/workflows/cek-proyek.yml/badge.svg)](https://github.com/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/actions/workflows/cek-proyek.yml)

**Lingkup kelompok kami:** lingkungan rumah

Memperbaiki pencahayaan dan keseimbangan warna foto yang diambil dalam kondisi gelap. Anggota dan perannya ada di [ANGGOTA.yml](ANGGOTA.yml); cara kerja kelompok ada di [PANDUAN.md](PANDUAN.md).

## Notebook

| Notebook | Tahap | Isi | Buka |
| --- | --- | --- | --- |
| `01_dataset_preprocessing.ipynb` | 1 | Statistik dataset, cek anotasi, preprocessing, gambar sebelum–sesudah | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/blob/main/notebooks/01_dataset_preprocessing.ipynb) |
| `02_metode_klasik.ipynb` | 2 | 2 metode klasik dan metriknya | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/blob/main/notebooks/02_metode_klasik.ipynb) |
| `03_metode_modern.ipynb` | 2 | Inferensi model pralatih dan metriknya | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/blob/main/notebooks/03_metode_modern.ipynb) |
| `04_evaluasi.ipynb` | 2 | Tabel perbandingan, uji ablasi, kasus gagal | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/blob/main/notebooks/04_evaluasi.ipynb) |

## Dataset (Tahap 1)

- Jumlah citra: 202
- Foto sendiri: 62
- Sumber data tambahan dan lisensinya: dataset LOL diunduh dari Kaggle. Lisensi tidak dicantumkan di halaman Kaggle (Unknown).
- Langkah preprocessing: 
Menentukan preprocessing citra malam
Preprocessing disesuaikan dengan arahan proyek, yaitu:
- Resize seluruh citra menjadi 512 × 512 piksel.
- Menggunakan interpolasi INTER_AREA.
- Mengubah ruang warna dari BGR ke LAB.
- Memisahkan kanal LAB menjadi:
  - L = luminans/kecerahan
  - A = informasi warna
  - B = informasi warna
- Tidak melakukan enhancement pada tahap preprocessing agar preprocessing tidak tercampur dengan metode perbaikan citra.

Menguji preprocessing
- Mengambil satu citra dari dataset.
- Menjalankan fungsi preprocessing.
- Memeriksa ukuran citra sebelum dan sesudah resize.
- Memeriksa kanal L, A, dan B.
- Membuat visualisasi citra asli, hasil resize, serta kanal LAB.

Rincian dataset, format anotasi, dan tautan Drive: [data/README.md](data/README.md). Contoh sebelum–sesudah ada di [outputs/figures/](outputs/figures/).

## Hasil (Tahap 2)

| Metode | Jenis | PSNR | SSIM |
| --- | --- | --- | --- |
| [isi: nama metode klasik 1] | klasik | [isi] | [isi] |
| [isi: nama metode klasik 2] | klasik | [isi] | [isi] |
| [isi: nama model] | modern | [isi] | [isi] |

- **Uji ablasi:** [isi: parameter atau langkah yang diubah, dan pengaruhnya pada metrik]
- **Kasus gagal:** [isi: minimal 3 contoh dan penyebabnya, gambar di outputs/figures/]
- **Kesimpulan:** [isi: metode mana yang terbaik untuk lingkup kami dan mengapa]

## Demo

Aplikasi: [isi: tautan https://huggingface.co/spaces/...]

Unggah foto gelap, tampilkan hasil perbaikan berdampingan dengan aslinya. Kode aplikasi ada di [app/](app/).

## Sumber dan atribusi

Tuliskan setiap kode, model, dataset, atau bantuan AI yang dipakai beserta sumbernya. Pemakaian tanpa sumber dihitung plagiarisme.

| Yang dipakai | Sumber | Dipakai untuk |
| --- | --- | --- |
| Dataset LOL (140 pasang foto) | Kaggle, Soumik Rakshit (https://www.kaggle.com/datasets/soumikrakshit/lol-dataset) | Pasangan gelap–terang sebagai data dan referensi |
| Bantuan AI: Claude (Anthropic) | https://claude.ai | Skrip data dan anotasi, serta draf dokumentasi README |
