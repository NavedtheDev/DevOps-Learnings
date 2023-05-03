* The if-else clause is one of the most used structures for specifying conditions. 



## if statement ##

* How does if works? The if statement is provided with a condition. The if statement evaluates this condition, and if this condition is true, statements inside the body of if are executed. If the condition is false, the statements inside the body of if are not executed. 

```
if (condition) {
    // executes when condition is true 
}
```

<b>NOTE</b>: The parentheses around the condition are optional. 

* Example, 

```
package main

import (
	"fmt"
)

func main() {
	var a int = 100
	var b string = "Fine"
	if a == 100 {
		fmt.Println(b)
	}
}
```
