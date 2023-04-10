```
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}
```

* Output is, 

```
Hello World!
```

* Packages are Go's way of organizing and reusing code. Every Go program must start with the package declaration.


* The next line is import "fmt". We use import keyword to include code from other packages to use with our program. Fmt package is a short form of format,and it implements formatting for input and output. so, Import fmt basically means that we are importing the fmt package in our code because we need the functionalities provided by this package. Also, note that in Go, package name during the import statement is surrounded by double quotes. 


* After this, we see a function declaration. you can consider them as the building blocks of a Go program. It is the entry point of the executable programs. Whenever we run a Go program, Go will automatically call the main function. 


* Then we have the curly braces surrounding
