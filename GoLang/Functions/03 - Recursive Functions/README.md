* Recursion is a concept where a function calls itself by direct or indirect means. 

* The function keeps calling itself until it reaches a base case.

* It is used to solve a problem where the solution is dependent on the smaller instance of the same problem. 

* Example,

```
package main
import "fmt"

func factorial(n int) int {
	if n == 0 {
		return 1
	}
	return n * factorial(n-1)
}

func main() {
	n := 7
	result := factorial(n)
	fmt.Println("Factorial of", n, "is :", result)
}
```
Output,
```
Factorial of 7 is : 5040
```
