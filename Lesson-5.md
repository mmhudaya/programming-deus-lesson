# Array  (cont.)
#1
Buat program untuk mengisi array dengan spesifikasi
- Panjang array hasil dari inputan (variable `n`)
- Isi array memilki pola
	- [n, n-1, n-2, n-3, .... , n - (n + 1)]
- Tampilkan hasil array tersebut
- Contoh
	- n = 5
	- hasilnya => [5,4,3,2,1]

```java
import java.util.Scanner;

public static void main(String[] args){
	Scanner sc = new Scanner(System.in);
	int n = sc.nextInt();
	int[] arr1 = new int[n];
	
	//Isi
	for(int i = 0; i < n; i++){
		arr1[i] = n - i;
	}
	
	//Tampilkan
	for(int i = 0; i < n; i++){
		System.out.print(arr1[i] + " ");
	}
}
```




#2
Buat program untuk mengisi array dengan spesifikasi
- Mencari nilai terbesar pada suatu array
- Contoh
	- [234, 62436, 8577, 1209, 10] => print nilai terbesar yaitu `62436`

Contoh mengisi array lewat inputan user
```java
import java.util.Scanner;
public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int[] arr1 = new int[5];
	//int[] arr1 = {1231, 12313215, 1231321, 876123, 87623}
	
	for(int i = 0; i < 5; i++){
		arr1[i] = sc.nextInt();
	}
	
	// Isi
	int max = arr1[0];
	for(int i = 1; i < 5; i++){
		if(max < arr1[i]){
			max = arr1[i];
		}
	}
	
	System.out.println(max);
}
```

#3
Buat program untuk mengisi array dengan spesifikasi
- Mencari nilai terkecil kedua pada suatu array
- Contoh
	- [234, 62436, 8577, 1209, 10] => print nilai terbesar yaitu `234`

Tools
- Loop
- Swap variable
- Perbandingan
- `== // !=`

```java
import java.util.Scanner;
public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int[] arr1 = new int[5];
	//int[] arr1 = {1231, 12313215, 1231321, 876123, 87623}

	for(int i = 0; i < 5; i++){
		arr1[i] = sc.nextInt();
	}

	// Isi
	int temp;
	int min = arr1[0]; // jadi exclude
	int min2 = arr1[1];

	if(min2 < min){
		min2 = arr1[0];
		min = arr1[1];
	}

	for(int i = 2; i < 5; i++){
		if(min > arr1[i]){
			temp = min;
			min2 = temp;
			min = arr1[i];
		}else{
			if(min2 > arr1[i]){
				min2 = arr1[i];
			}
		}
	}

	System.out.println(min2);
}
```

Selanjutnya
 - Loop + array (next session)
 - Modular Programming
 - Sorting / Searching
