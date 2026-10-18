# 02A. Botol Kemasan

| Ketentuan | Batas |
|:--|:--|
| **Time Limit** | 500 ms |
| **Memory Limit** | 256 MB |

## Deskripsi

Dalam kehidupan sehari-hari, kita sering membeli minuman kemasan botol, misalnya jus atau air mineral. Mari kita perhatikan beberapa fakta tentang minuman botol tersebut:

- Setiap minuman botol memiliki nama produk, kapasitas maksimum botol (dalam ml), dan sisa isi cairan saat ini (dalam ml).
- Ketika baru dibeli, botol biasanya terisi penuh.
- Botol berisi minuman bisa diminum sehingga isinya berkurang.
- Botol juga bisa diisi ulang (*refill*) jika belum penuh.
- Sisa cairan dalam botol tidak boleh bernilai negatif (kurang dari 0 ml) dan tidak boleh melebihi kapasitas maksimumnya.

Buatlah program berorientasi objek menggunakan bahasa C++ dengan ketentuan berikut.

### Ketentuan Kelas

**Nama kelas:** `MinumanKemasan`

#### Atribut (*State*)

- `namaProduk` (`string`)
- `kapasitas` (`integer`, dalam ml)
- `isiSekarang` (`integer`, dalam ml)

#### Konstruktor (*Constructor*)

- Buat konstruktor yang menerima parameter `namaProduk` dan `kapasitas`.
- Saat objek pertama kali dibuat melalui konstruktor ini, nilai `isiSekarang` secara otomatis diatur sama dengan `kapasitas`, sehingga botol dalam keadaan penuh.

#### Metode (*Method/Behaviour*)

- `minum(jumlah)`: Mengurangi `isiSekarang` sebanyak `jumlah` ml.
- `isiUlang(jumlah)`: Menambah `isiSekarang` sebanyak `jumlah` ml.
- `show()`: Menampilkan status botol saat ini, meliputi nama produk, kapasitas, dan sisa isi dalam ml.

### Program Utama (*Driver*)

Buat program yang membaca data dengan format berikut:

```text
<nama produk> <kapasitas>
<minum|isiulang> <jumlah>
...
...
show
```

Instruksi `show` menandai akhir dari data dan bertujuan untuk menampilkan status terakhir botol dengan format berikut:

```text
Nama Produk : <nama produk>
Kapasitas   : <kapasitas> ml
Isi Sekarang: <volume terakhir> ml
```

## Contoh Masukan

```text
yourTea 1000
minum 300
minum 500
isi 600
minum 200
show
```

## Contoh Keluaran

```text
Nama Produk : yourTea
Kapasitas   : 1000 ml
Isi Sekarang: 600 ml
```

