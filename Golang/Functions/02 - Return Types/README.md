## Returning multiple values ##

* Go allows returning multiple values. Example,

```
package main

import "fmt"

func operation(a int, b int) (int, int) {
	sum := a + b
	diff := a - b
	return sum, diff
}

func main() {
	sum, difference := operation(20, 10)
	fmt.Println(sum, difference)
}
```
Example,
```
30 10
```



## Returning named values ##

* We can give a name to our return variables in the function signature only. Example,

```
package main

import "fmt"

func operation(a int, b int) (sum int, diff int) {
	sum = a + b
	diff = a - b
	return
}

func main() {
	sum, difference := operation(20, 10)
	fmt.Println(sum, difference)
}
```
Example,
```
30 10
```


