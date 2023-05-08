* Syntax,

```
func <function_name>(<params>) <return_type> {
    // body of the function 
}
```

Example,

```
func addNumbers(a int, b int) int {
    // body 
}
```

* <b>return</b> keyword: used to return from a method when its execution is complete. When a return statement is reached in a function, the program returns to the code that invoked or called that function. A function can return a value or not even return anything. Example,

```
func addNumbers(a int, b int) int {
    sum := a + b
    return sum 
}
```

## Calling a function ##

* Syntax,

```
<function_name>(<arguments>)
```
Example,
```
addNumbers(2, 3)
```

* To recieve the values returned by a function, we store it in variables. Example,

```
sumOfNumbers := addNumbers(2, 3)
```

## Naming convention for functions ##

   1. must begin with a letter.
   2. can have any number of additional letters and symbols.
   3. cannot contain spaces.
   4. case-sensitive.









