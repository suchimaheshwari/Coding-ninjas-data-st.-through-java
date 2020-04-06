
public class Solution {

    public static LinkedListNode<Integer> mergeSort(LinkedListNode<Integer> head) {
        if(head==null)
            return head;
        if(head.next==null)
            return head;
        LinkedListNode<Integer> midNode=findmid(head);
        LinkedListNode<Integer> h2=midNode.next;
        midNode.next=null;
        LinkedListNode<Integer> part1=mergeSort(head);
        LinkedListNode<Integer> part2=mergeSort(h2);
        LinkedListNode<Integer> mergedList=mergeTwoList(part1,part2);
        return mergedList;
        
        }
    private static LinkedListNode<Integer> findmid(LinkedListNode<Integer> head) 
    {
        if(head==null)
            return head;
        LinkedListNode<Integer> slow=head,fast=head;
        while(fast.next!=null && fast.next.next!=null){
            slow=slow.next;
            fast=fast.next.next;
        }
        return slow;
    }
    public static LinkedListNode<Integer> mergeTwoList(LinkedListNode<Integer> head1, LinkedListNode<Integer> head2) {
        if(head1==null)
            return head2;
        if(head2==null)
            return head1;
        LinkedListNode<Integer> t1=head1,t2=head2,tail=null,head=null;
        if(t1.data<=t2.data)
        {
            head=t1;
            tail=t1;
            t1=t1.next;
        }
        else
        {
            head=t2;
            tail=t2;
            t2=t2.next;
        }
        while(t1!=null &&t2!=null)
        {
            if(t1.data<=t2.data)
            {
                tail.next=t1;
                tail=t1;
                t1=t1.next;
            }
            else
            {
                tail.next=t2;
                tail=tail.next;
                t2=t2.next;
            }
        }
        if(t1==null)
            tail.next=t2;
        if(t2==null)
            tail.next=t1;
        return head;

    }

}
