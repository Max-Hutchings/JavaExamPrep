# Math and Random
### Random
1. random.nextint(value) is not inclusive

```java
import java.util.Random;

Random random = new Random();
int randomValue = random.nextInt(50);
// Gives a value between 0 and 49
// 0 >= x < 50
```

2. Methods to get a random number:
    1. In constructor
    ```java
    Random random = new Random(15);
    int randomInt = random.nextInt();
   // This gives random between 0 and 15 excluding 15
    ```
    2. In .nextint method
    ```java 
    Random random = new Random();
    int randomInt = random.nextInt(15);
    // This gives and random between 0 and 15 excluding 15
   ```
   

### Math
1. Math.abs: turns any value to be positive.