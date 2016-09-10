# Bab 1 - Program Input, Output dan Proses

## Tujuan
*   Praktikan mampu memahami struktur dasar bahasa pemrograman C
*   Praktikan mampu mengenal penggunaan variabel dan tipe data
*   Praktikan mampu mengenal dan mengimplementasikan statement input dan output dalam bahasa code C

## Ringkasan Materi

### Struktur Bahasa Pemrograman C

Berikut ini contoh code snippet yang menunjukkan struktur umum bahasa pemrograman C

```c
#include <stdio.h> // preprocessor directive

// blok program utama (main method)
int main(int argc, char **argv) {
    // statement didalam blok main

    return 0; // return 0 jika tidak ada error
}
```

### Variabel dan Tipe data

Variabel digunakan untuk menyimpan nilai data yang dapat diubah nilai datanya. Variabel
memiliki tipe data dan identifier. Identifier adalah nama variabel yang digunakan sebagai
pengenal. Tipe data menandakan tipe dan jangkauan data yang dapat disimpan pada
variabel tersebut.

Bahasa C menyediakan tipe data sebagai berikut

No | Tipe Data | Memori | Nilai Minimum | Nilai Maksimum
---|-----------|--------|---------------|---------------
1 | byte | 8 bit | -128 | 127
2 | short | 16 bit | -32768 | 32767
3 | int | 32 bit | -2147483648  | 2147483647
4 | long | 64 bit | -9223372036854775808  | 9223372036854775807
5 | float | 32 bit | ±1.40239846E-45 | ±3.40382347E+8
6 | double | 64 bit | ±4.94065645841246544E-324 | ±1.79769313486231570E+308
7 | char | 16 bit | \u0000 | \uFFFF

Cara pendeklarasian variabel seperti ini

```
tipe_data nama_variabel;

// contoh
int a;
char c;
double f;
```

Untuk menginisialisasi nilainya seperti ini

```c
// contoh
char c = 'a';
int i = 89;
float f = 4.51f;
```

### Format Specifier

Secara umum, format specifier yang sering dipakai sebagai berikut, ini akan digunakan ketika kita memanfaatkan `scanf()` maupun `printf()`.

Format specifier | Tipe data
---------------- | ---------
%d | Integer, basis 10
%x | Integer, basis 16
%o | Integer, basis 8
%s | String
%c | Char
%f | Float

Untuk escape character sebagai berikut

Escape character | Penjelasan
---------------- | ----------
\a | audible bell
\b | backspace
\n | newline
\t | tab
\f | form feed
\r | carriage return
\v | vertical tab
\\ | backslash


### Output

Untuk mencetak suatu informasi ke layar monitor melalui stdout (standard output), kita dapat
menggunakan fungsi `printf()`. Format specifier wajib dipakai.

Contoh snippet

```c
#include <stdio.h>

int main() {
    int a = 45;
    int b = 30;
    printf("%d\n", a + b); // output: 75
    printf("Belajar Bahasa C\n"); // output: Belajar Bahasa C

    return 0;
}
```

### Input

Untuk melakukan input kedalam variabel melalui stdin (standard input), kita dapat menggunakan fungsi `scanf()`. Format specifier juga wajib dipakai.

Contoh snippet

```c
#include <stdio.h>

int main() {
    float f;
    scanf("%f", &f); // menginputkan nilai dan memasukkan nilainya ke variabel f
    printf("%.2f\n", f); // mencetak nilai f dengan 2 angka belakang koma
    return 0;
}
```

## Pelaksanaan Percobaan

### Contoh Code Output 1

```c
#include <stdio.h>

int main() {
    printf("%s%c\n","Pemrograman C",'|');
    printf("%30s%c\n","Pemrograman C",'|');
    printf("%-30s%c\n","Pemrograman C",'|');
    printf("%30.5s%c\n","Pemrograman C",'|');

    return 0;
}
```

### Contoh Code Output 2

```c
#include <stdio.h>

int main() {
    float x = 7654.123456789f;
    printf("%d %3d %8d\n",1234,-567,8910);
    printf("%d %3d %+8d\n",1234,-567,8910);
    printf(“%f %15f %15.3f\n",x,x,x); 

    return 0;
}
```

