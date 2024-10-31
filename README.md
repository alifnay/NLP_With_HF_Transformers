

<h1 align="center">NLP With Hugging Face Transformers</h1>
<p align="center">Berisi tentang pipeline dari Hugging Face Transformers untuk keperluan NLP (Natural Language Processing)</p>

<div align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
    <img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white">
</div>

<h2 align="center">Analisis</h2> 

### 1. Zero-Shot Classification
Zero-shot classification merupakan teknik yang sangat bermanfaat dalam klasifikasi teks. Metode ini sangat menarik untuk dicoba karena:
- **Fleksibilitas**: Dapat mengklasifikasikan data baru tanpa perlu melatih model dengan data spesifik.
- **Penghematan Waktu**: Mengurangi waktu dan sumber daya yang diperlukan untuk pelatihan model baru.
- **Akurasi**: Mampu memberikan hasil yang memuaskan meskipun model tidak dilatih pada dataset yang sama.

### 2. Text Generation
Text generation adalah alat yang mampu menciptakan teks baru yang relevan dengan input. Hasil analisis menunjukkan kemampuan model untuk:
- **Kreativitas**: Menghasilkan kalimat yang ekspresif dan bervariasi.
- **Kontekstualisasi**: Memahami konteks untuk menciptakan teks yang relevan.
- **Keterhubungan**: Menghasilkan teks yang koheren dalam struktur dan tema.

### 3. Fill Mask
Fill mask adalah teknik yang efektif dalam pemrosesan bahasa alami untuk memprediksi kata yang hilang dalam kalimat. Output analisis menunjukkan kemampuan model untuk:
- **Prediksi Kata**: Mengisi kata yang hilang berdasarkan konteks kalimat.
- **Variasi Skor Kepercayaan**: Menunjukkan tingkat kepercayaan yang bervariasi dalam prediksi yang dilakukan.

### 4. Named Entity Recognition (NER)
Named Entity Recognition (NER) adalah alat dalam analisis teks yang memungkinkan identifikasi dan klasifikasi entitas kunci. Output analisis menunjukkan kemampuan model untuk:
- **Akurasi Identifikasi**: Mengidentifikasi individu dan organisasi dengan tepat.
- **Skor Kepercayaan Tinggi**: Memberikan skor kepercayaan yang tinggi pada klasifikasi entitas yang dilakukan.

### 5. Question Answering
Question answering adalah alat dalam pemrosesan bahasa alami yang memungkinkan pengguna untuk mendapatkan jawaban cepat dan akurat terhadap pertanyaan yang diajukan. Output analisis menunjukkan kemampuan sistem QA untuk:
- **Kecepatan Respon**: Memberikan jawaban dengan cepat.
- **Akurasi Jawaban**: Menghasilkan jawaban yang tepat, termasuk jawaban numerik jika diperlukan.

### 6. Sentiment Analysis
Sentiment analysis adalah alat yang berguna dalam memahami emosi dan opini yang terdapat dalam teks. Teknik ini dapat digunakan dalam berbagai konteks, seperti:
- **Pemasaran**: Menilai reaksi konsumen terhadap produk atau layanan.
- **Analisis Media Sosial**: Memahami sentimen publik terhadap isu-isu terkini.
- **Umpan Balik Pelanggan**: Menganalisis feedback untuk meningkatkan layanan.

### 7. Summarization
Summarization adalah alat untuk menyajikan informasi secara ringkas dan jelas. Output analisis menunjukkan bahwa model mampu:
- **Menghasilkan Ringkasan Informatif**: Menyajikan informasi kunci dari teks panjang dengan efektif.
- **Memudahkan Pemahaman**: Membantu pembaca untuk memahami inti dari informasi yang disajikan.

### 8. Translation
Translation adalah alat untuk mengubah suatu bahasa menjadi ke bahasa lain. Teknik ini sangat berguna untuk:
- **Komunikasi Lintas Bahasa**: Memudahkan interaksi antara penutur bahasa yang berbeda.
- **Akses Informasi**: Memperluas jangkauan konten dan informasi di seluruh dunia.

<h2 align="center">Prasyarat</h2>
<ul>
    <li>Python 3.6 atau lebih baru</li>
    <li>Pip</li>
    <li>Library yang dibutuhkan:
        <ul>
            <li>`transformers`</li>
        </ul>
    </li>
</ul>

<h2 align="center">Contoh Penggunaan</h2> 
Berikut adalah contoh NLP menggunakan Hugging Face Transformers untuk Zero-Shot Classification

```python
from transformers import pipeline

# Membuat pipeline untuk Zero-Shot Classification
classifier = pipeline("zero-shot-classification")
classifier(
    "The stock market saw a significant increase today, with tech stocks leading the way.",
    candidate_labels=["finance", "economy", "Investment", "Market"],
)
