* A slice is an abstraction of an array. 

* They are also index-based and have a size, but is resized when needed. 

* A slice has three major components:

   1. Pointer : used to point to the first element of the array that is accesible through that slice. It is not necessary that the pointed element is laways the first element of the array.
   2. Length : number of elements it contains.  
   3. Capacity : number of elements in the underlying array counting from the firast element in the slice. 
   
* Length and capacity of a slice can be obtained from functions len() and cap() respectively. 

* To declare a slice, we declare an array without any size.

```
<slice_name> := []<data_type>{<values>}
```
Example,
```
nums := []int{1,2,3}
```

