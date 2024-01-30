# Basic Java Elements 
### Java key words
1. new 
2. instanceof
3. volatile: used to indicate that a variable value can be  modified by different threads. Any methods constantly 
   reading the variable will be notified to re-check the value.
```java
public class SharedData {
    private volatile int counter = 0;

    public void incrementCounter() {
        counter++;
    }

    public int getCounter() {
        return counter;
    }
}
```
4. while
5. transient: Use to prevent a value from being serialised. Which normally happens when converting an objects state 
   to a byte stream.
```java
import java.io.Serializable;

public class User implements Serializable {
    private String username;
    private transient String password;

    // constructors, getters and setters
}
```
3. enum: defines a type of class that represents a group of constants 
```java
public enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
}
```

### NOT java key words
1. Protect
2. transact


### Java packages 
1. Threads belongs to java.lang
2. importing a package can be used to make a subset of classes in a package visable in the current java source file.
3. 


### Naming conventions
1. constants are written in Upper case and seperated by "_". e.g. "MAXIMUM_VALUE"
2. Comments are written with // or /*  .... */


