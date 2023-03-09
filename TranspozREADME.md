public class Transpoz {
    public static void main(String[] args) {
        int [][] liste = {{1,2,3},{4,5,6},{7,8,9}};
        int [][] dizi = new int[3][3];
        for (int a = 0;a < 3;a++){
            for (int b = 0;b <3;b++){
                System.out.print(liste[a][b] + " ");
            }
            System.out.println();
            
        }
        System.out.println("-----------");
        for (int a = 0;a < 3;a++){
            for (int b = 0;b <3;b++){
                dizi [a][b] = liste [b][a];
                System.out.print(dizi [a][b] + " ");
            }
            System.out.println();
        }

    }
}
