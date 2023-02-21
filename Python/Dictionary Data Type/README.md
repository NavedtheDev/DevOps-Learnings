* It is a data type which is used to store <b>key:value</b> pairs.
* It does not allow duplicate values.
* Example,
```
days_and_unit_dictionary = {"days": 20, "unit": "hours"}
```



### Accesing items ina dictionary ###

* Items can be accessed by its <b>key name</b>.
* You can use <b>square brackets</b> or <b>get()</b> method.
* Example,
```
days_and_unit_dictionary["days"]

          OR
                   
days_and_unit_dictionary.get("days")
```



Now, our new program will look like this, 
```
def days_to_units(num_of_days, conversion_unit):
    if conversion_unit == "hours":
        return f"{num_of_days} Days are {num_of_days * 24} {conversion_unit}"
    elif conversion_unit == "minutes":
        return f"{num_of_days} Days are {num_of_days * 24 * 60} {conversion_unit}"
    else:
        return "unsupported unit"


def validate_and_execute():
    try:
        user_input_number = int(days_and_unit_dictionary["days"])

        # we want to do conversion only for positive numbers
        if user_input_number > 0:
            calculated_value = days_to_units(user_input_number, days_and_unit_dictionary["unit"])
            print(calculated_value)
        elif user_input_number == 0:
            print("0 is not an accepted input here")
        else:
            print("you entered a negative number")
    except ValueError:
        print("Your input is not a number")


user_input = ""
while user_input != "exit":
    user_input = input("Hey, enter number of days and conversion unit!\n")
    days_and_unit = user_input.split(":")
    print(days_and_unit)
    days_and_unit_dictionary = {"days": days_and_unit[0], "unit": days_and_unit[1]}
    print(days_and_unit_dictionary)
    print(type(days_and_unit_dictionary))
    validate_and_execute()
```
