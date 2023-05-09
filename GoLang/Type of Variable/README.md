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

<br>

* Now the TypeOf function can be used, not just for finding out the data type of the variable but also for finding the type of simply a value or literal as we say. 

```
package main

import (
	"fmt"
	"reflect"
)

func main() {
	var a string = "Hey all"
	var b int = 50

	fmt.Printf("a = %v is of type %v \n", a, reflect.TypeOf(a))
	fmt.Printf("b = %v is of type %v \n", b, reflect.TypeOf(b))
}
```

* Output will be, 

```
a = Hey all is of type string 
b = 50 is of type int
```
