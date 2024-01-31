# Arrays and ArrayLists
### Array Lists
#### array.remove();
1. Returns a boolean
2. Input: value of item in a list


#### Array.binarySearch(a, <value>)
1. Binary search repeadly divides the search interval in half and comparing them to match the element in the middle 
   fo the array. 
2. If the array/ArrayList is not sorted in order, it returns undefiend.
```java
Integer[] a = { 3, 4, 65,3, 1, 3, 45};
System.out.println(Arrays.binarySearch(a, 3));
// Prints undefined
```

#### array.get()
- Input: The array.get() method in Java takes an integer as an argument, which represents the index of the element you want to retrieve from the ArrayList.  
- Return: The array.get() method returns the element at the specified index in the ArrayList. If the index is out of range (index < 0 || index >= size of ArrayList), it throws an IndexOutOfBoundsException.

```java
List<double> list = new ArrayList<>();
System.out.println(list.get(list.size));
// This trys to print the last item in the list.
// list.size() = length; list.get(length) = lastIndex;
// If the code compiles, this will throw index out of bounds exception        
list.add(1);
/// This would cause code not to compile. 
// Cannot but int into double list
```

#### ArrayList.iterator()
1. Returns an iterator over the elements in the list in proper sequence
2. The returned iterator is fail-fast: if the list is structurally modified at any time after the iterator is 
   created, besides the iterators own remove or add methods, the iterator will throw a concurrent modificationException.
3. The iterator() method in Java's ArrayList class provides a way to access each element in the ArrayList one by one. It returns an Iterator object that can be used to traverse the elements in the ArrayList.  

5. The Iterator object has two main methods:  
   hasNext(): This method returns true if there are more elements in the ArrayList to iterate over, and false otherwise.
   next(): This method returns the next element in the ArrayList.
```java
import java.util.ArrayList;
import java.util.Iterator;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Cherry");

        Iterator<String> iterator = list.iterator();

        while (iterator.hasNext()) {
            String fruit = iterator.next();
            System.out.println(fruit);
        }
    }
}

```
In this code, we first create an ArrayList of String objects and add some fruits to it. We then obtain an Iterator for the list using the iterator() method. We use the hasNext() method of the Iterator to check if there are more elements in the list, and the next() method to retrieve the next element. This allows us to iterate over all the elements in the list.

### Similarities between arrays and ArrayLists
1. Both are used for storing elements 
2. Both can hold duplicate values 
3. Both preserve the order of elements



### How to make an Array
```java
int[] arr1 = new int[]{1, 2, 3, 4, 5};
//
int[] arr2;
arr2 = new int[]{1, 2, 3, 4, 5};
//
int[] arr3 = new int[5]; // All elements will be initialized to 0
//
int[] arr4 = new int[5];
arr4[0] = 1;
arr4[1] = 2;
arr4[2] = 3;
arr4[3] = 4;
arr4[4] = 5;
//
int[] arr5 = {1, 2, 3, 4, 5};
```

### How to make an array list
```java
ArrayList<Integer> arrList1 = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));
//
ArrayList<Integer> arrList2;
arrList2 = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));
//
ArrayList<Integer> arrList3 = new ArrayList<>(5); // All elements will be initialized to null
//
ArrayList<Integer> arrList4 = new ArrayList<>(5);
arrList4.add(1);
arrList4.add(2);
arrList4.add(3);
arrList4.add(4);
arrList4.add(5);
//
ArrayList<Integer> arrList5 = new ArrayList<>() {{
    add(1);
    add(2);
    add(3);
    add(4);
    add(5);
}};
//
```


### How to make List<>
1. This will not have the array list methods
```java
// No array list method
List<Integer> list = List.of(1, 2, 3, 4);

// No array list methods
List<Integer> list = Array.asList(1, 2, 3, 5);

```