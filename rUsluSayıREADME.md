
import java.util.Scanner;
public class recursiveUsluSayı {
    static int power() {
        Scanner girdi = new Scanner(System.in);
            System.out.print("Taban Sayısını Girin: ");
            int taban = girdi.nextInt();
            System.out.print("Üssü Girin: ");
            int ust = girdi.nextInt();
            int result = 1;
            for (int i = 1; i <= ust; i++) {
                if (ust == 0) {
                    result = 1;
                } else
                    result *= taban;
            }
        System.out.println("Sonuç : " + result);
            return power();
    }
    public static void main(String[] args) {
        power();

    }
}
