import java.util.Scanner;
public class üstlüSayı {
    public static void main(String[] args) {
        Scanner kul =new Scanner(System.in);
        int x ,y,total = 1 ;

        System.out.print("Taban Sayı: ");
        x = kul.nextInt();
        System.out.print("üs :");
        y = kul.nextInt();


        for (int i=  1; i <= y;i++){
            total *= x;

        }
        System.out.print("Sonuç:" + total );
    }
}
