package miclat;

import java.util.Scanner;

public class HexToBin {

    static final Scanner _scan = new Scanner(System.in);

    public static int HexToDec(String hexadecimalNumber) {
        String hexadecimals = "0123456789ABCDEF";
        boolean isHex = hexadecimals.contains(hexadecimalNumber);
        if (isHex) {
            return hexadecimals.indexOf(hexadecimalNumber);
        } else {
            return -1;
        }
    }
    public static String DecToBin(int input) {
        int _i = input;
        String s;
        String zeroes = "000";
        String output = "";
        int q;
        int r;
        while (_i != 0) {
            q = _i/2;
            r = _i%2;
            s = String.valueOf(r);
            output = s.concat(output);
            _i = q;
        }
        output = zeroes + output;
        boolean binLenIs4 = output.length() == 4;
        if (binLenIs4)
            return output;
        else
            return output.substring(output.length()-4);
    }

    public static void main(String[] args) {
        System.out.println("This program converts a hexadecimal digit into a four digit binary number.");
        System.out.print("Enter Hexadecimal digit: ");
        String s = _scan.nextLine();
        int dec = HexToDec(s);
        if (dec < 0) {
            System.out.format("%n%s is not a valid hexadecimal digit.%nGoodbye.", s);
        } else {
            System.out.format("%nThe binary value for %s is %s.%nGoodbye.", s, DecToBin(dec));
        }
    }
}