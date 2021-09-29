# RECURSION IN COMPETITIVE CODING <img src = "https://media1.giphy.com/media/JZ40cnfnN11KycrvMF/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width = 70px>

> Recursion can be defined as the technique of replicating or doing again an activity in a self-similar way calling itself again and again, and the process continues till specific condition reaches. 
> In the world of programming, when your program lets you call that specific function from inside that function, then this concept of calling the function from itself can be termed as recursion, and the function which makes this possible is called recursive function. 

<hr>

![image](https://user-images.githubusercontent.com/77975418/135303750-3d3a0231-1ce2-468c-9eb6-83690582b3df.png)

<h2>Recursion is really easy to understand. It is essentially a function calling itself.<h2>
  
# ILLUSTRATION BY CODE:
Just imagine writing a function that calculates the factorial of a number n (n!). 

Lets see how it would expand for 4!. Remember that 1! = 1.
  
(factorial 4)
  
(4 * (factorial 3))
  
(4 * (3 * (factorial 2)))
  
(4 * (3 * (2 * (factorial 1))))
  
(4 * (3 * (2 * 1)))
  
(4 * (3 * 2))
  
(4 * 6)
  
(24)

The factorial keeps multiplying the current number by the factorial of the number before it (4 * 3!) until it reaches its terminating condition (1! = 1) which then allows all the functions before it to evaluate the return statement (n * factorial(n-1)) and pass it back up the stack.
  
> <h3>Translated to C++ code: <h3>

int factorial(int n)
  
	if(n == 1)
  
		return 1;
  
	else
  
		return n * factorial(n-1);
  

A recursive function takes an input, determines if it should stop (here, if n == 1) or perform an operation (here, multiplying n by something) and passing the remainder of the argument (here, all of the numbers less than n, and > 1) to itself to do it all over again until it stops.
  
Every time you call a function, the computer goes off to evaluate that function for the arguments you passed in and then when that is done, it returns back to the original function call and returns a value. 

So when you call return n * factorial(n-1) the computer stops here to go evaluate factorial(n-1) and so on and so on until something different comes back (1) which then allows all of the stopped processes to return a value.

<b>For a better illustration on recursion through graphical representation and codes refer to the SOlved Examples Folder<b>
