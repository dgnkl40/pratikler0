import java.util.Scanner;

public class alıstırma {

    static boolean asalMi(int sayi) {
        int a = 0;
        for(int i = 2; i < sayi; i++)
        {
            if(sayi % i == 0) {
                a++;
            }
        }
        if(a == 0) {
            return true;
        }
        else {
            return false;
        }
    }
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("Bir Sayi Giriniz: ");
        int sayi = scan.nextInt();

        if(asalMi(sayi)) { // asalMi(sayi) == true
            System.out.println( sayi +" Asal bir sayidir.");
        }
        else {
            System.out.println(sayi +" Asal bir sayi degildir.");
        }
    }
}

