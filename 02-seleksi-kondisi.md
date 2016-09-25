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

 int uang;

    printf("Tipe Mata uang yang tersedia\n");
    printf("1. Dolar - USA (kurs USD 1 = Rp 13000,-)\n");
    printf("2. Yen - Jepang( kurs JPY 1 = Rp. 4000,- )\n");
    printf("3. Poundsterling - Inggris( kurs 1 Poundsterling = Rp. 10.500, -)\n");
    printf("4. Euro - MEE( kurs EUR 1 = Rp. 8900,- )\n");
    printf("5. Riyal - Arab Saudi( kurs 1 Riyal = Rp. 1100,-)\n");
    printf("Masukkan jenis mata uang anda : ");
    int pilihan;
    scanf("%d", &pilihan);

    switch(pilihan){
        case 1 :
            printf("Data diterima, jenis valuta Anda : Dolar Amerika Serikat\n");
            printf("Masukkan banyak uang nda (dalam dolar) : ");
            scanf("%d", &uang);
            printf("Uang yang diterima : Rp. %d ,-",uang*13000); break;
        case 2 :
            printf("Data diterima, jenis valuta Anda : Yen Jepang\n");
            printf("Masukkan banyak uang nda (Yen Jepang) : ");
            scanf("%d", &uang);
            printf("Uang yang diterima : Rp. %d ,-",uang*4000); break;
        case 3 :
            printf("Data diterima, jenis valuta Anda : Poundsterling Inggris\n");
            printf("Masukkan banyak uang nda (Poundsterling Inggris) : ");
            scanf("%d", &uang);
            printf("Uang yang diterima : Rp. %d ,-",uang*15000); break;
        case 4 :
            printf("Data diterima, jenis valuta Anda : Euro MEE\n");
            printf("Masukkan banyak uang nda (Euro MEE) : ");
            scanf("%d", &uang);
            printf("Uang yang diterima : Rp. %d ,-",uang*14000); break;
        case 5 :
            printf("Data diterima, jenis valuta Anda : Riyal Arab Saudi\n");
            printf("Masukkan banyak uang nda (Riyal Arab Saudi) : ");
            scanf("%d", &uang);
            printf("Uang yang diterima : Rp. %d ,-",uang*5000); break;
        default: printf("system not found\n");

    }

    return 0;
}
```

## Data dan Analisis Percobaan

### A. Conditional Assignment

1.	Jalankan Code Conditional Assignment dan benahi jika menemukan kesalahan!

2.	Tambahkan kode dibawah program diatas yang fungsinya meminta inputan user dengan memasukkan nama dan nim masing-masing mahasiswa dan jika benar maka akan mencetak nama dan nim mahasiswa, jika salah maka mencetak “input nama salah” jika memasukkan nama yang salah, “input nim salah” jika memasukka nim yang salah

3.	Buat program yang meminta untuk memasukkan nama dan password kemudian program akan meminta user untuk memasukkan nama dan password sesuai inputan sebelumnya. Jika benar maka program akan mencetak informasi biodata mahasiswa dan jika salah maka program akan mencetak “data tak ditemukan”.

### B. If - Else

1. Jalankan Code If - Else dan benahi jika menemukan kesalahan!

2. Masukkan nilai 30, 60 dan 80 saat program dijalankan, dan jawablah dengan screenshot hasil keluaran dari program!

### C. Nested If

1. Jalankan Code Nested If dan benahi jika menemukan kesalahan!

2. Masukkan nilai 5, 20, 30 saat program dijalankan, jelaskan alur jalan program dan beri screenshot keluaran dari program!

3. Ubah kode diatas dengan memanfaatkan operasi and!

### D. Switch Case

1. Jalankan Code Switch Case dan benahi jika menemukan kesalahan!

2. hapus kode `break` yang ada di program, pengaruh apa yang terjadi setelah pengubahan kode tersebut!

3. Apa perbedaan seleksi kondisi dengan menggunakan switch case dan if-else, dan kapan kita harus menggunakan if-else dan kapan menggunakan switch case?


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

**2)** Untuk menentukan kriteria kegemukan, digunakan IMT (Indeks Massa Tubuh), yang bisa dihitung menggunakan rumus :

IMT = b / (t * t)

b = berat badan (kg)
t = tinggi badan (m)

Kriteria untuk nilai IMT ditabelkan sebagai berikut :

Nilai IMT | Kriteria
----------|-----------
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