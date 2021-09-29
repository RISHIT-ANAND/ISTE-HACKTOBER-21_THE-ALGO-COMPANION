
The image above says a lot about Dynamic Programming. So, is repeating the things for which you already have the answer, a good thing ? A programmer would disagree. That's what Dynamic Programming is about. To always remember answers to the sub-problems you've already solved.

Dynamic programming is basically, recursion plus using common sense. 

What it means is that recursion allows you to express the value of a function in terms of other values of that function. Common sense tells you that if you implement your function in a way that the recursive calls are done in advance, and stored for easy access, it will make your program faster. 

This is what we call Memoization - it is memorizing the results of some specific states, which can then be later accessed to solve other sub-problems


Let us say that we have a machine, and to determine its state at time t, we have certain quantities called state variables. There will be certain times when we have to make a decision which affects the state of the system, which may or may not be known to us in advance. These decisions or changes are equivalent to transformations of state variables. The results of the previous decisions help us in choosing the future ones.


We need to break up a problem into a series of overlapping sub-problems, and build up solutions to larger and larger sub-problems. If you are given a problem, which can be broken down into smaller sub-problems, and these smaller subproblems can still be broken into smaller ones - and if you manage to find out that there are some overlapping subproblems, then you've encountered a DP problem


The intuition behind dynamic programming is that we trade space for time, i.e. to say that instead of calculating all the states taking a lot of time but no space, we take up space to store the results of all the sub-problems to save time later.




A simple lay man illustration

Writes down "1+1+1+1+1+1+1+1 =" on a sheet of paper.

"What's that equal to?"

Counting "Eight!"

Writes down another "1+" on the left.

"What about that?"

"Nine!" " How'd you know it was nine so fast?"

"You just added one more!"

"So you didn't need to recount because you remembered there were eight! Dynamic Programming is just a fancy way to say remembering stuff to save time later!"

Let's try to understand this by taking an example of Fibonacci numbers.

Fibonacci (n) = 1; if n = 0

Fibonacci (n) = 1; if n = 1

Fibonacci (n) = Fibonacci(n-1) + Fibonacci(n-2)

So, the first few numbers in this series will be: 1, 1, 2, 3, 5, 8, 13, 21... and so on!

A code for it using pure recursion:

 int fib (int n)
 
 {
 
        if (n < 2)
        
            return 1;
            
        return fib(n-1) + fib(n-2);
        
    }
    
Using Dynamic Programming approach with memoization:

void fib () 

{

        fibresult[0] = 1;
        
        fibresult[1] = 1;
        
        for (int i = 2; i<n; i++)
        
           fibresult[i] = fibresult[i-1] + fibresult[i-2];
           
    }
    
# Are we using a different recurrence relation in the two codes? No. Are we doing anything different in the two codes? Yes.

In the recursive code, a lot of values are being recalculated multiple times. We could do good with calculating each unique quantity only once. Take a look at the image to understand that how certain values were being recalculated in the recursive way:


# Majority of the Dynamic Programming problems can be categorized into two types:

1. Optimization problems.

2. Combinatorial problems.

Every Dynamic Programming problem has a schema to be followed:

- Show that the problem can be broken down into optimal sub-problems.
- Recursively define the value of the solution by expressing it in terms of optimal solutions for smaller sub-problems.
- Compute the value of the optimal solution in bottom-up fashion.
- Construct an optimal solution from the computed information.

# Bottom up vs. Top Down:

> Bottom Up - I'm going to learn programming. Then, I will start practicing. Then, I will start taking part in contests. Then, I'll practice even more and try to improve. After working hard like crazy, I'll be an amazing coder.

> Top Down - I will be an amazing coder. How? I will work hard like crazy. How? I'll practice more and try to improve. How? I'll start taking part in contests. Then? I'll practicing. How? I'm going to learn programming.
