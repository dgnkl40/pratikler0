import java.util.Scanner;
public class aktiviteOner {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int heat;
        System.out.print("Sıcaklık Giriniz: ");
        heat = input.nextInt();
        if (heat<5){
            System.out.print("Sizin için uygun aktivite Kayaktır.");
        } else if ((heat>=5)&&(heat<=15)) {
            System.out.print("Size uygun aktivite Sinemadır");
            
        } else if ((heat>=15)&&(heat<=25)) {
            System.out.print("Sizin için uygun aktivite Pikniktir.");
            
        } else if (heat>25) {
            System.out.print("Sizin için uygun aktivite Yüzmedir.");

        }

    }
}
