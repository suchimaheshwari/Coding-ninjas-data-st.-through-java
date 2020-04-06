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
        boolean ans=hasPath(edges,V1,V2,visited);
        System.out.println(ans);
    }
    public static boolean hasPath(int[][] edges,int V1, int V2,boolean visited[]){
        if(edges[V1][V2]==1)
            return true;
        Queue<Integer> q=new LinkedList<>();
        q.add(V1);
        visited[V1]=true;
        while(!q.isEmpty()){
            int n=q.remove();
            for(int i=0;i<edges.length;i++)
            {
             if(edges[n][i]==1 && !visited[i])
             {
                 q.add(i);
                 visited[i]=true;
             }
            }
        }
        if(visited[V2]==true)
            return true;
        else
            return false;
    }
}
