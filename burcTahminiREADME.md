import java.util.Scanner;
public class burcTahmini {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        int day, month;
        System.out.print("Doğduğun Ayı Gir: ");
        month = girdi.nextInt();
        System.out.print("Doğduğun Günü Gir: ");
        day = girdi.nextInt();
        if (((month == 3) && (day >= 21) && (day <= 31)) || ((month == 4) && (day >= 1) && (day <= 20))) {
            System.out.print("BURÇ: KOVA");
        } else if (((month == 4) && (day >= 21) && (day <= 30)) || ((month == 5) && (day >= 1) && (day <= 21))) {
            System.out.print("BURÇ: BOĞA");
        } else if (((month == 5) && (day >= 22) && (day <= 31)) || ((month == 6) && (day >= 1) && (day <= 22))) {
            System.out.print("BURÇ: İKİZLER");
        } else if (((month == 6) && (day >= 23) && (day <= 30)) || ((month == 7) && (day >= 1) && (day <= 22))) {
            System.out.print("BURÇ: YENGEÇ");
        } else if (((month == 7) && (day >= 23) && (day <= 31)) || ((month == 8) && (day >= 1) && (day <= 22))) {
            System.out.print("BURÇ: ASLAN");
        } else if (((month == 8) && (day >=23) && (day <=30)) || ((month == 9) && (day >= 1) && (day <=22))) {
            System.out.print("BURÇ: BAŞAK");
        } else if (((month == 9) && (day >=23) && (day <=31)) || ((month == 10) && (day >= 1) && (day <=22))) {
            System.out.print("BURÇ: TERAZİ");
        } else if (((month == 10) && (day >=23) && (day <=30)) || ((month == 11) && (day >= 1) && (day <=21))) {
            System.out.print("BURÇ: AKREP");
        } else if (((month == 11) && (day >=22) && (day <=31)) || ((month == 12) && (day >= 1) && (day <=21))) {
            System.out.print("BURÇ: YAY");
        } else if (((month == 12) && (day >=22) && (day <=30)) || ((month == 1) && (day >= 1) && (day <=21))) {
            System.out.print("BURÇ: OĞLAK");
        } else if (((month == 1) && (day >=22) && (day <=31)) || ((month == 2) && (day >= 1) && (day <=19))) {
            System.out.print("BURÇ: KOVA");
        } else if (((month == 2) && (day >=20) && (day <=28)) || ((month == 3) && (day >= 1) && (day <=20))) {
            System.out.print("BURÇ: İKİZLER");
        }
    }
}
