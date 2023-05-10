# Declaration ##

* Syntax,

```
var <pointer_name> *<data_type>
```

* Example,

```
var ptr *string
```



# Initialisation #

* Syntax, 

```
var <pointer_name> *<data_type> = &<variable_name>
```

* Example,

```
i := 10
var ptr *int = &i
```

* Another way of iniialising a pointer is, 

```
var <pointer_name> = &<variable_name>
```

* Example,

```
p := "Programming"
var ptr = &p
```

* Another method is to use the shorthand operator. Syntax,

```
<pointer_name> := &<variable_name>
```

* Example,

```
h := "hello"
ptr := &h
```

* Example Program,

```
package main

import "fmt"

func main() {
	s := "hello"
	var b *string = &s
	fmt.Println(b)
	var a = &s
	fmt.Println(a)
	c := &s
	fmt.Println(c)
}
```
Output,
```
0xc000054270
0xc000054270
0xc000054270
```
