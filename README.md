//======================================================================================================================================//
//================================================================FERDI SETYO HANDIKA===================================================//
//===================================================================227064516034=======================================================//

package uasalgoritma;
import java.util.Scanner;

public class UasAlgoritma3 {
public static void main(String[] args) {

        System.out.println("## COLDPLAY MUSIC of SPHERES  ##");
        System.out.println("========== WORLD TOUR ==========");
        System.out.println("GELORA BUNG KARNO STADIUM JAKARTA");
        System.out.println("Kategori ticket yang tersedia:");
        System.out.println("1. Category 1 (Rp5.000.000)");
        System.out.println("2. Category 2 (Rp4.000.000)");
        System.out.println("3. Category 3 (Rp3.250.000)");
        System.out.println("4. Category 4 (Rp2.500.000)");

        Scanner input = new Scanner(System.in);
        System.out.print("Silahkan Pilih Kategori Ticket (1-4) : ");
        int category = input.nextInt();

        System.out.print("Masukkan Jumlah Ticket Yang Ingin Dibeli : ");
        int jumlahTiket = input.nextInt();

        int[] hargaTiket = { 5000000, 4000000, 3250000, 2500000 };

        if (category >= 1 && category <= 4) {
            int HargaTiket = hargaTiket[category - 1];
            int totalHarga = HargaTiket * jumlahTiket;
            System.out.println("=============================================");
            System.out.println("      INVOICE PEMBELIAN TICKET COLDPLAY      ");
            System.out.println("=============================================");
            System.out.println("Kategori Ticket: Category " + category);
            System.out.println("Jumlah Ticket  : " + jumlahTiket);
            System.out.println("Harga Ticket   : Rp" + totalHarga);
            System.out.println("=============================================");

            System.out.print("Masukkan jumlah uang yang akan dibayarkan: ");
            int jumlahUang = input.nextInt();

            if (jumlahUang >= totalHarga) {
                int kembalian = jumlahUang - totalHarga;
                System.out.println("Kembalian     : Rp" + kembalian);
            } else {
                System.out.println("Jumlah uang yang dibayarkan tidak mencukupi!");
            }
            System.out.println("=============================================");
        } else {
            System.out.println("Kategori Ticket Tidak Valid!");
        }
    }
}

    
    
