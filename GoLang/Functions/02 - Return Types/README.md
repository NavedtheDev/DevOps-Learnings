## Returning multiple values ##

* Go allows returning multiple values. Example,

```
package main

import "fmt"

func operation(a int, b int) (int, int) {
	sum := a + b
	diff := a - b
	return sum, diff
}

func main() {
	sum, difference := operation(20, 10)
	fmt.Println(sum, difference)
}
```
Example,
```
30 10
```



## Returning named values ##

* We can give a name to our return variables in the function signature only. Example,

```
package main

import "fmt"

func operation(a int, b int) (sum int, diff int) {
	sum = a + b
	diff = a - b
	return
}

func main() {
	sum, difference := operation(20, 10)
	fmt.Println(sum, difference)
}
```
Example,
```
30 10
```



## Variadic functions ##


* function that accepts variable number of arguments.

* it is possible to pass a varying number of arguments of the same type as referenced in the function signature.

* to declare a variadic function, the type of the final parameter is preceded by an ellipsis "..."

* Syntax,

```
func <func_name>(param-1 type, param-2 type, param-3 ...type) <return_type>
```
Example,
```
func sumNumbers(numbers ...int) int

            AND
	    
func sumNumbers(str string, numbers ...int)
```

* Example program, 

```
package main

import "fmt"

func printDetails(student string, subjects ...string) {
	fmt.Println("hey", student, "here are your subjects:")
	for _, sub := range subjects {
		fmt.Printf("%s, ", sub)
	}

}

func main() {
	printDetails("Naved", "Computer Science", "Physics")
}
```
Output,
```
hey Naved here are your subjects:
Computer Science, Physics,
```



## Blanl identifier ##

* Used to ignore a value returned by the function.
* Example,

```
package main

import "fmt"

func f() (int, int) {
	return 10, 20
}

func main() {
	r, _ := f()
	fmt.Println(r)
}
```
Output,
```
10
```
