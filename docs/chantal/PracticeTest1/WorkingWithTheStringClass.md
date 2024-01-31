# Working with the String Class

## Immutability

Remember, Strings are immutable - once you create a String instance, you can't modify it. Operations like concat() on a String variable will *return* a new String object with the correct form, but will need to be saved.

```java
String str = "String";
str.concat("is");
str.concat("immutable");
System.out.println(str); //will print "String"
str = str.concat(" must be replaced");
System.out.println(str); //will print "String must be replaced"
```

## Characteristics

You need to use the function length() to get the length of a string, it doesn't have a length property like an Array.

You can only use double quotes for a string - to have quotes inside a string, escape the chars.

## String Formatting

Special characters in a formatted string:  

![Format specifiers table from https://www.geeksforgeeks.org/format-specifiers-in-java/](img/StringFormatSpecifiers.png)