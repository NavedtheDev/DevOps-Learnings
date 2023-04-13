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
* Here %s is a format specifier for string. The arguments consist of the name variable which is a string variable itself. 
* Note the ampersand sign over here, we need to use it with the scanner function. We will understand this more when we study about pointers.
* When we run the program, the program will prompt the user to enter their name. 
* Output will look like this,

```
Enter your name: Naved
Hey,  Naved
```

<br>

* Let us see how we can take multiple inputs using Scanf. Here is an example.

```
package main

import "fmt"

func main() {
	var name string
	var is_age bool

	fmt.Print("Enter your name and is your age greater than 18: ")
	fmt.Scanf("%s %t", &name, &is_age)
	fmt.Println("My name is ", name, "and my age is greater than 18: ", is_age)
}
```
<br>
* Output will look like,

```
Enter your name and is your age greater than 18: Naved true
My name is  Naved and my age is greater than 18: true
```


