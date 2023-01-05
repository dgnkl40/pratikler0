import java.util.Scanner;
public class ikinciDöngü {
    public static void main(String[] args) {
        Scanner azkaldı = new Scanner(System.in);
        //Java döngüler ile tek bir sayı girilene kadar kullanıcıdan girişleri kabul eden
        // ve girilen değerlerden çift ve 4'ün katları olan sayıları toplayıp ekrana basan programı yazıyoruz

        int s;
        int total = 0;

        do {
            System.out.print("Sayıyı giriniz: ");
            s = azkaldı.nextInt();
            if ((s % 2 == 0)&&(s % 4 == 0)){
                total +=s;
            }
        }
        while (s % 2 == 0);
        System.out.print("Toplam:" +total);
    }

}
