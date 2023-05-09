* A defer statement delays the execution of a function until the surrounding function returns.

* The deferred call's arguments are evaluated immediately, but the function call is not executed until the surrounding function returns. 

* Example,

```
package main

import "fmt"

func printName(str string) {
	fmt.Println(str)
}
func printRollNo(rno int) {
	fmt.Println(rno)
}
func printAddress(adr string) {
	fmt.Println(adr)
}
func main() {
	printName("Joe")
	defer printRollNo(23)
	printAddress("street-32")
}
```
Output,
```
Joe
street-32
23
```
