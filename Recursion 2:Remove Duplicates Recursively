public class Solution {
    public static String removeConsecutiveDuplicates(String s) {
        if(s.length()<=1)
            return s;
        String smallans=removeConsecutiveDuplicates(s.substring(1));
        if(smallans.charAt(0)==s.charAt(0))
            return smallans;
        else
            return s.charAt(0)+smallans;

    }

}
