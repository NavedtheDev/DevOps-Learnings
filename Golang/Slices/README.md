* A slice is an abstraction of an array. 

* They are also index-based and have a size, but is resized when needed. 

* A slice has three major components:

   1. Pointer : used to point to the first element of the array that is accesible through that slice. It is not necessary that the pointed element is laways the first element of the array.
   2. Length : number of elements it contains.  
   3. Capacity : number of elements in the underlying array counting from the firast element in the slice. 
   
* Length and capacity of a slice can be obtained from functions len() and cap() respectively. 

* To declare a slice, we declare an array without any size. Syntax,

```
<slice_name> := []<data_type>{<values>}
```
```
nums := []int{1,2,3}
```
* Example,

```
package main

import "fmt"

func main() {
	slice := []int{1, 2, 3}
	fmt.Println(slice)
}
```
Output,
```
[1 2 3]
```

* The core concept of slice is being a reference to the array. 

* To create a slice from an array, we have a start index and an end index. The element on the start index is included but the element at the end index is excluded. Syntax,

```
array[start_index : end_index]
```
Example,
```
package main

import "fmt"

func main() {
	arr := [10]int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
	slice := arr[1:8]
	fmt.Println(slice)
}
```
Output,
```
[2 3 4 5 6 7 8]
```

* We can even declare and initialize a slice using another slice. Syntax will be same as in the above case.

```
slice_2 = slice_1[1:4]
```

* There is one more way of declaring a slice and that is through the make function. It takes three parameters: data type, length, capacity(optional).
* Syntax,

```
slice := make([]<data_type, length, capacity)
```
Generally, make() is used to create an empty slice. So, if we print that slice, we will get zero value, since we have not initialised the slice yet. 

* 




