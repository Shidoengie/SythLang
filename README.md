# Codename: Syth
Syth is a strong typed language with a python like syntax
# Assignment
## Variables
- Variables are declared using `var`
    ```go
    var int a = 9
    ```
- Using var is optional and not declaring a variable assignment type will be the same as is using var
- Vars is mostly used for clarity
    ```py
    int a = 9
    ```
## Constants
- Constants are declared using `"const"`
    ```go
    const int a = 9
    ```
- Constants only allow assignment of constant values
    ```go
    int b = 9
    const int a = b
    #Error b is not constant
    ```
    ```go
    const int b = 9
    const int a = b
    #No Error b is constant
    ```
- You must initialize the constant with a value
    ``` go
    const int a
    #Error a is not initialized 
    ```
## Snapshot
- `"snap"` variable assigment are a mix between constant and variables allowing essentially working as a snapshot of the current values and not allowing further changes
- This comes at a significant performanace cost as it gets a copy of the current values no matter the type, especially for data collections.
    ```go
    int a = 9
    snap int b = a
    print(b) -> "9"
    a = 10
    print(b) -> "9"
    ```


## Full assignment syntax
```
(var assignment type) <type> <name> <asignmentOperator> <value>
```
# Core Datatypes
- bool
- int
- float
- double
- str
# Core Data Colections
## Arrays
- Array are data colections with a size
- Single typed lists
    ```py
    list[int] intList = [0,1,2]
    ```
- ### Full List Syntax 
    ```
    list[allowed types] <name> <assignment operator> [value,value,...]
    ```
## Lists
- Lists in Syth are data collections without a size this is in terms similar to Linked lists in other languages
- Lists in Syth allow for multiple type allowence 
    ```py
    list[int|str] strInt = [0,"a","b",1]
    ```
- Single typed lists
    ```py
    list[int] intList = [0,1,2]
    ```
- ### Full List Syntax 
    ```
    list[allowed types] <name> <assignment operator> [value,value,...]
    ```
## Dictionaries
- Dictionaries are collections of Key Value Pairs
- Dictionaries can be defined using the `"dict"` keyword

- Keys and their values Are separated using `":"` and Key value pairs are separated using `","`
   ```py
   dict[str:int] users = {"bob":1,"joe":2}
   ```
- ### Full Dictionary syntax
    ```
    dict[keytype:valuetype] <name> <assignment operator> {key:value,(...kvp)}
    ```