* A function is defined using the 'def' keyword. 
* Syntax,
```
def <name_of_function>():
    line 1 of code
    line 2 of code
```



* Here is an example of how to use function in Python.
```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units():
    print(f"20 Days are {20 * calculation_to_units} {name_of_unit}")
    print("All Good!")


days_to_units()
```
Output of the above program will be,
```
20 Days are 1728000 seconds
All Good!
```
Note that the function will not be executed unless and until it is called.



# Function Parameters #
* Information can be passed into functions as parameters.
* Parameters are also called arguments.
* Here is an example,
```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days, custom_message):
    print(f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}")
    print(custom_message)


days_to_units(20, "Awesome!")
days_to_units(35, "Looks good")
days_to_units(50, "nice")
days_to_units(110, "great")
```
Output of the above program will be,
```
20 Days are 1728000 seconds
Awesome!
35 Days are 3024000 seconds
Looks good
50 Days are 4320000 seconds
nice
110 Days are 9504000 seconds
great
```
