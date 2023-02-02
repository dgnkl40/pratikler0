import java.util.Scanner;
public class palindromSayı {
    static boolean ispalindrom(int number) {
        int sayı = number, tersnumber = 0, sonNumber;
        while (0 != sayı) {
            sonNumber = sayı % 10;
            tersnumber = (tersnumber * 10) + sonNumber;
            sayı /= 10;
        }
        if (number == tersnumber)
            return true;
        else
            return false;

    }

    public static void main(String[] args) {
        System.out.println(ispalindrom(9889));
        System.out.println(ispalindrom(528));
        System.out.println(ispalindrom(9));

    }
}
