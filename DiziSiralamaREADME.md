import java.util.Scanner;
import java.util.Arrays;
public class DiziSırala {
    static void dizi(int[] list ){
        int mtt =0 ;
        for (int i = 0 ; i < list.length;i++){
            for (int j =  0 ; j< list.length;j++){
                if (i!=j && list[i]<list[j]){
                    mtt = list[i];
                    list[i] = list[j];
                    list[j] = mtt;
                }
            }
        }
        for (int i : list){
            System.out.print(i + " ");
        }
    }
    public static void main(String[] args) {
        Scanner girdi = new Scanner(System.in);
        System.out.print("Dizinin Boyutu N: ");
        int n = girdi.nextInt();
        int [] list = new int[n];
        for (int i =0; i < list.length;i++){
            System.out.print((i+1)+". Eleman:");
            int a = girdi.nextInt();
            list[i]=a;
        }
        dizi(list);
        }
}




