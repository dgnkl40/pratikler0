import java.util.Scanner;
public class kombinasyon {
    public static void main(String[] args) {
       //Ödev
        //N elemanlı bir kümenin elemanları ile oluşturulacak r elemanlı farklı grupların sayısı
        // n’in r’li kombinasyonu olarak adlandırılır.
        // N’in r’li kombinasyonu C(n,r) şeklinde gösterilir.
        //Java ile kombinasyon hesaplayan program yazınız.
        //Kombinasyon formülü
        //C(n,r) = n! / (r! * (n-r)!)

        Scanner girdi = new Scanner(System.in);
        int n,r,nr , nFak = 1 , rFak = 1 , nrFak = 1 ,kombinasyon;

        do {
            System.out.print("Enter 1st Number: ");
            n = girdi.nextInt();
            System.out.print("Enter 2nd Number: ");
            r = girdi.nextInt();
            if (n<r){
                System.out.print("ERROR");
            }

        }while (n<r);

        nr = n-r;
        for (int i = 1; i <= n; i++) {
            nFak *= i;
        }
        for (int i = 1; i <= n; i++) {
            rFak *= i;
        }
        for (int i = 1; i <= n; i++) {
            nrFak *= i;
        }
        kombinasyon = nFak/(rFak * nrFak);

        System.out.print(kombinasyon);


    }

    }


