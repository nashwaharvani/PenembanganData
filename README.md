# Klasifikasi Depresi pada Mahasiswa dengan Decision Tree (CART)

Paket final untuk proposal Data Mining (narasi proposal + kode dalam satu notebook):
preprocessing, sampling 2.000 data, EDA, 4 skenario eksperimen, evaluasi, feature importance, dan aturan keputusan.

## Isi folder
- `Final_Proposal_Klasifikasi_Depresi_DecisionTree.ipynb` : notebook final (isi proposal Soal 1-6 + implementasi + kesimpulan otomatis + daftar pustaka)
- `requirements.txt` : daftar library
- `data/` : tempat menaruh dataset (CSV)
- `outputs/` : hasil otomatis (grafik PNG, tabel CSV, aturan keputusan TXT)

## Cara menjalankan
1. Unduh dataset Kaggle: https://www.kaggle.com/datasets/hopesb/student-depression-dataset
2. Simpan sebagai `data/student_depression_dataset.csv`
3. Install library: `pip install -r requirements.txt`
4. Jalankan: `jupyter notebook`, buka file .ipynb, lalu Kernel > Restart & Run All
   (atau upload semua ke Google Colab dan jalankan sel dari atas)

## Parameter penting (sel "0. Pengaturan")
- `USE_SAMPLE = True`, `N_SAMPLE = 2000` : memakai sampel 2.000 data (stratified)
- `TEST_SIZE = 0.20` : split 80:20
- `CV_FOLDS = 5` : cross-validation 5 lipatan
- `RANDOM_STATE = 42` : hasil selalu sama jika dijalankan ulang

## Skenario
S1 default | S2 tuning + pruning | S3 tanpa variabel dominan (pikiran bunuh diri) | S4 class_weight balanced

## Catatan
- Hasil model bukan alat diagnosis. Data berupa survei self-report.
- Nama kolom dataset dideteksi otomatis. Jika ada error nama kolom, cek `df_raw.columns`.
- Angka hasil (akurasi, dll.) akan keluar setelah kamu menjalankan notebook dengan data asli;
  isi bagian "Ringkasan" di akhir notebook dengan angka dari hasilmu sendiri.
