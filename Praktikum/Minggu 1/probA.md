# 01A. Input dan Output pada C++

**Time Limit:** 1 s  
**Memory Limit:** 256 MB

## Deskripsi

Bahasa pemrograman C++, meskipun dikembangkan dari bahasa C, memiliki pustaka dan fungsi tersendiri yang berbeda dengan bahasa C dalam melakukan operasi dasar input dan output (membaca masukan dan mencetak keluaran).

Dalam bahasa C, kita biasa menggunakan pustaka `<stdio.h>` yang memiliki fungsi `scanf()` untuk membaca masukan (*input*) dan `printf()` untuk mencetak keluaran (*output*). Kedua fungsi tersebut menggunakan penanda format yang disesuaikan dengan tipe data dan format yang diinginkan pada proses input/output, misalnya `%d` untuk menyatakan bilangan bulat dalam desimal, `%f` untuk bilangan pecahan (`float`), dan sebagainya.

Bahasa C++ menggunakan pustaka `<iostream>` untuk operasi input/output, yang menyediakan objek bernama `cin` dan `cout`. Keduanya digunakan untuk input dan output dengan simbol *stream* berikut:

- `>>` untuk masukan (*input*).
- `<<` untuk keluaran (*output*).

Contoh penggunaan:

```cpp
#include <iostream>
using namespace std;

int main() {
    int x;
    cin >> x;
    cout << x << endl;
    return 0;
}
```

Potongan program di atas membaca masukan untuk diisikan ke variabel `x`, lalu menampilkannya kembali dan mengakhirinya dengan baris baru menggunakan `endl`.

Anda dapat membaca lebih lanjut mengenai input dan output pada C++ melalui tautan berikut:

- [C++ I/O](https://en.cppreference.com/w/cpp/io)
- [`cin`](https://en.cppreference.com/w/cpp/io/cin)
- [`cout`](https://en.cppreference.com/w/cpp/io/cout)

### Mengatur Jumlah Angka di Belakang Desimal

Untuk mengatur jumlah digit di belakang desimal, kita dapat menggunakan `setprecision()` dari pustaka `<iomanip>` yang digabungkan dengan manipulator `fixed`.

Contoh:

```cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    float y;
    cin >> y;
    cout << fixed << setprecision(2) << y << endl;
    return 0;
}
```

Kode di atas memiliki efek yang sama dengan perintah `printf("%.2f\n", y)` pada bahasa C, yaitu menampilkan angka dengan tepat dua digit di belakang desimal.

## Batasan

\[
-100.000.000 < a,b,c,d < 100.000.000
\]

## Masukan

Masukan terdiri dari satu baris yang berisi empat bilangan bulat:

```text
a b c d
```

## Keluaran

Keluaran terdiri dari satu baris yang berisi nilai rata-rata dari keempat bilangan masukan, ditampilkan dengan dua angka di belakang tanda desimal.

## Contoh Masukan 1

```text
1 3 4 5
```

## Contoh Keluaran 1

```text
3.25
```
