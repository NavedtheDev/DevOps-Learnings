## Declaring Variables ##

* Variables in Golang can be declared using various syntax.

### Method 1 ###

```
var <variable_name> <data_type> = <value>
```

* A variable is initialised by using the var keyword. Keywords are predefined reserved words used in programming that have special meaning to the compiler. 
* Then we specify the variable name.
* Then the data type of the variable, following it is the assignment operator, then we have the value of data that we want to store.
* Example,
```
var s string = "Hello World"
var x int = 100
var b bool = true
var f float64 = 78.32
```

* Let's see a simple program.
```
package main
import "fmt"

func main(){
     var i int = 100
     fmt.Println(i)
}
```
Output will be,
```
100
```

### Method 2 ###

```
x := 100
```

* In this the compiler will implicitily assign the data type to the variable.


