# Bab 2 - Seleksi Kondisi

## Tujuan
* Praktikan mampu memahami konsep penggunaan conditional assignment
* Praktikan mampu memahami konsep percabangan menggunakan if-else, if-else if-else
* Praktikan mampu memahami konsep percabangan menggunakan 

## Ringkasan Materi

### Conditional Assignment

Sebelum mengenal menggunakan if kita dikenalkan bagaimana cara menggunakan dan kode untuk conditional assignment. Berikut kode dari conditional assignment :

```
type_data variabel = kondisi ? pernyataan_benar : pernyataan_salah
```

Dari kode diatas dapat dijelaskan bahwa pertama harus dilakukan pendeklarasian variabel
dan type data dari variabel yang kita buat, kemudian kita beri suatu kondisi setelah itu jika
kondisi benar maka program akan berjalan ke pernyaataan benar namun jika salah maka
akan melakukan pernytaan salah. 

Contoh : 

```
char s[] = (5>2) ? "Berhasil" : "Gagal";
```

Jika program tersebut dijalankan maka akan mencetak "Berhasil" kondisi pada
conditional assignment tersebut benar.

### Seleksi Kondisi menggunakan if-else

Untuk melakukan percabangan tunggal kita dapat menggunakan if saja namun untuk
percabangan yang lebih dari satu (percabangan majemuk) maka kita dapat menggunakan ifelse.

Bentuk dasar dari statemen ini adalah :

```
if (kondisi){
    Blok pernyataan;
}
else{
    Blok pernyataan
}
```

Namun untuk percabangan yang lebih dari 2, bentuk dasar yang digunakan adalah :

```
if (kondisi){
    Blok pernytaan 1;
}
else if (kondisi){
    Blok pernyataan 2;
}
else if (kondisi){
    Blok pernyataan 3;
}
else{
    Blok pernyataan 4;
}
```

### Nested If

Suatu if memungkinkan untuk terapat if didalan if inilah yang disebut sebagai nested if.
Alur programnya adalah jika kondisi if pertama benar makan program akan mengecek if
kedua jika benar maka mengecek if ketiga begitu seterusnya.

Bentuk dasar dari nested if adalah sebagai berikut :

```
if (kondisi){
    if(kondisi){
        if(kondisi){
            blok pernyataan;
        }
        Else{
            Blok pernyataan;
        }
    }
    Else{
        Blok pernyataan;
    }
}
Else{
    Blok pernyataan;
}
```

### Switch case

Selain menggunakan if untuk seleksi kondisi terdapat sintaks lain yaitu menggunakan
Switch case. Program akan menampilkan output sesuai dengan inputan yang diberikan
dengan batasan input berupa nilai awal sampai nilai akhir tertentu.

Bentuk dasar dari switch case adalah sebagai berikut :

```
switch (variabel) {
    case nilai1 : statement1; break;
    case nilai2 : statement2; break;
    case nilai3 : statement3; break;
    default : statement-def; 
}
```

## Pelaksanaan Percobaan

### Contoh Code Conditional Assignment

```c
#include <stdio.h>

int main() {

     int x = 5;
    ((x==5)) ? printf("Benar\n") : printf("Salah\n");

    return 0;
}
```

### Contoh Code If-else

```c
#include <stdio.h>

int main() {
    float nilai;

    printf("masukkan nilai : ");
    scanf("%f",&nilai);

    if (nilai > 60){
        printf("Anda Lulus\n");
    } else if (nilai >= 40){
        printf("Anda harus mengulang\n");
    } else {
        printf("Anda gagal\n");
    }

    return 0;
}
```
### Contoh Code Nested If

```c
#include <stdio.h>

int main() {

    int nilai;

    printf("masukkan nilai : ");
    scanf("%d",&nilai);

    if(nilai * 2 < 50){
        nilai += 10;
    }

    if (nilai <= 20){
        printf("Filkom\n");
        if (nilai % 2 == 1){
            printf("UB\n");
        } else{
            printf("Brawijaya\n");
        }
    } else {
        printf("PTIIK\n");
        if (nilai % 2 == 1){
            printf("UB\n");
        } else {
            printf("Brawijaya\n");
        }
    }

    return 0;
}
```
### Contoh Code Switch case

```c
#include <stdio.h>

int main() {


    return 0;
}
```

## Data dan Analisis Percobaan

tba

## Tugas Praktikum

**1)** Buatlah program sebagai berikut dengan menggunakan metode switch case

```
Menu :
1. menghitung luas dan keliling persegi panjang 
2. menghitung luas dan keliling lingkaran
3. menghitung luas dan keliling segitiga 
Pilihan anda : 3
Masukkan a : 3
Masukkan b : 4
Masukkan r : 5

Keliling segitiga   : 12 cm
Luas segitiga       : 6 cm2

Pilihan anda : 10
Data tak ditemukan, program dihentikan ...
``` 

**2)** Untuk menentukan kriteria kegemukan, digunakan IMT (Indeks Massa Tubuh), yang bisa dihitung menggunakan rumus :<Enter>
IMT = b / (t * t)

b = berat badan (kg)
t = tinggi badan (m)
Kriteria untuk nilai IMT ditabelkan sebagai berikut :

| Nilai IMT | Tipe Data |
----------|----------- |
IMT ≤ 18,5 | Kurus
18,5 < IMT ≤ 25 | Normal
25 < IMT ≤ 30 | Gemuk
IMT > 30 | Kegemukan
Susun program dengan tampilan sebagai berikut dengan menggunakan metode if-else!
```
Berat badan (kg)    : 45
Tinggi badan (m)    : 1.72
IMT     = 15,21             Termasuk kurus

Berat badan (kg)    : 85
Tinggi badan (m)    : 1.71
IMT     = 27,76             Termasuk gemuk
``` 

**3)** Susun program untuk masalah pengajian sebagai berikut :
Masukan yang dibutuhkan oleh program adalah : jumlah jam kerja tiap minggu. Keluaran program adalah : total upah dari pegawai tertentu.
Aturan yang diterapkan adalah :
- Batas kerja maksimal adalah 60 jam / minggu, dengan upah Rp. 5000,- / jam. Kelebihan jam kerja dari batas maksimum akan dianggap sebagai lembur dengan upah Rp. 6000,- /jam.
- Batas kerja minimal adalah 50 jam / minggu. Apabila pegawai mempunyai jam kerja di bawah batas kerja minimal ini, maka akan dikenakan denda sebesar Rp. 1000, - / jam.
```
Jam kerja   : 55
Upah    = Rp. 275000
Lembur  = Rp.      0
Denda   = Rp.      0
-----------------------
Total   = Rp. 275000
``` 