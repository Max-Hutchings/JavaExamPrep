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





