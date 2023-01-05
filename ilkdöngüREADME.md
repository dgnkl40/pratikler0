import java.util.Scanner;
public class ilkDöngü {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        int k;
        System.out.print("Sayıyı Giriniz: ");
        k = girdi.nextInt();

        int i = 1;
        while (i <= k) {
            if ((i % 3 == 0) && (i % 4 == 0))
            System.out.println(i );
            i++;


        }
    }
}
