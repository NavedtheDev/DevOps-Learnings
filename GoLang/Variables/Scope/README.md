* The scope of a variable can be defined as a part of the program where a particular variable is accessible or from where it can be referenced. 
* In Golang, scope is defined using block. A block is defined in Go as a possibly empty sequence of declarations and statements within matching brace brackets or curly brackets. 

```
{
// outer block

{

// inner block

}

}
```

* Inner blocks can access variables that are declared within outer blocks but outer blocks cannot access variables that are declared within inner blocks. 



* Now we've understood how variable scope works in terms of blocks. However, scope rules can also be determined based on where the variables are declared. We have two kinds of such variables, local and global variables. 

* Talking about local variables, there are variables that are declared inside a function or a block. These are not accessible outside the functional block and these variables can also be declared inside looping or conditional statements. 

```
package main
import "fmt"

func main(){
     name := "Alex"
     fmt.Println(name)
}
```
* Here, name is a local variable.

* Global variables are variables that are declared outside of a functional block. They are available throughout the lifetime of a program. They're declared at the top of the program outside all functional blocks and well, they can be accessed from any part of the program. 

```
package main
import "fmt"

var name string = "Alex"

func main(){
     fmt.Println(name)
}
```
* Here, name is a global variable.

