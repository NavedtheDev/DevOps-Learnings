* The if-else clause is one of the most used structures for specifying conditions. 



# if-else and else if statement #

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

* Output will be,

```
Fine
```

* The if statement may also have an optional else block that runs when the if condition is not met. 

```
if (condition) {
    // executes when condition is true 
} else {
    // executes when condition is false 
}
```

* Example,

```
package main

import (
	"fmt"
)

func main() {
	var a int = 100
	if a == 10 {
		fmt.Println("Fine")
	} else {
		fmt.Println("Wrong")
	}
}
```

* Output,

```
Wrong
```

<b>NOTE</b>: for the syntax in if-else block, the else statement should start from the same line where the if ends. Else, it will throw us an error. 



### else if statement ###

* Example,

```
ackage main

import (
	"fmt"
)

func main() {
	var a int = 100
	if a == 10 {
		fmt.Println("Very far")
	} else if a == 50 {
		fmt.Println("Close")
	} else {
		fmt.Println("Wrong")
	}
}
```















































