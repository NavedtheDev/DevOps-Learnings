* Avariable is only available from inside the region it is created.

* <b>Global Scope</b> = variables available from within any scope
* <b>Local Scope</b> = variables created inside any function can only be used inside that function



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

In the above example, the two variables passed in the function parameter are available only inside that function because they were created within that function.
