public class Solution
{
    public static LinkedListNode<Integer> removeDuplicates(LinkedListNode<Integer> head)
    {
        if(head==null)
            return head;
        if(head.next==null)
            return head;
        LinkedListNode<Integer> t1=head,t2=head.next;
        LinkedListNode<Integer> finalhead=head;
        while(t2!=null){
            if(t1.data.equals(t2.data))
            {
                t2=t2.next; 
            }
            else{
                t1.next=t2;
                t1=t2;
            }
        }

        t1.next=null;
        return finalhead;
    }
}
