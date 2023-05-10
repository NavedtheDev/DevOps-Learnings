* <b>& operator</b> - The address of a variable can be obtained by preceding the name of a variable with an ampersand sign (&), known as address-of operator. 

* <b>operator</b> - It is known as the dereference operator. When placed before an address, it returns the value at that address. 

* Example,

```
package main

import "fmt"

func main() {
	i := 10
	fmt.Printf("%T %v \n", &i, &i)
	fmt.Printf("%T %v \n", *(&i), *(&i))
}
```
Output,
```
*int 0xc000018098 
int 10
```
