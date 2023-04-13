* Let us know how can you find the data type of a variable? 
* To check or find the type of variable or object in Golang, we can use the capital T format specifier or the reflect.TypeOf function from the reflect package. \

<br>

* Let's start with capital T format specifier. This is the simplest way to find the type of variable in Golang. Here is an example,

```
package main

import "fmt"

func main() {
	var a string
	var b int

	fmt.Printf("a is %T and b is %T \n", a, b)
}
```

* Output will be,

```
a is string and b is int
```
