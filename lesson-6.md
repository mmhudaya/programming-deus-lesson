# Array and Loop (cont.)
## Latihan 1
BUAT PROGRAM UNTUK MENGISI ARRAY DENGAN INPUT
- Angka integer untuk panjang array positif
- Angka batas maksimal positif
- Contoh #1
	- Angka panjang array = 10
	- Angka batas maksimal = 3
	- [1, 2, 3, 1, 2, 3, 1, 2, 3, 1]
- Contoh #2
	- Angka panjang array = 10
	- Angka batas maksimal = 5
	- [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]

### Modulus
- 1 % 3 = 1
- 2 % 3 = 2
- 3 % 3 = 0
- 4 % 3 = 1
- 5 % 3 = 2
- 6 % 3 = 0

Tools:
- Loop
- Array
- Modulus
- If ... else ... (bisa ada bisa engga)

```java
import java.util.Scanner;

public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int angkaPanjangArray = sc.nextInt();
	int batasMaksimal = sc.nextInt();
	int[] arr = new int[angkaPanjangArray]; // [0,0,0,0,0,0] || [null,null,null,null]
	
	// Jawaban dengan if
	for(int i = 1; i <= angkaPanjangArray; i++){
		if(i % batasMaksimal == 0){
			arr[i-1] = batasMaksimal;
		}else{
			arr[i-1] = i % batasMaksimal;
		}
	}
	
	// Jawaban dengan if mulai dari 0
	for(int i = 0; i < angkaPanjangArray; i++){
		if((i + 1) % batasMaksimal == 0){
			arr[i] = batasMaksimal;
		}else{
			arr[i] = (i + 1) % batasMaksimal;
		}
	}
	
	// Jawaban tanpa if
	for(int i = 1; i <= angkaPanjangArray; i++){
		// 3 - (3 - (1 % 3)) % 3) = 1
		arr[i-1] = batasMaksimal - (batasMaksimal - i % batasMaksimal) % batasMaksimal;
	}
	
	// Print
	for(int i = 1; i <= angkaPanjangArray; i++){
		System.out.println(arr[i-1] + " ");
	}
	
}
```


### Operator boolean
- && , || , == , != ( && = AND OPERATOR) ( || = OR OPERATOR)
- <= , < , == , >, >= (Operator for number)

## Latihan 2
BUAT PROGRAM UNTUK MENGECEK APAKAH ANGKA ADALAH BILANGAN PRIMA ATAU BUKAN DENGAN INPUT
- Angka bilangan yang mungkin prima atau tidak
- Contoh #1
	- Input : 1
	- Bilangan Prima ? "Bilangan Prima"
- Contoh #2
	- Input : 2
	- Bilangan Prima ? "Bilangan Prima"
- Contoh #3
	- Input : 3
	- Bilangan Prima ? "Bilangan Prima"
- Contoh #4
	- Input : 4
	- Bilangan Prima ? "Bukan Bilangan Prima"

_Definisi bilangan prima adalah bilangan yang hanya bisa dibagi oleh angka 1 atau bilangan itu sendiri_

Tools
- Loop
- Modulus
- If ... else ...

```java
import java.util.Scanner;
public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int bilangan = sc.nextInt();
	int hasil = 0;
	
	for(int i = 1; i <= bilangan; i++){
		if(bilangan % i == 0){
			hasil = hasil + 1;
		}
	}

	if(hasil == 2){
		System.out.println("Prima");
	}else{
		System.out.println("Bukan");
	}
}
```

## Latihan 3
BUAT PROGRAM DENGAN SPESIFIKASI
- Input
	1. Panjang array
	2. Batas maksimal pattern array (nanti)
	3. Angka integer "A"
	4. Angka integer "B"
- Contoh #1
	1. Panjang array = 10
	2. Batas maksimal = 7
	3. A = 4
	4. B = 7
	- Ada array [1, 2, 3, 4 , 5, 6, 7, 1, 2, 3]
	- Outputnya = angka 6 , didapat dari (array indeks 4 + array indeks 7)
	
```java
int[] arr = new int[5];
arr[0] = 1;
arr[1] = 234;
arr[2] = 1876;
arr[3] = 98;
arr[4] = 91;


int A = 1;
int B = 4;

// misal pertambahan index 4 + 1
int hasil = arr[B] + arr[A]; //98 + 234
```

- Error handling
	- Kalau panjang array negatif, **program langsung selesai** Print "Panjang array tidak boleh negatif"
	- Kalau batas maksimal negatif, **program langsung selesai** Print "Panjang array tidak boleh negatif"
	- Kalau A negatif, **program langsung selesai** Print "Panjang array tidak boleh negatif"
	- Kalau B negatif, **program langsung selesai** Print "Panjang array tidak boleh negatif"
	- Kalau A lebih dari sama dengan panjang array, **program langsung selesai** Print "A tidak boleh lebih dari sama dengan panjang array"
	- Kalau B lebih dari sama dengan panjang array, **program langsung selesai** Print "B tidak boleh lebih dari sama dengan panjang array"

Tools
- Modulus
- Loop
- Banyak if


```java
import java.util.Scanner;

public static void main(String[] args){
	Scanner sc = new Scanner(System.in);
	int angkaPanjangArray = sc.nextInt();
	int batasMaksimal = sc.nextInt();
	int a = sc.nextInt();
	int b = sc.nextInt();
	int hasil = 0;
	
	// Jawaban
	if(panjangArray >= 0){
		int[] arr = new int[angkaPanjangArray];
		if(batasMaksimal >= 0){
			if(a >= 0 ){
				if(a < angkaPanjangArray){
					if(b >= 0){
						if(b < angkaPanjangArray){
							for(int i = 1; i <= angkaPanjangArray; i++){
								if(i % batasMaksimal == 0){
									arr[i-1] = batasMaksimal;
								}else{
									arr[i-1] = i % batasMaksimal;
								}
							}

							hasil = arr[a] + arr[b];
							for(int i = 1; i <= angkaPanjangArray; i++){
								System.out.print(arr[i-1] + " ");
							}
							
							System.out.println("Hasil = " + hasil);
							
						}else{
							// B lebih dari sama dengan panjang array
							System.out.println("B tidak boleh sama atau lebih besar dari panjang Array");
						}
					}else{
						// B negatif
        				System.out.println("B tidak boleh negatif");
					}
				}else{
					// A lebih dari sama dengan panjang array
					System.out.println("A tidak boleh sama atau lebih besar dari panjang Array");
				}
			}else{
				// A negatif
        		System.out.println("A tidak boleh negatif");
			}
		}else{
			// batas maksimal negatif
        	System.out.println("Batas Maksimal tidak boleh negatif");
		}
	}else{
		// panjang array negatif
		System.out.println("Panjang array tidak boleh negatif");
	}
	
}
```

## PR
Buat program dengan spesifikasi
- Input
	1. Panjang array dengan tipe integer (mendefinisikan panjang array)
	2. Rotasi dengan tipe integer (mendefiniskan jauh rotasi ke kanan pada isi array)
- Contoh #1
	- Panjang array = 10
	- Array akan terisi = [1,2,3,4,5,6,7,8,9,10]
	- Rotasi = 3
	- Array akan menjadi = [8,9,10,1,2,3,4,5,6,7]
- Contoh #2
	- Panjang array = 10
	- Array akan terisi = [1,2,3,4,5,6,7,8,9,10]
	- Rotasi = 1
	- Array akan menjadi = [10,1,2,3,4,5,6,7,8,9]


## Next
 - Loop + array (**next session**)
 - Modular Programming
 - Sorting / Searching
