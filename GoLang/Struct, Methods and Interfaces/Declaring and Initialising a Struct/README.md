# Declaraton #

* Syntax,

```
type <struct_name> struct {
    // list of fields
}
```

* Example,

```
type square struct {
    x float64
    y float64
}
```

* Type keyword is used to create a new user-defined type. 



# Initialization #

* There are many ways of doing this.

1.
```
var <variable_name> <struct_name> 
```

2.
```
<variable_name> := new(<struct_name>)
```

3.
```
<variable_name> := <struct_name> {
<field_name>: <value>,
<field_name>: <value>,
}
```









