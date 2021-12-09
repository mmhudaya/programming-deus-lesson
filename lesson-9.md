# Function
## Pre test
(1)
BUAT FUNCTION PENGURANGAN
Spesifikasi
 - Nama fungsi kalian yang tentukan
 - Cek semua case yang bisa diolah
 
Hasil
- Input: 2 dan 3 = -1
- Input:  3 dan 2 = 1

```java
public static main void(string[] args){
	System.out.println(pengurangan(2,3));
}

static int pengurangan(int a, int b){
	int hasil = a - b;
	return hasil;
}
```

(2)
BUAT FUNCTION PERKALIAN
Spesifikasi
 - Tidak boleh menggunakan operator `*`
 - Terdapat 2 fungsi
	 - Pertambahan
	 - Perkalian
 - Coba panggil fungsi pertambahan didalam fungsi perkalian

Hasil
 - Input: 2 dan 3 = 6
 - Input: 2 dan 0 = 0
 - Input: 2 dan 1 = 2
 - Input: -2 dan -3 = 6
 - Input: -2 dan 3 = -6
 - Input: 2 dan -3 = -6

```java
public static void main(String[] args){
	System.out.println(perkalian(2, -3));
}

static int perkalian(int a, int b){
	int hasil = 0;
	if(b >= 0){
		for(int i = 0; i < b; i++){
			hasil = pertambahan(hasil, a);
		}
	}else{
		b = b * -1;
		a = a * -1;
		for(int i = 0; i < b; i++){
			hasil = pertambahan(hasil, a);
		}
	}
	
	return hasil;
}

static int pertambahan(int a, int b){
	return a + b;
}
```

## Contoh 1
BUAT FUNCTION SEMUA ISI ARRAY DI KALI 2
```java
public static void main(String[ ] args) {
	int[] arr20 = inisialisasiArray(20);

	printArray(arr20);

	kaliDuaSemuaIsiArray(arr20);
	printArray(arr20);
}

//Basic
static int[] inisialisasiArray(int panjangArray){
	int[] arr = new int[panjangArray];

	for(int i = 0; i < panjangArray; i++){
		arr[i] = i+1;
	}

	return arr;
}

static void printArray(int[] arr){
	for(int i = 0; i < arr.length; i++){
		System.out.print(arr[i] + " ");
	}

	System.out.println();
}

//Operasi
static void kaliDuaSemuaIsiArray(int[] arr){
	for(int i = 0; i < arr.length; i++){
		arr[i] = arr[i] * 2;
	}
}
```

## Latihan 1
BUAT FUNCTION UNTUK MENGHITUNG PANGKAT
Spesifikasi
- Gunakan loop untuk menghitung nilai hasil pangkat

Contoh
 - `pangkat(2,3)`  = 8
 - `pangkat(1,0)` = 1

```java
public static void main(string[] args){
	System.out.println(pangkat(2,3));
}

static int pangkat(int a, int b){
	int hasil = 1;
	
	for(int i = 0; i < b; i++){
		hasil = hasil * a;
	}
	
	return hasil;
}
```

## Recursive
```matematika
a = 2;
a = a + 1;
```

```matematika
f(x) = x + 1;
f(f(1));

f(
  f(1) <-- 2
)

f(2) <--- 3
```
Pemanggilan function didalam dirinya sendiri

BUAT FUNCTION UNTUK PRINT ANGKA 1 HINGGA N
Spesifikasi
- Tidak boleh menggunakan syntax looping
	- For
	- While.. While
	- Do.. While
- Parameter
	- N

Contoh
- `satuHinggaN(10)` -> 10 9 8 7 6 5 4 3 2 1
- `satuHinggaN(4)` -> 4 3 2 1

Recursive harus ada _Stop Condition_ kalau engga nanti infinite loop

```java
public static void main(string[] args){
	nHinggaSatu(10);
}

static void nHinggaSatu(int n){
	if(n > 0){
		System.out.print(n + " ");
		nHinggaSatu(n);
	}
}
```


## PR
BUAT BEBERAPA FUNCTION
(1)
FUNCTION UNTUK INISIALISASI ARRAY DENGAN SPESIFIKASI
- Parameter
	- Panjang array
- Output
	- Parameter
		- Panjang array = 10
	- Hasil
		- [1,2,3,4,5,6,7,8,9,10]

```java
public static main void (string[] args){
	int[] arr = inisialisasiArray(20);
	
	printArray(arr, 20);
	
	geserArray(arr, 20, 5);
	
	printArray(arr, 20);
}

static int[] inisialisasiArray(int panjangArray){
	int[] arr = new int[panjangArray];
	for(int i = 0; i < panjangArray; i++){
		arr[i] = i + 1;
	}
	
	return arr;
}

static void geserArray(int[] arr, int panjangArray, int geser){
	for(int i = 0; i < panjangArray; i++){
		//swap
		//1 2 3 4 5 6 7 8 9 10
		//2 3 4 5 6 7 8 9 10 1
	}
}

static void printArray(int[] arr, int panjangArray){
	for(int i = 0; i < panjangArray; i++){
		System.out.print(arr[i] + " ");
	}
	
	System.out.println();
}
```

(2) [PR]
BUAT FUNCTION UNTUK GESER NILAI ARRAY
Spesifikasi
- Parameter
	- Array
	- Panjang Array
	- Jauh geser
- Return function
	- Array hasil geser

- Contoh	
	- `geserArray(arr, 10, 5)`
	- Asalnya: 1 2 3 4 5 6 7 8 9 10
	- Jadi: 6 7 8 9 10 1 2 3 4 5

(3)
BUAT FUNCTION UNTUK MELAKUKAN PRINT ISI ARRAY
Spesifikasi
- Parameter
	- Array
	- Panjang array
- Return function
	- Void
- Saat di panggil keluar print array di console java
- Contoh
	- `printArray(arr, 10);`
		- 1 2 3 4 5 6 7 8 9 10


## Next
- Modular Programming **(Next Session)**
	- Buat minesweeper
		- Buat lapangannya
		- Buat bomnya dimana aja
		- Buat fungsionalitas membuat angka hint bom dimana saja
