import java.util.Scanner;
public class mukemmelSayı {
    public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      int number ;
      int wnumber = 0;

      System.out.print("Bir Sayı Girin: ");
      number = input.nextInt();

      for (int i = 1;i <number;i++){
          if (number%i==0){
              wnumber +=i;

          }
      }
      if (wnumber == number){
          System.out.print(number + " Mükemmel bir sayıdır.");
      } else{
          System.out.print(number + " Mükemmel sayı değildir.");

      }
    }
}
