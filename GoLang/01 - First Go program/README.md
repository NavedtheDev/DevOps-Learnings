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


* Then we have the curly braces surrounding the line fmt.println("Hello World!"). These curly braces denote the starting and the ending of the function. 


* Coming to the last piece of the program, the statement is made of three components. First, we specify the name of the package to be used, which is fmt. Then we specify the name of the function that's present inside that package. Here the function's name is println, which means print, and then go to new line. The .operator between fmt and println is known as the member access operator. It is used to access members of a package. In this case, we are accessing println function, which is a member of the fmt package. The third part is the text Hello World enclosed within the quotes, anything within the quotes becomes a string. Now, we call the function printeln by passing it the string expression as the only argument. 
