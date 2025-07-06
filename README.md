# 💱 Analisis Interdependensi dan Peramalan Nilai US Dollar Index (DXY) dan Nilai Tukar EUR/USD Menggunakan Pendekatan Vector Autoregressive (VAR)

## 📌 Latar Belakang

Pasar valuta asing (forex) merupakan indikator penting dari kondisi ekonomi global. Hubungan antara **US Dollar Index (DXY)** dan **nilai tukar EUR/USD** mencerminkan interaksi antara dua kekuatan ekonomi utama dunia: Amerika Serikat dan Uni Eropa. Mengingat besarnya pengaruh kedua mata uang ini terhadap perdagangan dan investasi global, memahami keterkaitannya serta melakukan peramalan terhadap pergerakannya menjadi sangat krusial bagi pembuat kebijakan, investor, dan analis keuangan.

Proyek ini menerapkan pendekatan **Vector Autoregressive (VAR)** untuk menganalisis serta meramalkan dinamika antara DXY dan EUR/USD selama periode sepuluh tahun (Juli 2015 – Juni 2025).

## 🛠 Metodologi

Langkah-langkah analisis yang dilakukan meliputi:

1. **Pengumpulan Data**: Data bulanan DXY dan EUR/USD diambil dari [Investing.com](https://www.investing.com/).
2. **Analisis Eksploratori**: Visualisasi dan deskriptif statistik terhadap kedua deret waktu.
3. **Uji Linearitas**: Menggunakan uji *Terasvirta* untuk memastikan kecocokan model linier.
4. **Uji Stasioneritas**: Menggunakan transformasi Box-Cox dan uji Dickey-Fuller untuk memastikan stasioneritas dalam varians dan rata-rata.
5. **Uji Kausalitas Granger**: Menguji apakah nilai masa lalu dari satu variabel dapat memprediksi variabel lainnya.
6. **Pemodelan VAR**:

   * Penentuan lag optimal berdasarkan kriteria AIC.
   * Estimasi parameter menggunakan metode *least squares*.
7. **Uji Diagnostik**:

   * Uji white noise (Ljung-Box).
   * Uji normalitas multivariat (Mardia’s test).
   * Uji heteroskedastisitas (ARCH-LM).
8. **Peramalan**: Prediksi nilai DXY dan EUR/USD untuk 6 bulan ke depan.
9. **Evaluasi Model**: Akurasi hasil ramalan diukur menggunakan Mean Absolute Percentage Error (MAPE).

## 📊 Kesimpulan

* Model **VAR(3)** dipilih sebagai model terbaik berdasarkan nilai AIC.
* Tidak ditemukan **kausalitas langsung** antar variabel berdasarkan uji Granger, namun terdapat keterkaitan kuat pada lag ke-3.
* Hasil uji diagnostik menunjukkan bahwa residual model bersifat white noise, berdistribusi normal, dan bersifat homoskedastik.
* Hasil peramalan menunjukkan akurasi yang tinggi dengan nilai **MAPE sebesar 2,95% untuk DXY** dan **3,2% untuk EUR/USD**.
* Persamaan akhir dari model menunjukkan bahwa **kedua variabel saling memengaruhi secara signifikan pada lag ke-3**, mendukung pendekatan multivariat dalam peramalan nilai tukar.

Analisis ini membuktikan bahwa pendekatan VAR efektif dalam menangkap dinamika hubungan antar deret waktu keuangan, khususnya dalam konteks pergerakan nilai tukar mata uang. Model yang dibangun dapat menjadi alat bantu yang bermanfaat dalam proses pengambilan keputusan ekonomi dan strategi pasar keuangan.
