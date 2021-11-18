# Array, Loop, and Logic
## Recap
Dari beberapa sesi-sesi sebelumnya ini adalah beberapa hal yang sudah di pelajari
### Tipe Data
- Data angka
	- Angka pecahan
		- `double` -> isinya 1234.5678
		- `float` -> isinya 1234.5678
	- Angka bulat
		- `integer` -> isinya 1234
- Data alphanumeric, symbol
	- 1 Karakter
		- `char` -> isi nya '1'
	- Lebih dari 1 karakter
		- `string` -> isi nya 'lebih dari 1 karakter apapun!'
- Data logical (binary variable)
	- `boolean` -> isi nya true or false
### Operator
- Operator angka
	- _Kabataku_
		- `*` Kali -> perkalian 2 tipe data angka (contoh: 1 * 2 atau 1.2 * 3.4)
		- `/` Bagi -> pembagian 2 tipe data angka (contoh: 1 / 2 atau 1.2 / 3.4)
		- `+` Tambah -> pertambahan 2 tipe data angka (contoh: 1 + 2 atau 1.2 + 3.4)
		- `-` Kurang -> pengurangan 2 tipe data angka (contoh: 1 - 2 atau 1.2 - 3.4)
- Operator _string_ (karakter)
	- `+` tambah / concat -> menyatukan 2 karakter (contoh: 'a' + 'b' = 'ab')
- Operator boolean
	- `&&` / AND -> `true && true` adalah true
	- `||` / OR -> `false || false` adalah false
- Operator general
	- `==` / EQUAL
		- `1 == 1` : true
		- `true == true` : true
		- `32 == 33` : false

### Modulus
Hasil bagi
Contoh:
 - 3 modulus 5 = 3 (3/5 = 0 , sisanya 3)
 - 10 modulus 3 =1 (10/3 = 3, sisanya 1)

### If Statement
Logika kondisi percabangan
Syntax:
```java
if(kondisi){
	// kondisi true
}else{
	// selain kondisi true
}
```

### Array
Variable yang dapat menyimpan banyak data.
Elemen:
 - Tipe data array (harus sama)
 - Panjang array
 - Isi array
 - Index array
```java
int[] arr = new int[5];
```

### Loop
Perulangan
Macam-macam:
 - For
 - Do...while..
 - while..do..

---
## Latihan 1
BUAT PROGRAM UNTUK MENGUBAH ANGKA DENGAN SATUAN DETIK KE FORMAT JAM MENIT DAN DETIK
- Contoh:
	- Input: 3601 -> Output: 1 jam 0 menit 1 detik
	- Input: 603 -> Output: 0 jam 10 menit 3 detik
	- Input: 3666 -> Output: 1 jam 1 menit 6 detik
	- Input: 10 -> Output: 0 jam 0 menit 10 detik

```java
import java.util.Scanner;

public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int waktu = sc.nextInt();
	
	int jam = waktu / 3600;
	int menit = (waktu % 3600) / 60;
	int detik = (waktu % 3600) % 60;
	
	System.out.print(jam + " jam "+ menit + " menit " + detik + " detik");
}
```

## Latihan 2
BUAT PROGRAM UNTUK MENGECEK ISI DARI SUATU ARRAY DENGAN ISI 1 ATAU 0 MENJADI ANGKA DESIMAL
- Contoh
	- Input array = [1,0,1,1,1,1,0,1] -> Output = 189
	- Input array = [0] -> Output = 0
	- Input array = [1] -> Output = 1
	- Input array = [1,0] -> Output = 2


```java
import java.util.Scanner;

public static main void(String[] args){
	// Manual deklarasi array
	int[] biner = {1,0,0,0,1,1};
	int hasil = 0;
	int panjangArray = biner.length - 1;
	
	for(int i = 0; i < biner.length; i++){
		if(biner[i] == 1){
			hasil = hasil + (int) Math.pow(2, panjangArray);
		}
		
		panjangArray--;
		
	}
	
	System.out.print(hasil);
}
```


## Latihan 3
Buat program dengan spesifikasi
- Input
	1. Panjang array dengan tipe integer (mendefinisikan panjang array)
	2. Rotasi dengan tipe integer (mendefiniskan jauh rotasi ke kanan pada isi array)
- Contoh #1
	- Panjang array = 10
	- Array akan terisi = [1,2,3,4,5,6,7,8,9,10]
	- Rotasi = 3
	- Print: 4,5,6,7,8,9,10,1,2,3
- Contoh #2
	- Panjang array = 10
	- Array akan terisi = [1,2,3,4,5,6,7,8,9,10]
	- Rotasi = 1
	- Print: 2,3,4,5,6,7,8,9,10,1

```java
import java.util.Scanner;

public static main void(string[] args){
	Scanner sc = new Scanner(System.in);
	int panjangArray = sc.nextInt();
	int[] arr = new int[panjangArray];
	int rotasi = sc.nextInt();
	
	// Mengisi array
	for(int i = 0; i < panjangArray; i++){
		arr[i] = i + 1;
	}
	
	//Rotasi
	for(int i = 0; i < panjangArray; i++){
		System.out.print(arr[(i + rotasi) % panjangArray] + ", ");
	}
	
}
```


### Latihan 4
BUAT PROGRAM DENGAN SPESIFIKASI SEBAGAI BERIKUT
Contoh:
	- Tinggi piramid = 4
Hasil
```
   *
  ***
 *****
*******
```
Contoh:
	- Tinggi piramid = 2
Hasil
```
 *
***
```

Contoh:
	- Tinggi piramid = 6
Hasil
```
     *
    ***
   *****
  *******
 *********
***********
```
Contoh:
	- Tinggi piramid = 3
Hasil
```
  *
 ***
*****
```


```java
import java.util.Scanner;
public static main void(string[] args){
	Scanner sc = new Scanner(System.in);
	int tinggiPiramid = sc.nextInt();
	
	//Jawaban
	for(int i = 0; i < tinggiPiramid; i++){
		for(int j = 0; j < tinggiPiramid + i; j++){
			if(j < (tinggiPiramid - 1) - i){
				System.out.print(" ");
			}else{
				System.out.print("*");
			}
			System.out.println();
		}
	}
}
```

```java
import java.util.Scanner;
public static main void(string[] args){
	Scanner sc = new Scanner(System.in);
	int tinggiPiramid = sc.nextInt();
	
	//Jawaban
	for(int i = 0; i < tinggiPiramid; i++){
		// Spasi
		for(int j = 0; j < tinggiPiramid - 1 - i; j++){
			System.out.print(" ");
		}
		
		// Bintang kiri dan kanan
		for(int j = 0; j < (2*i) + 1; j++){
			System.out.print("*");
		}
		
		System.out.println();
	}
}
```


## Next
 - Loop + array **(Next Session)**
 - Modular Programming **(Next Session)**
	 - Function
	 - Recursive
	 - Paradigm / Pattern
 - Sorting / Searching
	 - Sorting
		 - Basic Sorting
		 - Methods
			 - Bubble Sort
			 - Quick sort
			 - Merge Sort
			 - Binary Sort
	 - Searching
		 - Binary Search
		 - Linear Search
 - Data structure
	 - Linked List
	 - Tree
--------

```matlab
f(x) = x + 1;

1 + f(2);
```


```java
public int f(int x){
	return x + 1;
}

public static main void(string[] args){
	System.out.println(1 + f(2))
}
```
