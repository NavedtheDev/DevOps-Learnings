* What is $ SHELL in echo $SHELL command ? It is a variable and to be more specific, it is an environment variable. Variables just as in any programming language are used   to store information. In this example, the word SHELL in uppercase represents an environmental variable, which stores the value of the type of shell used by the user.   To print the variable value, We proceed the variable name with a $ symbol.

* Environment variables in specific, store information about the user's login session, which is used by the shell when executing commands. To see a list of all environment variables, use

```
env
```

* To set an environment variable, we can use the export command. Say you want to create a new environment variable called office and set a value of caleston to it. Use     the export command and in the argument, use office = caleston. This will set the variable for the current shell and any other processes or programs started by the     shell. 

## PATH variable ## 

* Speaking about the environment variables, when a user issues an external command into the shell, the shell uses a path variable to search for these external commands. To see the directories defined in the path variable, use the command echo $PATH . If the path variable does not have the location of a command or a program defined, running a command by itself will result in a failure. 
 
* To check if the location of a command can be identified, use the which command. 
