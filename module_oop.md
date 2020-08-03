# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?
* In systems design, a **_fail-fast_** system is one which immediately reports at its interface any condition that is
 likely to indicate a failure. 
* **_Fail-fast_** systems are usually designed to stop normal operation rather than attempt to continue a possibly flawed
 process.
* The **_fail fast_** principle stands for stopping the current operation as soon as any unexpected error occurs.
* Adhering to this principle generally results in a more stable solution.
*** 

## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?
* Traverse linked list using two pointers. 
* Move one pointer by one and other pointer by two. 
* When the fast pointer reaches end slow pointer will reach middle
 of the linked list.
```java
// Java program to find middle of linked list 
class LinkedList 
{ 
    Node head; // head of linked list 
  
    /* Linked list node */
    class Node 
    { 
        int data; 
        Node next; 
        Node(int d) 
        { 
            data = d; 
            next = null; 
        } 
    } 
  
    /* Function to print middle of linked list */
    void printMiddle() 
    { 
        Node slow_ptr = head; 
        Node fast_ptr = head; 
        if (head != null) 
        { 
            while (fast_ptr != null && fast_ptr.next != null) 
            { 
                fast_ptr = fast_ptr.next.next; 
                slow_ptr = slow_ptr.next; 
            } 
            System.out.println("The middle element is [" + 
                                slow_ptr.data + "] \n"); 
        } 
    } 
}
```

#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?
1. Declare and initialize an array.
2. Duplicate elements can be found using two loops. 
3. The outer loop will iterate through the array from 0 to length of
 the array. The outer loop will select an element. 
4. The inner loop will be used to compare the selected element with the rest of the elements of the array.
5. If a match is found which means the duplicate element is found then, display the element.
```java
public class DuplicateElement {  
    public static void main(String[] args) {
        System.out.println("Duplicate elements in given array: ");  
        //Searches for duplicate element  
        for(int i = 0; i < arr.length; i++) {  
            for(int j = i + 1; j < arr.length; j++) {  
                if(arr[i] == arr[j])  
                    System.out.println(arr[j]);  
            }  
        }  
    }  
}  
```

#### What is a linked list? How to find if a linked list has a loop?
1. **_Linked List_** is a part of the Collection framework present in _java. util package_. 
2. This class is an implementation of the LinkedList data structure which is a linear data structure where the elements
 are not stored in contiguous locations and every element is a separate object with a data part and address part.
3. The elements are linked using pointers and addresses. Each element is known as a __node__.
4. The nodes cannot be accessed directly instead we need to start from the head and follow through the link to reach
 to a node we wish to access.
5. Advantages of **_Linked List_**:
    * Insertion and Deletion Operations are Easier.
    * Efficient Memory Utilization, i.e. no need to pre-allocate memory.
    * Faster Access time,can be expanded in constant time without memory overhead.
* To find if a linked list has a loop:
    * Have two references to the list and move them at different speeds.
    * If the linked list has a loop they will definitely meet.
    * Else either of the two references(or their next) will become null.
```java
public class LinkedList {
    boolean hasLoop(Node first) {
    
        if(first == null) // list does not exist..so no loop either
            return false;
    
        Node slow, fast; // create two references.
    
        slow = fast = first; // make both refer to the start of the list
    
        while(true) {
    
            slow = slow.next;          // 1 hop
    
            if(fast.next != null)
                fast = fast.next.next; // 2 hops
            else
                return false;          // next node null => no loop
    
            if(slow == null || fast == null) // if either hits null..no loop
                return false;
    
            if(slow == fast) // if the two ever meet...we must have a loop
                return true;
        }
    }
}
```

#### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?
#### How does HashMap work?
#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)

### Other

#### What is a garbage collector, in a nutshell?

## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?
#### Which order should we catch the exceptions? Why?

### Object-oriented

#### What is a class?
#### What is an object?
#### What is a constructor?
#### Do we require parameter for constructors?
#### What is an interface?
#### What are access modifiers?
#### What is data hiding?
#### Can a static method use non-static members?
#### What is the difference between hiding a static method and overriding an instance method?
#### Define the following terms: Instantiation, Attribute, Method
#### Could we access a static variable (or method) from a non-static method? Why?
#### Could we access a non-static variable (or method) from a static method? Why?
#### How many instances you have of a static variable of a given class?
#### Why is it not a good practice to write a lot of static methods?
#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?
#### What is the ‘this’ reference?
#### What are base class, subclass and superclass?
#### Draw an object oriented family (as entities, with relations) on the whiteboard.
#### Difference between overloading and overriding?
#### What are the Object Oriented Principles? Explain the concepts with realistic examples!
#### What is method overloading?
#### What is method overriding?
#### Explain how object oriented languages attempt to simplify memory management for Programmers.
#### Explain the “Single Responsibility” principle!
#### What is an object oriented program? Explain, show.
#### How do you make a class immutable? What do you need to watch out for?
#### How many instances can be created for an abstract class?

## Programming languages

### Java

#### What is autoboxing and unboxing?
#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?
#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?
#### What is the purpose of the ‘equals()’ method?
#### What is the difference between '==' and 'equals()'?
#### What does the ‘static’ keyword mean?
#### Why is the main() method declared as static? Explain.
#### What is the default access modifier in a class?
#### What is the JVM?
#### What is the difference between the JRE and the JDK?
#### What is the difference between long and Long?
#### Can a long store bigger numbers than a Long?
#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.
#### What are the access modifiers in Java? Which one could we use for class?
#### Can an “enum” contain methods in Java? Explain.
#### When would you use a private/protected/public attribute? What is the difference?
#### How do you prevent developers from subclassing a class?
#### How do you prevent developers from overriding a method in a subclass?
#### How do you prevent developers from changing the value of a variable?
#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!
#### What happens if you try to call something, that you have no access to, because of data hiding?
#### What happens if you try to delete/drop an item from an array, while you are iterating over it?
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?
#### What happens if you try to add an item to the end of an array, while you are iterating over it?
#### If you need to access the iterator variable after a for loop, how would you do it?
#### Which interfaces extend the Collection interface in Java. Which classes?
#### What is the connection between equals() and hashCode()? How are they used in HashMap?
#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?
#### What is Error in Java and how does it relate to Exception?
#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?
#### What is the largest number you can work with in Java?
#### When you use method overriding, can you change the access level of the method, from protected to public? Why?When you use method overriding, can you change the access level of the method, from public to protected? Why?
#### Can the main method be overridden? Explain your answer!
#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?
#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?
#### What does "final" mean in case of a variable, method or a class?
#### What is the super keyword?
#### What are “generics”? When to use? Show examples.
#### What is the benefit of having “generic” containers?
#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?
#### What is an annotation? What can be annotated and how? Show examples.

### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?

### Database

#### How can you connect your application to a database server? What are the possible ways?
#### What do you know about database normalization?
