import java.util.Scanner;
public class ebobEkok {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);

        System.out.print("İlk sayıyı giriniz: ");
        int n1 = girdi.nextInt();
        System.out.print("İkinci sayıyı giriniz: ");
        int n2 = girdi.nextInt();
        int ebob = 1;
        int ekok = 1;
       for (int i = 1;i < n1;i++){
           if (n1%i==0 && n2%i==0){
               ebob = i;
           }
       }
        if (ebob == 1){
            System.out.println("Sayılar aralarında asaldır.");
        }
        else {
            System.out.println("EBOB: " + ebob);
        }


       for (int k = 1;k < n1;k++){
           ekok= (n1*n2) / ebob;
           }
       System.out.println("EKOK "+ ekok);
       }


    }

