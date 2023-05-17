* A loop is a sequence of instructions that is continually repeated until a certain condition is reached. 

* Syntax, 

```
for initialization; condition; post {
      // statements 
}
```

   1.This initialization statement is optional and it executes before the for loop starts. It is mostly used in simple statements like variable declarations or increment or assignment statement. <br>
   2. Then we have the condition statement. The condition statement holds a Boolean expression, which is evaluated at the starting of each iteration of the loop. If the value of the conditional statement is true, then the loop will execute. <br>
   3. Then we have the post statement, which is also optional and is executed after each iteration of the for loop. After the post statement, the condition statement evaluates again. If the value of the conditional statement is false, then the loop ends. It can also be written in the loop body.
   
   
   
* If we skip the condition as well, we get an infinite loop. 

* While implementing looping constructs, you would also have scenarios where you want to skip a particular iteration in the loop, or even completely break out of the loop if something happens. We have a statement called break. 

* <b>break</b>: The break statement ends the loop immediately when it is encountered. 

* <b>continue</b>: The continuous statement skips the current iteration of loop and continues with the next iteration.
