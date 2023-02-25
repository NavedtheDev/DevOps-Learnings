```
from datetime import datetime

user_input = input("enter your goal and a deadline separated by colon\n")
input_list = user_input.split(":")

goal = input_list[0]
deadline = input_list[1]

deadline_date = datetime.strptime(deadline, "%d.%m.%Y")
today_date = datetime.today()
time_till = deadline_date - today_date

time_remaining = int(time_till.total_seconds() / 60 / 60)
print(f"Time remaining for your goal: {goal} is {time_remaining} hours")
```
