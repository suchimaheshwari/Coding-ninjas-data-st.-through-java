import java.util.Scanner;
public class Solution {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int V = s.nextInt();
        int E = s.nextInt();
        int[][] matrix=new int[V][V];
        for(int i=0;i<E;i++){
            int sv=s.nextInt();
            int ev=s.nextInt();
            int weight=s.nextInt();
            matrix[sv][ev]=weight;
            matrix[ev][sv]=weight;
        }      
        dijkstra(matrix);
    }
    public static void dijkstra(int[][] matrix)
    {
        boolean visited[]=new boolean[matrix.length];
        int distance[]=new int[matrix.length];
        distance[0]=0;
        for(int i=1;i<distance.length;i++){
            distance[i]=Integer.MAX_VALUE;
        }
        for(int i=0;i<matrix.length-1;i++)
        {
            int mindistancevertex=findmindistancevertex(distance,visited);
            visited[mindistancevertex]=true;
            for(int j=0;j<matrix.length;j++){
                if(matrix[mindistancevertex][j]!=0 && !visited[j] ){
                    if(distance[j]>distance[mindistancevertex]+matrix[mindistancevertex][j])
                    {
                        distance[j]=distance[mindistancevertex]+matrix[mindistancevertex][j];
                    }
                }
            }

        }

        for(int i=0;i<matrix.length;i++){
            System.out.println(i+" "+distance[i]);
        }

    }
    public static int findmindistancevertex(int[] distance,boolean[] visited){
        int minvertex=-1;
        for(int i=0;i<distance.length;i++){
            if(!visited[i] && (minvertex==-1 || distance[i]<distance[minvertex]))
                minvertex=i;
        }
        return minvertex;
    }
}
