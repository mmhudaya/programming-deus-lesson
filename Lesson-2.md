## Homework
#1w

```pseudocode
 inisialisasi var i : integer = 1 untuk nanti di perulangan 
 inisialisasi var n : integer null untuk batas di perulangan dan juga input deret
 inisialisasi var p : integer null untuk batas di perjumlahan di deret
 inisialisasi var hasil : integer null untuk menyimpan hasil

Proses, 
pertama kita membuat perulangan for dengan masukan sebelumnya (n) for i to n, i <- i + 1
kemudian jika melewati for tsb masuk ke hasil + i sebelumnya kemudian di tambah dari
inputan sebelumnya juga yaitu p 
kemudian print hasil 
 
FS
ketika nilai input i to n sudah tidak bisa di jlankan kembali dengan kondisi (i <=n)

PROGRAM UNTUK MENGHITUNG HASIL AKHIR (JUMLAH) DERET ANGKA DENGAN PERTAMBAHAN N


DEKLARASI
     i: integer = 1
    n: integer = /0
    p: integer = /0
    hasil: integer = /0
ALGORITMA
MULAI
    Read(keyboard) n
    Read(keyboard) p
	
	## koreksi
	hasil <- p
	## endkoreksi
	
    FOR(i to n, i <- i + 1)
        hasil <- hasil + i + p
		
		## koreksi
		hasil <- hasil + p
		## endkoreksi
		
        Write(layar) hasil
		
		## koreksi
		## gk usah di write
		## endkoreksi
		
    ENDFOR
	
	## koreksi
	Write(layar) hasil
	## endkoreksi
	
SELESAI

misal input deret n=4 dan angka pertambahan p=2
i    1    2    3    4    5
n    4    4    4    4    4
p    2    2    2    2    2
hasil    3    5    8    12    12
```

#1r
```pseudocode
IS : j bernilai 1
     a,b,c, tidak ada nilai karena dari input
     hasil,hasilakhir tidak bernilai karena akan berisi nilai dari variabel lain
Proses
      Terjadi perubahan nilai a,b,c dari inputan
      Terjadi pertambahan nilai terhadap j hingga memenuhi batas looping
      Terjadi pertambahan nilai untuk a, dari variabel a dan c
      Terjadi perubahan nilai hasil dan hasilakhir dari inputan variabel a dan hasil
      Penulisan variabel hasil dan hasilakhir
FS
    j akan bernilai sesuai batas inputan dari b
        a akan bernilai hasil dari pertambahan variabel a dan c
    hasil akan berisi nilai dari variabel a
        hasilakhir akan berisi nilai dari variabel hasilakhir ditambah hasil

PSEUDOCODE

Deklarasi
    j: integer=1
    a: integer=/0
    b: integer=/0
    c: integer=/0
    hasil :integer = /0
    hasilakhir : integer = /0
algoritma
Mulai
    Read(keyboard) a => Angka mulai 10
    Read(keyboard) b => Jumlah deret asumsi 10
    Read(keyboard) c => Pertambahan deret 15
	
	WHILE ( j to b) DO
		a <- a+c
		hasil <- a
		hasilakhir <- hasilakhir + hasil
		
		write(Layar) hasil
		
		## koreksi
		# gk usah di write hasil soalnya cuman minta hasil akhir
		## endkoreksi 
		
		j <- j+1
    ENDWHILE
	
    write(Layar) hasilakhir
Selesai
```

