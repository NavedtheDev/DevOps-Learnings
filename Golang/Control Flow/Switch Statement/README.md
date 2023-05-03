* In switch-case control mechanism, we use the value of a variable or an expression to change the control flow of program execution, via a multi-way branch. 

* Let's see the syntax of switch. 

```
switch expression {
    case value_1:
      // execute when expression equals to value_1
      
    case value_2:
      // execute when expression equals to value_2
      
    default: 
      // execute when no match is found 
}
```

* This switch statement tests the value of an expression and compares it with multiple cases. Once the case match is found, a block of statements associated with that particular case is executed. Each case in a block of a switch has a different name, or a number, or a value, which is referred to as an identifier. 

* The value that's provided in the expression is compared with all the cases inside the switch block until the match is found. In case no match is found, the default statement is executed and the control goes out of the switch block. 

* Example, 

```
package main

import (
	"fmt"
)

func main() {
	var i int = 100
	switch i {
	case 10:
		fmt.Println("i is 10")
	case 100:
		fmt.Println("Exactly")
	default:
		fmt.Println("neither 10 nor 100")

	}
}
```

* Output, 

```
Exactly
```


