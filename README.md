# Clustering

Kumpulan notebook untuk persiapan UTS Data Mining II menggunakan K-Means.

## Isi

- [Audio / Signal](UTS_Datmin_II_Audio.ipynb): input folder/ZIP audio atau NPZ sinyal, standardisasi, dan clustering.
- [Image](UTS_Datmin_II_Image.ipynb): input folder, ZIP, atau NPZ gambar; preprocessing dan clustering.
- [Text](UTS_Datmin_II_Text.ipynb): input CSV, folder TXT, ZIP TXT, atau NPZ teks; satu alur preprocessing NLTK, TF-IDF, dan clustering. Satu file TXT menjadi satu dokumen.

## Cara pakai

1. Buka notebook di Google Colab atau Jupyter Notebook.
2. Install library yang diperlukan sesuai petunjuk di notebook.
3. Pilih satu bagian input di awal notebook dan hapus bagian input yang tidak dipakai sebelum Run All.
4. Sesuaikan lokasi dataset, nama kolom jika diperlukan, dan nilai k.
5. Ikuti petunjuk di notebook dan jalankan cell secara berurutan. Input folder dan ZIP juga mencakup subfolder.

## Input NPZ

| Notebook | Isi NPZ yang digunakan |
|---|---|
| Image | `x_train`: gambar grayscale 28×28 dengan piksel 0–255; `y_train`: label |
| Audio / Signal | `x_train`: sinyal 128 titik; `y_train`, `sample_rate_hz`, `time_seconds`, dan `class_names` sesuai dataset latihan |
| Text | `texts`: array teks mentah satu dimensi bertipe Unicode; ganti nama key jika berbeda |

Setiap bagian NPZ mencetak nama array agar bisa diperiksa. Contoh Image dan Signal memakai maksimal 2.000 data train; ubah `n` sesuai kebutuhan. Data test tetap terpisah dan label tidak dimasukkan ke fitur clustering.

NPZ Signal mempertahankan sampling 128 Hz dan memakai nilai amplitudo sebagai fitur, lalu langsung ke standardisasi. Ikuti petunjuk bagian yang perlu dihapus pada setiap notebook sebelum Run All.
