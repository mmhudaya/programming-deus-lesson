# Array
[1,2,3,44,5,6,6,7]

Program untuk mengisi array [1, ... 10]
Print 1 2 3 4 5 6 7 8 9 10 
```java
public static void main(String args[]){
	//Deklarasai
	int[] arr = new int[10];
	
	//Program
	for(int i = 0 ; i < 10; i++){
		arr[i] = i+1;
	}
	
	//Program output
	for(int i = 0; i < 10; i++){
		System.out.println(arr[i]);
	}
	
}
```

Cara deklarasi array semi-dinamis (sesuai input keyboard)
```java
import java.util.Scanner;

public static void main(String[] args){
	Scanner sc = new Scanner(System.in);
	int panjangArray;
	
	panjangArray = sc.nextInt();
	
	int[] arr1 = new int[panjangArray]; // <-- deklarasi semi dinasmis array
}
```

BUAT PROGRAM UNTUK MENGISI ARRAY DENGAN SYARAT
1. Array dengan index ganjil di isi 1
2. Array dengan index genap di isi 0
3. Panjang array 20

Contoh: [0,1,0,1,0,1]

Dan tampilkan isi array tersebut.

```java
public static void main(String args[]){
	//Deklarasai
	int[] arr = new int[20];
	
	//Program
	for(int i = 0 ; i < 20; i++){
		// ...
		arr[i] = i % 2; // cara selain dengan `if`
	}
	
	//Program output
	for(int i = 0; i < 10; i++){
		System.out.println(arr[i]);
	}
}
```


BUAT PROGRAM UNTUK MENGISI ARRAY DENGAN SYARAT
1. Array dengan index ganjil di isi 0
2. Array dengan index genap di isi 1
3. Panjang array 20

Contoh: [1,0,1,0,1,0]

Dan tampilkan isi array tersebut.

```java
public static void main(String args[]){
	//Deklarasai
	int[] arr = new int[20];
	
	//Program
	for(int i = 0 ; i < 20; i++){
		// ...
		arr[i] = Math.pow(0, i % 2); // cara selain dengan `if`
	}
	
	//Program output
	for(int i = 0; i < 10; i++){
		System.out.println(arr[i]);
	}
}
```

-- bukan array
- PROGRAM UNTUK MENAMPILKAN SEPERTI INI ( LOOP DIDALAM LOOP )
	- 1, 1,2,3,4,5
	- 2, 2,3,4,5,6
	- 3, 3,4,5,6,7
	- 4, 4,5,6,7,8
	- ....
	- n, n, n+1, n+2, n+3, ..., n+n


```pseudocode
PROGRAM MEMBUAT PERKALIAN DENGAN LOOP PERTAMBAHAN
DEKLARASI
	a: integer = \0
	b: integer = \0
	hasil: integer = 0
PROGRAM
MULAI
	Read(keyboard) a 	\\a <- 2
	Read(keyboard) b 	\\b <- 4
	
	FOR() DO
		// 2 + 2 + 2 + 2
	ENDFOR
	
SELESAI
```

```java
import java.util.Scanner;

public static void main(String[] args){
	//Deklarasai
	int hasil = 0;
	int a;
	int b;
	
	//Program
	Scanner sc = new Scanner(System.in);
	a = sc.nextInt();
	b = sc.nextInt();
	
	for(int i = 0; i < b; i++){
		hasil += a;
	}
	
	System.out.println(hasil);
	
}
```


BUAT PROGRAM MENAMPILKAN  Pyramid 1
Tools: 
- Loop dalam loop
```pseudocode
Input = 3

Print
*
**
***

Input = 5

Print
*
**
***
****
*****
```
Tools
```java
System.out.print() //Print tanpa breakline atau enter
System.out.println() // Print dengan enter

Contoh
System.out.print("a");
System.out.print("b");
hasil nya = ab

Contoh
System.out.println("a");
System.out.println("b");
hasil nya
a
b
```

Jawaban pyramid 1
```java
public static void main(String[ ] args) {
	//Deklarasai
	int n;

	//Program
	Scanner sc = new Scanner(System.in);
	n = sc.nextInt();

	for(int i = 0; i < n; i++){
		for(int j = 0; j <= i; j++){
			System.out.print("*");
		}
		System.out.println();
	}
}	
```

Pyramid 2
```pseudocode
Input = 3

Print
***
**
*

Input = 5

Print
*****
****
***
**
*
```
Jawaban Pyramid 2
```java
public static void main(String[ ] args) {
	//Deklarasai
	int n;

	//Program
	Scanner sc = new Scanner(System.in);
	n = sc.nextInt();
	
	for(int i = n; i >= 1; i--){
		for(int j = 1; j <= i; j++){
			System.out.print("*");
		}
		System.out.println();
	}
	
}
```

Pyramid 3
```pseudocode
Input = 3

Print
***
 **
  *

Input = 5

Print
*****
 ****
  ***
   **
    *
```

Pyramid 4 3-loop
```java
public static void main(String[ ] args) {
	//Deklarasai
	int n;

	//Program
	Scanner sc = new Scanner(System.in);
	n = sc.nextInt();

	for(int i = n; i >= 1; i--){
		//Spasi
		for(int k = 0; k < n-i; k++){
			System.out.print(" ");
		}

		//Bintang
		for(int j = 1; j <= i; j++){
			System.out.print("*");
		}
		System.out.println();
	}
}
        
```

Pyramid 4 2-loop
```java
public static void main(String[ ] args) {
	//Deklarasai
	int n;

	//Program
	Scanner sc = new Scanner(System.in);
	n = sc.nextInt();

	for(int i = n; i >= 1; i--){
		//Bintang
		for(int j = 1; j <= n; j++){
			if(n - i >= j){
				//Spasi
				System.out.print(" ");
			}else{
				System.out.print("*");
			}

		}
		System.out.println("");
	}
}
        
```

Pyramid 5
```pseudocode
Input = 3

Print
***
**
*
*
**
***

Input = 5

Print
*****
****
***
**
*
*
**
***
****
*****
```

Jawaban Pyramid 5
```java
public static void main(String[ ] args) {
	//Deklarasai
	int n;

	//Program
	Scanner sc = new Scanner(System.in);
	n = sc.nextInt();
	
	for(int i = n; i >= 1; i--){
		for(int j = 1; j <= i; j++){
			System.out.print("*");
		}
		System.out.println();
	}
	
	for(int i = 0; i < n; i++){
		for(int j = 0; j <= i; j++){
			System.out.print("*");
		}
		System.out.println();
	}
}
```

Array sum previous [PR]
```pseudocode
- Buat array [1,2,3,4,..n]
 = Isi array 1 hingga n
 = nama variable `arr1`
- Buat array [1,3,6,10,...,]
 = Pertambahan seluruh isi array index sebelumnya di `arr1`
 = nama variable `arr2`
- Tampilkan seluruh hasil array di `arr2`

Tools
 - Looping
 - Array
 - Pertambahan
```
