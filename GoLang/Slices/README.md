* A slice is an abstraction of an array. 

* They are also index-based and have a size, but is resized when needed. 

* A slice has three major components:

   1. Pointer : used to point to the first element of the array that is accesible through that slice. It is not necessary that the pointed element is laways the first element of the array.
   2. Length : number of elements it contains.  
   3. Capacity : number of elements in the underlying array counting from the first element in the slice. 
   
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

* When you change a value in the slice, it also gets changed in the underlying array, since slice is a reference to an underlying array. 

* append() is a built-in function which adds the elements at the end of the slice. Example,

```
slice = append(slice, 7, 8, 9)
```

<b>NOTE</b>: Capacity of our slice gets doubled whenever we append our slice more than it's present capacity.

* We can append a slice to another slice by using the three dots. Syntax,

```
slice = append(slice, slice_1...)
```

* We can delete elements from a slice by creating anew slice which does not contain the element that has to be deleted. Example,

```
package main

import "fmt"

func main() {
	arr := [10]int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
	i := 2
	fmt.Println(arr)

	slice_1 := arr[:i]
	slice_2 := arr[i+1:]

	new_slice := append(slice_1, slice_2...)
	fmt.Println(new_slice)
}
```
Output,
```
[1 2 3 4 5 6 7 8 9 10]
[1 2 4 5 6 7 8 9 10]
```

* To copy elements from one slice to another we use copy() function. It also returns the number of elements that have been copied which is the minimum of the length of the destination slice or the length of the source slice. Note that the slices must be initialized with tye same data type. Example,

```
package main

import "fmt"

func main() {
	src_slice := []int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
	dest_slice := make([]int, 3)

	num := copy(dest_slice, src_slice)

	fmt.Println(dest_slice)
	fmt.Println("Numbers of elements copied: ", num)
}
```
Output,
```
[1 2 3]
Numbers of elements copied:  3
```

* Looping through a slice is same as looping through an array.

