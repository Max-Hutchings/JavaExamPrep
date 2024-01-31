# Basic Java Elements

## Packages

Some packages available in Java:

* java.lang - provides classes that are fundamental to the design of Java - class Thread belongs to this package. Other classes include the data type wrapper classes (i.e. Integer), Math, String, Object (root of class hierarchy), Runtime, System.
* java.io - classes that deal with system input and output through data streams, serialization and the file system i.e. File, FileReader & FileWriter, InputStream, PrintStream etc.
* java.net - classes for implementing network applications i.e. URL, Socket, ServerSocket, Proxy etc.
* java.util.concurrent - classes useful for concurrent programming

## Naming Conventions

Classes - nouns, mixed case with first letter always capitalised (including first letter of internal word). Use whole words, avoiding acronyms unless more commonly used.

Interfaces - capitalized like class names.

Methods - verbs, camelCase.

Variables - camelCase, shouldn't start w/ _ or $ even if allowed, sort and meaningful.

Constants - uppercase, words separated by _ i.e. int MIN_WIDTH;
