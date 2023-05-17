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



* Let us learn about the string conversion package. This package consists of methods that we can use to convert integer to string and vice versa. 
* The first method is called Itoa(). It converts integer to string and it just returns one value, which is the string formed with a given integer. Let's see an example.

```
package main

import (
	"fmt"
	"strconv"
)

func main() {
	var i int = 58
	var s string = strconv.Itoa(i)
	fmt.Printf("%q", s)

}
```

* Output will be, 

```
"58"
```

* The next method is Atoi(), which converts string to integer, and it returns two values, the corresponding integer and if there's any error. 

```
package main

import (
	"fmt"
	"strconv"
)

func main() {
	var s string = "200"
	i, err := strconv.Atoi(s)

	fmt.Printf("%v, %T \n", i, i)
	fmt.Printf("%v, %T", err, err)

}
```

* Output will be,

```
200, int 
<nil>, <nil>
```
