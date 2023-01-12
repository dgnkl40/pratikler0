import java.util.Scanner;
public class yıldızUcgen {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Bir Sayı Giriniz: ");
        int n = girdi.nextInt();
        int i = 0;
        while ( i <= n ) {
            for (int j = 0; j < (n - i); j++) {
                System.out.print(" ");
            }
            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("*");
            }
            System.out.println(" ");
            i++;
        }


    }
}
