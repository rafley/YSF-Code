package praktikum3;

import java.util.Scanner;

public class Latihan4 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int pilihan, beli, jmlMinuman, diskon, ttlBelanja;

        System.out.println("Selamat datang di program aplikasi membeli minuman");
        System.out.println("1. Beli Minuman\n2. Keluar");
        System.out.print("Pilih menu : ");
        pilihan = input.nextInt();
        if (pilihan == 1) {
            System.out.println("Harga minuman Rp.10000");
            System.out.print("Masukkan jumlah minuman : ");
            jmlMinuman = input.nextInt();
            beli = jmlMinuman * 10000;
            if (beli>= 30000 && beli < 50000) {
                diskon = (beli * 5) / 100;
            } else if (beli > 50000) {
                diskon = (beli * 10) / 100;
            } else {
                diskon = 0;
            }
            ttlBelanja = beli - diskon;
            System.out.println("Anda membeli minuman sebanyak " + jmlMinuman + " buah dengan total harga RP." + beli + " dan potongan Rp." + diskon + " ,total belanja keseluruhan Rp." + ttlBelanja);
        } else if (pilihan == 2) {
            System.out.println("Anda keluar dari program");
        } else {
            System.out.println("Menu tidak tersedia");
        }
    }
}
