import java.util.Scanner;
public class tersUcgen {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Basamak Sayısı Girin: ");
        int n = girdi.nextInt();

        for (int i = 0;i<=n;i++){
            for (int a = 1;a <=(n+i);a++){
                System.out.print(" ");
            }
            for (int b = 1;b <=2*n-(2*i+1);b++){
                System.out.print("#");
            }
            System.out.println(" ");
        }
    }
}
