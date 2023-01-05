import java.util.Scanner;
public class kuvvetHesaplama {
    public static void main(String[] args) {
        Scanner bır = new Scanner(System.in);

        int k;

        System.out.print("Son Sayıyı Girin: ");
        k = bır.nextInt();

        for (int a = 1; a<=k; a*=3){
            System.out.println(a);
        }
        for (int b= 1; b <= k; b*=4){
            System.out.println(b);
        }
    }
}
