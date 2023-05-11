* Function is called by directly passing the value of the variable as an argument.

* the parameter is copied into another location of your memory.

* So, when accessing or modifying the variable within your function, only the copy is accessed or modified, and the original value is never modified.

* All basic types (int, float, bool, string, array) are passed by value.

* Example,

```
package main

import "fmt"

func modify(s string) {
	s = "world"
}

func main() {
	a := "hello"
	fmt.Println(a)
	modify(a)
	fmt.Println(a)
}
```
Output,
```
hello
hello
```
