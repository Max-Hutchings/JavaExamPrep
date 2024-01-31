# Operators 
### Ternary operators
Example:
```java
larger = (a > b)? c : d;
```

### Relational Operator
1. ==
2. !=
3. >
4. <
5. <=

### Arithmetic
1. "+"
2. "-"
3. "*"
4. "/"
5. "%" 



### Comparisons with "==" and .equals()
1. "==" compares the object reference; is the object stored in the same place in memory. 
2. The `.equals()` method, by default, behaves the same as the "==" operator. However, it can be overridden in a class to perform a custom comparison. For example, it can be modified to compare the contents of two objects.
```java
class fruit{
    int a = 0;
    public fruit(int a){
        this.a = a;
    }
}

public class B {
    public static void main(String[] args){
        fruit obj = new fruit(1);
        fruit obj1 = new fruit(1);
        System.out.print(obj == obj1);
        Systme.out.print(obj.equals(obj1));
    }
}
// The objects are stored in different places in memory as they are different objects
// The .equals() method has not been overridden in fruit so its remains as standard, being the same as ==.
// The String class does override .equals()
```