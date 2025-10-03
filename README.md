# Credit Approval Dataset Preprocessing

Proyek ini berisi tugas untuk melakukan *preprocessing data* pada dataset *Credit Approval* dari UCI Machine Learning Repository.  
Dataset ini sering digunakan untuk percobaan dalam klasifikasi (credit card approval).  

## Tahapan Preprocessing
Langkah-langkah yang dilakukan dalam preprocessing ini meliputi:

1. *Import Dataset*
   - Menggunakan pandas untuk membaca file crx.data dari UCI.
   - Mengganti tanda '?' menjadi NaN.

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
- Preprocessing_Data.ipynb → Notebook dengan langkah-langkah preprocessing + penjelasan tiap tahap.
- README.md → Penjelasan tentang proyek ini.

## Dataset
Dataset bisa diunduh dari:  
[UCI Credit Approval Dataset](https://archive.ics.uci.edu/dataset/27/credit%2Bapproval)

## Cara Menjalankan
1. Clone repository ini atau download sebagai ZIP.
   
   Clone:
   ```bash
   git clone https://github.com/username/Preprocessing-Data_Data-Mining.git
   cd Preprocessing-Data_Data-Mining
2. Buka file 'Preprocessing_Data.ipynb' di Jupyter Notebook/VSCode.
3. Jalankan sel secara berurutan untuk melihat hasil preprocessing.

  




