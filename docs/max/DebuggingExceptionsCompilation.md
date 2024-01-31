# Exceptions, Debugging compilation

### Compilation Error (NOT EXCEPTION!)
#### These take place when trying to compile. Exceptions are caught sooner!
When the program will fail to compile.
1. e.g. assigning the wrong data type. An upper case character cannot be a primitive char
```java
char c = "C";
// This will cause a compilation Error

int n = 5;
c = n;
// This will also cause a compilation Error
```
2. Local variables must be initialized before use. Otherwise, a compilation error.
```java
String go;
System.out.println(go);
```

3. Wrong Syntax 
```java
if(b =! c){}
// This is not the correct way aroung. 
// Should be if (b!=c) []
```

4. Incorrect brackets 
```java
1 if (true == false)
2    i ++;
3    j ++;
4 else {}...
// Compilation error on line 4 where it gets unexpected else. It expected {} befor ethen.
```



### Illegal state exception
- The IllegalStateException is a runtime exception in Java. It is thrown to indicate that a method has been invoked at an illegal or inappropriate time.
- For example, calling a method on an object that requires the object to be in a certain state (like being initialized), but the object is not yet in that state.


### Exception Handling and try, catch, finaly blocks
1. Every exception handle block MUST start with a try{}
2. Catch blocks can handle multiple exceptions. Each specificed exception must be seperated with a " | ". 
```java
try{} catch(ArrayIndexOutOfBoundsException|ArithmeticException e){}
```
3. A multi-catch block cannot have exceptions in the same inheritance hierarchy.
```java
// This is not allowed 
try{} catch(Exception e | ArithmeticException e){}
```
4. If you want different handling, you can have different catch statements.
```java
try {
    // Your code here
} catch (ArrayIndexOutOfBoundsException e) {
    // Handle ArrayIndexOutOfBoundsException
} catch (ArithmeticException e) {
    // Handle ArithmeticException
}
```
5. You can have exceptions from the same hierarchy, but more specific exceptions must come first!
```java
try {
    // Your code here
} catch (ArrayIndexOutOfBoundsException e) {
    // Handle ArrayIndexOutOfBoundsException
} catch (ArithmeticException e) {
    // Handle ArithmeticException
}
```

#### Finally{}
1. Finally runs no matter what happens with the try or catch block. Therefore, what finally says always gooes!
```java
public class Main {
    public static void main(String[] args) {
        try {
            System.out.println("In try block");
            throw new Exception("Exception thrown in try block");
            return 0;
        } catch (Exception e) {
            return 10;
        } finally {
            return 20;
        }
    }
}

// This will always return 20 no matter what.
```



### Exception Handling keywords
1. Finally: it ensures that the code within its block gets executed regardless of whether an exception was thrown or not.
2. Throws: It's used in the method signature to indicate that callers of the method need to handle or propagate this type of exception.
3. Throw: explicitly throw an exception from a method or any block of code. We can throw either checked or unchecked exceptions. This immediately stops the execution of the method and passes the thrown exception up to the calling method.
```java
public class Main {
    public static void main(String[] args) {
        try {
            methodThatThrowsException();
        } catch (Exception e) {
            System.out.println("Caught exception: " + e.getMessage());
        }
    }

    static void methodThatThrowsException() throws Exception {
        throw new Exception("This is an exception");
    }
}
```



### ArrayIndexOutofBonds
1. The code WILL compile (obviously), hence getting an exception.
2. This exception takes place when trying to access an element in an array that doesnt exist.
3. Watch out for more generic exceptions on top. In the example below, the "Exception" catch catchs all exceptions, 
   so the more specific exception cannot be read. This leads the code to not compile.
```java
// Code will not compile because broad exception first.
try{
    int[] array = new int[2];
    array[5] = 100;
}catch(Exception e){
    e.printStackTrace();
}
catch(ArrayIndexOutOfBoundsException a){
    e.printStackTrace()
}
```

### Logical error
#### NOT POINTED OUT BY THE PROGRAM
1. Cause the program to produce incorrect results or behave in unintended ways.
2. For example, if you were to write a program to calculate the average of two numbers and mistakenly used multiplication instead of addition in your formula, the program would still compile and run, but it would not produce the correct output. This would be a logical error.
3. It's important to note that logical errors can be the most difficult to debug because the compiler or interpreter does not point them out. They require a good understanding of the program's intended behavior and often involve stepping through the code and checking the program's state at various points to identify where the logic is going wrong.


