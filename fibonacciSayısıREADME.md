import java.util.Scanner;
public class fibonacciSayısı {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Basamak Sayısını Girin: ");
        int n = girdi.nextInt();
        int result=0;
        int n1 = 0;
        int n2 = 1;
        System.out.print("Fibonacci Sayısının " + n + " Basamağı: " );
        for (int i = 1; i<=n;i++){
            System.out.print( n1 + " , ");
            result = n1 + n2;
            n1 = n2 ;
            n2 = result;
            

        }
    }
}
