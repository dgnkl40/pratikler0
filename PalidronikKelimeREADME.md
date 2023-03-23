public class PalidronikKelime {
   static boolean isPalidronik(String klm){
       int a = 0;
       int b = klm.length() - 1;
       while(a < b){
           if (klm.charAt(a) == klm.charAt(b)){
               return true;
           }
           a++;
           b--;
       }

   
      return false;
   }
    public static void main(String[] args) {
        System.out.println(isPalidronik());
    }
}
