
# Market-Basket-Analysis

**Market Basket Analysis** atau `Association Rules` adalah teknik dalam data mining yang digunakan untuk menemukan hubungan atau pola asosiatif antara item dalam dataset yang besar, terutama dalam konteks transaksi ritel. Teknik ini sering digunakan untuk memahami perilaku konsumen dengan menganalisis data transaksi untuk menemukan kombinasi item yang sering dibeli bersama. 

## Komponen Utama dalam Market Basket Analysis:

1. **Itemset**: 
   - Sekumpulan item yang terdapat dalam satu transaksi. Contoh: {roti, susu}.

2. **Support**: 
   - Ukuran seberapa sering suatu itemset muncul dalam dataset. Support dihitung dengan membagi jumlah transaksi yang mengandung itemset tersebut dengan total jumlah transaksi. 
   - Rumus: 
     \[
     \text{Support(X)} = \frac{\text{Jumlah Transaksi yang Mengandung X}}{\text{Total Transaksi}}
     \]

3. **Confidence**: 
   - Mengukur seberapa sering item B muncul dalam transaksi yang juga mengandung item A. Confidence adalah probabilitas bersyarat yang menunjukkan kekuatan aturan asosiatif.
   - Rumus:
     \[
     \text{Confidence(A → B)} = \frac{\text{Support(A dan B)}}{\text{Support(A)}}
     \]

4. **Lift**: 
   - Ukuran untuk mengevaluasi seberapa besar peningkatan probabilitas membeli item B ketika item A sudah dibeli, dibandingkan dengan ketika item B dibeli tanpa memperhatikan item A.
   - Rumus:
     \[
     \text{Lift(A → B)} = \frac{\text{Confidence(A → B)}}{\text{Support(B)}}
     \]
   - Lift > 1: menunjukkan adanya korelasi positif antara A dan B.
   - Lift = 1: menunjukkan bahwa A dan B independen satu sama lain.
   - Lift < 1: menunjukkan adanya korelasi negatif antara A dan B.

### Contoh Penggunaan:
Jika dalam sebuah supermarket ditemukan bahwa pelanggan yang membeli roti sering kali juga membeli susu, maka aturan asosiatif ini bisa ditulis sebagai:
- Aturan: **Roti → Susu**
- Dengan support 10%, confidence 70%, dan lift 1.2, berarti 10% dari semua transaksi melibatkan roti dan susu, dan 70% dari transaksi yang melibatkan roti juga melibatkan susu, dengan probabilitas pembelian susu yang meningkat 20% saat roti dibeli.

### Algoritma yang Digunakan:
Algoritma yang umum digunakan dalam Market Basket Analysis termasuk:
- **Apriori Algorithm**: Menggunakan pendekatan bottom-up di mana frequent itemsets diperoleh dengan membangun itemsets yang lebih besar dari itemsets yang lebih kecil yang sering muncul.
- **FP-Growth**: Membuat struktur data yang disebut FP-Tree untuk menemukan frequent itemsets lebih efisien tanpa perlu menghasilkan kandidat itemset seperti dalam Apriori.

### Aplikasi Praktis:
- **Penentuan layout toko**: Item yang sering dibeli bersama dapat ditempatkan berdekatan.
- **Rekomendasi produk**: E-commerce bisa merekomendasikan produk berdasarkan riwayat pembelian pelanggan.
- **Promosi bundle**: Menawarkan diskon pada kombinasi produk yang sering dibeli bersama.

Market Basket Analysis sangat bermanfaat dalam memahami perilaku konsumen dan meningkatkan strategi pemasaran serta penjualan.
