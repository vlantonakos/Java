A map contains values on the basis of key, i.e. key and value pair. Each key and value pair is known as an entry. A Map contains unique keys.

A Map is useful if you have to search, update or delete elements on the basis of a key.
Java Map Hierarchy

There are two interfaces for implementing Map in java: Map and SortedMap, and three classes: HashMap, LinkedHashMap, and TreeMap. The hierarchy of Java Map is given below:
![image](https://github.com/vlantonakos/Java/assets/107072477/de6ae3cd-cea2-4d7f-9209-375e696543e3)

Class	          Description

HashMap	        HashMap is the implementation of Map, but it doesn't maintain any order.
LinkedHashMap	  LinkedHashMap is the implementation of Map. It inherits HashMap class. It maintains insertion order.
TreeMap	        TreeMap is the implementation of Map and SortedMap. It maintains ascending order.

Java Map Example: Generic (New Style)

    import java.util.*;  
    class MapExample2{  
     public static void main(String args[]){  
      Map<Integer,String> map=new HashMap<Integer,String>();  
      map.put(100,"Amit");  
      map.put(101,"Vijay");  
      map.put(102,"Rahul");  
      //Elements can traverse in any order  
      for(Map.Entry m:map.entrySet()){  
       System.out.println(m.getKey()+" "+m.getValue());  
      }  
     }  
    }  
OUTPUT:
102 Rahul
100 Amit
101 Vijay

Java Map Example: comparingByKey()

    import java.util.*;  
    class MapExample3{  
     public static void main(String args[]){  
    Map<Integer,String> map=new HashMap<Integer,String>();          
          map.put(100,"Amit");    
          map.put(101,"Vijay");    
          map.put(102,"Rahul");   
          //Returns a Set view of the mappings contained in this map        
          map.entrySet()  
          //Returns a sequential Stream with this collection as its source  
          .stream()  
          //Sorted according to the provided Comparator  
          .sorted(Map.Entry.comparingByKey())  
          //Performs an action for each element of this stream  
          .forEach(System.out::println);  
     }  
    }  
OUTPUT:
100=Amit
101=Vijay
102=Rahul

Java Map Example: comparingByValue()

    import java.util.*;  
    class MapExample5{  
     public static void main(String args[]){  
    Map<Integer,String> map=new HashMap<Integer,String>();          
          map.put(100,"Amit");    
          map.put(101,"Vijay");    
          map.put(102,"Rahul");    
          //Returns a Set view of the mappings contained in this map    
          map.entrySet()  
          //Returns a sequential Stream with this collection as its source  
          .stream()  
          //Sorted according to the provided Comparator  
          .sorted(Map.Entry.comparingByValue())  
          //Performs an action for each element of this stream  
          .forEach(System.out::println);  
     }  
    }  
OUTPUT:
100=Amit
102=Rahul
101=Vijay
