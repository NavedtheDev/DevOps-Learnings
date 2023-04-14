* The process of converting one data type to another is known as Type Casting. 
* Let's start with converting an integer to float. We can do this by simply wrapping the integer around float 64 or float 32. 

```
package main

import (
	"fmt"
)

func main() {
	var i int = 90
	var f float64 = float64(i)

	fmt.Printf("%.2f\n", f)
}
```

* Output will be, 

```
90.00
```

