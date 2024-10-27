# SUMMARY
## STAGE 1
1. **Dominasi Cash Loans**: Cash loans memiliki jumlah kredit yang jauh lebih besar dibandingkan dengan revolving loans, menunjukkan preferensi pelanggan terhadap cash loans. Namun, revolving loans memiliki tingkat default yang lebih rendah.

2. **Pendidikan dan Pendapatan**: Tingkat pendidikan yang lebih tinggi berkorelasi dengan pendapatan yang lebih tinggi, terutama bagi nasabah dengan risiko rendah. Nasabah berisiko tinggi dengan academic degrees tetap menunjukkan kemungkinan gagal bayar yang lebih besar.

3. **Status Perkawinan dan Kredit**: Nasabah yang sudah menikah umumnya menerima jumlah kredit yang lebih tinggi. Namun, nasabah berstatus janda memiliki jumlah kredit lebih rendah untuk nasabah dengan status baik (Target 0).

4. **Jenis Kelamin dan Pendapatan**: Laki-laki umumnya memiliki pendapatan yang sedikit lebih tinggi dibandingkan perempuan, dengan pola risiko yang berbeda berdasarkan gender. Kategori "XNA" (mungkin data yang tidak teridentifikasi) juga menunjukkan pendapatan yang relatif tinggi.

5. **Jenis Tempat Tinggal dan Anuitas**: Nasabah yang memiliki rumah atau tinggal di apartemen memiliki jumlah angsuran bulanan yang lebih tinggi, sementara yang tinggal dengan orang tua memiliki jumlah anuitas terendah. Perilaku pembayaran bervariasi berdasarkan jenis tempat tinggal dan profil risiko.

6. **Perhitungan Default Rate**: Pengukuran default rate pada dataset bureau mencakup kredit tertunggak dan total kredit. Kredit tertunggak yang tinggi pada kategori seperti bad debt mengungkapkan pola risiko tertentu.

7. **Jenis Kredit dan Pembayaran**: Kredit aktif dan sold menunjukkan pembayaran tahunan tertinggi, yang menunjukkan keandalan pelanggan yang lebih baik, sementara status closed dan bad debt menunjukkan kontribusi tahunan yang lebih rendah.

8. **Rekomendasi**:
   - Fokus pada optimasi cash loans dan manajemen risikonya.
   - Sediakan program edukasi keuangan dan program loyalitas untuk meningkatkan retensi pelanggan, terutama bagi nasabah berpendidikan tinggi dan pelanggan setia.
   - Kembangkan opsi pembayaran yang fleksibel untuk nasabah berisiko tinggi, terutama untuk kontrak active dan approved.

## STAGE 2
1. Data Cleansing
   - HC_application_train: Penanganan missing values dengan mean/median (untuk data numerik) dan modus/Unknown (untuk kategorikal). Outliers diatasi menggunakan Interquartile Range (IQR), dan fitur AMT_INCOME_TOTAL ditransformasi menggunakan log. Encoding dilakukan dengan Label Encoding, dan class imbalance diatasi dengan SMOTE.
   - HC_bureau dan bureau_balance: Digabungkan sebelum diproses lebih lanjut. Missing values ditangani dengan median, outliers menggunakan IQR, dan fitur-fitur ditransformasi menggunakan Yeo-Johnson. Fitur kategorikal di-encode menggunakan Ordinal dan Frequency Encoding. Class imbalance diatasi dengan SMOTE pada kolom CREDIT_DAY_OVERDUE.
   - HC_POS_CASH_balance, credit_card_balance, dan instalments_payments: Missing values diisi dengan median atau mean. Outliers diatasi dengan capping, transformasi log diterapkan pada beberapa fitur, dan kategorikal encoding menggunakan One-Hot Encoding.
2. Feature Engineering
   - Feature Selection: Menghapus fitur redundan berdasarkan analisis korelasi dan metode seperti RFE, Correlation Matrix Spearman, dan Feature Importance. Fitur penting yang dipertahankan mencakup EXT_SOURCE_MEAN, NUM_DOCUMENTS, dll.
   - Feature Extraction: Membuat fitur baru seperti EXT_SOURCE_MEAN dan CREDIT_TYPE_Encoded. Pada HC_bureau, fitur dengan korelasi tinggi atau informasi yang berlebihan dihapus. Pada HC_POS_CASH_balance ditambahkan fitur seperti remaining_instalment_pct dan credit_duration. Pada credit_card_balance dan instalments_payments, fitur tambahan seperti Payment to Balance Ratio dan Debt-to-Income Ratio ditambahkan untuk memperkaya model.
