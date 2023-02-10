import java.util.Scanner;
public class desens {
    static int recursive(int sayi) {
        if (sayi >= 0) {
            System.out.print(sayi + " ");
            return recursive( sayi- 5);
        }
        return sayi;
    }
    static int recursive1(int sayi, int sayiA) {
        if (sayiA >= sayi) {
            System.out.print(sayi + " ");
            return recursive1(sayi + 5, sayiA);
        }
        return sayi;
    }
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Bir Sayı Girin: ");
        int sayi = girdi.nextInt();
        int sayiA = sayi;
        recursive1(recursive(sayi), sayiA);
    }
}
