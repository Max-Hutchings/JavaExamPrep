### Methods
1. The method signature, e.g. train(), is part of the declaration.
2. Protected methods can be accessed within the same package or in its subclasses defined in a different package.
3. A method can be declared without an access modifier. e.g. dont say public or private or protected. In this case, they have public by default. Available to anything within the package.


### Abstract methods
1. Declared in a class without providing an implementation (no braces, followed by a semicolon).
2. Only abstract classes can contain abstract methods.
3. A class containing abstract methods should also be declared abstract.

```java
// THis will result in a compilation error as the class is not abstract.
class A{
    public abstract String abstractMethod();
}
```


### Overloaded methods
1. Where lots of the same method have different inputs.
2. The main() method can be overloaded.
3. The Number class is used for floats and doubles. Therefore, an intput of Number in an overloaded method will take 
   all the floats and doubles. 
   ```java
    public class A {
   
    public static void getVal(Number a){
    System.out.println("I am printed");
   }
    
    public static void getVal(int a){
    
   }
   
   public static void getVal(Object object){
   }
   
    public static void main(String[] args){
    getVal(1.23f);
    getVal(1.246345445d);
   }
   }
   
   // Prints the statement. 
    ```
4. Subclasses can overload superclass methods.
5. Overloaded methods can be final.
6. Overloaded methods can be synchronized: In Java, the term "synchronized" is a keyword that is used as a modifier for methods and blocks. When a method is declared as synchronized, it means that only one thread at a time can access and execute that method on the same object. This is used to prevent race conditions in multi-threaded environments.
7. If null is the input for an overloaded method, the method with the most specified input will be called.
```java
public class Main {
    // Method with no parameters
    public void display() {
        System.out.println("Display method with no parameters");
    }
    public void display(Object object) {
        System.out.println("Display method with no parameters");
    }
    // Method with one parameter
    public void display(String msg) {
        System.out.println("Display method with one parameter: " + msg);
    }
    // Method with two parameters
    public void display(String msg, int num) {
        System.out.println("Display method with two parameters: " + msg + ", " + num);
    }
    public static void main(String[] args) {
        Main main = new Main();
        // Calling the method with no parameters
        main.display(null);
        
    }
}

// This will call the display(String) method as its most specific.
```


### Static 
1. Static methods MUST use static variables.
```java
// This will not work as the static method cannot access non-static variables.
public class B {
    int a = 0;
    static void getVal(){
        a++;
    }
}
```




