* The <b>try</b> block: let's you "test" a block of code for errors.
* The <b>except</b> block: catches the error and let's you handle it.



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


user_input = input("Hey, enter a value\n")
validate_and_execute()
```
