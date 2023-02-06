```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days):
    if num_of_days > 0:
        return f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}"
    else:
        return "Wrong Input"


user_input = input("Hey, enter a value\n")
user_input_number = int(user_input)

calculated_value = days_to_units(user_input_number)
print(calculated_value)
```



## Boolean Data Type ##

* Boolean can only have two values: <b>TRUE</b> or <b>FALSE</b>

```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days):
    print(num_of_days > 0)       // this will print either TRUE or FALSE
    if num_of_days > 0:
        return f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}"
    elif num_of_days == 0:      //  elif is a combination of else and if
        return "0 is not an accepted input here"
    else:
        return "Wrong Input"


user_input = input("Hey, enter a value\n")
user_input_number = int(user_input)

calculated_value = days_to_units(user_input_number)
print(calculated_value)
```



* type( ) prints out the data type of the variable. For example,

```
condition_check = num_of_days > 0
print(type(condition_check))       // an example of nested function call
```
* Another small example,
```
print(type(30.99))
```
