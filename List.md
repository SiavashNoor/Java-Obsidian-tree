## List Interface

List interface is the child interface of Collection interface. It inhibits a list type data structure in which we can store the ordered collection of objects. It can have duplicate values.

List interface is implemented by the classes ArrayList, LinkedList, Vector, and Stack.
```java
1.  List <data-type> list1= new ArrayList();  
2.  List <data-type> list2 = new LinkedList();  
3.  List <data-type> list3 = new Vector();  
4.  List <data-type> list4 = new Stack();
```

There are various methods in List interface that can be used to insert, delete, and access the elements from the list.



The classes that implement the List interface are given below:::::
- [[ArrayList]]
- [[LinkedList]]
- [[Vector]]
- [[Stack]]

Important:   The ArrayList and LinkedList are widely used in Java programming. The Vector class is deprecated since Java 5.
```java
-   //Creating a List of type String using ArrayList  
-   List<String> list=new ArrayList<String>();  

-   //Creating a List of type Integer using ArrayList  
-   List<Integer> list=new ArrayList<Integer>();  

-   //Creating a List of type Book using ArrayList  
-   List<Book> list=new ArrayList<Book>();  

-   //Creating a List of type String using LinkedList  
-   List<String> list=new LinkedList<String>();
```


### How to Sort List

There are various ways to sort the List, here we are going to use Collections.sort() method to sort the list element. The _java.util_ package provides a utility class **Collections** which has the static method sort(). Using the **Collections.sort()** method, we can easily sort any List.


### Java List Iterator  interface

ListIterator Interface is used to traverse the element in a backward and forward direction.

```java
  import java.util.*;  
  public class ListIteratorExample1{  
  public static void main(String args[]){  
   List<String> al=new ArrayList<String>();    
           al.add("Amit");    
           al.add("Vijay");    
          al.add("Kumar");    
           al.add(1,"Sachin");    
           ListIterator<String> itr=al.listIterator();    
           System.out.println("Traversing elements in forward direction");    
          while(itr.hasNext()){    
           System.out.println("index:"+itr.nextIndex()+" value:"+itr.next());               }              System.out.println("Traversing elements in backward direction");              while(itr.hasPrevious()){    
          System.out.println("index:"+itr.previousIndex()+" value:"+itr.previous());    
        
		  }    
  }     }
```



an example :
a book list


```java
-   import java.util.*;  
-   class Book {  
-   int id;  
-   String name,author,publisher;  
-   int quantity;  
-   public Book(int id, String name, String author, String publisher, int quantity) {  
-       this.id = id;  
-       this.name = name;  
-       this.author = author;  
-       this.publisher = publisher;  
-       this.quantity = quantity;  
-   }  
-   }  
-   public class ListExample5 {  
-   public static void main(String[] args) {  
-       //Creating list of Books  
-       List<Book> list=new ArrayList<Book>();  
-       //Creating Books  
-       Book b1=new Book(101,"Let us C","Yashwant Kanetkar","BPB",8);  
-       Book b2=new Book(102,"Data Communications and Networking","Forouzan","Mc Graw Hill",4);  
-       Book b3=new Book(103,"Operating System","Galvin","Wiley",6);  
-       //Adding Books to list  
-       list.add(b1);  
-       list.add(b2);  
-       list.add(b3);  
-       //Traversing list  
-       for(Book b:list){  
-       System.out.println(b.id+" "+b.name+" "+b.author+" "+b.publisher+" "+b.quantity);  
-       }  
-   }  
-   }
```

