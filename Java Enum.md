Java Enums

The Enum in Java is a data type which contains a fixed set of constants. 

Points to remember for Java Enum

   Enum improves type safety
   Enum can be easily used in switch
   Enum can be traversed
   Enum can have fields, constructors and methods
   Enum may implement many interfaces but cannot extend any class because it internally extends Enum class
   
Java Enum Example: Defined inside class

    class EnumExample3{  
    enum Season { WINTER, SPRING, SUMMER, FALL; }//semicolon(;) is optional here  
    public static void main(String[] args) {  
    Season s=Season.WINTER;//enum type is required to access WINTER  
    System.out.println(s);  
    }}  
Output:
WINTER
        

    class EnumExample1{  
    //defining enum within class  
    public enum Season { WINTER, SPRING, SUMMER, FALL }  
    //creating the main method  
    public static void main(String[] args) {  
    //printing all enum  
    for (Season s : Season.values()){  
    System.out.println(s);  
    }  
    System.out.println("Value of WINTER is: "+Season.valueOf("WINTER"));  
    System.out.println("Index of WINTER is: "+Season.valueOf("WINTER").ordinal());  
    System.out.println("Index of SUMMER is: "+Season.valueOf("SUMMER").ordinal());  
      
    }}  
Output:
WINTER
SPRING
SUMMER
FALL
Value of WINTER is: WINTER
Index of WINTER is: 0
Index of SUMMER is: 2
    
