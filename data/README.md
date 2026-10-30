# Data

Dataset lengkap **tidak** disimpan di repo ini. Repo hanya berisi `sample/` (≤ 20 gambar yang sudah disensor) untuk contoh dan demo.

## Ringkasan

- Tautan folder Google Drive (akses terbatas): [isi: https://drive.google.com/drive/folders/...]
- Jumlah citra: [isi]
- Foto sendiri per anggota: [isi: mis. andi 20, budi 15, ...]
- Sumber data tambahan dan lisensinya: [isi, atau "tidak ada"]
- Jumlah baris anotasi: [isi]
- Cara pengambilan foto (perangkat, waktu, lokasi umum): [isi]

## Anotasi

Pasangan citra gelap–terang sebagai referensi (mis. dataset LOL) dan foto malam sendiri. Foto sendiri tanpa pasangan dinilai dengan metrik tanpa referensi (NIQE/BRISQUE, opsional lewat paket pyiqa).

Simpan sebagai `anotasi.csv` di folder Drive, satu baris per citra (atau per pasangan), dengan kolom persis seperti [format_anotasi.csv](format_anotasi.csv). Baris contoh di berkas itu fiktif.

## Etika dan privasi

Wajah orang wajib diburamkan di data/sample. Jangan menulis NIM, nama orang lain, atau data pribadi lain di repo ini.
