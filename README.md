# Linear_Searching

import java.util.Random;
import java.util.random.*;

public class LinearSearching {
    public static void main(String[] args){
        int num [] = LinearSearching.addElements();
        System.out.println(num);
        System.out.println(LinearSearching.MAX(num));;
    }
    public static int[] addElements(){
        int num [] = new int [Integer.MAX_VALUE/5];
        Random rnd = new Random();
        int val = 0;
        for (int i = 0; i < num.length; i++){
            val = rnd.nextInt(num.length-1)+1;
            num [i] = val;
        }
        return num;
    }
    public static int MAX(int num[]){
        long start = System.nanoTime();
        int highest = 0;
        for (int i = 0; i < num.length; i++){
            if (num [i]> highest){
                highest = num[i];
            }
        }
        long end = System.nanoTime();
        System.out.println("Jakob Maraguinot");
        System.out.println("Processing timeL "+(end-start)+ " Units");
        return highest;
    }      
}
