* An array a collection of similar data elements that are stored at contiguous memory locations. 

* Arrays are also known as homogenous data types since we can store elements of a single data type in one array and not different data types in one single array. 

### Why do we need arrays ###

* In programming, most of the time we need to store large amount of data of similar type. 

* <b>NOTE</b>: Arrays in Golang are a fixed length. That is, once they're declared and the size is mentioned, we cannot change the length of the array. 

* An array in Golang, has a pointer that points to the first element in the array. Since memory is contiguous, we can even calculate the address of any element that we    want to.

* It also has a property called length which denotes the number of elements in the array, and a property called capacity, which denotes the number of elements that it
  can contain. In case of arrays, length and capacity is same. 

* Syntax,

```
var <array_name> [<size>] <data_type>
```

Example,

```
var sports [5] string
```

* Let's see how we can initialize an array now. 

```
var nums [3] int = [3]int{1,2,3} 

OR 

grades := [3]int{1,2,3}

OR 

grades := [...]int{1,2,3}
```














