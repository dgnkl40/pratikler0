import java.util.Scanner;
public class basamakToplamı {

    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        int sayi = girdi.nextInt();
        int toplam = 0;

        while (sayi > 0){
            toplam += (sayi%10);
            sayi = sayi / 10;
        }
        System.out.print(toplam);
    }
    }
