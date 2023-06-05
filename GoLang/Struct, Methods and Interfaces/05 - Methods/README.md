* Method is similar to a function with one simple addition. 

* A method augments a function by adding an extra parameter section immediately after the func keyword that accepts a single argument. This argument is called a receiver. 

* Whenever there is a strong relationship between a function and a struct, we can use a method.

* A method is a function that has a defined receiver. 

* Syntax, 

```
func (<receiver>) <method_name>(<parameters>) <return_params> {
    //code
}
```

* Some methods can be associated with a named type, circle for instance, or a pointer to a named type. Example,

```
func (c Circle) area() float64 {
//code
}
```
And,
```
func (c *Circle) area() float64 {
//code
}
```
