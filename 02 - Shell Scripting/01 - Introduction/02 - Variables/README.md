```
mission_name=lunar-mission
mkdir $mission_name

rocket-add $mission_name

rocket-start-power $mission_name
rocket-internal-power $mission_name
rocket-crew-ready $mission_name
rocket-start-sequence $mission_name
rocket-start-engine $mission_name
rocket-lift-off $mission_name

rocket-status $mission_name
```

* Note, that a variable name may only contain alphanumeric or underscores. Also, it is case-sensitive. 

* We can alo use variables to store the result of another command. Example, 

```
mission_name=lunar-mission
mkdir $mission_name

rocket-add $mission_name

rocket-start-power $mission_name
rocket-internal-power $mission_name
rocket-crew-ready $mission_name
rocket-start-sequence $mission_name
rocket-start-engine $mission_name
rocket-lift-off $mission_name

rocket_status=$(rocket-status $mission_name)
echo "Status of launch: $rocket_status"
```