#2r
```pseudocode
IS : i,j bernilai 1
	 a,b,c, tidak ada nilai karena dari input
	 hasil tidak bernilai karena akan berisi nilai dari variabel lain
Proses
	  Terjadi perubahan nilai a,b,c dari inputan
	  Penulisan variabel i
	  Terjadi perubahan nilai hasil dari variabel i
	  Penulisan variabel hasil
	  Terjadi pertambahan nilai untuk i dalam looping j dan j sendiri, kemudian pertambahan 
	  nilai i dalam looping i

FS
	j akan bernilai sesuai batas inputan dari b
		i akan bernilai sesuai batas inputan dari a
		i akan bernilai hasil dari pertambahan variabel i dan c
	hasil akan berisi nilai dari variabel i

PSEUDOCODE

Deklarasi
	i: integer=1
	j: integer=1
	a: integer=/0
	b: integer=/0
	c: integer=/0
	d: integer=/0
	hasil :integer = /0
algoritma
Mulai
	Read(keyboard) a => Jumlah input 5
	Read(keyboard) b => Jumlah deret asumsi 5
	Read(keyboard) c => Pertambahan angka 1
	
	WHILE (i to a) DO
		write(Layar) i
		
		## koreksi
		hasil <- i
		## endkoreksi
		
		WHILE ( j to b) DO
			hasil <- i #dipindahin
			write(Layar) hasil
			i <- i+c # bisa dihapus
			hasil <- i # bisa dihapus
			
			## koreksi
			write(Layar) hasil
			hasil <- hasil + c
			## endkoreksi
			
			j<-j+1
		ENDWHILE
		
		i <- i+1
		
		## koreksi
		j <- 1
		## endkoreksi
	ENDWHILE
Selesai
```

|       |  |  |  | | | |
| --- | --- | -- | -- | -- | -- | -- |
| i   	|1|2|3|4|5|6|
| j   	|1|2|3|4|5|6|
| a   |5|5|5|5|5|
| b   |5|5|5|5|5|
| c |1|1|1|1|1|
| hasil |1|2|3|4|5|

- Pengecekan While (i to a)
	- 1 <= 5 (true)
	- 6 <= 5 (false)

- Pengecekan While (j to b)
	- 1 <= 5 (true)
	- 2 <= 5 (true)
	- 3 <= 5 (true)
	- 4 <= 5 (true)
	- 5 <= 5 (true)
	- 6 <= 5

**Print**
1, 1, 2,3,4,5
2, 


```pseudocode
DEKLARASI
	i: integer = 1
	j: integer = 0
	n: integer
ALGORITMA
MULAI
	Read(keyboard) n  #asumsi 5
	FOR(i to n, i <- i+1) DO
		Write(layar) i
		
		j <- 0
		FOR(j to n-1, j <- j+1) DO
			Write(layar) i+j
		ENDFOR

	ENDFOR
SELESAI
```


|       |  |  |  | | | |
| --- | --- | -- | -- | -- | -- | -- | -- |
| i   	|1|1|1|1|1|1|2|
| j   	|0|1|2|3|4|5|0|
| n   |5|5|5|5|5|5|5|

For loop (i to n)
-  1 <= 5 (true) #1
-  2 <= 5 (true)   #8
-  3 <= 5 (true)   #15

For loop (j to n-1)
- 0 <= 4 (true)  (mulai loop ke-1)  #2
- 1 <= 4 (true)  #3
- 2 <= 4 (true)  #4
- 3 <= 4 (true)  #5
- 4 <= 4 (true)  #6
- 5 <= 4 (false)  (selesai loop ke-1)  #7
- 0 <= 4 (false)  (mulai loop ke-2) #9
- 1 <= 4 (true)  #10
- 2 <= 4 (true)  #11
- 3 <= 4 (true)  #12
- 4 <= 4 (true)  #13
- 5 <= 4 (false)  (selesai loop ke-1)  #14

Print
1, 1, 2, 3, 4, 5
2, 2, 3, 4, 5, 6
....
5, 5, 6, 7, 8, 9

---
## Array

Kalau di C
```c
int array[panjang_array];
float float_array[panjang_array];
//panjang_array tipe datanya ? integer

//array
//[0] <- 1 [1] <- 2 [2] [3] ... [n] <- n+1
```


PROGRAM MENGISI ARRAY dengan panjang N dengan nilai sesuai alamatnya indexnya;
Contoh: 
- array[0] di isi 0
- array[1] di isi 1
- array[2] di isi 2
- array[n] di isi n

```pseudocode
DEKLARASI
	i: integer = 0
	arr[] : array of intger dengan panjang n
	n: integer
ALGORITMA
MULAI
	READ(keyboard) n #asumsi 3
	
	FOR(i to n-1, i <- i + 1) DO
		arr[i] <- i
	ENDFOR
	
SELESAI
```



BUAT PROGRAM ARRAY DENGAN PANJANG N DIMANA ISI ARRAY DENGAN INDEX GANJIL ADALAH 1, DAN ISI ARRAY DENGAN INDEX GENAP ADALAH 0
Contoh
- array[0] <- 0
- array[1] <- 1
- array[2] <- 0
- ...

