import java.util.Scanner;
public class ucakBileti {
    public static void main(String[] args) {
       double km , yas, gidis,totalOne,totalTwo,totalOneGd ;
        Scanner girdi = new Scanner(System.in);
        System.out.print("Gidilecek Mesafe(KM): ");
        km = girdi.nextDouble();
        System.out.print("Yolcunun Yaşı: ");
        yas = girdi.nextDouble();
        System.out.println("1-Tek Yön  2-Gidiş Dönüş");
        System.out.print("Yolculuk Tipi:");
        gidis = girdi.nextDouble();
        totalOne = (km * 0.10);
        if ((km > 0) && (yas >= 0) && ((gidis == 1) || (gidis ==2))){
            if (gidis == 2) {
                totalTwo = (totalOne * 2) - (((totalOne * 2) * 20) / 100);
                System.out.print("Toplam Tutar:" + totalTwo +"TL");
            }
            else if (yas < 12){
                totalTwo = totalOne / 2 ;
                System.out.print("Toplam Tutar: " + totalTwo +"TL");
            }
            else if ((yas >= 12) && (yas <= 24)) {
                totalTwo = totalOne - ((totalOne * 10) / 100 );
                System.out.print("Toplam Tutar:" + totalTwo +"TL");
            }
            else if (yas >= 65) {
                totalTwo = totalOne - ((totalOne * 30) / 100);
                System.out.print("Toplam Tutar:" + totalTwo +"TL");
            }
        }
        else{
            System.out.print("Hatalı Veri Girdiniz");
        }
    }
}
