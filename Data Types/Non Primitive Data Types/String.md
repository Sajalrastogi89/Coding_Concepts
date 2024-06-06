# String Class in Java

## Introduction
The `String` class in Java represents a sequence of characters. It is widely used for representing textual data and is one of the most commonly used classes in Java.

## Features
- **Immutable:** Strings in Java are immutable, meaning their values cannot be changed after creation.
- **String Literal:** Strings can be created using string literals enclosed in double quotes (`" "`).
- **Constructor:** Strings can also be created using the `new` keyword and a constructor.
- **Concatenation:** Strings support concatenation using the `+` operator or the `concat()` method.
- **Length:** The length of a string can be obtained using the `length()` method.
- **Character Access:** Individual characters in a string can be accessed using array notation (`[]`) or the `charAt()` method.
- **Substring:** Substrings of a string can be obtained using the `substring()` method.
- **Comparison:** Strings can be compared using methods like `equals()` and `compareTo()`.
- **Search:** Strings support methods for searching substrings (`indexOf()`, `lastIndexOf()`, `contains()`).
- **Formatting:** Strings support formatting using the `format()` method.

## Usage
```java
String str1 = "Hello"; // String literal
String str2 = new String("World"); // Constructor

// Concatenation
String message = str1 + " " + str2;

// Length
int length = message.length();

// Character Access
char firstChar = message.charAt(0);

// Substring
String sub = message.substring(0, 5);

// Comparison
boolean isEqual = str1.equals(str2);

// Search
int index = message.indexOf("World");

// Formatting of String
String formattedString = String.format("Hello, %s!", "World");
