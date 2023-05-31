Synchronization in Java is the capability to control the access of multiple threads to any shared resource.

Java Synchronization is better option where we want to allow only one thread to access the shared resource.

Why use Synchronization?

The synchronization is mainly used to:
    To prevent thread interference.
    To prevent consistency problem.

Java Synchronized Method

    //example of java synchronized method  
    class Table{  
     synchronized void printTable(int n){//synchronized method  
       for(int i=1;i<=5;i++){  
         System.out.println(n*i);  
         try{  
          Thread.sleep(400);  
         }catch(Exception e){System.out.println(e);}  
       }  
      
     }  
    }  
      
    class MyThread1 extends Thread{  
    Table t;  
    MyThread1(Table t){  
    this.t=t;  
    }  
    public void run(){  
    t.printTable(5);  
    }  
      
    }  
    class MyThread2 extends Thread{  
    Table t;  
    MyThread2(Table t){  
    this.t=t;  
    }  
    public void run(){  
    t.printTable(100);  
    }  
    }  
      
    public class TestSynchronization2{  
    public static void main(String args[]){  
    Table obj = new Table();//only one object  
    MyThread1 t1=new MyThread1(obj);  
    MyThread2 t2=new MyThread2(obj);  
    t1.start();  
    t2.start();  
    }  
    }  
OUTPUT:
5
10
15
20
25
100
200
300
400
500

Example of synchronized method by using annonymous class

    //Program of synchronized method by using annonymous class  
    class Table{  
     synchronized void printTable(int n){//synchronized method  
       for(int i=1;i<=5;i++){  
         System.out.println(n*i);  
         try{  
          Thread.sleep(400);  
         }catch(Exception e){System.out.println(e);}  
       }  
      
     }  
    }  
      
    public class TestSynchronization3{  
    public static void main(String args[]){  
    final Table obj = new Table();//only one object  
      
    Thread t1=new Thread(){  
    public void run(){  
    obj.printTable(5);  
    }  
    };  
    Thread t2=new Thread(){  
    public void run(){  
    obj.printTable(100);  
    }  
    };  
      
    t1.start();  
    t2.start();  
    }  
    }  
OUTPUT:
5
10
15
20
25
100
200
300
400
500  


Synchronized Block in Java

Points to Remember
   Synchronized block is used to lock an object for any shared resource.
   Scope of synchronized block is smaller than the method.
   A Java synchronized block doesn't allow more than one JVM, to provide access control to a shared resource.
   The system performance may degrade because of the slower working of synchronized keyword.
   Java synchronized block is more efficient than Java synchronized method.
   
Synchronized Block Example Using Anonymous Class

    // A Sender class  
    class Sender   
    {   
      public void SenderMsg(String msg)  
      {   
        System.out.println("\nSending a Message: "  + msg);  
        try  
        {   
          Thread.sleep(800);   
        }   
        catch (Exception e)   
        {   
          System.out.println("Thread interrupted.");   
        }   
        System.out.println("\n" +msg+ "Sent");  
      }  
    }   
    // A Sender class for sending a message using Threads   
    class SenderWThreads extends Thread   
    {   
      private String msg;   
      Sender sd;   
      
      // Receiver method to receive a message object and a message to be sent   
      SenderWThreads(String m, Sender obj)  
      {   
        msg = m;  
        sd = obj;   
      }   
      
      public void run()   
      {   
        // Checks that only one thread sends a message at a time.   
        synchronized(sd)   
        {   
          // synchronizing the sender object   
          sd.SenderMsg(msg);  
        }   
      }   
    }   
    // Driver Code   
    public class ShynchronizedMultithreading  
    {   
      public static void main(String args[])   
      {   
        Sender sender = new Sender();   
        SenderWThreads sender1 = new SenderWThreads( "Hola " , sender);  
    SenderWThreads sender2 =  new SenderWThreads( "Welcome to Javatpoint website ", sender);  
      
        // Start two threads of SenderWThreads type   
        sender1.start();   
        sender2.start();   
      
        // wait for threads to end   
        try  
        {   
          sender1.join();   
          sender2.join();   
        }   
        catch(Exception e)   
        {   
          System.out.println("Interrupted");   
        }   
      }   
    }  
Output:
Sending a Message: Hola 
Hola Sent
Sending a Message: Welcome to Javatpoint website 
Welcome to Javatpoint website Sent
   
       
