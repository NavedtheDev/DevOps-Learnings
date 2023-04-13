
* Scanf function is used to take user input. Here is an example.

```
package main
import "fmt"

func main() {
	var name string
	fmt.Print("Enter your name: ")
	fmt.Scanf("%s", &name)
	fmt.Println("Hey, ", name)
}
```
* Here %s is a string format specifier.
