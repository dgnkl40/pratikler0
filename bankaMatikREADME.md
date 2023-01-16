import java.util.Scanner;
public class bankaMatik {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        String userName,password;
        int right = 3;
        double bakiye = 0;
        int select;
        int price ;
        while (right > 0){
            System.out.print("Kullanıcı Adınızı Giriniz: ");
            userName = girdi.nextLine();
            System.out.println("Parolanızı Giriniz: ");
            password = girdi.nextLine();

            if (userName.equals("dkul") && password.equals("4080")) {
                System.out.println("KULBANKA Hoşgeldiniz.");
                do {
                    System.out.print("1-Para Yatırma\n" + "2-Para Çekme\n" + "3-Bakiye Sorgulama\n" + "4-ÇIKIŞ\n");
                    System.out.print("Yapmak İstediğiniz İşlemi Giriniz: ");
                    select = girdi.nextInt();
                    switch (select) {
                        case 1:
                            System.out.print("Yatırmak İstediğiniz Tutarı Girin: ");
                            price = girdi.nextInt();
                            bakiye += price;
                            break;
                        case 2:
                            System.out.print("Çekmek İstediğiniz Tutarı Giriniz: ");
                            price = girdi.nextInt();

                            if (bakiye < price) {
                                System.out.print("Hatalı Tutar");
                            } else {
                                bakiye -= price;
                            }
                            break;
                        case 3:
                            System.out.println("Bakiyeniz: " + bakiye);
                            break;
                    }
                }
                while (select != 4);
                System.out.print("ÇIKIŞ Yaptınız");
            }else {
                right --;
                System.out.print("Hatalı kullanıcı adı veya şifre girdiniz.Lütfen tekrar deneyiniz.");
                if(right == 0){
                    System.out.print("Hesabınız bloke olmuştur.Bankanızla iletişime geçiniz.");
                }
                else {
                    System.out.println("Kalan Hakkınız : " + right);
                }



                }
            }
        }

    }
