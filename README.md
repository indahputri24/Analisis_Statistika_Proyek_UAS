# Statistical Analysis with Python

Proyek UAS mata kuliah Statistika dan Probabilitas yang menerapkan statistika inferensial pada lima dataset publik dari Kaggle. Fokusnya adalah memeriksa asumsi data, memilih metode uji yang sesuai (parametrik atau nonparametrik), lalu menginterpretasikan hasilnya.

## Isi Repositori

| File | Keterangan |
|---|---|
| `Notebook_Analisis_Statistika.ipynb` | Notebook analisis (Google Colab) |
| `Laporan_Proyek_Analisis.pdf` | Laporan lengkap beserta interpretasi |

## Dataset

| Dataset | Baris | Digunakan pada |
|---|---|---|
| [Profile of Body Metrics and Fashion Colors](https://www.kaggle.com/datasets/rulanugrh/profile-of-body-metrics-and-fashion-colors) | 25.000 | Bab I, II, III, VII, VIII |
| [Blood Sugar Level](https://www.kaggle.com/datasets/hssiqueira/blood-sugar-level) | 326 | Bab IV |
| [Iris Flower Dataset](https://www.kaggle.com/datasets/arshid/iris-flower-dataset) | 147 | Bab V |
| [Supplement Sales Data](https://www.kaggle.com/datasets/zahidmughal2343/supplement-sales-data) | 4.384 | Bab VI |
| [Fish Market](https://www.kaggle.com/datasets/vipullrathod/fish-market) | 159 | Bab IX |

## Tools

Python (Google Colab), Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels, scikit-learn.

## Metode Analisis

| Bab | Metode |
|---|---|
| I | Uji normalitas (visual, Shapiro-Wilk, D'Agostino-Pearson, Jarque-Bera) |
| II | Uji *t* 1-sampel |
| III | Uji Levene dan Mann-Whitney U (pengganti uji *t* saling bebas) |
| IV | Uji Wilcoxon (pengganti uji *t* berpasangan) |
| V | ANAVA 1 arah, dengan uji homogenitas Hartley, Bartlett, dan Levene |
| VI | ANAVA 2 arah, dengan uji asumsi residual |
| VII | Korelasi Pearson |
| VIII | Regresi linear sederhana |
| IX | Regresi linear berganda, VIF, dan uji asumsi residual |

## Temuan Utama

- **Uji *t* 1-sampel:** rata-rata berat badan sampel (57,64 kg) berbeda signifikan dari 60 kg (t = -70,48; p < 0,05).
- **Laki-laki vs perempuan:** data tidak normal dan varians tidak homogen, sehingga dipakai Mann-Whitney U. Berat badan kedua kelompok berbeda signifikan (p < 0,05).
- **Sebelum vs sesudah makan malam:** selisih data tidak normal, sehingga dipakai Wilcoxon. Kadar gula darah 2 jam setelah makan malam (rata-rata 169,4) signifikan lebih tinggi daripada sebelumnya (rata-rata 112,2).
- **ANAVA 1 arah (Iris):** *sepal width* berbeda signifikan antarspesies (F = 48,63; p < 0,05).
- **ANAVA 2 arah (suplemen):** lokasi, platform, dan interaksinya tidak berpengaruh signifikan terhadap unit terjual (p = 0,268; 0,258; 0,185).
- **Korelasi dan regresi sederhana:** tinggi dan berat badan berkorelasi positif sedang (r = 0,503). Model: berat = -37,46 + 0,55 × tinggi (R² = 25,3%). Asumsi residual terpenuhi.
- **Regresi berganda (Fish Market):** berat dan tinggi ikan menjelaskan 83,4% variasi lebar ikan (F = 391,0; p < 0,05).

## Keterbatasan

Pada regresi berganda, uji Breusch-Pagan menunjukkan heteroskedastisitas dan uji Breusch-Godfrey menunjukkan autokorelasi residual (keduanya p < 0,05). Model lebih tepat dipakai untuk melihat arah hubungan antarvariabel daripada prediksi yang presisi.

## Cara Menjalankan

1. Unduh dataset dari tautan Kaggle di atas.
2. Unggah ke Google Drive, lalu sesuaikan path pada sel pembacaan data di notebook (contoh: `/content/drive/MyDrive/PANDAS/...`).
3. Jalankan sel secara berurutan (*Runtime → Run all*).

## Penulis

Indah Putri Lestari
