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
```
   OR 
```
grades := [3]int{1,2,3}
```
   OR 
```
grades := [...]int{1,2,3}
```

* A simple program,

```
package main

import "fmt"

func main() {
	var nums [3]int = [3]int{1, 2, 3}
	fmt.Println(nums)
}
```
Output,
```
[1 2 3]
```

* We can find the length of an array using a built in length function. The len function over here takes an array as an input and returns us the size of the array. Example,

```
package main

import "fmt"

func main() {
	var nums [3]int = [3]int{1, 2, 3}
	fmt.Println(len(nums))

}
```
Output,
```
3
```

* An array is numbered and these numbers are called array index. The first element of an array has the index zero, while the last element here has the index length minus one. We can access array elements using these indexes as well. Example,

```
package main

import "fmt"

func main() {
	var nums [3]int = [3]int{1, 2, 3}
	fmt.Println(nums[1])
}
```
Output,
```
2
```

* We can loop through an array using for loop.

* We can also loop through an array using the range keyword. The range keyword is mainly used in for loops, in order to iterate over all the elements of an array, slice, or map. 

* For arrays, range sets the scope of iteration up to the length of the array. 

* Syntax, 

```
for index, element := range nums {
	fmt.Println(index, "=>", element)
}
```

* In the case of arrays and slices, the first value returned is the index, and the second value is the element itself. Example,

```
package main

import "fmt"

func main() {
	var nums [5]int = [5]int{1, 2, 3, 4, 5}

	for index, element := range nums {
		fmt.Println(index, "=>", element)
	}
}
```
Output,
```
0 => 1
1 => 2
2 => 3
3 => 4
4 => 5
```








