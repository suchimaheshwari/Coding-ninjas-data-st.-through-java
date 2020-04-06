public class solution {
    public static void printKeypad(int input){
        printKeypad(input,"");}

    public static void printKeypad(int input,String output){
        if(input==0)
        {   System.out.println(output);
         return;
        }
        int rem=input%10;

        char helperArray[]=helper(rem);


        printKeypad(input/10,helperArray[0]+output);
        printKeypad(input/10,helperArray[1]+output);
        printKeypad(input/10,helperArray[2]+output);

        if(helperArray.length==4){
            printKeypad(input/10,helperArray[3]+output);
        }





    }
    public static char[] helper(int n){
        if(n==2)
        {
            char []ch={'a','b','c'};

            return ch;
        }
        else if(n==3)
        {
            char ch[]={'d','e','f'};
            return ch;
        } 
        else if(n==4)
        {
            char ch[]={'g','h','i'};
            return ch;
        }  else if(n==5)
        {
            char ch[]={'j','k','l'};
            return ch;
        }  else if(n==6)
        {
            char ch[]={'m','n','o'};
            return ch;
        }  else if(n==7)
        {
            char ch[]={'p','q','r','s'};
            return ch;
        }  else if(n==8)
        {
            char ch[]={'t','u','v'};
            return ch;
        }  else if(n==9)
        {
            char ch[]={'w','x','y','z'};
            return ch;
        } 
        else 
        {
            char ch[]={' '};
            return ch;
            //  return new char[0];
        }    

    }	
}
