* One of the most used ways of taking user input is through Scanf function, which is provided by the fmt package. Scanf function takes the format string, along with the list of variable number of arguments. 
* This string contains custom specifiers that the Scanf function uses to format the final output string. 
* Here is an example. 
 
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



* Let us see how we can take multiple inputs using Scanf.
