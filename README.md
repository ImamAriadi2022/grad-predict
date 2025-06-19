# Aplikasi Prediksi Status Kelulusan Mahasiswa

Aplikasi web interaktif yang dibangun untuk memprediksi status kelulusan seorang mahasiswa (Tepat Waktu atau Terlambat) berdasarkan riwayat akademik mereka per semester.

Proyek ini menggunakan model machine learning yang sudah dilatih pada sebuah dataset historis mahasiswa dan disajikan dalam antarmuka yang mudah digunakan menggunakan Streamlit.

![Demo Aplikasi](https://i.imgur.com/sSg0aCj.png)
*(Saran: Ganti gambar di atas dengan screenshot aplikasi Anda sendiri untuk hasil terbaik)*

## ✨ Fitur Utama

-   **Antarmuka Web Interaktif**: Pengguna dapat memasukkan data akademik melalui form yang intuitif.
-   **Prediksi Real-time**: Dapatkan hasil prediksi secara langsung setelah data diinput.
-   **Model Machine Learning**: Menggunakan model klasifikasi yang telah dilatih (`model.pkl`) untuk akurasi prediksi.
-   **Mudah Dijalankan**: Dibangun dengan Streamlit, aplikasi ini dapat dijalankan secara lokal hanya dengan beberapa perintah.

## 🛠️ Teknologi yang Digunakan

-   **Bahasa**: Python
-   **Framework Aplikasi Web**: Streamlit
-   **Machine Learning**: Scikit-learn
-   **Manipulasi Data**: Pandas

## 🚀 Panduan Instalasi dan Penggunaan

Ikuti langkah-langkah berikut untuk menjalankan aplikasi ini di komputer Anda.

### 1. Prasyarat

Pastikan Anda telah menginstal:
-   [Python 3.11](https://www.python.org/downloads/)
-   [Git](https://git-scm.com/downloads/)

### 2. Clone Repositori

Buka terminal atau Command Prompt, lalu clone repositori ini:
```bash
git clone [https://github.com/ImamAriadi2022/grad-predict.git](https://github.com/ImamAriadi2022/grad-predict.git)
cd grad-predict
```

### 3. Buat dan Aktifkan Virtual Environment

Sangat disarankan untuk membuat *virtual environment* agar dependensi proyek tetap terisolasi.

**a. Buat environment:**
```bash
python -m venv venv
```

**b. Aktifkan environment:**
-   **Di Windows:**
    ```bash
    .\venv\Scripts\activate
    ```
-   **Di macOS / Linux:**
    ```bash
    source venv/bin/activate
    ```

### 4. Instal Dependensi

Instal semua pustaka Python yang dibutuhkan yang tercantum dalam file `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 5. Jalankan Aplikasi Streamlit

Setelah semua dependensi terinstal, jalankan aplikasi dengan perintah berikut:
```bash
python src/main.py
```

### 6. Buka Aplikasi di Browser

Terminal akan menampilkan URL lokal tempat aplikasi berjalan. Buka URL tersebut (biasanya `http://localhost:8501`) di browser Anda untuk mulai menggunakan aplikasi.

## 📊 Dataset

Model machine learning pada proyek ini dilatih menggunakan file `Dataset.csv`. Dataset ini berisi data historis mahasiswa dengan beberapa fitur (kolom) seperti:

-   `IP S1` - `IP S8`: Indeks Prestasi (IP) per semester.
-   `SKS S1` - `SKS S8`: Jumlah Satuan Kredit Semester (SKS) yang diambil per semester.
-   Dan fitur lainnya yang relevan.

Kolom target (label) yang digunakan untuk prediksi adalah `STATUS KELULUSAN`, yang memiliki nilai seperti `TEPAT WAKTU` atau `TERLAMBAT`.

## 🤖 Model Machine Learning

File `model.pkl` adalah objek model Scikit-learn yang sudah dilatih dan disimpan (di-serialisasi) menggunakan `pickle`. Aplikasi `app.py` akan memuat model ini untuk melakukan prediksi pada data baru yang dimasukkan oleh pengguna.

*Catatan: Skrip untuk melatih model tidak disertakan dalam repositori ini, hanya aplikasi untuk inferensi (penggunaan model).*

## 👤 Penulis

-   **Imam Ariadi** - [ImamAriadi2022](https://github.com/ImamAriadi2022)