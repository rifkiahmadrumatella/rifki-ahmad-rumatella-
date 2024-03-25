import java.time.LocalDate;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input data diri
        System.out.print("Masukkan nama kamu yang paling ganteng: ");
        String nama = scanner.nextLine();

        System.out.print("Masukkan jenis kelamin asal jangan banci (P/L/): ");
        String jenisKelaminInput = scanner.nextLine();
        String jenisKelamin = (jenisKelaminInput.equalsIgnoreCase("P")? "Perempuan" : "Laki-laki");

        System.out.print("Masukkan tanggal lahir bagi yang masih ingat (2005-04-04): ");
        String tanggalLahirString = scanner.nextLine();
        LocalDate tanggalLahir = LocalDate.parse(tanggalLahirString);

        // Hitung umur
        int umur = LocalDate.now().getYear() - tanggalLahir.getYear();

        // Output data diri
        System.out.println("\nData diri:");
        System.out.println("Nama: " + nama);
        System.out.println("Jenis Kelamin: " + jenisKelamin);
        System.out.println("Tanggal Lahir: " + tanggalLahir);
        System.out.println("Umur: " + umur + " tahun");

        scanner.close();
    }
}
