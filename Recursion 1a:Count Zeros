public class solution {
    public static int countZerosRec(int input){
        if(input<10){
            if(input==0)
            return 1;
        else
            return 0;
        }
        int smallAns= countZerosRec(input/10);
        if(input%10==0)
            smallAns=1+smallAns;
        return smallAns;
        }
}
