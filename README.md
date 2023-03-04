# Codename: Syth
Syth is a strong typed language with a python like syntax
# Assignment
## Variables and constants
- Variables can be declared as such
    ```py
    int a = 9
    ```
- Constants are declared using `"const"`
    ```go
    const int a = 9
    ```

#### Automatic type assignment and dynamically typed  variables 
# LIKELY NOT TO BE ADDED \\/ \\/ \\/
## Auto type assignment
- Automatic typing can be done with the `"var"` keyword 
    ```go
    var a = 9
    ```
- Please note that attempting to assign a different type to the initial assigned type **will cause an error**
    ```go
    var a = 9
    a = true
    #Error
    ```
- You can use `":="` as a shorthand for `"var"` and type assignment 
    ```go
    a := 9
    ```
## Dynamic type assignment
- Dynamically typed variables can be declared using the `"dy"` keyword
    ```go
    dy a = 9
    ```
- As apposed to the `"var"` keyword attempting to assign a type to the variable that differs from the initiallly assigned type *does not cause an error*
    ```go
    dy a = 9
    a = true
    #This is valid
    ```
# LIKELY NOT TO BE ADDED ^^^^
## Full assignment syntax
```
(const) <type> <name> <asignmentOperator> <value>
```
# Core Datatypes
- bool
- int
- float
- double
- str
# Core Data Colections
## Lists
- Lists in Syth are a collection of values
- Lists in Syth allow for multiple type allowence 
    ```py
    list[int, str] strInt = [0,"a","b",1]
    ```
- Lists in Syth can also have sizes
   ```py
   list[int, str,3] sizedList = [0,"a","b"]
   ```
- Both type allowence and size are optional you can have a list with a infinite size that allows all types
    ```py
    list anytype = [0,0.0,"a",true]
    ```
- ### Full List Syntax 
    ```
    list[allowed types,size] <name> <assignment operator> [value,value,...]
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
