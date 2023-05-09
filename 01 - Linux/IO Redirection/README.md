* Let us get familiar with the concept of standard streams in Linux. There are three data streams created when you launch a Linux command. 

   1. Stdin is the standard input string. This accepts text as its input. 
   2. Text output from the command that you see printed on your screen is delivered via the stdout or the standard out stream. 
   3. Error messages from the command are sent through the standard error stream, with IO redirection. 
   
* The standard input-output and error can be redirected to text files. Let's see how to do that next. 

* To redirect standard output to a file instead of printing it on the screen, we can use the forward arrow symbol followed by the name of the file. The forward arrow symbol overwrites the contents of the file with the stdout. Example,

```
echo $SHELL > shell.txt
```

```
cat shell.txt
/bin/bash
```

* If you want to append stdout to an existing file, use the double forward arrow symbol. 

```
echo "Bash shell" >> shell.txt
```

```
cat shell.txt
/bin/bash
Bash shell
```

* In order to redirect just the error messages, we need to use the number 2 followed by a forward arrow symbol, and then the name of the file in which the errors will be written. Example,

```
cat missing_file 2> error.txt
```

```
cat error.txt
cat: missing_file: No such file or directory
```
If the file doesn't exist, a new one will be created. Otherwise, the file will be overwritten. 

* To append the standard error to an existing file, use the number 2 double forward symbol. Example,

```
cat missing_file 2>> shell.txt
```

```
cat shell.txt
cat: missing_file: No such file or directory
```

* If you want your command to execute and not print error messages on the screen, even if it generates a standard error, you can redirect to /dev/null, like this. 
* /dev/null is referred to as the bit bucket. The place where you dump anything you don't need, in this case, the standard error, which we do not want to be printed on the screen. 

* Another useful command to work with standard input and standard output is the tee command. Instead of the redirect operator, we can use a command-line pipe followed by the tee command and the file name to redirect the output. The difference is that with tee, the standard output is still printed on the screen before overwriting the contents of the file with the same string. 

* Use tee -a option to append the file instead of overwriting it. 







