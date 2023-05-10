* Syntax,

```
*<pointer_name> 
```

* We can also change the value of the variable using this syntax,

```
*<pointer_name> = <new_value>
```

* Example,

```
package main

import "fmt"

func main() {
	s := "hello"
	fmt.Printf("%T %v \n", s, s)
	ps := &s
	*ps = "world"
	fmt.Printf("%T %v \n", s, s)
	fmt.Printf("%T %v \n", ps, *ps)
}
```
Output,
```
string hello 
string world 
*string world 
```
