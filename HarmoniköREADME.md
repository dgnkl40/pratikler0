public class Harmonikö {
    public static void main(String[] args) {
        int [] list = {1,2,3,4,5,6};
        double sum = 0.0;
        double avarege =0.0;
        int i;
        for ( i = 0;i < list.length;i++){

            sum += (1.0/list[i]);

        }System.out.println(sum/list.length);

    }
}
