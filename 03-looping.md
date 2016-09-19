# Bab 3 -  Perulangan

## Tujuan

* Praktikan mampu memahami konsep penggunaan perulangan dengan menggunakan for 
* Praktikan mampu memahami konsep penggunaan perulangan dengan menggunakan while 
* Praktikan mampu memahami konsep penggunaan perulangan dengan menggunakan do-while 
* Praktikan mampu memahami penggunaan pernyataan break dan continue 

## Ringkasan Materi

### Perulangan dengan menggunakan for

Kata kunci `for` digunakan untuk mengulang pengeksekusian satu atau sejumlah pernyataan. Perulangan menggunakan `for` mempunyai batas awal, batas akhir dan kenaikan yang telah ditentukan terlebih dahulu. Perulangan akan dilakukan dengan membandingkan pencacah dengan batas akhir hingga ditemukan kondisi benar pada batas akhir, Bentuk umum penulisan perulangan menggunakan `for` adalah :  

```
for (initialization; loop condition; step) {
    // statement
}
```

initialization = nilai awal dari sebuah looping

loop condition = kondisi dimana looping harus dijalankan jika condition bernilai true

step = update variabel yang digunakan dalam looping

### Perulangan dengan menggunakan while

Kata kunci `while` digunakan untuk melakukan suatu proses perulangan yang memerlukan suatu kondisi tertentu untuk menghentukan perulangan. Perulangan akan dilakukan dengan membandingkan syarat perulangan dengan kondisi saat itu hingga ditemukan kodisi salah satu pada syarat perulangan. Bentuk umum penulisannya adalah : 

```
while (kondisi_perulangan) {
    // statement
}
```

### Perulangan dengan menggunakan do while

Hampir sama dengan perulangan menggunakan while, perulangan dengan do-while juga digunakan untuk melakukan perulangan yang memerlukan suatu kondisi tertentu untuk menghentikan perulangan. Perbedaan mendasar dengan perulangan menggunakan while adalah, dengan do-while, pengecekan kondisi dilakukan di belakang setelah baris statemen dalam blok do-while dijalankan (minimal 1 kali). Bentuk umum penulisan dengan do-while sebagai berikut : 

```
do {
    // statement
} while (kondisi_perulangan);
```

### Pernyataan break dan continue

Pernyataan break adalah pernyataan untuk mengentikan perulangan, sehingga akan keluar dari perulangan tersebut walaupun proses perulangan belum berakhir.

Bentuk pernyataan continue akan melewati bagian pernyataan setelah pernyataan ini dituliskan dan memeriksa ekspresi logika (boolean) yang mengkontrol pengulangan. Jika operasi logika bernilai true, maka pengulangan tetap dilanjutkan. Pada dasarnya pernyataan ini akan melanjutkan bagian pengulangan pada pernyataan loop.

## Pelaksanaan Percobaan

### Loop for

```c
#include <stdio.h>

int main() {
    int nilai;
    for (nilai = 1 ; nilai <= 10 ; nilai++) {
        printf("%d\n", nilai);
    }
    return 0;
}
```

### Loop while

```c
#include <stdio.h>

int main() {
    int nilai = 1;
    while (nilai <= 10) {
        printf("%d\n", nilai);
        nilai++;
    }
    return 0;
}
```

### Loop do while

```c
#include <stdio.h>

int main() {
    int nilai = 1;
    do {
        printf("%d\n", nilai);
        nilai++;
    } while (nilai <= 10);
    return 0;
}
```

### Break dan continue

```c
#include <stdio.h>

int main() {
    int nilai;

    printf("pernyataan break batas 10\n");
    for (nilai = 1 ; nilai <= 10 ; nilai++) {
        if (nilai == 5) break;
        else printf("%d\n", nilai);
    }

    printf("\npernyataan continue batas 10\n");
    for (nilai = 1 ; nilai <= 10 ; nilai++) {
        if (nilai == 5) continue;
        else printf("%d\n", nilai);
    }

    return 0;
}
```

## Data dan Analisis Hasil Percobaan

### A. Looping For

1.	Jelaskan dan perbaiki jika menemui kesalahan! 
 
2.	Apa fungsi dan variabel nilai dalam statemen for? 
 
3.	Dalam statemen for hapus bagian step, kemudian apa yang terjadi, jelaskan! 

4.	Dalam statement for hapus satu persatu secara bergantian mulai dari initialization, loop condition, dan step , amati yang terjadi dan jelaskan! 

### B. Looping while

1.	Jelaskan dan perbaiki jika menemui kesalahan! 

2.	Setelah mengamati hasil keluaran, sebutkan perbedaan looping dengan menggunakan for dan while! 

3.	Hapus statemen i++ pada baris 6 kemudian amati yang terjadi dan jelaskan! 

4.	Ubah syntaks di atas untuk membuat deret angka kelipatan 2! 

### C. Looping do-while

1.	Jelaskan dan perbaiki jika menemui kesalahan! 

2.	Setelah mengamati hasil keluaran, sebutkan perbedaan looping dengan menggunakan for, while dan do while! 

3.	Hapus statement i++ pada baris 6, amati yang terjadi dan jelaskan! 

4.	Ubah nilai dari variabel nilai baris ke 3 menjadi 11, amati yang terjadi dan jelaskan! 

### D. Break dan continue

1.	Jelaskan dan perbaiki jika menemui kesalahan! 

2.	Jelaskan alur logika untuk pernyataan break dan continue pada program diatas! 

3.	Hapus pernyataan break pada baris 8 dan tuliskan kembali pernyataan break setelah else baris ke 8, amati yang terjadi dan jelaskan! 

4.	Pada if penyataan continue baris ke 14 ubah pernyataan samadengan (==) menjadi  pernyataan kurang dari samadengan (<=) 

## Tugas Pratikum

**1)** Buatlah program dengan tampilan sebagai berikut :

```
Masukkan nilai n = 4 
* 
* * 
* * * 
* * * *
``` 

**2)** Buatlah looping yang menuliskan nama anda secara vertikal, dengan huruf yang sesuai dengan 
huruf yang di tulisan. Contoh menuliskan A : 

```
       A 
     A   A 
    A     A 
   A A A A A 
  A         A 
 A           A 
```

**3)** Buatlah program sederhana untuk menghitung beberapa volume bidang dengan tampilan awal sebagai berikut : 

```
MENU 
0. KELUAR 
1. HITUNG VOLUME BALOK 
2. HITUNG VOLUME BOLA 
3. HITUNG VOLUME KERUCUT 
4. HITUNG VOLUME SILINDER 
5. HITUNG VOLUME LIMAS SEGITIGA 
MASUKKAN PILIHAN ANDA :   
```


 