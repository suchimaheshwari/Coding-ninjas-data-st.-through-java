public class solution 
{
    public static void mergeSort(int[] input)
    {

        if(input.length<=1)
            return;
        int mid=input.length/2;
        int[] part1=new int[mid];
        int[] part2=new int[input.length-mid];
        for(int i=0;i<mid;i++)
        {
            part1[i]=input[i];
        }
        int k=0;
        for(int i=mid;i<input.length;i++){
            part2[k]=input[i];
            k++;
        }
        mergeSort(part1);
        mergeSort(part2);
        merge(input,part1,part2);
    }
    private static void merge(int[] input,int part1[],int part2[]){

        int i=0,j=0,k=0;
        while(i<part1.length && j<part2.length){
            if(part1[i]<part2[j])
            {
                input[k]=part1[i];
                k++;
                i++;
            }
            else {
                input[k]=part2[j];
                k++;
                j++;
            }
        }
        while(i<part1.length)
        {
            input[k]=part1[i];
            k++;
            i++;
        }
        while(j<part2.length){
            input[k]=part2[j];
            k++;
            j++;
        }



    }
}
