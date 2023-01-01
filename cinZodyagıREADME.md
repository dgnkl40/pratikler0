import java.util.Scanner;
public class cinZodyagı {
    public static void main(String[] args) {
        double yıl;
        int result;
        Scanner girdi = new Scanner(System.in);
        System.out.print("Doğum Yılını Girin: ");
        yıl = girdi.nextDouble();
        result = (int) (yıl % 12);
        if (yıl > 0) {
            switch (result) {
                case 0:
                    System.out.print("Çin Zodyağı Burcunuz: MAYMUN");
                    break;
                case 1:
                    System.out.print("Çin Zodyağı Burcunuz: HOROZ");
                    break;
                case 2:
                    System.out.print("Çin Zodyağı Burcunuz: KÖPEK");
                    break;
                case 3:
                    System.out.print("Çin Zodyağı Burcunuz: DOMUZ");
                    break;
                case 4:
                    System.out.print("Çin Zodyağı Burcunuz: FARE");
                    break;
                case 5:
                    System.out.print("Çin Zodyağı Burcunuz: ÖKÜZ");
                    break;
                case 6:
                    System.out.print("Çin Zodyağı Burcunuz: KAPLAN");
                    break;
                case 7:
                    System.out.print("Çin Zodyağı Burcunuz: TAVŞAN");
                    break;
                case 8:
                    System.out.print("Çin Zodyağı Burcunuz: EJDERYA");
                    break;
                case 9:
                    System.out.print("Çin Zodyağı Burcunuz: YILAN");
                    break;
                case 10:
                    System.out.print("Çin Zodyağı Burcunuz: AT");
                    break;
                case 11:
                    System.out.print("Çin Zodyağı Burcunuz: KOYUN");
                    break;
                default:
                    System.out.print("Burç Bulunamadı");
            }

        }else {
            System.out.print("DOĞUM YILI HATALI");
        }
    }
}
