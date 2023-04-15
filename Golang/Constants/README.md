* Constants they those variables whose values once initialized cannot be modified.
* The syntax to declare a constant in Golang is:

```
const <const_name> <data_type> = <value>
```

* It's initialized by using the const keyword. Then you assign the constant with a name. Then you specify the data type of the constant. The data type in case of constants is optional to provide. If you do not provide it, it's implicitly inferred by the compiler. Then we have the assignment operator. Then the value you want to store in the constant. 

<br>

* We have two kinds of constants, typed and untyped. 
* Constants are untyped unless they're explicitly given a data type at declaration and they allow for much more flexibility. Example,

```
const age = 12
const s_name, s_age = "Naved", 21
```

* Types constants, these are constants where you explicitly specify the data type in the declaration. Example,

```
const name string = "Naved Ahmad"
const age = 21
```

