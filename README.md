# MODUL TUJUH
 ## SOAL 1
Program di atas adalah program untuk menentukan apakah sebuah titik berada di dalam salah satu atau kedua lingkaran, atau di luar keduanya.
   
   ## Overview
      Program ini terdiri dari satu file bernama 'main.go' dan mencakup komponen-komponen utama berikut:
      - Pernyataan 'package main', yang mendefinisikan paket untuk program yang dapat dieksekusi.
      - Pernyataan 'import', yang digunakan untuk menyertakan paket-paket yang diperlukan (dalam hal ini, 'fmt' dan 'math').
      - Fungsi 'main()', yang merupakan titik awal dari setiap program Go.
      - Struct Titik menyimpan koordinat (x, y) suatu titik.
      - Struct Lingkaran menyimpan koordinat pusat lingkaran (x, y) dan jari-jari r.
      - Fungsi jarak(p, q) menghitung jarak Euclidean antara dua titik p dan q.
      - Fungsi diDalam(lingkaran, titik) mengevaluasi apakah jarak dari titik ke pusat lingkaran lebih kecil atau sama dengan jari-jari lingkaran, yang berarti titik berada di dalam lingkaran.
      
   ## Code Explanation
   ```go
   type Titik struct {
	x, y int
   }
   ```
   Kode di atas adalah definisi struct di dalam bahasa pemrograman Go (Golang). Struct ini digunakan untuk merepresentasikan data titik pada koordinat kartesius dengan dua atribut x dan y
  
   ```go
   type Lingkaran struct {
	  x, y, r int
   }
   ```
   Kode di atas adalah definisi sebuah struct di dalam bahasa pemrograman Go (Golang). Struct ini digunakan untuk merepresentasikan sebuah lingkaran dalam ruang 2D dengan atribut x, y ,dan r

   ```go
   func jarak(p, q Titik) float64 {
	   return math.Sqrt(math.Pow(float64(p.x-q.x), 2) + math.Pow(float64(p.y-q.y), 2))
   }
   ```
   Kode di atas adalah fungsi untuk menghitung jarak antara dua titik dalam ruang 2D menggunakan rumus jarak Euclidean.

   ```go
   func diDalam(lingkaran Lingkaran, titik Titik) bool {
	   jarakKePusat := jarak(Titik{lingkaran.x, lingkaran.y}, titik)
	   return jarakKePusat <= float64(lingkaran.r)
   }
   ```
   Kode di atas adalah fungsi untuk menentukan apakah sebuah titik berada di dalam atau di tepi lingkaran tertentu.

   ```go
   var lingkaran1, lingkaran2 Lingkaran
   ```
   Kode di atas adalah kode deklarasi variabel dalam bahasa pemrograman Go yang digunakan untuk mendeklarasikan dua variabel lingkaran1 dan lingkaran2 dengan tipe data Lingkaran. 

   ```go
   var titik Titik
   ```
   Kode di atas adalah kode deklarasi variabel yang digunakan untuk mendeklarasikan variabel titik dengan tipe data Titik. 

   ```go
   var lingkaran1, lingkaran2 Lingkaran
   ```
   Kode di atas adalah kode deklarasi variabel yang digunakan untuk mendeklarasikan dua variabel lingkaran1 dan lingkaran2 dengan tipe data Lingkaran. 

   ```go
   fmt.Scan(&lingkaran1.x, &lingkaran1.y, &lingkaran1.r)
   fmt.Scan(&lingkaran2.x, &lingkaran2.y, &lingkaran2.r)
   fmt.Scan(&titik.x, &titik.y)
   ```
   Kode di atas adalah kode yang digunakan untuk membaca input dari pengguna melalui fungsi fmt.Scan.

   ```go
   diDalam1 := diDalam(lingkaran1, titik)
   diDalam2 := diDalam(lingkaran2, titik)
   ```
   Kode di atas adalah kode yang memanggil fungsi diDalam untuk memeriksa apakah sebuah titik berada di dalam lingkaran tertentu. Variabel diDalam1 menyimpan hasil pengecekan untuk lingkaran1 dan titik, sementara diDalam2 menyimpan hasil pengecekan untuk lingkaran2 dan titik. 

   ```go
   if diDalam1 && diDalam2 {
		fmt.Println("Titik di dalam lingkaran 1 dan 2")
	} else if diDalam1 {
		fmt.Println("Titik di dalam lingkaran 1")
	} else if diDalam2 {
		fmt.Println("Titik di dalam lingkaran 2")
	} else {
		fmt.Println("Titik di luar lingkaran 1 dan 2")
	}
   ```
   Kode di atas adalah kode yang memanggil fungsi diDalam untuk memeriksa apakah sebuah titik berada di dalam lingkaran tertentu. Variabel diDalam1 menyimpan hasil pengecekan untuk lingkaran1 dan titik, sementara diDalam2 menyimpan hasil pengecekan untuk lingkaran2 dan titik. 

 
 
