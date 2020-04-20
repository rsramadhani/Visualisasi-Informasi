# VISUALISASI INFORMASI - UTS


Visualisasi data merupakan representasi visual dan teknik interaksi dengan memanfaatkan indera penglihatan manusia yang diolah dalam pikiran sehingga memungkinkan pengguna dapat melihat, menjelajahi, dan memahami sejumlah besar informasi sekaligus.Visualisasi informasi membantu pengguna untuk memperoleh pengetahuan melalui berbagai macam variabel data yang disajikan dalam bentuk grafis.

### Manfaat Visualisasi Data

1. Memudahkan pengguna melihat, menjelajahi, dan memahami sejumlah informasi sekaligus.
2. Membantu pengguna untuk memperoleh pengetahuan baru tentang sebuah proses.
3. Membantu pengguna untuk menentukan keputusan.

### Framework yang digunakan pada visualisasi data ini adalah:

Codeigniter v3.x.x (PHP Framework)
Uikit v3.x.x (UI Framework)
Google Charts (Visualization Framework)

### Tahapan Visualisasi

##### 1. Menentukan data row yang akan kita olah. 

Data row merupakan sekumpulan baris data yang memuat beberapa variabel informasi. Tabel dibawah ini merupakan contoh data row. Data row dapat berasal dari satu atau beberapa tabel dalam sql, misalnya, atau berasal dari sumber lain misalnya API sebuah sistem atau file excel. Tahap pertama yang harus kita siapkan dalam visualisasi data adalah memastikan bahwa data yang kita miliki sudah dalam bentuk terstruktur dalam baris data. 

#### 2. Menyusun problem statement.

Data row pada poin 1 memuat variabel gender, semester, dan ipk untuk mahasiswa dengan nim tertentu. Tabel tersebut sudah memiliki informasi, misalnya, mahasiswa dengan nim 0786373 adalah laki-laki yang sedang menempuh semester 3 dan memiliki IPK 3.25. Tetapi data tersebut belum memiliki informasi secara menyeluruh yang dapat memberikan pengetahuan tertentu. Oleh sebab itu kita perlu untuk menyusun problem statemen yang dapat menggambarkan informasi apa saja yang akan disampaikan kepada pengguna.

#### 3. Membuat data tabel dalam format cross tabulation.

Langkah berikutnya adalah menyusun cross tabulation berdasarkan baris data dan problem statement. Satu probem statement akan menghasilkan satu cross tabulation. Mungkin tahap ini akan memerlukan algoritma untuk membuat data row menjadi format cross tabulation yang kita inginkan.

#### 4. Menentukan teknik visualisasi. 

Teknik visualisasi merupakan bentuk visual yang digunakan untuk menampilkan data. Secara umum teknik visualisasi terdiri dari Pie Chart (diagram lingkaran), Bar Chart (diagram batang), line chart (diagram garis), atau gabungan antara bar chart dan line chart. Pada tahap ini, kita menganisa teknik yang tepat untuk setiap cross tabulation yang sudah dibuat pada tahap sebelumnya.
Menentukan layout. Tahap layouting merupakan tahap menentukan posisi dari setiap visualisasi pada layar utama visualisasi agar pengguna dapat menerima sejumlah besar informasi sekaligus. Oleh sebab itu halaman visualisasi sebaiknya merupakan single page sehingga aspek penyampaian informasi secara sekaligus dapat terpenuhi.

### Algoritma Konversi

Berdasarkan format data json yang ada, kita perlu untuk mengkonversi sehingga menjadi tabulasi yang diharapkan. 
* Buatlah variabel array C.
* Lakukan perulangan untuk setiap data.
* Jika belum terdapat region yang sama didalam C simpan variabel region dan unit.
* Jika terdapat region yang sama dalam C maka jumlahkan unit.

Proses menggambar grafik dilakukan oleh fungsi drawChart(dataArray,type,container). Teknik ini dipakai untuk mengurangi penulisan kode secara berulang. Parameter pada fungsi drawChart() diantaranya adalah:

#### dataArray
Data dalam format Array yang diperoleh dari hasil parsing data yang diperoleh dari variabel PHP. Proses parsing data dilakukan menggunakan Javascript menggunakan fungsi JSON.parse().

#### type
Tipe chart yang digunakan (‘pie', ‘bar', ‘column')

#### container
Nama id dari elemen yang akan digunakan sebagai container grafik. Menampilkan data penjualan berdasarkan region dilakukan oleh kode berikut:

    ...
    drawChart(region['dataArray'], 'pie','region');
    ...
 
