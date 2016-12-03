# Bab 4 - Array

## Tujuan
* Praktikan mampu mengenal array pada pemrograman C
* Praktikan mampu mengenal penggunaan array pada pemrograman C
* Praktikan mampu mengimplementasikan macam-macam array pada pemrograman C

## Ringkasan Materi

### A.	Array

Array adalah variabel yang dapat menyimpan beberapa nilai dengan tipe data yang sama dalam ukuran tertentu. Index array secara default dimulai dari 0, sehingga apabila ada array dengan panjang “n” maka index array dimulai dari 0 hingga n-1. Contohnya seperti dibawah ini:

```
Array  :	     [    ]   [    ]   [    ]   [    ]   . . .    [    ]
Index  :            0        1        2       3                n-1
```

Untuk mendeklarasikan array pada C dapat dilakukan seperti di bawah ini.

Syntax :
```
    Tipe_data  Nama_array [ Ukuran_array ];
```

Contoh :
```
    int dataArr [10];
    double data [5];
```

### B.	Array 1 Dimensi

Array 1 dimensi adalah array yang menggunakan satu set kurung siku.

Contoh deklarasi array 1 dimensi:

```	
int dataArr [8];
char kata [20];
```

Pemberian nilai pada array bisa dilakukan dengan memberi nilai langsung ataupun satu-persatu sesuai dengan indexnya. Apabila ingin memberi nilaii langsung pada array kita bisa menggunakan satu set kurung kurung kurawal, contohnya seperti di bawah ini:

```
int data [5] = {10, 11, 7, 5, 8};
atau
int nilai [] = {10, 11, 7, 5, 8};
```

Jika ingin memberi nilai langsung sesuai indexnya bisa seperti contoh di bawah ini:

```
data[3] = 10;
```
		
Untuk lebih jelasnya tentang array 1 dimensi bisa melihat contoh dibawah ini (Array1D.c)

### C.	Array Multi-Dimensi

Array Multi-Dimensi adalah array yang menggunakan lebih dari satu set kurung siku. Salah satu contoh array multi-dimensi adalah array dua dimensi.

Contoh deklarasi array 2 dimensi :

```	
int arr2Dimensi [5][2] ;
double arr2 [3][7]; 
```

Dalam array 2 dimensi kita dapat menganggap 1 set kotak pertama adalah baris dan 1 set kotak kedua adalah kolom. Untuk memberi nilai pada array 2 dimensi kita bisa lakkukan seperti contoh di bawah ini:

```
int arrData [3][2] = {{1, 2}, {3, 4}, {5, 6}};
```

atau 

```
arrData[1][1] = 10;
```

Untuk lebih jelasnya tentang array 2 dimensi bisa melihat contoh dibawah ini (Array2D.c)

### D.	Pointer

Pointer adalah variabel yang menyimpan suatu alamat dari variabel lainnya. Untuk mendeklarasikan pointer kita menggunakan tanda asterisk (*) di depan nama variabel dan menggunakn tanda & untuk mendapatkan alamat dari suatu variabel.

Contoh:
```
	Tipe_data *nama_variabel;
	int *data;
```

untuk mendapatkan alamat dari suatu variabel bisa menggunakan tanda dan (&).

```
	int nilai = 10;
	int *data = &nilai;
```  

## Pelaksanaan Percobaan

```c
//Array1D.c
#include<stdio.h>

int main(){
	int i ;
	int data[]={11,3,4,7,24};
	
	//menghitung jumlah byte yang dibutuhkan, karena int butuh 4byte maka (jumlah memory / 4)
	int panjang = sizeof(data)/4;
	
	
	
	printf("sebelum\n");
	//mencetak semua nilai pada array sebelum diubah
	for(i = 0; i < panjang; i++){
		printf("index ke-%d adalah %d\n",i,data[i]);
	}
	
	
	for(i = 0; i < panjang; i++){
		// nilai data sebelumnya di kali 2
		data[i] =  data[i]*2;
	}
	printf("\n\nSesudah\n");
	//mencetak semua nilai pada array sesudah diubah
	for(i = 0; i < panjang; i++){
		printf("index ke-%d adalah %d\n",i,data[i]);
	}
}
```

```c
//array2D
#include<stdio.h>
//mendefinisikan fungsi length
#define length(arr) ((int) (sizeof (arr) / sizeof (arr)[0]))

int main(){
	
	/* membuat array dengan baris 3 dan kolom 3
		   0  1  2
		0 [] [] []
		1 [] [] []
		2 [] [] []
	*/
	int data[3][3];
	int i,j;
	//mengetahui panjang kolom
	int kolom = length(data);
	//mengetahui panjang baris
	int baris = length(data[0]);
	
	// mengisi data array
	for(i=0; i < kolom; i++){
		for(j=0; j < baris; j++){
			data[i][j] = i * j;
		}
	}
	//mencetak nilai dalam array
	for(i=0; i < kolom; i++){
		for(j=0; j < baris; j++){
			printf("%d ",data[i][j]);
		}
		printf("\n");
	}
	
}
```

## Data dan Analisis Percobaan
	
### Array 1 Dimensi
1.	Jalankan program Array1D diatas	, benahi jika ada kesalahan!
2.	Tambahkan statement berikut (data[5] = 10) sebelum for pertama , apa yang terjadi ? jelaskan?
3.	Ubahlah nilai panjang menjadi 10, apa yang terjadi ? jelaskan?

### Array 2 Dimensi
1.	Jalankan program Array2D diatas, benahi jika ada kesalahan!
2.	Ubahlah (baris = length(data[0])) menjadi (baris = length(data[0][0])), apa yang terjadi? Jelaskan?


## Tugas Praktikum

1.	Buatlah program untuk melakukan penjumlahan dan pengurangan array 2 dimensi (Matrik) ?
2.	Buatlah program untuk menggabungkan 2 buah array menjadi 1?
3.	Buatlah program untuk melakukan pengurutan data dari nilai terkecil hingga terbesar? 
