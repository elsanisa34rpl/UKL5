# UKL5

    package com.mycompany.ukl5;

    import java.util.ArrayList;
    import java.util.Scanner;

    import java.util.Random;


    /**
    *
    * @author LOQ
    */
     public class UKL5 {

    public static void main(String[] args) {
       
        Random rand = new Random();
        Scanner input = new Scanner(System.in);

        ArrayList<Integer> historyKomputer = new ArrayList<>();
        ArrayList<Integer> historyPemain = new ArrayList<>();

        int skorKomputer = 0;
        int skorPemain = 0;

        System.out.println("=== Permainan Lempar Dadu ===");
        System.out.println("Pertama mencapai 5 kemenangan akan menang!");

        while (skorKomputer < 5 && skorPemain < 5) {

            System.out.print("\nTekan tombol apapun untuk melempar dadu...");
            input.nextLine();
            

            int daduKomputer = rand.nextInt(6) + 1; // 1-6
            int daduPemain = rand.nextInt(6) + 1;

            // Simpan ke riwayat
            historyKomputer.add(daduKomputer);
            historyPemain.add(daduPemain);

            System.out.println("Nilai dadu komputer: " + daduKomputer);
            System.out.println("Nilai dadu pemain  : " + daduPemain);
            
            
            
            

            // Tentukan pemenang ronde
            if (daduPemain > daduKomputer) {
                skorPemain++;
                System.out.println(">> Pemain menang di ronde ini!");
            } else if (daduKomputer > daduPemain) {
                skorKomputer++;
                System.out.println(">> Komputer menang di ronde ini!");
            } else {
                System.out.println(">> Seri!");
            }

            System.out.println("Skor: Pemain " + skorPemain + " - " + skorKomputer + " Komputer");
        }

        System.out.println("\n=== Permainan Selesai ===");

        if (skorPemain == 5) {
            System.out.println("Pemenangnya adalah: PEMAIN");
        } else {
            System.out.println("Pemenangnya adalah: KOMPUTER");
        }

        // Rekap semua lemparan
        System.out.println("\n--- Rekap Lemparan Komputer ---");
        System.out.println(historyKomputer);

        System.out.println("\n--- Rekap Lemparan Pemain ---");
        System.out.println(historyPemain);

        System.out.println("\nTotal kemenangan pemain  : " + skorPemain);
        System.out.println("Total kemenangan komputer: " + skorKomputer);

        input.close();
    }
    <img width="899" height="854" alt="Screenshot 2025-12-03 232215" src="https://github.com/user-attachments/assets/90c5f434-e7bd-40fa-9e7e-ce59623db564" />



