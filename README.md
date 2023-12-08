[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12218193&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

## My Response

1.
The first is that when we are analyzing an algorithm we ignore any constants that might arise, this can change things significantly.  On a lower level, $x^2$ and $4x^2$ are not the same function even though the would have the same complexity, $4x^2$ increases faster than its parent function.

The second is that the complexity of an algorithm doesn't take into account the hardware of the machine running the program.  It could run faster or slower based on the resources available.

Cade brought up this one while I was talking to him in lab.  The bounds of our complexity can come into question for instance a program might have upper and lower are $2^n$ and $n$ respectively, which are two very different functions that leave a lot of room for movement between them.

2.
According to Wikipedia the average time complexity of searching for a value in a binary search tree is $log(n)$, with this we can compute the approximate time for the program to finish.

first we need the values of $log(1000)$ and $log(10000)$ these we can then put into a ratio as to the difference between 1000 elements and 10000 elements

$log(1000) = 3$

$log(10000) = 4$

Now we can build an equation similar to how chemistry builds their unit conversions $5seconds/3searches * 4searches / 1$ this would cancel out our searches and leave us with $5seconds / 3 * 4 / 1$ which further simplifies to $1.6667seconds * 4 \approx 6.7seconds$.

3.
The algorithm might not be written in a way that meets the expected time complexity, as in the program might still find the value we're looking for in the tree but an error in the code means that it is not a fully proper tree search algorithm with a complexity of $\Theta(logn)$.

Like with the second point I provided above, these two different algorithms might have been run on two different computers or something was going on in the background that was taking up avaliable resources, then the two different runs could still have the same asymptotic complexity but they wouldn't necessarily have predictable outcomes.

The graph might be made up of different data types, such as strings and integers, and if that is the case then it can take longer since strings can be very long, the time it takes the program to check a value can add up if it is having to comb through many different long strings.  Such as, if we were looking for a value at one point but there are a bunch of long city names, such as "Mooselookmeguntic, Maine" (I did have to google long city names for that one, I know of a couple but have no idea how to spell them) above it the program would take a while checking each of those names against the desired search value.








