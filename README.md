# 🏥 Analisis Sentimen RS Al-Irsyad Surabaya

Aplikasi web untuk menganalisis sentimen ulasan Rumah Sakit Al-Irsyad Surabaya menggunakan metode Naive Bayes.

## ✨ Fitur

- 📊 **Analisis Data**: Lihat distribusi dan statistik data ulasan
- 🔮 **Prediksi Sentimen**: Prediksi sentimen untuk ulasan baru (single atau multiple)
- 📈 **Visualisasi**: Word cloud dan grafik distribusi kata
- 🤖 **Machine Learning**: Model Naive Bayes dengan preprocessing lengkap

## 🚀 Cara Menjalankan

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Jalankan Aplikasi

```bash
streamlit run app.py
```

### 3. Buka di browser

Aplikasi akan terbuka di `http://localhost:8501`

## 📋 Cara Penggunaan

### Upload Data (Opsional)
1. Siapkan file CSV dengan kolom:
   - `text`: berisi teks ulasan
   - `sentimen`: berisi label "positif" atau "negatif"
2. Upload di menu "Beranda"
3. Klik "Latih Model dengan Data Ini"

### Prediksi Sentimen Baru
1. Pilih menu "Prediksi Sentimen"
2. Masukkan ulasan yang ingin diprediksi
3. Klik "Prediksi Sentimen"

### Lihat Analisis & Visualisasi
- Menu "Analisis Data": Statistik dan distribusi data
- Menu "Visualisasi": Word cloud dan grafik

## 🔧 Preprocessing Pipeline

1. **Lowercase**: Ubah ke huruf kecil
2. **Clean Text**: Hapus angka, tanda baca, emoji
3. **Tokenization**: Pecah menjadi kata-kata
4. **Normalization**: Ubah singkatan ke bentuk baku
5. **Stemming**: Ubah ke bentuk dasar (Sastrawi)
6. **Stopwords Removal**: Hapus kata-kata umum
7. **TF-IDF**: Ekstraksi fitur numerik

## 📦 Dependencies

- streamlit: Web framework
- pandas: Data manipulation
- scikit-learn: Machine learning
- nltk: Natural language processing
- Sastrawi: Indonesian stemmer
- matplotlib/seaborn: Visualization
- wordcloud: Word cloud generation

## 🎯 Model

- **Algorithm**: Multinomial Naive Bayes
- **Features**: TF-IDF (max 5000 features, unigram + bigram)
- **Classes**: Positif, Negatif

## 📁 Struktur File

```
├── app.py                  # Aplikasi Streamlit utama
├── requirements.txt        # Dependencies
├── README.md              # Dokumentasi
├── model.pkl              # Model terlatih (auto-generated)
├── vectorizer.pkl         # TF-IDF vectorizer (auto-generated)
└── term_dict.pkl          # Dictionary untuk stemming (auto-generated)
```

## 🌐 Deploy ke Streamlit Cloud

1. Upload ke GitHub repository
2. Buka [share.streamlit.io](https://share.streamlit.io)
3. Connect repository dan deploy
4. Aplikasi akan live di URL yang diberikan

## 🐛 Troubleshooting

### Error NLTK Data
Jika ada error terkait NLTK data, jalankan:
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

### Error Model Not Found
Jika model belum ada, upload data melalui menu "Beranda" untuk melatih model baru.

## 👥 Tim Pengembangan

Dikembangkan untuk analisis sentimen ulasan rumah sakit menggunakan metode Naive Bayes.

---

🚀 **Selamat menggunakan aplikasi!**
