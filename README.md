# Klasifikasi

Klasifikasi adalah permasalahan dalam machine learning, yang memiliki tujuan untuk mempelajari tentang bagaimana mengelompokkan suatu data ke dalam suatu kelas yang sesuai yang telah disediakan sebelumnya. Klasifikasi ini mirip dengan permasalahan klasterisasi, dimana kita memiliki tujuan untuk membentuk kelompok data, namun pada klasifikasi ini, kita telah memiliki label atau kelas untuk mengelompokkan data-data tersebut sehingga klasifikasi ini termasuk ke dalam kategori supervised learning. Contoh sederhana dari masalah klasifikasi ini adalah masalah untuk mengklasifikasi sebuah email spam dimana kelasnya adalah email spam atau tidak.  
Terdapat beberapa algoritma untuk menyelesaikan masalah klasifikasi ini yakni Decision Tree, Naive Bayes, Logistic Regression, Support Vector Machine (SVM) dan sebagainya. Berikut ini akan dijelaskan mengenai algoritma-algoritma tersebut.

## Decision Tree

Decision tree adalah salah satu contoh penyelesaian masalah klasifikasi yang menggunakan struktur seperti pohon. Decision tree ini dapat digunakan untuk menyelesaikan masalah-masalah klasifikasi dan regresi. Pada bagian ini, akan difokuskan untuk penerapan decision tree pada kasus klasifikasi.  
Decision tree seperti namanya memiliki tujuan untuk membentuk pohon keputusan yang nantinya akan berguna untuk memprediksi kelas dari suatu data yang tidak diketahui kelasnya. Pohon tersebut memiliki implementasi yang mirip dengan logika berpikir manusia. Di dalam pohon tersebut terdapat elemen-elemen yakni root, decision node, leaf.

1. Root merupakan sebuah node yang terletak paling atas. Root ini dalam kasus decision tree merupakan salah satu atribut dalam dataset yang dimiliki. Root ini adalah atribut yang pertama kali ditinjau dalam menentukan kelas dari sebuah data.
2. Decision node adalah sebuah sub node dari sebuah node induk yang menunjukkan atribut berikutnya yang akan ditinjau. Decision node ini terletak diantara root dan leaf.
3. Leaf merupakan node yang berada paling akhir sekaligus menyatakan hasil dari kelas sebuah data yang diprediksi

Dalam membangun sebuah decision tree, hal pertama yang akan kita lakukan adalah menentukan root node. Root node ini biasanya ditentukan dengan menggunakan salah satu dari beberapa algoritma yang berkaitan dengan decision tree. Selanjutnya root node ini akan dilakukan proses splitting untuk menentukan sub-sub node selanjutnya. Proses tersebut akan terus dilanjutkan hingga tercipta sebuah decision tree yang lengkap dengan leafnya.

Algoritma-algoritma yang digunakan dalam proses splitting suatu node adalah sebagai berikut.

1.  ID3  
    Algoritma ini adalah salah satu algoritma yang digunakan untuk membangun sebuah decision tree dari dataset. ID3 menggunakan konsep yang disebut sebagai entropy dan information gain. Entropy adalah suatu ukuran yang menyatakan ketidakpastian/keberagaman yang terdapat dalam dataset. Nilai dari entropy ini berkisar dari 0 hingga 1. 0 menyatakan bahwa data yang dimiliki semuanya seragam sedangkan 1 menyatakan bahwa data dalam dataset ini memiliki keragaman.
    Information gain atau disebut sebagai gain saja mengukur seberapa bagus sebuah atribut dalam mengklasifikasikan kelas dari suatu data. Atribut yang memiliki gain tertinggi akan digunakan sebagai root node
2.  C4.5  
    Algoritma C4.5 adalah pengembangan dari algoritma C4.5. Karena merupakan pengembangan, maka algoritma ini memiliki konsep yang hampir sama dengan algoritma ID3. Perbedaannya adalah untuk menentukan atribut terbaik, maka algoritma C4.5 menggunakan gain ratio yakni hasil dari pembagian antara information gain dan split information
3.  CART  
    CART adalah salah satu algoritma yang digunakan dalam klasifikasi decision tree. Algoritma CART menggunakan pengukuran bernama Gini Index untuk menentukan atribut optimal dalam menyusun decision tree.
    Gini index ini mengukur tingkat impurity dari sebuah atribut. Atribut dengan gini index terendah akan menjadi prioritas utama
4.  CHAID  
    CHAID (Chi-Square Automatic Interaction Detection) adalah algoritma decision tree yang menggunakan chi-square dalam menentukan atribut optimum dalam menyusun pohon keputusan.
