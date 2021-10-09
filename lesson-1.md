SIMPLE PROGRAMMING
- tipe data
- loop
 = while
 = for
 = do-while
- if-else
===aditional===
- switch


BEGINNING PROGRAMMING
- modular programming
- data structure

PARADIGM PROGRAMMING
- Object oriented programming
- Functional programming
- dll


1. Deskripsikeun suatu kejadian
2. State
3. Pseudocode dan Flowchart
----
4. Simple programming



## Program
Untuk menjalankan suatu proses atau algoritma
Butuh:
1. **Code (PROSES)**
	1. 
2. Tujuan (OUTPUT)
3. Hardware (PROSES)





## Code
Struktur suatu bahasa mesin yang memiliki syntax untuk menjalankan suatu proses untnuk mencapai tujuan

### Aya naon wae
#### Variable 
```math
 y = mx + c
 ax + by = c
```

##### Tipe Data
1. Integer
	1. Contoh: -1,-2,1,2,3,4,5,6,
2. String
	1. Contoh: Kumpulan dari karakter => "Kata naon lah"
3. Char
	1. Contoh: karakter => "a" "1" "!" "2"
4. Float
	1. Contoh: 0.1,0.2,0.000003
5. Boolean
	1. Contoh: True False
6. Double
	1. Contoh:  0.1,0.2,0.000003

Java
```java
// Scope Start
// 4.698798754
float data = 4.698798754;

System.out.println(a);
// Scope end
```


Python
```py
parse_float("0.000001")
```


#### Syntax
PSEUDOCODE #1
```pseudocode
PROGRAM PERTAMBAHAN 2 BILANGAN
DEKLARASI
	a: float
	b: float
	hasil: float
ALGORITMA
MULAI
	Read (keyboard) a,b
	hasil <- a + b
	Write (layar) hasil
SELESAI
```

PSEUDOCODE #2
```pseudocode
PRORGRAM PENENTU SUHU APAKAH PANAS, DINGIN, NORMAL
 - Panas kalau lebih dari 40 derajat
 - Digin kalau kurang dari 15 derajat
 - Sisanya termasuk suhu normal
DEKLARASI
	suhu: float
	hasil: string
ALGORITMA
MULAI
	Read (keyboard) suhu
	IF suhu > 40 THEN
		hasil <- panas
	ELSE IF suhu < 15 THEN
			hasil <- dingin
		ELSE
			hasil <- normal
		ENDIF
	ENDIF
	Write(layar) hasil
SELESAI
```

PSEUDOCODE #3
```pseudocode
PROGRAM MENENTUKAN INDEKS IPK
 - Lebih dari sama dengan 3.5 Cum laude
 - lebih dari sama dengan 3.0 dan kurang dari 3.5 sangat memuasakan
 - kurang dari 3.0 dan lebihd ari 2.0 memuaskan
 - selain itu tidak terindex
 
DEKLARASI
 	ipk: float
	hasil: string
ALGORITMA
MULAI
	Read(keyboard) ipk
	IF ipk >= 3.5 THEN
		hasil <- "cum laude"
		ELSE IF ipk >= 3.0 AND ipk < 3.5 THEN
			hasil <- "sangat memuaskan"
			ELSE IF ipk < 3.0 AND ipk > 2.0 THEN
				hasil <- "memuaskan"
			ELSE
				hasil <- "tidak terindex"
			ENDIF
		ENDIF
	ENDIF
	
	Write(layar) hasil
SELESAI
```


Truth table (done)

| A      | B | AND | OR |
| ----------- | ----------- | ----------- | ----------- |
| True      | True       | True | True|
| True   | False        | False | True|
| False   | True        | False | True|
| False   | False        | False | False|


### Loop
1. For
```pseudocode
DEKLARASI
	A: integer = 1
ALGORITMA
MULAI
	FOR (A <- 1 TO 10, A <- A + 1) DO
		Write(layar) A
	ENDFOR
SELESAI
```

```pseudocode
IS
	A = 1
Proses
	A = (layar) 1 -> (layar) 2 -> (layar) 3 -> (layar) 4 -> (layar) 5 ->
	(layar) 6 -> (layar) 7 ->(layar) 8 -> (layar) 9 -> (layar) 10 -> 11
FS
	A = 11
```

2. While do
```pseudocode
DEKLARASI
	A: integer = 11
ALGORITMA
MULAI
	WHILE(A <= 10) DO
		Write(layar) A
		A <- A + 1
	ENDWHILE
SELESAI
```
4. Do while
```pseudocode
DEKLARASI
	A: integer = 11
ALGORITMA
MULAI
	DO
		Write(layar) A
		A <- A + 1
	WHILE(A<=10)
	ENDWHILE
SELESAI
```


### Simple test
```pseudocode
PROGRAM MENJUMLAHKAN ANGKA DARI 1 hingga N
1 - 3 => 1 + 2 + 3
```


```pseudocode
Pseudocode
Penjumlahan angka dari 1 Hingga N
1-3 => 1+2+3
Deklarasi
    a : integer = 0
    b : integer = 1
    c : integer = 1
    n : integer
    hasil : integer
ALGORITMA    
MULAI
    Read (keyboard) n
    For (c to n, c <- c + 1) Do
        write hasil <- a
		b <- b + 1
		a <- a + b
    End For
    Write (layar) hasil
SELESAI
```


