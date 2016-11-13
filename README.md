# swapDigitPairs
package q8;

import java.util.Scanner;
public class Q8 {

    public static void main(String[] args) throws Exception {
    System.out.println(swapDigitPairs(482596));
    System.out.println(swapDigitPairs(1234567));
    System.out.println(swapDigitPairs(12));
    System.out.println(swapDigitPairs(1));
    System.out.println(swapDigitPairs(0));
}
   
public static int swapDigitPairs(int number) {
    int result = 0;
    int place = 1;
    while (number > 9) {
        result += place * 10 * (number % 10);
        number /= 10;
        result += place * (number % 10);
        number /= 10;
        place *= 100;
    }
    return result + place * number;
}}
