# 📚 Chatbot RAG – SOP Fakultas Sains dan Matematika UNDIP

Project ini merupakan implementasi **Retrieval-Augmented Generation (RAG)** untuk menjawab pertanyaan seputar Standar Operasional Prosedur (SOP) Fakultas Sains dan Matematika Universitas Diponegoro.

Chatbot akan menjawab pertanyaan berdasarkan dokumen SOP yang tersedia pada folder `data/`.

---

## 📦 A. Panduan Instalasi Project ke Lokal

### 1. Clone Repository

1. Klik tombol **Code** pada halaman repository GitHub.
2. Copy link HTTPS berikut:

```
https://github.com/PIP-Bravo/Chatbot-RAG.git
```

3. Buka **VS Code**
4. Buka folder lokasi penyimpanan project
5. Buka terminal baru pada VS Code
6. Jalankan perintah berikut:

```bash
git clone https://github.com/PIP-Bravo/Chatbot-RAG.git
```

7. Masuk ke folder project:

```bash
cd Chatbot-RAG
```

Jika berhasil, seluruh file project akan terunduh ke komputer lokal.

---

## 🐍 B. Membuat Virtual Environment

Sangat disarankan menggunakan environment terpisah agar tidak mengganggu konfigurasi Python utama.

### 1. Buat Virtual Environment (Conda)

Buka terminal baru lalu jalankan:

```bash
conda create -n chatbot_rag_env python==3.12.0
```

> Gunakan versi Python **3.12.0** agar tidak terjadi konflik dependency.

### 2. Aktifkan Environment

```bash
conda activate chatbot_rag_env
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Tunggu hingga seluruh dependency berhasil terinstall.

Jika tidak ada error, berarti instalasi berhasil.

---

## 🔐 C. Konfigurasi Environment Variable

Sebelum menjalankan project, buat file `.env` di root folder project.

Isi file `.env` dengan format berikut:

```
GITHUB_TOKEN="Masukkan_Github_Token_Kamu_Disini"
```

### Cara Membuat GitHub Token

1. Masuk ke GitHub
2. Settings → Developer Settings
3. Personal Access Tokens → Generate new token
4. Copy token dan masukkan ke file `.env`

---

## 🚀 D. Cara Menjalankan Project

Pastikan virtual environment sudah aktif.

### 1. Fine-tuning Embeddings

```bash
python finetune_embeddings.py
```

Tunggu hingga proses selesai.

---

### 2. Generate Embeddings

```bash
python embeddings.py
```

---

### 3. Jalankan Query

```bash
python query_data.py "Pertanyaan_kamu_disini"
```

Contoh:

```bash
python query_data.py "Bagaimana prosedur pengisian IRS?"
```

> Catatan:  
> Pertanyaan hanya dapat dijawab jika sesuai dengan isi dokumen pada folder `data/`.

---

## 🧠 Knowledge Base yang Digunakan

Chatbot ini menggunakan dokumen resmi berikut:

- SOP Pengisian IRS  
- SOP Permohonan Izin Aktif Kuliah Setelah Cuti  
- SOP Permohonan Izin Cuti Akademik  
- SOP Permohonan Izin Keterlambatan Pembayaran UKT  
- SOP Legalisir Ijazah dan Transkrip  
- SOP Pengajuan Beasiswa  
- SOP Pengajuan Proposal Kegiatan Organisasi  

Seluruh dokumen tersebut merupakan milik:

**Fakultas Sains dan Matematika  
Universitas Diponegoro**

---

## 📂 Struktur Project

```
Chatbot-RAG/
│
├── data/                 # Dokumen PDF SOP
├── datasets/             # Dataset Qa untuk train model embeddings
├── embeddings.py
├── finetune_embeddings.py
├── generate_qa.py
├── query_data.py
├── evaluate.py
├── requirements.txt
└── README.md
```

---

## 🛠 Teknologi yang Digunakan

- Python 3.12
- Retrieval-Augmented Generation (RAG)
- Embedding Model
- Vector Similarity Search
- GitHub API
- dotenv
- Conda Environment

---

## 📌 Troubleshooting

Jika terjadi error:

- Pastikan Python versi sesuai (3.12.0)
- Pastikan environment sudah aktif
- Pastikan `.env` sudah dibuat
- Pastikan semua dependency sudah terinstall

Cek versi python:

```bash
python --version
```

---

## 👤 Author

**Alfonso Clement S**

Jika terdapat pertanyaan atau kendala, silakan hubungi melalui:

Email: sutancs42@gmail.com  
GitHub: https://github.com/PIP-Bravo

---

## 🎯 Tujuan Project

Project ini dibuat sebagai implementasi konsep:

- Retrieval-Augmented Generation
- Knowledge-based QA System
- Embedding & Semantic Search
- Integrasi LLM dengan Dokumen Resmi