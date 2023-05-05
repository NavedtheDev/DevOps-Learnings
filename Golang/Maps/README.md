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
