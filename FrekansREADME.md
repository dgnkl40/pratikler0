import java.util.Arrays;

public class Frekans {
public static void main(String[] args) {
        int [] list = {98,2,4,5,88,7,66,4,7,99,99,7,4,88};
        int [] repeat = new int [list.length];
        int bas = 1 ;
        Arrays.sort(list);
        System.out.println(Arrays.toString(list));
        for (int a = 0;a < list.length;a++){
            for (int b = 0;b < list.length;b++){
                if ((a != b) && (list[a] == list[b])){
                    if (b<a){
                        break;
                    }
                    bas++;
                }
            }
            if (bas > 1){
                System.out.println(list[a] +" sayısı " + bas + " kere yazılmıştır.");
                bas = 1;
            }
        }

    }
}
