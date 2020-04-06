import java.util.Scanner;
import java.util.Arrays;
 class Edge implements Comparable<Edge>{
    int source;
    int destination;
    int weight;
    public int compareTo(Edge o){
        return this.weight-o.weight;
        // if(this.weight>o.weight)
        //     return 1;
        // else if(this.weight<o.weight)
        //     return -1;
        // else
        //     return 0;
    }
}
public class Solution {
    public static void kruskals(Edge input[],int V){
        Arrays.sort(input);
        int count=0;
        int k=0;
        Edge output[]=new Edge[V-1];
        int parent[]=new int[V];
        for(int j=0;j<V;j++){
            parent[j]=j;
        }
        while(count!=V-1){
            Edge currentEdge=input[k];
            int sourceparent=parentcall(parent,currentEdge.source);
            int destinationparent=parentcall(parent,currentEdge.destination);
            if(sourceparent!=destinationparent)
            {
                output[count]=currentEdge;
                count++;
                parent[sourceparent]=destinationparent;
            }
            k++;
        }
        for(int i=0;i<V-1;i++){
            if(output[i].source<=output[i].destination)
                System.out.println(output[i].source+" "+output[i].destination+" "+output[i].weight);
            else
                System.out.println(output[i].destination+" "+output[i].source+" "+output[i].weight);
        }
    }
        public static int parentcall(int[] parent,int vertex){
            if(vertex==parent[vertex])
                return  vertex;
            return parentcall(parent,parent[vertex]);
        }








        
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int V = s.nextInt();
        int E = s.nextInt();
        Edge input[]=new Edge[E];
        for(int i=0;i<input.length;i++){
            input[i]= new Edge();
            input[i].source=s.nextInt();
            input[i].destination=s.nextInt();
            input[i].weight=s.nextInt();
        }
        kruskals(input,V);
    }}
