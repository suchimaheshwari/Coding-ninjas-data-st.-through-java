import java.util.ArrayList;
import java.util.*;
import java.lang.*;
class TrieNode{

	char data;
	boolean isTerminating;
	TrieNode children[];
	int childCount;

	public TrieNode(char data) {
		this.data = data;
		isTerminating = false;
		children = new TrieNode[26];
		childCount = 0;
	}
}

public class Trie {

	private TrieNode root;
	public int count;
	public Trie() {
		root = new TrieNode('\0');
	}
	private void add(TrieNode root, String word){
		if(word.length() == 0){
			if (!root.isTerminating) {
				root.isTerminating = true;
				return;
			}
            else 
                return;
		}		
		int childIndex = word.charAt(0) - 'a';
		TrieNode child = root.children[childIndex];
		if(child == null){
			child = new TrieNode(word.charAt(0));
			root.children[childIndex] = child;
			root.childCount++;
		}
		add(child, word.substring(1));
	}

	public void add(String word)
    {
		add(root,word);
	}

	public boolean findPalindromePair(ArrayList<String> vect)
    {
        ArrayList<String> s=new ArrayList<>();
	for(int i=0;i<vect.size();i++)
    {
        String st=vect.get(i);
         add(st);
        String str=reverse(st);
        s.add(str);
    }
        for(int i=0;i<s.size();i++)
        {
           boolean b=search(root,s.get(i));
            if(b==true)
                return true;
        }
        return false;
	}
     public boolean search(TrieNode root,String word)
    {
    if(word.length()==0)
    {
        return true;
    }
        int ci=word.charAt(0)-'a';
        TrieNode chld=root.children[ci];
        if(chld==null)
            return false;
        return search(chld,word.substring(1));
    }
    private String reverse(String i){
        String newstr = "";
        while (i.length() != 0){
            newstr = i.charAt(0) + newstr;
            i = i.substring(1);
        }
        //System.out.println(newstr);
        return newstr;
    }
}
