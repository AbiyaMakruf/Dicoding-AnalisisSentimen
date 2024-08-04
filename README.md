# Penilaian Proyek
Proyek ini berhasil mendapatkan bintang ?/5 pada submission dicoding course Belajar Pengembangan Machine Learning.

<img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-PengembanganDanPengoperasianSistemMachineLearning/main/images/nilai.png" width="500">

Kriteria tambahan yang saya kerjakan sehingga mendapat nilai terbaik:
1. Menggunakan algoritma deep learning di luar dari contoh latihan.
2. Akurasi pada training set dan testing set di atas 92%. 
3. Dataset memiliki minimal tiga kelas.
4. Memiliki jumlah data minimal 10.000 sampel data.
5. Melakukan 3 percobaan skema pelatihan yang berbeda. Skema ini dapat dibedakan dari variasi algoritma pelatihan, metode ekstraksi fitur, pelabelan, dan pembagian data dengan memilih minimal 2 kombinasi.
7. Melakukan inference atau testing dalam file .ipynb atau .py yang menghasilkan output berupa kelas kategorikal (contoh: negatif, netral, dan positif).

# EDA
1. Distribusi nilai polaritas

    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output1.png" width="400">

2. Distribusi kelas polaritas

    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output2.png" width="400">

3. Wordcloud

    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output3.png" width="400">
    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output4.png" width="400">
    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output5.png" width="400">
    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output6.png" width="400">

4. Distribusi panjang text

    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output7.png" width="400">

5. Text yang paling sering muncul

    <img src="https://raw.githubusercontent.com/AbiyaMakruf/Dicoding-AnalisisSentimen/main/images/output8.png" width="400">

# Analisis Model 
## Skema Pelatihan 
- Model 1
  - Algoritma Pelatihan: LSTM
  - Pembagian Data: Training 70, val 20, test 10
- Model 2
  - Algoritma Pelatihan: CNN
  - Pembagian Data: Training 80, val 10, test 10
- Model 3
  - Algoritma Pelatihan: GRU
  - Pembagian Data: Training 90, val 5, test 5

## Akurasi masing-masing model
| Model | Accuracy Train | Accuracy Test |
|-------|----------------|---------------|
| LSTM  | 0.944952       | 0.926333      |
| CNN   | 0.953500       | 0.920667      |
| GRU   | 0.951074       | 0.935333      |

# Prediksi
```
Text: pemakai tokopedia temukan penjual barang bagus penjual berkualitas original pakaian gadget sparepart sepeda motor sedih fitur kurir rekomendasi gratis ongkos kirim bikin paket layanan berbayar murah gratisan bagus dunia harap tokopedia bikin promo gimmick bikin customer pindah app miss tokopedia
True Label: positive
Predicted Label (LSTM): positive
Predicted Label (CNN): positive
Predicted Label (GRU): positive

Text: kurir sicepat ganti nama si lambat si lambat tokopedia bagus langganan pke aplikasi tokped bawa nama jelek kurir sicepat min tolong kasih peringatan sicepat nakal kurirnya ngirimnya lambaaaaattttt kali
True Label: negative
Predicted Label (LSTM): negative
Predicted Label (CNN): negative
Predicted Label (GRU): negative

Text: saran belanja kurir rekomendasi pengirimannya komplain alasannya follow perkembangansaran free ongkos kirim pakai salah kurir kurir kurir
True Label: neutral
Predicted Label (LSTM): neutral
Predicted Label (CNN): neutral
Predicted Label (GRU): neutral
```

# How to reproduce

## Membuat virtual environtments
- Buat virtual environtments dengan cara menjalankan perintah berikut
    ```
    conda create --name analisis-sentimen python==3.9.15
    ```

- Aktifkan environtment
    ```
    conda activate analisis-sentiment
    ```

## Install requirements
- Clone repository dan pastikan environtment sudah berjalan

- Lakukan install requirements dengan menjalankan
    ```
    pip install -r requirements.txt
    ```

## Scraping
- Untuk melakukan scraping gunakan `notebook-scraping.ipynb`
- Tentukan `id` dari aplikasi yang ingin di unduh review nya
- Tentukan `count` untuk menentukan berapa banyak jumlah review

## Training
- Ubah path dari dataset sesuai dengan dataset yang ingin di train
- Jalankan dan tunggu hasil akhirnya.