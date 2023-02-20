* Loops are used to execute logic multiple times.
* Python has 2 loop commands.

## While Loops ##
* It executes a set of statements as long as a condition is true.
* Here is an example.



```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days):
    return f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}"


def validate_and_execute():
    try:
        user_input_number = int(user_input)
        if user_input_number > 0:
            calculated_value = days_to_units(user_input_number)
            print(calculated_value)
        elif user_input_number == 0:
            print("0 is not an accepted input here")
        else:
            print("you entered a negative number")
    except ValueError:
        print("Your input is not a number")


user_input = ""
while user_input != "exit":
    user_input = input("Hey, enter a value\n")
    validate_and_execute()
```


## Lists and For Loops ##


* Lists is a datatype to store multiple items in a single variable.
* split( ) is a function that returns the lists of any input value.
* Here is an example.

```
calculation_to_units = 24 * 60 * 60
name_of_unit = "seconds"


def days_to_units(num_of_days):
    return f"{num_of_days} Days are {num_of_days * calculation_to_units} {name_of_unit}"


def validate_and_execute():
    try:
        user_input_number = int(num_of_days_element)
        if user_input_number > 0:
            calculated_value = days_to_units(user_input_number)
            print(calculated_value)
        elif user_input_number == 0:
            print("0 is not an accepted input here")
        else:
            print("you entered a negative number")
    except ValueError:
        print("Your input is not a number")


user_input = ""
while user_input != "exit":
    user_input = input("Hey, enter a value\n")
    print(type(user_input.split(", ")))
    print(user_input.split(", "))
    for num_of_days_element in user_input.split(", "):
        validate_and_execute()
```



* You must be wondering on how to create lists within our program.
* Here is an example.

```
my_list = ["January", "February", "March"]
print(my_list[2])
my_list.append("April")
print(my_list)
print(my_list[3])
```

* append( ) is a function which is used to add a new item to a list.
