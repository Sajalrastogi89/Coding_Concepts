# Mapping Contexts in Java Streams  

## 1. Primitive to Primitive  
- **Method Used**: `map`  
- **Description**: Use this method within primitive streams (like `IntStream`).  
- **Example**:  
    ```java  
    IntStream intStream = IntStream.of(1, 2, 3);  
    IntStream squaredStream = intStream.map(i -> i * i); // int to int  
    ```  

## 2. Object to Primitive  
- **Method Used**: `mapToInt`, `mapToDouble`, or `mapToLong`  
- **Description**: Depending on the target primitive type.  
- **Example**:  
    ```java  
    List<String> words = Arrays.asList("apple", "banana", "cherry");  
    IntStream lengthsStream = words.stream()  
                                    .mapToInt(String::length); // String to int  
    ```  

## 3. Object to Object  
- **Method Used**: `map`  
- **Description**: For converting one object type to another.  
- **Example**:  
    ```java  
    List<String> words = Arrays.asList("apple", "banana", "cherry");  
    List<Integer> lengths = words.stream()  
                                  .map(String::length) // String to Integer  
                                  .collect(Collectors.toList());  
    ```  

## 4. Primitive to Object  
- **Method Used**: `mapToObj`  
- **Description**: For converting primitive types to their corresponding object types.  
- **Example**:  
    ```java  
    IntStream intStream = IntStream.of(1, 2, 3);  
    List<String> stringNumbers = intStream.mapToObj(String::valueOf) // int to String  
                                            .collect(Collectors.toList());  
    ```