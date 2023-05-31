TreeSet provides an implementation of the Set interface that uses a tree for storage. 
Objects are stored in a sorted and ascending order.

```  import java.util.*;
public class TreeSetDemo {

   public static void main(String args[]) {
      // Create a tree set
      TreeSet ts = new TreeSet();
     
      // Add elements to the tree set
      ts.add("C");
      ts.add("A");
      ts.add("B");
      ts.add("E");
      ts.add("F");
      ts.add("D");
      System.out.println(ts);
   }
}
```
Output
[A, B, C, D, E, F]

