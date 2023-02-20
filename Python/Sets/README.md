* Unlike Lists datatype, Sets datatype doesn't allow storing duplicate values.
* set( ) function is used to convert an existing list into a set. The parameter of our set( ) function will be the list.
* Lists is represented using [ ] brackets whereas sets is represented using { } brackets.
<br>

* Here is an example on how you can create sets in your program.

```
my_set = {"January", "February", "March"}
for element in my_set:
    print(element)
    
my_set.add("April")            // to add an element in a set
print(my_set)
my_set.remove("January")      //  to delete an element from a set
print(my_set)
```
* However, we cannot access elements of a set like we did on lists. Items in a set set do not have a defined order. 
* Instead we can only access the elements of a set in a loop.
