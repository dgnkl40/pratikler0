public class CokBoyutluArray {
    public static void main(String[] args) {
        String [][] letter = new String[7][4];
        for (int s = 0;s< letter.length;s++){
            for (int k = 0;k <letter[s].length;k++){
                if (s == 0 || s  == 3 || s == 6){
                    letter[s][k] = " * ";
                } else if ((k ==0) || k == 3 ){
                    letter[s][k]= " * ";}
                else {
                    letter[s][k]= "   ";
                }
            }

}
        for(String[] row:letter){
            for (String col:row){
                System.out.print(col);
            }
            System.out.println();

        }
    }
}
