import java.util.Scanner;
public class harmonikSayı {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);

        System.out.print("N sayısını girin: ");
        int n = girdi.nextInt();
        double i = 1;
        double toplam =0.0;

        while(i<=n){
            toplam += (1/i);
            i++;
        }
        System.out.print("Harmonik Seri : " + toplam);

    }
}
