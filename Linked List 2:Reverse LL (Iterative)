public class Solution 
{
    public static LinkedListNode<Integer> reverse_I(LinkedListNode<Integer> head) 
    {
    LinkedListNode<Integer> prev=null,curr=head,temp;
        while(curr!=null)
        {
            temp=curr.next;
            curr.next=prev;
            prev=curr;
            curr=temp;
        }
        return prev;





    }
}