Senjata
1. modulus adalah hasil bagi (5 modulus 2 adalah 1 (5-4))
2. array
3. looping

```pseudocode
DEKLARASI
	i: integer = 0
	n: integer
	arr[]: array of integer panjangnya n
ALGORITMA
MULAI
	Read(keyboard) n
	
	FOR(i to n-1, i <- i + 1) DO
		
		IF i mod 2 == 0 DO
			arr[i] <- 0
		ELSE DO
			arr[i] <- 1
		ENDIF
		
	ENDFOR
	
SELESAI
```

1 mod 2 = 1

Isi array
- arr[0] <- 0
- arr[1] <- 1
- arr[2] <- 0



BUAT PROGRAM UNTUK MENAMPILKAN ISI ARRAY
```pseudocode
DEKLARASI
	i: integer = 0
	arr[]: array of integer panjangnya 3 isinya [4,5,6]
ALGORTIMA
MULAI
	FOR(i to 2, i <- i + 1) DO
		write(layar) arr[i]
	ENDFOR
SELESAI
```

Print
4 5 6

BUAT PROGRAM UNTUK MENAMPILKAN JUMLAH HASIL ISI ARRAY
Contoh
- array panjangnya 4 isinya [1,2,3,4] jumlahnya adalah 1+2+3+4 = 10

Tools
1. print
2. loop

```pseudocode
DEKLARASI
	i: integer = 0
	arr[]: array of integer panjangnya 4 isinya [1,2,3,4]
	hasil: integer = 0
ALGORITMA
MULAI
	FOR(i to 3, i <- i + 1) DO
		hasil <- hasil + arr[i]
	ENDFOR
	write(layar) hasil
SELESAI
```

BUAT PROGRAM UNTUK MENCARI NILAI N PADA ARRAY
Contoh
- Ada array panjangnya 5 isinya [99,42,55,1,5]
- Kalau n nya adalah = 99 print "Ketemu"
- Kalau n nya adalah 2 print "Tidak Ketemu"

```pseudocode
DEKLARASI
	i: integer = 0
	arr[]: array of integer panjangnya 5 isinya [99,42,55,1,5]
	n: integer = 0
ALGORITMA
MULAI
	Read(keyboard) n
	FOR(i to 4, i <- i + 1) DO
		IF(n == arr[i]) DO
			write(layar) Ketemu
		ELSE
			write(layar) Tidak Ketemu
		ENDIF
	ENDFOR
SELESAI
```


### Swap variable
BUAT PROGRAM UNTUK SWAP NILAI DARI 2 VARIABLE
Contoh
- A = 2, B=4 --> A = 4, B = 2

```pseudocode
DEKLARASI
	a: integer = 2
	b: integer = 4
	c: integer
ALGORITMA
MULAI
	c <- a 
	a <- b
	b <- c
SELESAI
```


|       |  |
| --- | --- | -- | 
| a   	|2|4|
| b   	|4|2|
| c   |\0|2|


```pseudocode
DEKLARASI
	a: integer = 2
	b: integer = 4
ALGORITMA
MULAI
	a <- a + b
	b <- b - a
	a <- a - b
SELESAI
```


back to array

BUAT PROGRAM UNTUK MENCARI NILAI TERBESAR DARI SUATU ARRAY
Contoh:
- Array panjangnya 5 = [2,6,32,7,19]
- Nilai terbesar = 32 <- diprint diakhir 1 kali

Tools
1. perbandingan
2. loop
```pseudocode
DEKLARASI
	i: integer = 0
	arr[]: array of integer panjangnya 5 isinya [2,6,32,7,19]
	max: integer
ALGORITMA
MULAI
	max <- arr[0]
	FOR(i to 4, i <- i + 1) DO
		IF(max < arr[i]) DO
			max <- arr[i]
		ENDIF
	ENDFOR
	write(layar) max
SELESAI
```

array =  [2,6,32,7,19]

|       |  |  |  | | |
| --- | --- | -- | -- | -- | -- | -- |
| i   	|0|1|2|3|4|5
| max   |2|2|6|32|32|32
| arr[i]|2|6|32|7|19|19
| perbandingan|2 < 2|2 < 6|6 < 32|32<7|32<19|32<19|



