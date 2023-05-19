* What if we want the same script to follow the same sequences without writing additional scripts? 

* One way to do that would be to duplicate the entire set of code. Obviously, it's not a neat approach, because our script has duplicates now, the same set of code multiple times. 

* Second way is to move our code within a function. A function within a shell script is a piece of code or a block of code that performs a particular function that can be reused throughout the script. 

* From anywhere within the script, to run this block of code, we simply need to call the function by it's name and pass in the argument. It's also called as a function parameter. We can call and pass in the arguments multiple number of times. 

* Our script now has two major functions. At the top, we have the function definition. And below, we have the main part of the script that calls that function. 

<b>NOTE:</b> Function must always be defined first before calling it. 

* In functions we need to take care of 'exit' statements. Because if the first script fails, the script will exit. However, we do not want that. We want the script to continue. So, instead of exit statements in functions, we use the 'return' statement. It will print the exit code iof the script as weel as it will not exit the script, it will only exit the function. 

* Return statement in shell scripts do not work like thosein programming languages. They are used to return exit status only. You cannot retrieve the return value by assigning the function call to a variable. Instead, we must retrieve the return code using the '$?' built-in variable that retrieves exit codes of previously run command.  
