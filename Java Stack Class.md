The stack is a linear data structure that is used to store the collection of objects. 
It is based on Last-In-First-Out (LIFO). 
Java collection framework provides many interfaces and classes to store the collection of objects. 
One of them is the Stack class that provides different operations such as push, pop, search, etc.

In Java, Stack is a class that falls under the Collection framework that extends the Vector class. 
It also implements interfaces List, Collection, Iterable, Cloneable, Serializable. 
It represents the LIFO stack of objects. Before using the Stack class, we must import the java.util package. 
The stack class arranged in the Collections framework hierarchy, as shown below.

![image](https://github.com/vlantonakos/Java/assets/107072477/eb3aa10e-39be-4cee-b3eb-658295ea5bac)
![image](https://github.com/vlantonakos/Java/assets/107072477/a76bb53c-9abe-45cc-94e6-6c9be4f661c3)
![image](https://github.com/vlantonakos/Java/assets/107072477/06fb2ff6-f5b9-4da3-b84f-5eb436f89a6c)

![image](https://github.com/vlantonakos/Java/assets/107072477/c5a86aa4-f520-4c2f-ae40-9ad7f167fd62)

    import java.util.Stack;  
    public class StackSizeExample   
    {    
    public static void main (String[] args)   
    {   
    Stack stk = new Stack();  
    stk.push(22);  
    stk.push(33);  
    stk.push(44);  
    stk.push(55);  
    stk.push(66);  
    // Checks the Stack is empty or not  
    boolean rslt=stk.empty();  
    System.out.println("Is the stack empty or not? " +rslt);  
    // Find the size of the Stack  
    int x=stk.size();  
    System.out.println("The stack size is: "+x);  
    }  
    }  
Output:
Is the stack empty or not? false
The stack size is: 5


Iterate Elements

Iterate means to fetch the elements of the stack. We can fetch elements of the stack using three different methods are as follows:
    Using iterator() Method
    
    import java.util.Iterator;  
    import java.util.Stack;  
    public class StackIterationExample1   
    {     
    public static void main (String[] args)   
    {   
    //creating an object of Stack class  
    Stack stk = new Stack();  
    //pushing elements into stack  
    stk.push("BMW");  
    stk.push("Audi");  
    stk.push("Ferrari");  
    stk.push("Bugatti");  
    stk.push("Jaguar");  
    //iteration over the stack  
    Iterator iterator = stk.iterator();  
    while(iterator.hasNext())  
    {  
    Object values = iterator.next();  
    System.out.println(values);   
    }     
    }  
    }  
    
    Using forEach() Method
    Using listIterator() Method
Output:
BMW
Audi
Ferrari
Bugatti
Jaguar


   Using the forEach() Method
   
    import java.util.*;  
    public class StackIterationExample2  
    {  
    public static void main (String[] args)   
    {   
    //creating an instance of Stack class  
    Stack <Integer> stk = new Stack<>();  
    //pushing elements into stack  
    stk.push(119);  
    stk.push(203);  
    stk.push(988);  
    System.out.println("Iteration over the stack using forEach() Method:");  
    //invoking forEach() method for iteration over the stack  
    stk.forEach(n ->  
    {  
    System.out.println(n);  
    });  
    }  
    }  
Output:
Iteration over the stack using forEach() Method:
119
203
988

     
   Using listIterator() Method
   
    import java.util.Iterator;  
    import java.util.ListIterator;  
    import java.util.Stack;  
       
    public class StackIterationExample3  
    {  
    public static void main (String[] args)   
    {   
    Stack <Integer> stk = new Stack<>();  
    stk.push(119);  
    stk.push(203);  
    stk.push(988);  
    ListIterator<Integer> ListIterator = stk.listIterator(stk.size());  
    System.out.println("Iteration over the Stack from top to bottom:");  
    while (ListIterator.hasPrevious())   
    {  
    Integer avg = ListIterator.previous();  
    System.out.println(avg);  
    }  
    }  
    }  
Output:
Iteration over the Stack from top to bottom:
988
203
119  
    
