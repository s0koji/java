java
====
import java.util.Scanner;
class pr1 {
	public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int s = 0;
        String m = in.nextLine();
        int lee[] = new int[m.length()];
           for(int i = m.length(); i>0; i--) {
                 lee[i-1] = Integer.parseInt(""+ m.charAt(i-1));
                    if(lee[i-1] != 0 && lee[i-1] != 1) {
                        System.out.println("Введённое число не двоичной");
                        return;
                    }
                 s = (int) (Math.pow(2, m.length() - i))*lee[i-1] + s;
           }
         System.out.println("Двоичное : " + m);
         System.out.println("Десятичное: " + s);

    }
}
