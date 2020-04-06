public class solution {
    public static int binarySearch(int input[], int element) {
        return helper(input,element,0,input.length-1);
    }
    private static int helper(int input[],int element,int si,int ei)
    { 
        if(si>ei)
            return -1;

        int mid=(si+ei)/2 ;
        if(element==input[mid])
            return mid;
        else if(element<input[mid])
            return helper(input,element,si,mid-1);
        else         
            return helper(input,element,mid+1,ei);



    }
}
