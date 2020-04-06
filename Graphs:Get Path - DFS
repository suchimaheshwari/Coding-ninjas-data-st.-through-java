import java.util.Scanner;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int V = s.nextInt();
        int E = s.nextInt();
        int edges[][]=new int[V][V];
        for(int i=0;i<E;i++){
            int sv=s.nextInt();
            int ev=s.nextInt();
            edges[sv][ev]=1;
            edges[ev][sv]=1;
        }
        int V1=s.nextInt();
        int V2=s.nextInt();
        boolean visited[]=new boolean[V];
        ArrayList<Integer> ans=getPathDFS(edges,visited,V1,V2);
        if(ans!=null){
        for(int elem:ans)
        {
            System.out.print(elem+" ");
        }
    }
    }
    public static ArrayList<Integer> getPathDFS(int[][] edges,boolean[] visited,int V1,int V2){
        if(V1==V2)
        {
            ArrayList<Integer> ans=new ArrayList<>();
            visited[V1]=true;
            ans.add(V1);
            return ans;
        }
        visited[V1]=true;
        for(int i=0;i<edges.length;i++)
        {
            if(edges[V1][i]==1 && !visited[i])
            { 
                ArrayList<Integer> arr=getPathDFS(edges,visited,i,V2); 
                if(arr!=null)
                {
                    arr.add(V1);

                    return arr;
                }
            }
        }
        return null;
    }
}
