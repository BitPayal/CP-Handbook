`                                           `**RECURRSION**

Recursion is defined as a process which calls itself directly or indirectly and the corresponding function is called a recursive function.

**PROPERTIES OF RECURRSION**

1-The primary property of recursion is the ability to solve a problem by breaking it down into smaller sub-problems, each of which can be solved in the same way.

2-A recursive function must have a base case or stopping criteria to avoid infinite recursion.

3-Recursion involves calling the same function within itself, which leads to a call stack.

4-Recursive functions may be less efficient than iterative solutions in terms of memory and performance.

**TYPES OF RECURRSION**

1-Tail recursion,  

2-Head recursion,  

3-Tree recursion and 

4-Nested recursion.

For further info about the types, check out this link :[TYPES OF RECURRSION](https://www.geeksforgeeks.org/types-of-recursions/)

**MATHEMATICAL INTREPRTATION:**

Used for repetitive computations in which each action is stated in terms of a previous result e.g.: fact(n) = n \* fact (n-1)

**STEPS:**

•For a problem to be written in recursive form, two conditions are to be satisfied

`   `1-It should be possible to express the problem in recursive form, Solution of the problem in terms of solution of the same problem on smaller sized data i.e. try to find sub problem in the problem.

2- The problem statement must include a stopping condition

**EXAMPLE:**
**
`          `Factorial(n)   =1                                        if n=0 --------> **STOPPING CONDITION**

`                                          `=n\*factorial(n-1)           if n>0 --------->**RECURSIVE DEFINITION**

Let's understand it by executing a simple factorial code:

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.001.png)

FOR BETTER UNDERSTANDING, LET’S SEE THE STEPS ONE BY ONE.

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.002.png)

**EXAMPLE 2:    FIBONACCI SERIES**
**
`   `It is a series starting from 0 and 1 and the next element is the sum of the previous two elements.

By reading this statement, you should get the idea of the recurrence definition of the program

i.e𝑓𝑖𝑏𝑛=𝑓𝑖𝑏𝑛−1+𝑓𝑖𝑏𝑛−2

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.003.png)
**


`                        `By the above two problems, you must have got the idea of recursion. for some recursion problem there is iterative problem possible.

**DRAWBACK OF RECURRSION OVER ITERATION**

**Recursion uses a memory stack, and it stays inside the memory until it gets its return value. As** recursion call the function itself again, after reaching the stopping condition it returns the value, but till then the function calls remain in the memory stack.

Iteration solves this memory overhead problem.

**AN EFFICIENT ITERATIVE CODE FOR FIBONACCI SERIES**

We can use three variables: first term, second term and next term, with first term as 0 and second term as 1 and start the loop for size of series of we want. In each step next term can be calculated as first term + second term, then print this value, after that store the value of second term in first term variable, and next term value in second term variable and cycle goes on

FOR BETTER UNDERSTANDING REFER TO THE CODE BELOW:

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.004.png)

Here there is no stack overhead **Space complexity: O (1)**

**Tower of Hanoi**

**Objective:** To solve the Tower of Hanoi puzzle that contains three disks. The stack of disks has to be shifted from Rod 1 to Rod 3 by abiding by the set of rules that has been mentioned above.

Follow the steps below to solve the problem:

- Create a function **towerOfHanoi** where pass the **N** (current number of disk), **from\_rod**, **to\_rod**, **aux\_rod.**
- Make a function call for N – 1 th disk.
- Then print the current the disk along with **from\_rod** and **to\_rod**
- Again make a function call for N – 1 th disk.



`         `![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.005.png)

`       `TIME COMPLEXITY

The time complexity of the Tower of Hanoi solution using stacks is O(2^n), where n is the number of disks. This is because the number of moves required to solve the Tower of Hanoi problem grows exponentially with the number of disks. For each disk, there are two possible moves, leading to a total of 2^n moves.

`                                                            `RECURSIVE TREE

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.006.png)

`                                       `FLOWCHART

|![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.007.png)||
| :- | :- |



`                                                    `**Josephus Problem**

OBJECTIVE:The problem is, there are a total **n** numbers of people in a circle. There is a sword in the hand of 1st person (at position 1), and he has to kill a **kth** person from him, and then pass the sword to the person next to the one who got killed. After doing the same process several times, only one person will be left safe, so we have to find that safe position.

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.008.png)![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.009.png)

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.010.png)![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.011.png)



RECURSIVE APPROACH

We can write the Josephus Function as :

**Josephus(n, k) = (Josephus(n — 1, k) + k-1) % n + 1**

After the first person (kth from the beginning) is killed, n-1 persons are left. So we call Josephus(n — 1, k) to get the position with n-1 persons. But the position returned by Josephus(n — 1, k) will consider the position starting from k%n + 1. So, we must make adjustments to the position returned by Josephus(n — 1, k).

![](Aspose.Words.f8727895-c832-47e9-80a9-3b740011b5b9.012.png)
#

||<p></p><p>**PRACTICE QUESTIONS**</p><p>1\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/B></p><p>2\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/J></p><p>3\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/I></p><p>4\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/L></p><p>5\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/L></p><p>6\. <https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/R></p><p>7\. [https://codeforces.com/group/MWSDmqGsZm/contest/223339/proble](https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/U)</p><p>[m/U](https://codeforces.com/group/MWSDmqGsZm/contest/223339/problem/U)</p><p></p><p></p><p></p><p></p><p></p><p>Happy Coding :)</p><p></p>|
| :- | :- |

