import java.util.Arrays;
import java.util.Scanner;
public class MaxMiny {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Bir Sayı Girin: ");
        int n = girdi.nextInt();
        int [] list = {2,53,14,6,8,-29,41,-92,5,33,-62};
        Arrays.sort(list);
        int min = list[0];
        int max = list[0];
        int eYakinb = 0;
        int eYakink = 0;


        for (int i :list){
            if (i < min){
                min = i;
            }
            if (max < i){
                 max = i;

            }
        }
        for (int i:list){
            if (n >= i){
                eYakink = i;
            }
            if (n <= i){
                eYakinb = i;
                break;
            }
        }System.out.println(Arrays.toString(list));
        System.out.println("Girilen Sayı: "+ n);
        System.out.println("Girilen Sayıya En Yakın Büyük Değer: "+ eYakinb);
        System.out.println("Girilen Sayıya En Yakın Küçük Değer: "+ eYakink);
    }
}
