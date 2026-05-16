### Rinaldi Dasa Bahtiar - H1D024065  Praktikum Kecerdasan Buatan - Shift A  

# Klasifikasi Gambar Rock-Paper-Scissors menggunakan CNN

Program ini adalah implementasi Jaringan Saraf Tiruan Konvolusional (CNN) untuk mengklasifikasikan gambar tangan yang membentuk simbol **Batu (Rock)**, **Kertas (Paper)**, dan **Gunting (Scissors)**. Program ini dibangun menggunakan pustaka TensorFlow dan Keras.

## Deskripsi Proyek
Program ini melakukan preprocessing gambar secara otomatis menggunakan `ImageDataGenerator`, membangun arsitektur model CNN, melatih model dengan dataset yang tersedia, dan mengevaluasi akurasinya.

## Struktur Dataset
Dataset harus diletakkan dalam folder `rockpaperscissors/` dengan struktur sebagai berikut:
```text
rockpaperscissors/
├── paper/      # Berisi gambar tangan simbol kertas
├── rock/       # Berisi gambar tangan simbol batu
└── scissors/   # Berisi gambar tangan simbol gunting
```
Dataset akan dibagi secara otomatis menjadi **80% data training** dan **20% data validation**.

## 🛠️ Prasyarat (Dependencies)
Pastikan Anda telah menginstal pustaka yang diperlukan:
```bash
pip install numpy pandas tensorflow
```

## Cara Menjalankan
1. Pastikan folder dataset `rockpaperscissors` berada di direktori yang sama dengan `main.py`.
2. Jalankan skrip utama:
   ```bash
   python main.py
   ```

## Arsitektur Model
Model yang digunakan adalah model **Sequential** dengan struktur:
- **Conv2D & MaxPooling2D**: Tiga blok lapisan konvolusi untuk ekstraksi fitur gambar.
- **Flatten**: Mengubah matriks fitur menjadi vektor satu dimensi.
- **Dense Layer**: Lapisan terhubung penuh dengan 512 neuron (ReLU).
- **Output Layer**: 3 neuron dengan aktivasi **Softmax** untuk klasifikasi multi-kelas (Rock, Paper, Scissors).

## Konfigurasi Training
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy
- **Epochs**: 10

## Hasil
Setelah proses training selesai, program akan menampilkan:
- Ringkasan arsitektur model.
- Grafik akurasi dan loss (jika ditambahkan visualisasi).
- Akurasi akhir pada data validasi.
- Prediksi probabilitas untuk data validasi.

---
*Dibuat untuk Praktikum KB Pertemuan 8*
