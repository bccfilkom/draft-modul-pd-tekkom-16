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

tba

## Data dan Analisis Percobaan

tba

## Tugas Praktikum

tba