IS
	a = 1
	b = 1
	c = 1
	Proses = \0
	n = \0

|       |  |  |  | | 
| ----------- | ----------- | ----------- | ----------- | ----------- |
| a   	|1|3|6|6|
| b   	|1|2|3|3|
| c   	|1|2|3|4|
| n   	|3|3|3|3|
| hasil |1|3|6|6|
	
FS
	A = 11
	
	
```pseudocodeo
DEKLARASI
 	i: integer = 1
	n: integer = /0
	hasil: integer = /0
ALGORITMA
MULAI
	Read(keyboard) n
	FOR(i to n, i <- i + 1)
		hasil <- hasil + i
		Write(layar) hasil
	ENDFOR
SELESAI
```

|       |  |  |  | | 
| --- | --- | -- | -- | -- |
| i   	|1|2|3|4|
| n   	|3|3|3|3|
| hasil |1|3|6|6|

```pseudocode
PROGRAM MELAKUKAN PRINT SEMUA ANGKA GANJIL 1 hingga N

DEKLARASI
	i: integer = 1
	n: integer = \0
ALGORITMA
MULAI
	Read(keyboard) n
	FOR(i to n, i <- i + 1)
		IF(i mod 2 == 1)
			Write(layar) i
		ENDIF
	ENDFOR
SELESAI
```

|       |  |  |  | | | |
| --- | --- | -- | -- | -- | -- | -- |
| i   	|1|2|3|4|5|6|
| n   	|5|5|5|5|5|5|
| pengecekan loop|1 < 5|2 < 5|3 < 5|4 < 5|5 < 5|6 < 5|
| pengecekan ganjil|1 mod 2 = 1|2 mod 2 = 0|3 mod 2 = 1|4 mod 2 = 0|5 mod 2 = 0|5 mod 2 = 0|
| print|1|No|3|No|5|No|


Contoh pseudocode `while`
```pseudocode
PROGRAM MENAMPILKAN ANGKA 1 hingga N
DEKLARASI
	i: integer = 1
	n: integer = \0
ALGORITMA
MULAI
	Read(keyboard) n
	WHILE(i <= n) DO   ||  FOR(i to n, i <- i + 1)
		Write(layar) i
		i <- i + 1     ||  // i <- i + 1
	ENDWHILE
SELESAI
```

### Simple test #2
```pseudocode
PROGRAM MENAMPILKAN JUMLAH ANGKA GANJIL DAN
JUMLAH ANGKA GENAP DARI 1 HINGGA N MENGGUNAKAN LOOP WHILE
 - 1 sampai 10 = 1+3+5+7+9 , 2+4+6+8+10
```

#1w

```pseudocode
Deklarasi
    i:integer=1
    n: integer=/0
    hasil :integer = /0
algoritma
Mulai
    Read(keyboard) n
    WHILE (i to n) DO
        if(i mod 2 == 1)
            hasil <- hasil + i
            
		elseif (i mod 2 == 0)
			hasil <- hasil + 1    
		ENDIF
        
        write(Layar) hasil
        i<-i+1
    ENDWHILE
Seleasi

```
|       |  |  |  | | | |
| --- | --- | -- | -- | -- | -- | -- |
| i   	|1|2|3|4|5|6|
| n   	|5|5|5|5|5|5|
| hasil |1|2|5|6|11|11|
| print|1|2|5|6|11|No|


#2r
```pseudocode
Deklarasi
    i : integer = 1
    n : integer = \0
	hasil_genap: integer = 0
	hasil_ganjil: integer = 0
Algoritma
Mulai
    Read (keyboard) n
    While (i <= n) Do
        If ( i mod 2 == 1) then
			hasil_ganjil <- hasil_ganjil + i
            write (layar) hasil_ganjil
        Else
			hasil_genap <- hasil_genap + i
            write (layar) hasil_genap
        End If
		i <- i + 1
    EndWhile
Selesai
```

|       |  |  |  | | | |
| --- | --- | -- | -- | -- | -- | -- |
| i   	|1|2|3|4|5|6|
| n   	|5|5|5|5|5|5|
| hasil_genap   |\0|2|2|4|4|4|
| hasil_ganjil   |1|1|3|3|5|5|
| print genap|No|2|No|6|No|No|
| print ganjil|1|No|4|No|8|No|



## Tugas
Buat
 1. IS, Proses, FS
 2. Pseudocode
 3. Flowchart
 
dari program untuk
- PROGRAM UNTUK MENGHITUNG HASIL AKHIR (JUMLAH) DERET ANGKA DENGAN PERTAMBAHAN N
	- Contoh: angka_mulai = 10 (dinamis), jumlah_deret = 10 (dinamis), pertambahan = 15 (dinamis)
	- Hasil: 35 (10+15) + 50 (35+15) + 65(50+15) + 80 (65+15) + ... + 10 kali
	
	
- PROGRAM UNTUK MENAMPILKAN SEPERTI INI ( LOOP DIDALAM LOOP )
	- 1, 1,2,3,4,5
	- 2, 2,3,4,5,6
	- 3, 3,4,5,6,7
	- 5, 4,5,6,7,8
	- ....
	- n, n+2, n+3, n+4, n+5, ..., n+n

- Contoh: n = 5
	- 1, 1,2,3,4,5
	- 2, 2,3,4,5,6
	- 3, 3,4,5,6,7
	- 4, 4,5,6,7,8
	- 5, 5,6,7,8,9
