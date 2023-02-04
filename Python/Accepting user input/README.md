* In order to make our program more convenient, our program should be able to accept any input.
* The input value that we get from input() function, is always treated as a string and not a number.
* Process of turning one data type to another is called casting.
* Here is an example.

```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days):
    return f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}"
    
    
user_input = input("Hey, enter a value\n")
user_input_number = int(user_input)

calculated_value = days_to_units(user_input_number)
print(calculated_value)
```
