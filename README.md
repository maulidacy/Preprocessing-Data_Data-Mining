# Credit Approval Dataset Preprocessing

Proyek ini berisi tugas untuk melakukan *preprocessing data* pada dataset *Credit Approval* dari UCI Machine Learning Repository.  
Dataset ini sering digunakan untuk percobaan dalam klasifikasi (credit card approval).  

## Tahapan Preprocessing
Langkah-langkah yang dilakukan dalam preprocessing ini meliputi:

1. *Import Dataset*
   - Menggunakan pandas untuk membaca file crx.data dari UCI.
   - Tanda ? dianggap sebagai nilai missing.

2. *Handle Missing Values*
   - Kolom numerik diisi dengan *median*.
   - Kolom kategorikal diisi dengan *modus* (nilai yang paling sering muncul).

3. *Handle Outliers*
   - Outlier dibatasi dengan metode *IQR (Interquartile Range)*.
   - Nilai yang terlalu kecil/besar dipotong ke batas bawah/atas.

4. *Encoding Data Kategorikal*
   - Menggunakan *OneHotEncoder* agar data kategorikal berubah jadi variabel dummy.

5. *Split Dataset*
   - Membagi data menjadi *80% train* dan *20% test*.
   - Target label: + → *1 (approved)*, - → *0 (rejected)*.

6. *Feature Scaling*
   - Fitur numerik distandardisasi dengan *StandardScaler* (mean = 0, std = 1).
   - Scaling hanya di-fit ke data train untuk mencegah data leakage.

## File di Repo
- preprocessing.ipynb → Notebook dengan langkah-langkah preprocessing + penjelasan tiap tahap.
- preprocessing.py → Script Python untuk menjalankan preprocessing secara langsung (opsional).
- README.md → Penjelasan tentang proyek ini.

## Dataset
Dataset bisa diunduh dari:  
[UCI Credit Approval Dataset](https://archive.ics.uci.edu/dataset/27/credit%2Bapproval)

## Cara Menjalankan
1. Clone repository ini:
   ```bash
   git clone https://github.com/username/Preprocessing-Data_Data-Mining.git
   cd Preprocessing-Data_Data-Mining
2. Install library yang dibutuhkan:
    ```bash
   pip install pandas numpy scikit-learn
3. Jalankan script atau notebook:

   Notebook: buka Preprocessing_Data.ipynb di Jupyter/VSCode.
   
   Script:
   ```bash
   python Preprocessing_Data.py


