import java.util.LinkedList; 
import java.util.Scanner;
import java.util.Queue;
// import java.io.*; 
import java.util.*; 
public class Solution{
	public static void help(int edges[][],boolean visited[],ArrayList<Integer> arr,int start){  
        visited[start]=true;
        arr.add(start);
        int n=edges.length;   
          for(int j=0;j<n;j++){
              if(edges[start][j]==1&&!visited[j]){
                 help(edges,visited,arr,j); 
              }
          }
    }
    public static void helpp(int edges[][]){
        boolean visited[]=new boolean[edges.length];
        for(int i=0;i<edges.length;i++){
          if(!visited[i]){
              // this array list is creating again and again
             ArrayList<Integer> arrans= new ArrayList<Integer>();
             help(edges,visited,arrans,i);
             Collections.sort(arrans);
             for(int j=0;j<arrans.size();j++)
                System.out.print(arrans.get(j)+" ");   
                System.out.println();
          }
        }
    }
    public static void main(String[] args){
		Scanner s = new Scanner(System.in);
		int n = s.nextInt();
        // total number of edges e
		int e = s.nextInt();
        int edges[][]=new int[n][n];
        for(int i=0;i<e;i++){
            int fv=s.nextInt();
            int sv=s.nextInt();
            edges[fv][sv]=1;
            edges[sv][fv]=1;
        }
        helpp(edges);
    }
}