### Contoh Code Variabel

```c
#include <stdio.h>

int main() {
    int nilai=10;
    double nilai_2=5.3;
    int hasil;
    char s[] = "Belajar Java";
    printf("%d\n",nilai+nilai_2);
    printf("Kita sedang %s\n",s);

    return 0;
}
```

### Contoh Code Input

```c
#include <stdio.h>

int main() {
    int nilai1, nilai2, hasil;
    printf("Masukkan nilai 1 : ");
    scanf("%d", &nilai1);
    printf("Masukkan nilai 2 : ");
    scanf("%d", &nilai2);

    hasil = nilai1 + nilai2;
    printf("maka hasil = %d\n", hasil);

    return 0;
}
```

## Data dan Analisis Hasil Percobaan

### A. Output

1.	Jalankan program Output1 – Output2 dan benahi jika menemukan kesalahan! 

2.	Pada program Output1 baris 3 – 6, jelaskan arti dari kode tersebut dan temukan perbedaannya! 

4.	Pada program output1 baris 3 ganti karakter ‘|’ menjadi ‘ab’ amati dan jelaskan! 

5.	Pada program Output1 setelah baris 6 tambahkan kode program dengan syntax `printf("%-30.8s%c\n","Pemrograman C",'|');` kemudian amati perbedaannya dengan baris 6 dan simpulkan! 

6.	Pada program Output2 tambahkan kode program yang mencentak nilai x dengan format 2 angka dibelakang koma! 

7.	Pada program Output2 tambahkan kode berikut `printf("%g  %15e %15.3f\n",x,x,x);` amati apa yang terjadi dan jelaskan! 

8.	Dari kedua jenis output tersebut simpulkan dan temukan perbedaannya! 

### B. Variabel

1.	Jalankan program Variabel dan benahi jika menemukan kesalahan! 

2.	Setelah baris 5 tambahkan syntax untuk mengurangkan nilai dari variabel nilai dan nilai_2, amati yang terjadi dan jelaskan! (benahi jika menemukan kesalahan)  

3.	Setekah baris 8 tambahkan variabel dengan type data char dengan nama variabel: ch dan mempunyai nilai sama seperti pada variabel s dan amati apa yang terjadi, jelaskan!  

4.	Tambahkan variabel dengan nama nilai3 yang bertipe data integer dan diberi nilai awal 100 kemudian lakukan pembagian yang disimpan pada variabel hasil kemudian cetak menggunakan kelas `printf()`!

5.	Tambahkan variabel dengan nama nilai3 yang bertipe data integer dan diberi nilai awal 100 kemudian lakukan pembagian tanpa harus disimpan disebuah variabel melainkan cetak pada layar menggunakan `printf()`!

6.	Jelaskan perbedaan antara no 4 dan no 5!

### C. Input

1.	Jalankan program Input dan benahi jika menemukan kesalahan! 

2.	Tambahkan perintah untuk memasukkan nama dan NIM user dan ditampilkan pada akhir program! 

## Tugas Praktikum

**1)** Buatlah program dengan tampilan sebagai berikut :

```
Masukkan operator pertama : 3
Masukkan operator kedua : 2
Hasil penjumahan : 5
Hasil pengurangan : 1
Hasil perkalian : 6
Hasil pembagian : 1.5
``` 

**2)** Buatlah program untuk menghitung pemakaian daya listrik dirumah tangga secara
sederhana. Tampilan program sebagai berikut :

```
Program penghitung pemakaian listrik sederhana
Masukkan Nama : Bpk Asisten
Keluarahan : Java
Masukkan posisi awal Kwh Meter : 8000
Masukkan posisi akhir Khw Meter : 9000
Masukkan biaya beban saat ini : 140
Masukkan PPJ (dalam persen) : 10
===================PLN Java===================
Nama : Bpk Asisten
Kelurahan : Java
Pemakaian bulan ini : 1000 Kwh Meter
Tarif Listrik : Rp 140000,-
PPJ 10% : Rp 14000,-
Total Bayar : Rp 154000,-
==============================================
```