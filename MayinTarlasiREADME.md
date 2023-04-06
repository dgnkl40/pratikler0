import java.util.Random;
import java.util.Scanner;

public class MayinMetot {
    int satirS,sutunS,size;
    int [][] Mmap;
    int [][] Kmap;
    boolean oyun = true;

    Scanner girdi = new Scanner(System.in);
    Random rand = new Random();

    MayinMetot(int satirS,int sutunS){
        this.satirS=satirS;
        this.sutunS=sutunS;
        this.Mmap=new int[satirS][sutunS];
        this.Kmap=new int[satirS][sutunS];
        this.size=satirS*sutunS;
    }
    public void run (){
        int satir,sutun,basari=0;
        mayinOlustur();
        System.out.println("Oyun Başlıyor!!!");
        while (oyun) {
            print(Kmap);
            System.out.println("Satır : ");
            satir = girdi.nextInt();
            System.out.print("Sutun : ");
            sutun = girdi.nextInt();
            if (satir < 0 || satir >= satirS || sutun < 0 || sutun >= sutunS){
                System.out.println("Hatalı Sayı Girdiniz");
                System.out.println("Tekrar Sayı Giriniz");
                continue;
            }
            if (Mmap [satir][sutun] != -1){
                kontrol(satir,sutun);
                basari++;
                if (basari == (size -(size/4))){
                    System.out.println("Tebrikler Kazandın.");
                    break;
                }
            }else {
                oyun = false;
                print(Mmap);
                System.out.println("Oyun Bitti");
            }

        }
    }
    public void kontrol (int sa ,int su){
       if (Mmap[sa][su] == 0){
        if ((su < sutunS - 1) && (Mmap[sa][su + 1] ==- 1 )){
            Kmap[sa][su ]++;
        }
        if ((su > 0 ) && (Mmap[sa][su - 1] ==- 1) ){
            Kmap[sa][su ]++;
        }
        if ((sa < satirS - 3 ) && (Mmap[sa + 1][su ] ==- 1 )){
            Kmap[sa ][su ]++;
        }
        if ((sa > 0 ) &&(Mmap[sa -1 ][su ] ==- 1 )){
            Kmap[sa ][su ]++;
        }if (Kmap[sa][su] == 0){
            Kmap[sa][su] =-2;
           }
       }

    }
    public void mayinOlustur(){
       int randSatir,randSutun,count=0;
       while (count < (size/4)){
           randSatir=rand.nextInt(satirS);
           randSutun=rand.nextInt(sutunS);
           if (Mmap[randSatir][randSutun] != -1){
               Mmap[randSatir][randSutun] = -1;
               count++;
           }
       }
    }
    public void print (int [][] arr){
        System.out.println("==============");
        for (int a = 0;a< arr.length;a++){
            for (int b = 0;b< arr[0].length;b++ ){
                System.out.print(" "+arr [a][b] +" ");
            }

            System.out.println();;
        }System.out.println("==============");
    }
}
// ------------------------------------------------------
import java.util.Scanner;

public class MayınTarlası {
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        int satir;
        int sutun;

        System.out.println("Mayın Tarlasına Girdin.Bastığın Yerlere Dikkat Et.");
        System.out.println("Satır Gir: ");
        satir = girdi.nextInt();
        System.out.println("Sütun Gir: ");
        sutun = girdi.nextInt();



        MayinMetot mayin = new MayinMetot(satir ,sutun);
        mayin.run();

    }
}
