# Word Count MapReduce Project

Proyek ini menghitung jumlah kata (**word count**) dari teks **Pembukaan UUD 1945** menggunakan teknik MapReduce di Hadoop. Proses dilakukan dengan memanfaatkan Hadoop Streaming dan Python (mapper.py dan reducer.py).

## Tujuan

1. Membuat implementasi MapReduce untuk menghitung jumlah kata pada dokumen teks.
2. Menjalankan proses MapReduce di Hadoop Standalone Cluster.
3. Menyimpan hasil word count ke file output dan mempublikasikan proyek di GitHub.

## Fitur

- Menggunakan **Hadoop Streaming** untuk menjalankan MapReduce.
- Pemrosesan teks dengan Python.
- Word count output tersimpan dalam file `.txt`.

## Langkah Kerja

### 1. Persiapan Input
- Salin teks **Pembukaan UUD 1945** dari [website DPR RI](https://www.dpr.go.id/jdih/uu1945).
- Simpan teks dalam file `pembukaan_uud1945.txt`.

### 2. Implementasi Kode
#### a) Mapper (mapper.py)
Mapper membaca baris teks, memisahkan kata-kata, dan menghitungnya.

#### b) Reducer (reducer.py)
Reducer menggabungkan hasil dari mapper dan menghasilkan total word count untuk setiap kata.

### 3. Eksekusi MapReduce
- Jalankan **Hadoop Standalone Cluster** menggunakan `hadoop-streaming-3.2.3.jar`.
- Kirim data ke HDFS dan jalankan MapReduce.

### 4. Output
Hasil word count disimpan dalam file `output_word_count.txt`.

### Contoh Output
Berikut adalah cuplikan hasil dari proses MapReduce:

Allah	1
Atas	1
Bahwa	1
Dan	1
Dasar	1
Esa	1
Indonesia	12
Keadilan	1
Kebangsaan	1