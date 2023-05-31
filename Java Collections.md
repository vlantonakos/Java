The Collection in Java is a framework that provides an architecture to store and manipulate the group of objects.

Java Collections can achieve all the operations that you perform on a data such as searching, sorting, insertion, manipulation, and deletion.

Java Collection means a single unit of objects. Java Collection framework provides many interfaces (Set, List, Queue, Deque) and classes (ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet).

![image](https://github.com/vlantonakos/Java/assets/107072477/d538e6f2-4422-42ec-97c3-a4761d618ff8)

--------------------------------------------------------------------------------------------------------------------
List Interface

List interface is the child interface of Collection interface. It inhibits a list type data structure in which we can store the ordered collection of objects. It can have duplicate values.

List interface is implemented by the classes ArrayList, LinkedList, Vector, and Stack.

To instantiate the List interface, we must use :

    List <data-type> list1= new ArrayList();  
    List <data-type> list2 = new LinkedList();  
    List <data-type> list3 = new Vector();  
    List <data-type> list4 = new Stack();  


ArrayList

The ArrayList class implements the List interface. It uses a dynamic array to store the duplicate element of different data types. The ArrayList class maintains the insertion order and is non-synchronized. The elements stored in the ArrayList class can be randomly accessed.

    import java.util.*;  
    class TestJavaCollection1{  
    public static void main(String args[]){  
    ArrayList<String> list=new ArrayList<String>();//Creating arraylist  
    list.add("Ravi");//Adding object in arraylist  
    list.add("Vijay");  
    list.add("Ravi");  
    list.add("Ajay");  
    //Traversing list through Iterator  
    Iterator itr=list.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ravi
Vijay
Ravi
Ajay


LinkedList

LinkedList implements the Collection interface. It uses a doubly linked list internally to store the elements. It can store the duplicate elements. It maintains the insertion order and is not synchronized. In LinkedList, the manipulation is fast because no shifting is required.
    
    import java.util.*;  
    public class TestJavaCollection2{  
    public static void main(String args[]){  
    LinkedList<String> al=new LinkedList<String>();  
    al.add("Ravi");  
    al.add("Vijay");  
    al.add("Ravi");  
    al.add("Ajay");  
    Iterator<String> itr=al.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ravi
Vijay
Ravi
Ajay


Vector

Vector uses a dynamic array to store the data elements. It is similar to ArrayList. However, It is synchronized and contains many methods that are not the part of Collection framework.

Consider the following example.

    import java.util.*;  
    public class TestJavaCollection3{  
    public static void main(String args[]){  
    Vector<String> v=new Vector<String>();  
    v.add("Ayush");  
    v.add("Amit");  
    v.add("Ashish");  
    v.add("Garima");  
    Iterator<String> itr=v.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ayush
Amit
Ashish
Garima


Stack

The stack is the subclass of Vector. It implements the last-in-first-out data structure, i.e., Stack. The stack contains all of the methods of Vector class and also provides its methods like boolean push(), boolean peek(), boolean push(object o), which defines its properties.

Consider the following example.

    import java.util.*;  
    public class TestJavaCollection4{  
    public static void main(String args[]){  
    Stack<String> stack = new Stack<String>();  
    stack.push("Ayush");  
    stack.push("Garvit");  
    stack.push("Amit");  
    stack.push("Ashish");  
    stack.push("Garima");  
    stack.pop();  
    Iterator<String> itr=stack.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ayush
Garvit
Amit
Ashish


--------------------------------------------------------------------------------------------------------------------
Set Interface

Set Interface in Java is present in java.util package. It extends the Collection interface. It represents the unordered set of elements which doesn't allow us to store the duplicate items. We can store at most one null value in Set. Set is implemented by HashSet, LinkedHashSet, and TreeSet.

Set can be instantiated as:

    Set<data-type> s1 = new HashSet<data-type>();  
    Set<data-type> s2 = new LinkedHashSet<data-type>();  
    Set<data-type> s3 = new TreeSet<data-type>();  
    

HashSet

HashSet class implements Set Interface. It represents the collection that uses a hash table for storage. Hashing is used to store the elements in the HashSet. It contains unique items.

    import java.util.*;  
    public class TestJavaCollection7{  
    public static void main(String args[]){  
    //Creating HashSet and adding elements  
    HashSet<String> set=new HashSet<String>();  
    set.add("Ravi");  
    set.add("Vijay");  
    set.add("Ravi");  
    set.add("Ajay");  
    //Traversing elements  
    Iterator<String> itr=set.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Vijay
Ravi
Ajay


LinkedHashSet

LinkedHashSet class represents the LinkedList implementation of Set Interface. It extends the HashSet class and implements Set interface. Like HashSet, It also contains unique elements. It maintains the insertion order and permits null elements.

    import java.util.*;  
    public class TestJavaCollection8{  
    public static void main(String args[]){  
    LinkedHashSet<String> set=new LinkedHashSet<String>();  
    set.add("Ravi");  
    set.add("Vijay");  
    set.add("Ravi");  
    set.add("Ajay");  
    Iterator<String> itr=set.iterator();  
    while(itr.hasNext()){  
    System.out.println(itr.next());  
    }  
    }  
    }  
Output:
Ravi
Vijay
Ajay


--------------------------------------------------------------------------------------------------------------------
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
