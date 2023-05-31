The hashCode() is a method of Java Integer Class which determines the hash code for a given Integer. 
It overrides hashCode in class Object. 
By default, this method returns a random integer that is unique for each instance. 

    public class IntegerHashCodeExample1 {  
        public static void main(String[] args)  
        {  
            //Create integer object  
            Integer i = new Integer("155");  
            //Returned hash code value for this object   
            int hashValue = i.hashCode();  
            System.out.println("Hash code Value for object is: " + hashValue);  
        }  
    }  
Output:
Hash code Value for object is: 155
------------------------------------------------------------------------------------------------------------------------------------------------------

    import java.util.Scanner;  
    public class IntegerHashCodeExample2 {  
        public static void main(String[] args) {  
          //Create integer object  
          System.out.print("Enter the desired input value: ");  
          Scanner readInput = new Scanner(System.in);         
            Integer i = readInput.nextInt();  
            readInput.close();  
            // Returned hash code value for this object   
            int hashValue = i.hashCode();  
            System.out.println("Hash code Value for object is: " + hashValue);  
            }  
    }  
Output:
1.	Enter the desired input value: 4343
Hash code Value for object is: 4343
2.	Enter the desired input value: abcd
Exception in thread "main" java.util.InputMismatchException
	at java.util.Scanner.throwFor(Scanner.java:864)
	at java.util.Scanner.next(Scanner.java:1485)
	at java.util.Scanner.nextInt(Scanner.java:2117)
	at java.util.Scanner.nextInt(Scanner.java:2076)
	at  myPackage.IntegerHashCodeExample1.main(IntegerHashCodeExample1.java:11)
------------------------------------------------------------------------------------------------------------------------------------------------------

    // Example of hashCode(int value)  
    public class IntegerHashCodeExample4 {  
        public static void main(String[] args)  
        {  
            int hashValue = Integer.hashCode(155);  
            System.out.println("Hash code Value for object is: " + hashValue);  
        }  
    }  
Output:
Hash code Value for object is: 155
------------------------------------------------------------------------------------------------------------------------------------------------------

    // Example of hashCode(int value)  
    import java.util.Scanner;  
    public class IntegerHashCodeExample5 {  
        public static void main(String[] args) {  
          //Create integer object  
          System.out.print("Enter the desired input value: ");  
          Scanner readInput = new Scanner(System.in);         
            Integer i = readInput.nextInt();  
            readInput.close();  
            // Returned hash code value for this object   
            int hashValue = Integer.hashCode(i);  
            System.out.println("Hash code Value for object is: " + hashValue);  
            }  
    }  
Output:
Enter the desired input value: 4569
Hash code Value for object is: 4569
