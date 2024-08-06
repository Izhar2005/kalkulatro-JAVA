

---

## Kalkulator Sederhana dalam Java

Program ini adalah sebuah kalkulator sederhana yang ditulis dalam bahasa pemrograman Java. Program ini memungkinkan pengguna untuk melakukan operasi aritmatika dasar seperti penjumlahan, pengurangan, perkalian, dan pembagian.

### Cara Kerja Program

1. **Pengambilan Input dari Pengguna:**
   - Program meminta pengguna untuk memasukkan dua angka dan operator aritmatika.
   - Angka pertama diambil dan disimpan dalam variabel `angka1`.
   - Operator aritmatika diambil dan disimpan dalam variabel `operator`.
   - Angka kedua diambil dan disimpan dalam variabel `angka2`.

2. **Operasi Aritmatika:**
   - Program menggunakan pernyataan `switch` untuk menentukan operasi yang akan dilakukan berdasarkan operator yang dimasukkan.
   - Jika operator adalah `+`, maka program akan menjumlahkan `angka1` dan `angka2`.
   - Jika operator adalah `-`, maka program akan mengurangkan `angka1` dengan `angka2`.
   - Jika operator adalah `*`, maka program akan mengalikan `angka1` dengan `angka2`.
   - Jika operator adalah `/`, program akan memeriksa apakah `angka2` adalah nol. Jika tidak, maka program akan membagi `angka1` dengan `angka2`. Jika ya, program akan menampilkan pesan kesalahan.

3. **Penanganan Kesalahan:**
   - Jika pengguna memasukkan operator yang tidak valid, program akan menampilkan pesan kesalahan.
   - Program juga menangani kesalahan pembagian dengan nol.

### Kode Sumber

```java
import java.util.Scanner;

public class Kalkulator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Masukkan angka pertama cuy: ");
        double angka1 = scanner.nextDouble();

        System.out.print("Masukkan operator (+, -, *, /): ");
        char operator = scanner.next().charAt(0);

        System.out.print("Masukkan angka kedua cuy: ");
        double angka2 = scanner.nextDouble();

        double hasil;
        switch (operator) {
            case '+':
                hasil = angka1 + angka2;
                System.out.println("Hasil: " + hasil);
                break;
            case '-':
                hasil = angka1 - angka2;
                System.out.println("Hasil: " + hasil);
                break;
            case '*':
                hasil = angka1 * angka2;
                System.out.println("Hasil: " + hasil);
                break;
            case '/':
                if (angka2 != 0) {
                    hasil = angka1 / angka2;
                    System.out.println("Hasil: " + hasil);
                } else {
                    System.out.println("Gak bisa dibagi nol cuy.");
                }
                break;
            default:
                System.out.println("Operator yang dimasukkan gak valid cuy.");
                break;
        }
        scanner.close();
    }
}
```

### Penjelasan Kode

- **import java.util.Scanner;**
  Mengimpor kelas Scanner untuk membaca input dari pengguna.

- **public class Kalkulator { ... }**
  Mendefinisikan kelas utama bernama `Kalkulator`.

- **public static void main(String[] args) { ... }**
  Mendefinisikan metode `main` yang merupakan titik masuk program.

- **Scanner scanner = new Scanner(System.in);**
  Membuat objek Scanner untuk membaca input dari pengguna.

- **double angka1 = scanner.nextDouble();**
  Membaca angka pertama yang dimasukkan oleh pengguna dan menyimpannya dalam variabel `angka1`.

- **char operator = scanner.next().charAt(0);**
  Membaca operator yang dimasukkan oleh pengguna dan menyimpannya dalam variabel `operator`.

- **double angka2 = scanner.nextDouble();**
  Membaca angka kedua yang dimasukkan oleh pengguna dan menyimpannya dalam variabel `angka2`.

- **switch (operator) { ... }**
  Menggunakan pernyataan `switch` untuk menentukan operasi yang akan dilakukan berdasarkan operator.

- **case '+': hasil = angka1 + angka2; ...**
  Melakukan penjumlahan jika operator adalah `+`.

- **case '-': hasil = angka1 - angka2; ...**
  Melakukan pengurangan jika operator adalah `-`.

- **case '*': hasil = angka1 * angka2; ...**
  Melakukan perkalian jika operator adalah `*`.

- **case '/': ...**
  Memeriksa apakah `angka2` adalah nol sebelum melakukan pembagian. Jika `angka2` tidak nol, maka melakukan pembagian.

- **default: System.out.println("Operator yang dimasukkan gak valid cuy.");**
  Menampilkan pesan kesalahan jika operator yang dimasukkan tidak valid.

Program ini dirancang untuk memberikan pengalaman pengguna yang sederhana dan intuitif dalam melakukan operasi aritmatika dasar.

---


