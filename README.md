# Association Rules

_Association rules_ adalah teknik _data mining_ yang digunakan untuk mencari hubungan antar variabel yang satu dengan variabel yang lain. _Association rules_ termasuk dalam kategori _unsupervised learning_ karena pada dasarnya, data yang akan digunakan tidak memiliki label. Pada _Association Rules_ terdapat 3 satuan umum yang digunakan yakni

1. **_Support_**  
   Support mengukur persentase munculnya item dalam transaksi
2. **_Confidence_**  
   Confidence mengukur persentase kemunculan item A yang juga mengandung item B dalam transaksi
3. **_Lift_**  
   Lift mengukur relasi antara item A dan item B dalam transaksi yakni seberapa kuat item A dan item B muncul secara bersamaan. Nilai lift > 1 menyatakan bahwa item A dan item B memiliki relasi yang kuat dan nilai lift = 1 menyatakan bahwa tidak ada relasi antara item A dan item B

Dalam _Association Rules_ terdapat beberapa algoritma yang sering digunakan seperti algoritma Apriori dan algoritma _Frequent Pattern Growth_

## Algoritma Apriori

Algoritma Apriori adalah algoritma yang bekerja dengan menggunakan _frequent itemsets_ untuk menghasilkan _Association Rule_. Frequent Itemsets adalah item-item yang memiliki _support_ yang lebih besar dari nilai minimum _support_ yang ditentukan. Jika item A dan item B adalah pasangan item yang memiliki support diatas nilai minimum support, maka masing-masing item A dan B juga memiliki nilai support yang ada di atas nilai minimum support. Dalam algoritma ini juga dikenal konsep k-itemset yakni itemset yang berisi k buah item.  
Secara umum, algoritma Apriori memiliki langkah-langkah sebagai berikut.

1. Tentukan nilai minimum support
2. Iterasi pertama : Buat daftar dari 1-itemset dengan melakukan scan terhadap seluruh transaksi
3. Eliminasi 1-itemset yang memiliki nilai support yang kurang dari nilai minimum support
4. Iterasi kedua: Buat kembali 2-itemset dengan mengkombinasikan k-itemset sebelumnya dan eliminasi 2-itemset yang memiliki nilai support yang tidak memenuhi
5. Ulangi iterasi dengan menambah nilai k pada k-itemset hingga tidak terdapat lagi k-itemset yang memenuhi minimum support

## Algoritma Frequent Pattern Growth (FP-Growth)

Algoritma FP-Growth merupakan pengembangan dari algoritma Apriori. Berbeda dengan algoritma Apriori dimana kita menghasilkan kandidat frequent-itemset disetiap iterasi, FP-Growth bekerja dengan menggunakan FP-Tree. FP-Tree struktur penyimpanan data yang dimampatkan dengan memetakan setiap transaksi ke dalam lintasan tertentu. Jika terdapat transaksi yang memiliki item yang sama , maka lintasaannya dapat saling menimpa.  
Secara umum, langkah-langkah yang diperlukan dalam algoritma FP-Growth adalah sebagai berikut

1.  Tentukan nilai minimum support
2.  Buat sebuah kumpulan 1-itemset yang memenuhi nilai minimum support dan disusun secara menurun
3.  Bangun FP Tree berdasarkan transaksi yang tersedia
4.  Setelah semua transaksi dimasukkan kedama FP Tree, buat dengan melakukan reverse terhadap daftar sebelumnya

## Penerapan Algoritma Apriori dalam Bahasa Pemrograman Python

Untuk penjelasan terkait penerapan algoritma Apriori, dapat mengunjungi berkas [**Tugas1_Machine_Learning_H071191002.ipynb**](https://github.com/yukiao/Pembelajaran-Mesin/blob/association_rules/Tugas1_Machine_Learning_H071191002.ipynb) pada branch ini
