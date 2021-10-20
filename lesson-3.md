# Simple progamming with Java

1
```pseudocode
DEKLARASI
	n: integer
ALGORTIMA
MULAI
	READ(keyboard) n
	n <- n / 3
	Write(layar) n
SELESAI
```

1 in java
```java
import java.util.Scanner;

class Solution{
	public static void main(String[] args){
		//Deklarasi
		int n;
		
		//Read (keyboard) n
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		
		n = n/3;
		
		//Write (layar) n
		System.out.println(n);
	}
}
```

2
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

2 in java
```java
import java.util.Scanner;

class Solution{
	public static void main(String[] args){
			//Deklarasi
			float suhu;
			String hasil;

			//Read (keyboard) n
			Scanner sc = new Scanner(System.in);
			suhu = sc.nextFloat();

			if(suhu > 40){
				hasil = "panas";
			}else if(suhu < 15){
				hasil = "dingin";
			}else{
				hasil = "normal";
			}

			//Write (layar) hasil
			System.out.println(hasil);
	}
}
```


3
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

3 in java
```java
import java.util.Scanner;

class Solution{
	public static void main(String[] args){
		//Deklarasi
		float ipk;
		String hasil;

		//Read (keyboard) n
		Scanner sc = new Scanner(System.in);
		ipk = sc.nextFloat();

		if(ipk >= 3.5){
			hasil = "cum laude";
		}else if(ipk ){
			hasil = "sangat memuaskan";
		}else if(){
			hasil = "memuaskan";
		}else{
			hasil = "tidak terindex";
		}

		//Write (layar) hasil
		System.out.println(hasil);
	}
}
```

4
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

4 in java
```java
class Solution{
	public static void main(String[] args){
		//Deklarasi
		int A = 1;
		
		for(A = 1; A <= 10; A++){
			System.out.println(A);
		}
	}
}
```

5
```pseudocode
DEKLARASI
	A: integer = 1
ALGORITMA
MULAI
	WHILE(A <= 10) DO
		Write(layar) A
		A <- A + 1
	ENDWHILE
SELESAI
```

5 in java
```java
class Solution{
	public static void main(String[] args){
		//Deklarasi
		int A = 1;
		
		while(A <= 10){
			System.out.println(A);
			A = A + 1;
		}
	}
}
```

6
```pseudocode
Penjumlahan angka dari 1 Hingga N
1-3 => 6
1-5 => 15

Deklarasi
    n: integer
    hasil: integer = 0
	i: integer
	
ALGORITMA    
MULAI
    Read (keyboard) n
    
	...
	
    Write (layar) hasil
SELESAI
```

6 in java
```java
import java.util.Scanner;

class Solution{
	public static void main(String[] args){
		//Deklarasi
		int hasil = 0;
		int n;
		int i = 1;
		
		//Read (keyboard) n
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		
		while(i <= n ){
			hasil += i; // hasil = hasil + i;
			i++;
		}
		
		//Write (layar) hasil
		System.out.println(hasil);
	}
}
```

7
```pseudocode
PROGRAM MELAKUKAN PRINT SEMUA ANGKA GANJIL 1 hingga N

DEKLARASI
	i: integer = 1
	n: integer = \0
ALGORITMA
MULAI
	Read(keyboard) n
	
	...
	
SELESAI
```

7 in java
```java
import java.util.Scanner;

class Solution{
	public static void main(String[] args){
		//Deklarasi
		int i = 1;
		
		//Read (keyboard) n
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		
		for(i = 1; i <= n; i++){
			if(i % 2 == 1){
				System.out.println(i);
			}
		}
		
	}
}
```
