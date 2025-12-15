# 📘 Judul Proyek
**Klasifikasi Tingkat Obesitas Berdasarkan Kebiasaan Hidup  
Menggunakan Machine Learning dan Deep Learning**

---

## 👤 Informasi
- **Nama**: Saifullah Isnan Ramadhani  
- **Program Studi**: Teknologi Rekayasa Perangkat Lunak  
- **Mata Kuliah**: Data Science  
- **Repository**: https://github.com/username/uas-data-science  
- **Video**: https://youtu.be/link-video-anda  

---

## 1. 🎯 Ringkasan Proyek
Proyek ini bertujuan untuk membangun sistem klasifikasi tingkat obesitas berdasarkan kebiasaan hidup individu menggunakan pendekatan **Machine Learning** dan **Deep Learning**.  

Tahapan utama dalam proyek ini meliputi:
- Menyelesaikan permasalahan klasifikasi pada domain kesehatan (obesitas)
- Melakukan data preparation (cleaning, encoding, scaling, dan splitting)
- Membangun **3 model klasifikasi**:
  - Baseline Model
  - Advanced Machine Learning Model
  - Deep Learning Model
- Melakukan evaluasi model menggunakan metrik yang sesuai
- Menentukan model terbaik berdasarkan hasil evaluasi

---

## 2. 📄 Problem & Goals

### Problem Statements
- Bagaimana memprediksi tingkat obesitas individu berdasarkan kebiasaan hidup seperti pola makan, aktivitas fisik, konsumsi air, dan penggunaan teknologi.
- Model mana yang memberikan performa terbaik dalam mengklasifikasikan tingkat obesitas pada data tabular multiclass.

### Goals
- Mengembangkan tiga model klasifikasi (Baseline, Advanced, Deep Learning).
- Membandingkan performa model menggunakan metrik evaluasi yang relevan.
- Menentukan model terbaik untuk klasifikasi tingkat obesitas.

---

## 📁 Struktur Folder
project/
│
├── data/ # Dataset (tidak di-commit, download manual)
│
├── notebooks/ # Jupyter notebooks
│ └── UAS_DataScience.ipynb
│
├── src/ # Source code (jika diperlukan)
│
├── models/ # Saved models
│ ├── logistic_regression.pkl
│ ├── random_forest.pkl
│ └── mlp_model.keras
│
├── images/ # Visualizations (EDA, confusion matrix, dll)
│
├── requirements.txt # Dependencies
├── .gitignore
└── README.md


---

## 3. 📊 Dataset
- **Sumber**: UCI Machine Learning Repository  
  https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition  
- **Jumlah Data**: 2.111 sampel  
- **Tipe Data**: Tabular (Numerik & Kategorikal)

### Fitur Utama

| Fitur | Deskripsi |
|------|----------|
| Age | Usia individu |
| Height | Tinggi badan (meter) |
| Weight | Berat badan (kg) |
| FCVC | Frekuensi konsumsi sayur |
| FAF | Frekuensi aktivitas fisik |
| CH2O | Konsumsi air per hari |
| TUE | Durasi penggunaan teknologi |
| BMI | Body Mass Index (hasil feature engineering) |
| NObeyesdad | Target kelas tingkat obesitas |

---

## 4. 🔧 Data Preparation
Tahapan data preparation yang dilakukan:
- **Cleaning**:  
  - Pengecekan missing values  
  - Penghapusan data duplikat  
  - Analisis outliers (tidak dihapus karena masih realistis)
- **Transformasi**:  
  - Encoding fitur kategorikal menggunakan Label Encoding  
  - Scaling fitur numerik menggunakan MinMaxScaler
- **Splitting**:  
  - Train-Test Split (80:20) dengan stratified sampling  
  - Validation set digunakan pada model deep learning

---

## 5. 🤖 Modeling

### Model 1 – Baseline
- **Logistic Regression**
- Digunakan sebagai model dasar untuk pembanding performa

### Model 2 – Advanced Machine Learning
- **Random Forest Classifier**
- Mampu menangkap hubungan non-linear dan memberikan feature importance

### Model 3 – Deep Learning
- **Multilayer Perceptron (MLP)**
- Arsitektur neural network untuk data tabular multiclass

---

## 6. 🧪 Evaluation
### Metrik Evaluasi
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Hasil Singkat

| Model | Accuracy | Catatan |
|-----|---------|--------|
| Logistic Regression | ± 0.78 | Model baseline, cenderung underfitting |
| Random Forest | ± 0.99 | Model terbaik, performa sangat stabil |
| MLP (Deep Learning) | ± 0.90 | Mampu menangkap pola non-linear |

---

## 7. 🏁 Kesimpulan
- **Model terbaik**: Random Forest  
- **Alasan**:  
  Memberikan performa tertinggi dengan akurasi hampir sempurna dan generalisasi yang baik pada data uji.  
- **Insight penting**:  
  Faktor fisik (BMI, Weight, Height) dan kebiasaan hidup memiliki pengaruh besar terhadap tingkat obesitas.

---

## 8. 🔮 Future Work
- Menambah jumlah dan variasi data
- Melakukan hyperparameter tuning lebih lanjut
- Mencoba arsitektur deep learning yang lebih kompleks
- Mengembangkan sistem ke tahap deployment (Streamlit / FastAPI)

---

## 9. 🔁 Reproducibility
### Environment
- Python 3.10
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- tensorflow

### Menjalankan Proyek
```bash
pip install -r requirements.txt
