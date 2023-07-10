* There are different ways of performing arithmetic operations in shell. 

* One is using the expression command, run as expr. Example,

```
expr 2 + 9
```
Output,
```
11
```
<b>NOTE:</b> The operator and the values must be separated by a space. 

Similarly, we can do other mathematical operations like subtraction, multiplication and division. While doing multiplication, we must escape the star symbol with a backslash, because star is a reserved character in shell. Example,

```
expr 2 \* 9
```
Output,
```
18
```

This method can also be done using varaiable substitution. Example,

![Screenshot (170)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/cb3bbefd-631d-4c2d-929b-eddacac4df23)



* Another way to perform arithematic operations in bash is to use double parentheses. Example,

![Screenshot (171)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/b202b710-ff2b-42ae-9c55-1d9ee58f72ad)



* Both of these above methods only return decimal output, not floating-point numbers. For this we can use the 'bc' utility. Example,

![Screenshot (172)](https://github.com/NavedtheDev/DevOps-Learnings/assets/98219227/da09b562-6759-4bd5-9c36-3df5850da3b6)
