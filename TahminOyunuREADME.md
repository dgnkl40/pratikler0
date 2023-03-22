import java.util.Arrays;
import java.util.Random;
import java.util.Scanner;

public class TahminOyunu {
    public static void main(String[] args) {
        Random rast = new Random();
        int sayi = rast.nextInt(100);
        int [] yanlis = new int[7];
        int tahmin;
        int hak = 0 ;
        Scanner girdi = new Scanner(System.in);
        while (hak < 7 ){
            System.out.println("Tahmini Girin: ");
            tahmin = girdi.nextInt();
            if(tahmin < 0 || tahmin > 100 ){
                System.out.println("0-100 Arasında Bir Sayı Girin.");
                continue;
            }if (tahmin == sayi){
                System.out.println("Doğru Tahmin.Tebrikler Kazandın.");
                break;
            }else {
                System.out.println("Hatalı Giriş Yaptınız.");
                if (tahmin < sayi){
                        System.out.println(tahmin + " Sayısı Gizli Sayıdan Küçüktür ");
                }
                else  {
                    System.out.println( tahmin + " Sayısı Gizli Sayıdan Büyüktür");
            }
                yanlis [hak++] = tahmin;
                System.out.println("Kalan Hak " + (7 - hak));
                System.out.println(Arrays.toString(yanlis));
            }
        }
        System.out.println("--------------");
        System.out.println("GİZLİ SAYI =>" +  sayi);
    }}

