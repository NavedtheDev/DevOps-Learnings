* We can access fields of a struct using the dot operator. Syntax,

```
<variable_name>.<field_name>
```

* Example,

```
package main

import "fmt"

type square struct {
	x int
	y int
}

func main() {
	var c square
	c.x = 5
	c.y = 5
	fmt.Printf("%+v \n", c)
}
```
Output,
```
{x:5 y:5}
```
