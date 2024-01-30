# Loops
### Formation
1. For loops must be written carefully. For example, the following code does not loop.
```java
for (int i = 0; i > 5; i++){}
// i will never be larger than 5
```

2. With nest loops, the inner loop increments all of the times for every round of the outer
```java
outer : for (int i = 0; i < 2; i++){
    for (int j = 0; j< 2; j++){
        if (i == j ){
            continue outer;
            // This skips through all of the inner for that round of outer
        }
        System.out.println("i= " + i + ", j= " + j);
        }
        }
        
        // Prints i=1, j=0
```