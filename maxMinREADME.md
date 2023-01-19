import java.util.Scanner;
public class maxMin {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);

        System.out.print("Girilecek Sayı Adedi: ");
        int n = girdi.nextInt();
        int number;
        int max =0 ,min = 0;

        for (int i = 1;i<=n;i++){
        System.out.print(i +". sayıyı giriniz: ");
        number = girdi.nextInt();
        if (i==1){
          max=number;
          min=number;
        }
        if (number>max){
          max=number;
        }
        if (number<min){
            min=number;

        }

        }
        System.out.println("En Büyük Sayıyı: " + max);
        System.out.print("En Küçük Sayıyı: " + min);
    }
}
