import java.lang.reflect.Array;
import java.util.Arrays;
public class TekrarlıArray {
    static boolean isFind(int [] arr ,int value){
        for (int a : arr) {
           if (a == value)
            return true;
        }

        return false;
    }
    public static void main(String[] args) {
        int [] list = {31,2,5,9,2,14,6,31,9,6,7,28,39,28};
        int [] repeat = new int[list.length];
        int startİndex = 0;
        for (int a = 0;a < list.length;a++){
            for (int b = 0;b < list.length;b++){
                if (  (a != b) && (list[a] == list[b]) && (list[a]%2 == 0) ){
                       if (!isFind(repeat ,  list[a])){
                           repeat[startİndex++] = list[a];
                           break;
                       }

                }
            }
        }
        for (int value : repeat){
            if (value !=0){
                System.out.print( " " + value );
            }
        }
    }
}
