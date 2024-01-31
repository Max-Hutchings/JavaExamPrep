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

### Do While loops
1. Similar to a normal while loop, but backwards.
```java
int apple = 7;
int basket = 5;
for (int i = 0; i < apple; i++){
    apple--;
    do {
        basket -= 1;
        }
    while (basket >= 2);
        }
System.out.println(apple + " "+ basket);

// Prints 3 - 2
// Process for do while
// is basket >= 2?
// Then basket -= 1
```

### Breaking a specific loop
1. use break <title> - from the example below to pick which loop breaks.
2. to make a + b = 4, use break A
```java
int a=0; int b = 0;
A:for(int i = 0; i<2;i++){
    B:for (int j=0; j<4; J++){
        if (I*J>=3){
            a = i;
            b = j;
            break _____;
        }
    }
}
System.out.println(a + b);
```

