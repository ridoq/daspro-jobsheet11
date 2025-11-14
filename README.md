#   Percobaan 1 : Deklarasi, Inisialisasi, dan Menampilkan Array 2 Dimensi
    Pada percobaan ini dilakukan pembuatan kode program untuk mendeklarasikan, inisialisasi, dan menampilkan elemen pada array 2 dimensi. Data yang disimpan merupakan data nama penonton bioskop mini yang akan di duduk di dalam ruangan dengan dengan jumlah kursi 4 baris 2 kolom. 

---

##  Soal

1.  Apakah pengisian elemen array harus dilakukan secara berurutan mulai dari indeks ke-0? Jelaskan!
2.  Mengapa terdapat null pada daftar nama penonton?
3.  Lengkapi daftar penonton pada langkah ke-4 sebagai berikut

    ```java
    penonton[0][0] = "Amin";
    penonton[0][1] = "Bena";
    penonton[1][0] = "Candra";
    penonton[1][1] = "Dela";
    penonton[2][0] = "Eka";
    penonton[2][1] = "Farhan";
    penonton[3][0] = "Gisel";
    penonton[3][1] = "Hana";
    ```

4.  Tambahkan kode program sebagai berikut:

    ```java
    System.out.println(penonton.length);
    System.out.println(penonton[0].length);
    System.out.println(penonton[1].length);
    System.out.println(penonton[2].length);
    System.out.println(penonton[3].length);
    ```

    Jelaskan fungsi dari penonton.length dan penonton[0].length! Apakah penonton[0].length, penonton[1].length, penonton[2].length, dan penonton[3].length memiliki nilai yang sama? Mengapa? 

5.  Modifikasi kode program pada pertanyaan 4 untuk menampilkan panjang setiap baris pada array menggunakan for loop. Compile, run, lalu amati hasilnya. 

    ```java
    System.out.println(penonton.length);

    for(int i = 0; i < penonton.length; i++){
        System.out.println("Panjang baris ke-" + (i+1) + ": " + penonton[i].length);
    }
    ```

6.  Modifikasi kode program pada pertanyaan 5 untuk menampilkan panjang setiap baris pada array menggunakan foreach loop. Compile, run, lalu amati hasilnya.

    ```java
    System.out.println(penonton.length);

    for(String[] barisPenonton : penonton){
        System.out.println("Panjang baris: " + barisPenonton.length);
    }
    ```

7.  Tambahkan kode program untuk menampilkan nama penonton pada baris ke-3 menggunakan for loop. Compile, run, lalu amati hasilnya. 

    ```java
    System.out.println("Penonton pada baris  ke-3: ");

    for(int i = 0; i < penonton[2].length; i++){
        System.out.println(penonton[2][i]);
    }
    ```

8.  Modifikasi kode program pada pertanyaan 7 menjadi perulangan dengan foreach loop. Compile, run, lalu lakukan amati hasilnya. 

    ```java
    System.out.println("Penonton pada baris  ke-3: ");

    for(String i : penonton[2]){
        System.out.println(i);
    }
    ```

9.  Modifikasi kembali kode program pada langkah 11 untuk menampilkan nama penonton untuk setiap baris. Compile dan run program kemudian amati hasilnya.

    ```java
    for(int i = 0; i < penonton.length; i++){
        System.out.println("Penonton pada baris ke-" + (i+1) + ": " + String.join(", ", penonton[i]));
    }
    ```

10. Menurut Anda, apa kekurangan dan kelebihan foreach loop dibandingkan dengan for loop?
11. Berapa indeks baris maksimal untuk array penonton?
12. Berapa indeks kolom maksimal untuk array penonton?
13. Apa fungsi dari String.join()?

---

##  Jawaban

1.  Jawabannya tidak harus, pengisian elemen array dapat dilakukan dari indeks ke berapapun, namun jika pengisiannya tidak berurutan atau dilewati, maka elemen sebelumnya akan bernilai default sesuai tipe data nya
2.  Karena elemen array indeks terakhir ([3][1]) tidak diisi, maka nilainya akan diisi nilai default, kenapa _null_? karena tipe data array adalah String, jadi nilai default String adalah null