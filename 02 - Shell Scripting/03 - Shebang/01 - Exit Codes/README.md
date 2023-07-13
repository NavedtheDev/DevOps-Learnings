* When we run a command, it is either successful or failed. Apart from the message that we see on our screen, each command also returns an exit code or a return code. 

* A successful command returns an exit status of zero, and a failed command returns an exit status that is not zero(>1). 

* Where do we see these exit codes? Exit code of a command is stored in a special built-in variable called dollar question mark. To see the xit code of a command, run,

```
echo $?
```

<b>NOTE:</b> This gets updated immidiately after a command is run, so the output is only reliable once, right after the command finishes it's execution and before we run any other command, including the echo $ command itself. 

* It's a good practice to use exit codes in your script to indicate to the caller or the user of the script, the status of your script. 

* If we don't specify any exit status, then the script will always automatically set the exit code to zero. For the script to return non-zero when the script is failed, enter the statement 'exit 1' . 

* As a best practice, always make sure your script returns an appropriate exit code.
