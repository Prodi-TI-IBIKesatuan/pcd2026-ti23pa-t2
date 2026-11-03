# Data

Dataset lengkap tidak disimpan di repo ini. Repo hanya berisi `sample/` (≤ 20 gambar yang sudah disensor) untuk contoh dan demo.

## Ringkasan

* Tautan folder Google Drive (akses terbatas): https://drive.google.com/drive/folders/1joDeQtj9KFQZiE5Hr3ppgadUhE9jLWSu?usp=sharing
* Jumlah citra: 202 (140 pasangan gelap–terang dari LOL + 62 foto malam sendiri)
* Foto sendiri per anggota: adhimas 15, arya 15, fadly 15, toriq 17
* Sumber data tambahan dan lisensinya: dataset LOL (140 pasangan dipakai dan dianotasi), diunduh dari Kaggle (https://www.kaggle.com/datasets/soumikrakshit/lol-dataset, diunggah oleh Soumik Rakshit). Lisensi: tidak dicantumkan di halaman Kaggle (Unknown); dipakai untuk keperluan akademik.
* Jumlah baris anotasi: 202
* Cara pengambilan foto (perangkat, waktu, lokasi umum): diambil dengan kamera ponsel pada malam hari di sekitar rumah masing-masing anggota.

## Anotasi

Pasangan citra gelap–terang sebagai referensi (mis. dataset LOL) dan foto malam sendiri. Foto sendiri tanpa pasangan dinilai dengan metrik tanpa referensi (NIQE/BRISQUE, opsional lewat paket pyiqa).

Simpan sebagai `anotasi.csv` di folder Drive, satu baris per citra (atau per pasangan), dengan kolom persis seperti [format_anotasi.csv](https://github.com/Prodi-TI-IBIKesatuan/pcd2026-ti23pa-t2/blob/main/data/format_anotasi.csv). Baris contoh di berkas itu fiktif.

## Etika dan privasi

Wajah orang wajib diburamkan di data/sample. Jangan menulis NIM, nama orang lain, atau data pribadi lain di repo ini.
