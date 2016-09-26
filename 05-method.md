# Bab 5 - Program Dengan Menggunakan Method

## Tujuan

* Praktikan mampu mengenal method pada pemrograman C 
* Praktikan mampu mengenal penggunaan method pada pemrograman C 
* Praktikan mampu mengimplmentasikan macam-macam method pada pemrograman C 

## Ringkasan Materi

### Method Void pada C

Method merupakan suatu program yang terletak terpisah dari program utama, tetapi tetap merupakan bagian dari program yang dibuat. Dengan menggunakan method dapat membuat program menjadi lebih mudah dimengerti dan mudah dalam pendokumentasian. Method void merupakan sebuah method yang tidak mengembalikan nilai yang ada pada method tersebut. Berikut merupakan contoh dari penggunaan method void pada C (prak_void.c).

### Method Return Value pada C

Method return value merupakan method yang mengembalikan suatu nilai ketika kembali ke program utamanya disertai dengan membawa suatu nilai. Berikut merupakan contoh dari penggunaan method return value pada C (prak_retval.c)

### Method rekursif pada C

Method rekursif adalah method yang dimana ia memanggil dirinya sendiri ketika kondisi tertentu. Berikut merupakan contoh dari penggunaan method rekursif pada C (prak_rekursif.c)

### Pass by value dan pass by reference

Perbedaan pass by value dengan pass by reference adalah sebagai berikut..

#### Pass by value

* Parameter dalam method atau function merupakan copy dari variabel asli yang dilewatkan di parameter method
* Perubahan yang terjadi pada variabel yang dilewatkan tersebut tidak berpengaruh pada nilai asli variabelnya

Contoh code

```c
// Pass by value
#include <stdio.h>

void test(float f) {
    f = -1.5f;
}

int main() {
    float f = 3.14f;
    test(f);
    printf("%.2f\n", f); // output : 3.14

    return 0;
}
```

#### Pass by reference

* Parameter dalam method atau function merupakan reference menuju lokasi memori dimana variabel tersebut menyimpan nilainya
* Perubahan yang terjadi pada variabel yang dilewatkan tersebut berpengaruh pada nilai asli variabelnya
* Menggunakan pointer untuk menunjuk ke reference variabel sebenarnya

Contoh code

```c
// Pass by reference
#include <stdio.h>

// menunjuk ke alamat memori sebenarnya dengan pointer
void test(float *f) {
    *f = -1.5f;
}

void multiplyArray(int *arr, int length, int multiplier) {
    for (int i = 0 ; i < length ; i++) {
        arr[i] *= multiplier;
    }
}

int main() {
    float f = 3.14f;
    int array[] = {1, 2, 3, 4, 5};

    test(&f);
    multiplyArray(&array, sizeof(array) / sizeof(*array), 2); // array = [2, 4, 6, 8, 10]

    printf("%.2f\n", f); // output : -1.50
    return 0;
}
```

## Pelaksanaan Percobaan

### Contoh code method void

```c
// prak_void.c
#include <stdio.h>

void greeting(char nama[]) {
    printf("Hello, %s\n", nama);
}

void morningGreeting() {
    printf("Good morning\n");
}

int main() {
    char nama[50]; // 50 karakter nama
    printf("Masukkan nama : ");
    scanf("%s", &nama);
    morningGreeting();
    greeting(nama);

    return 0;
}
```

### Contoh code method return value

```c
// prak_retval.c
#include<stdio.h>

int faktorial(int n) {
    int hasil = 1;
    for (int i = 1 ; i <= n ; i++) {
        hasil *= i;
    }
    return hasil;
}

int main() {
    printf("Nilai dari 5! = %d\n", faktorial(5));

    return 0;
}
```

### Contoh code method rekursif

```c
// prak_rekursif.c
#include<stdio.h>

int faktorial(int n) {
    return (n == 1) ? 1 : n * faktorial(n - 1);
}

int main() {
    printf("Nilai dari 5! = %d\n", faktorial(5));

    return 0;
}
```

### Contoh code pass by reference

```c
// prak_reference.c
#include <stdio.h>

// menunjuk ke alamat memori sebenarnya dengan pointer
void multiplyArray(int *arr, int length, int multiplier) {
    for (int i = 0 ; i < length ; i++) {
        arr[i] *= multiplier;
    }
}

void print(int arr[], int length) {
    for (int i = 0 ; i < length ; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int array[] = {1, 2, 3, 4, 5};
    multiplyArray(&array, sizeof(array) / sizeof(*array), 7);
    print(array, sizeof(array) / sizeof(*array));
    return 0;
}
```

## Data dan Analisis Percobaan

tba

## Tugas Praktikum

**1)** Buatlah program untuk menentukan apakah bilangan tersebut bilangan prima atau bukan dengan menginputkan sebuah bilangan yang di inginkan. Setelah itu program akan mengoutputkan bilangan prima 1-100!

**2)** Buatlah program yang akan menghasilkan deret 25 bilangan pertama fibonacci!
