* A map is a data structure that provides you with an unordered collection of key-value pairs. 

* They are used to look up a value by it's associated key. You store values into the map based on a key. 

* The strength of a map is its ability to retrieve data quickly based on the key. 

* A key works like an index that points to the value you associate with that key. 

* Go maps are implemented using hash tables and they have efficient add, get and delete operations. 

* Syntax, 

```
var <map_name> map[key_data_type>]<value_data_type>
```
This syntax created an empty map. So, if we try to add values in it, it will throw us an error. 

* To create maps with key-value pairs, we need to initialize it as well. Syntax,

```
<map_name> := map[<key_data_type>]<value_data_type>{<key_value_pairs>}
```

* Example,

```
codes := map[string]string{"en": "english", "fr": "french"}
```

* We can also use make() to create a map. The make() takes argumented type of the map, and it returns us an initialized map. Capacity here is an optional argument. Syntax,

```
<map_name> := make(map[<key_data_type>]<value_data_type>,<initial_capacity>) 
```

* To determine how many items or key-value pairs a map has, we use the len() function. It will return zero for an uninitialized map.

* We can also access the items of a map by referring to its key name, simply by specifying the name of the map and writing its key name inside the square brackets. Syntax,

```
fmt.Println(map_name["key_name"])
```

* Now, when we say getting a key while talking about maps, we mean getting the value associated with the key. When you index a map in Go, you get two return values. The first is the value and second(optional) is a boolean that indicates if the key exists. If the key doesn't exist, the first value will be the default zero value. Example,

```
package main

import "fmt"

func main() {
	codes := map[string]int{"en": 1, "hh": 2}
	value, found := codes["en"]
	fmt.Println(found, value)
}
```
Output,
```
true 1
```

* Now, adding an item to the map is done by using a new index key and assigning a value to it. Example,

```
package main

import "fmt"

func main() {
	codes := map[string]int{"en": 1, "hh": 2}

	codes["it"] = 3
	fmt.Println(codes)
}
```
Output,
```
map[en:1 hh:2 it:3]
```

* We can also update the value of a specific item by referring to its key name. It will overwrite or update the value of that key with the new value. Example,

```
package main

import "fmt"

func main() {
	codes := map[string]int{"en": 1, "hh": 2}

	codes["en"] = 3
	fmt.Println(codes)
}
```
Output,
```
map[en:3 hh:2]
```


