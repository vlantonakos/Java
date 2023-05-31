SortedSet Interface

SortedSet is the alternate of Set interface that provides a total ordering on its elements. The elements of the SortedSet are arranged in the increasing (ascending) order. The SortedSet provides the additional methods that inhibit the natural ordering of the elements.

The SortedSet can be instantiated as:

    SortedSet<data-type> set = new TreeSet();  

TreeSet

Java TreeSet class implements the Set interface that uses a tree for storage. Like HashSet, TreeSet also contains unique elements. However, the access and retrieval time of TreeSet is quite fast. The elements in TreeSet stored in ascending order.

    import java.util.*;  
    public class TestJavaCollection9{  
    public static void main(String args[]){  
    //Creating and adding elements  
    TreeSet<String> set=new TreeSet<String>();  
    set.add("Ravi");  
    set.add("Vijay");  
    set.add("Ravi");  
    set.add("Ajay");  
    //traversing elements  
    Iterator<String> itr=set.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ajay
Ravi
Vijay
