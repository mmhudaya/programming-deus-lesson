# Modular Programming
Pattern pemograman
- Reusable (Bisa di pake berulang-ulang)
- Jelas

```python
pd.read_csv('C:\\nama_csv.csv')

# Fungsi
read_csv

# Parameter
'C:\\nama_csv.csv'
```

```java
public static main void(String[] args){
	// Line 1 - 100
	Bagian si A
	
	// Line 101 - 200
	Bagian si B
}
```

Penjabaran fungsi
```pseudocode
BUAT PROGRAM UNTUK PERTAMBAHAN 2 ANGKA
DEKLARASI
	a: tipe data integer
	b: tipe data integer
PROGRAM
MULAI
	a + b
SELESAI
```

```java
import java.util.Scanner;
public static main void(String[] args){
	Scanner sc = new Scanner(System.in);
	int a = sc.nextInt();
	int b = sc.nextInt();
	
	System.out.println(a + b);
	
	System.out.println(pertambahan(2,3));
}

public int pertambahan(int a, int b){
	return a + b;
}
```

## Target
Nanti diakhir bakal ada project besar
- Game 2048

## Function
Contoh python
```python
def pertambahan(a,b):
	return a + b;
````
Contoh java
```java
public int pertambahan(int a, int b){
	return a + b;
}
```
Contoh javascript
```js
function pertambahan(a,b){
	return a + b;
}
```

Elemen `f(x)`
- Parameter
	- `x`
- Nama function
	- `f`
- Return function
	- Nilai kembali dengan tipe data tertentu
		- (di matematika harusnya semuanya angka)
		- (kalau di pemograman bisa berbeda-beda)

Elemen `int pertambahan(int a, int b)`
- Parameter
	- `int a`
		- `int`: integer
	- `int b`
		- `int`: integer
- Nama function
	- `pertambahan`
- Return function
	- `int` : integer


### Passing parameter
```c++
void main(String[] args){
	int a = 10;
	int b = 10;
	
	int c = pertambahanByRef(a, b);
	
	//a = 11
	//b = 11
	//c = 22
	
	System.out.println(a); // 11
	System.out.println(b); // 11
	System.out.println(c); // 22
	
	c = pertambahanByVal(a,b);
	
	System.out.println(a); // 10
	System.out.println(b); // 10
	System.out.println(c); // 22
}

int pertambahanByVal(int a, int b){
	// int a = nilai value yang di passing (10);
	// int b = nilai value yang di passing (10);
	a = a + 1; (memory[x4] = memory[x4] + 1)
	b = b + 1; (memory[x5] = memory[x5] + 1)
	return a + b;
}

int pertambahanByRef(int &a, int &b){
	a = a + 1; (memory[x1] = memory[x1] + 1)
	b = b + 1; (memory[x2] = memory[x2] + 1)
	return a + b;
}
```
1. Pass by value
	- a = 10, b = 10 f(10,10)
2. Pass by reference
	- a = 10, b = 10, f(address_a, address_b)

## Contoh 1
BUAT PROGRAM UNTUK MENGHITUNG JARAK TEMPUH. KITA MEMPUNYAI DATA KECEPATAN DAN WAKTU BERJALANNYA SUATU BENDA DENGAN KECEPATAN TERSEBUT (DALAM DETIK).

Kecepatan
- 100km/jam
- 200m/detik

Waktu berjalan
- 10 detik
- 2 detik

kecepatan * waktu berjalan

```java
// v untuk kecepatan, t untuk waktu berjalan
public int jarakTempuh(int v, int t){
	return v * t;
}
```


```java
int v;
int t;

int jarakTempuhVariable = v * t;
jarakTempuhVariable * 100; <---


jarakTempuh(v, t) * 20; <----

```


## Contoh 2
BUAT FUNGSI UNTUK MELAKUKAN PERKALIAN

Syarat
- Gak boleh pake operator perkalian

Parameter
- 2 angka tipe integer
	- a, b

Return function
- integer

```java
public static void main(String[] args){
	System.out.println(perkalian(2,5)); //10
	
	System.out.println(perkalian(-2,3)); //-6
	
	System.out.println(perkalian(2,-3)); //-6 (masih gk jalan) --> 0
}

// a = 2, b = 5 ---> 10
public int perkalian(int a, int b){
	int temp = 0;
	
	if(b < 0){
		b = b * -1;
		// Loop
		for(int i = 1; i <= b; i++){
			temp = temp + a;
		}
		
		temp = temp * -1;
	}else{
		// Loop
		for(int i = 1; i <= b; i++){
			temp = temp + a;
		}
	}
	
}

public int perkalianContoh2(int a, int b){
	// Contoh 2
	int negatif = -1;
	if(b >= 0){
		negatif = negatif * -1;
	}
	
	// Loop
	for(int i = 1; i <= b * negatif; i++){
		temp = temp + a;
	}
	
	
	return temp * negatif;
}
```

## Contoh 3
BUAT PROGRAM UNTUK KONVERSI SUHU

Suhu
 - Celcius
	 - fahrenheit
		 - c = (f - 32) *  5/9
	 -  kelvin
		 -  c = k - 273.15
 - Fahrenheit
	 - celcius
		 - f = (9/5) × **C** + 32
 - Kelvin
	 - celcius
		 - k = **C** + 273,15

Fungsi
- fahrenheitToCelcius
- kelvinToCelcius
- celciusToFahrenheit
- celciusToKelvin
- kelvinToFahrenheit
	- kelvinToCelcius
	- celciusToFahrenheit

```java
public float fahrenheitToCelcius(float f){
	return (f - 32) * 5/9;
}

public float kelvinToCelcius(float k){
	return k - 273.15;
}

public float celciusToFahrenheit(float c){
	return (9/5) * c + 32;
}

public float celciusToKelvin(float c){
	return c + 273.15;
}

public float kelvinToFahrenheit(float k){
	return celciusToFahrenheit(kelvinToCelcius(k));
}
```

## Scope Variable

1. Local variable
	- Gk mungkin masuk ke scope diluar function nya
2. Global variable
	- Masuk ke scope local function

```java
int a = 10;
int b = 10;

public static void main(String[] args){
	System.out.println(a); // 10
}

public void pertambahan(){
	 a = a + 1;
	 b = b + 1;
}
```

### Project
#### 2048

Analysis
- Penampung / Array
	- 2 dimensi
- Move
	- Atas
	- Kanan
	- Kiri
	- Bawah
- Kelipatan
	- Merge / Pertambahan 2 angka yang sama
- Pergeseran
- Muncul angka random di suatu tiles
- Score
- Valid move
	- Muncul angka random kalau move nya valid
- Winning condition
	- Suatu angka mencapai 2048
- Lose Condition
	- Array penuh dan tidak ada valid move


Scope
Fitur minumum
1. Bisa mulai game
2. Bisa geser atas, bawah, kiri, kanan
3. Bisa ada pertambahan angka yang sama
4. Bisa ngeluarin angka random
5. Bisa menang game
6. Bisa kalah game

Fitur nice to have
1. Kalau misal mau make GUI boleh2 aja
2. Random angkanya ada 2 dan 4
	- 2 = 90 %, 4 = 10%


## Next
- Modular Programming **(Next Session)**
	- Loop
	- Array
	- Passing by value
	- Passing by reference
	- Passing array
	- Random
	- Recursive
