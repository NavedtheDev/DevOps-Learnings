* What if we want the same script to follow the same sequences without writing additional scripts? 

* One way to do that would be to duplicate the entire set of code. Obviously, it's not a neat approach, because our script has duplicates now, the same set of code multiple times. 

* Second way is to move our code within a function. A function within a shell script is a piece of code or a block of code that performs a particular function that can be reused throughout the script. 

* From anywhere within the script, to run this block of code, we simply need to call the function by it's name and pass in the argument. It's also called as a function parameter. We can call and pass in the arguments multiple number of times. 

* Our script now has two major functions. At the top, we have the function definition. And below, we have the main part of the script that calls that function. 

<b>NOTE:</b> Function must always be defined first before calling it. 
