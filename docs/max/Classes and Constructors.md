# Classes and Constructors
### valid constructors 
```java
train(){}
//
public train(int i, char j){}
```

### NOT valid constructors
```java
// Final cannot be as not inherited by a subclass
public final train(int i){}
// It initializes an object, it doesn't make sense to by synchronized
public synchronized train(int i){}
// They don't return anything. No return type needed.
public void train(int i){}
```


### Default constructors 
1. If no constructor is added to a class, the class gets a default constructor.
2. The default constructor of a class always calls the no-argument constructor of the super class.