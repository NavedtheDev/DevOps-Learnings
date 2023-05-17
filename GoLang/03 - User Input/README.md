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

* NOTE : Scanf function reads from the input source sequentially. Hence, we must give the list of arguments in the order that's specified in the format string. 

<br>

* The fmt scanner function returns two values, count, which is the number of arguments that the function writes successfully, and the error, which is any error that's thrown during the execution of the Scanf function. 
* Let us understand this with an example.

```
package main

import "fmt"

func main() {
	var a string
	var b int

	fmt.Print("Enter a string and a number: ")

	count, err := fmt.Scanf("%s %d", &a, &b)

	fmt.Println("count: ", count)
	fmt.Println("error: ", err)
	fmt.Println("a: ", a)
	fmt.Println("b: ", b)
}
```
<br>

* Output will look like this,

```
Enter a string and a number: Naved 5
count:  2
error:  <nil>
a:  Naved
b:  5
```

* Here we just entered a string and an integer. So the program ran successfully with no errors. But now consider this output,

```
Enter a string and a number: Naved Ahmad
count:  1
error:  expected integer
a:  Naved
b:  0
```

* Instead of passing a string and an integer, we passed a string and then again a string. It was expecting a string and a number, but we passed two strings instead. 
* So count is one because we stored input successfully in just one argument, and that is variable A. 
* As you can see, error is expected integer, since we were expecting an integer, but it got a string instead so it gave us an error. 
