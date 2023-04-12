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
