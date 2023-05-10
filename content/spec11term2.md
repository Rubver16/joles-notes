Hey guys these are not done yet but if you want to have a look through feel free anyways lol contact me if anything is wrong/doesn't make sense
## Combinatorics
### Inclusion Exclusion
What is Inclusion Exclusion principle?
Let $n(X)$ represent the number of things in a set, such as red marbles or people in a team.  
**Two variables**
> $n(A)+n(B)-n(A\cap B)=n(A \cup B)$ 

The idea is that we end up counting the objects in $n(A \cap B)$ twice, we have to subtract the extra's at the end to account for this.  
For example,
* There are 219 people doing methods in our year.
* There are 164 people doing english in our year.

If we were to count the number of people in our year who do methods or english (or both), adding these numbers together would give 383 people, which is way more people than in our year!  
This is because we counted everyone who does methods and english (a lot) twice, once in the 219 people who do methods and once in the 164 people doing english. Therefore, to get the correct answer we have to subtract all the people who do both.

**Three variables**
> $n(A)+n(B)+n(C)-n(A\cap B)-n(B\cap C)-n(A\cap C)+n(A \cap B\cap C)=n(A \cup B \cup C)$ 

This is long. Lets work through it logically by seeing which parts we count too many and not enough times.  

Since we add $n(A)$ and $n(B)$, we end up counting all the objects in $n(A\cap B)$ twice, when we should only count them once, so we need to subtract $n(A\cap B)$. Similarly, we need to subtract $n(B\cap C)$ and $n(A\cap C)$ for the same reason.  
Now, considering $n(A \cap B\cap C)$, we count it three times in $n(A),n(B),n(C)$ and subtract it three times in   
$n(A \cap B),n(B \cap C),n(A \cap C)$, so we don't count it at all. Since we need to count it once, we add it once at the end.
### Pascal's Rule
What is Pascals rule?
> Pascals Rule: $\binom{n}{r}+\binom{n}{r+1}=\binom{n+1}{r+1}$. 

Pascals rule is imporant since it relates the binomial coefficients $\binom{n}{r}$ to the numbers in pascals triangle. Here is an optional explanation below of why if you are interested.  
For example, we know that the third row of Pascals triangle (1, 3, 3, 1) can be represented in binomial coeffecients as follows:  
$\binom{3}{0}$, $\binom{3}{1}$, $\binom{3}{2}$, $\binom{3}{3}$  
Now, we know that the next row of Pascals triangle is defined by the sum of the previous, as such. So the 4th row would look like  
$1$, $\binom{3}{0}$ + $\binom{3}{1}$, $\binom{3}{1}$ + $\binom{3}{2}$, $\binom{3}{2}$ + $\binom{3}{3}$, $1$   
However, **using Pascal's rule**, we also know that $\binom{3}{0}$ + $\binom{3}{1}$=$\binom{4}{1}$, $\binom{3}{1}$ + $\binom{3}{2}$=$\binom{3}{1}$ and $\binom{3}{2}$ + $\binom{3}{3}$=$\binom{4}{3}$. Furthermore, since $1=\binom{4}{0}$ and $1=\binom{4}{4}$, the 4th row can be represented as:  
$\binom{4}{0}$, $\binom{4}{1}$, $\binom{4}{2}$, $\binom{4}{3}$, $\binom{4}{4}$  
Here, what i've shown is that if one row can be represented as binomial coeffecients, the next can also. Furthermore, since the first row (1,1) can be represented as $\binom{1}{0}$, $\binom{1}{1}$, it intuitively follows that the second row can be expressed as $\binom{2}{0}$, $\binom{2}{1}$, $\binom{2}{2}$ too, and so on.

**Why might this show up in a test?**  
Because of pascals rule, we can express pascals triangle in terms of binomial coeffecient. That is, the $n^{th}$ row of pascal's triangle is:  
$\binom{n}{0}$, $\binom{n}{1},\dots,\binom{n}{n-1}$, $\binom{n}{n}$  
In a test, the questions they might ask is to ask to to caluculate binomial coefficients from a row of pascals triangle, or for some binomial coeffecient close to another binomial coeffecient. For example:
* Circle $\binom{6}{4}$ on pascals triangle.
* Given that $\binom{9}{3}=84,\binom{9}{4}=126$, what is $\binom{10}{4}$ ?


We can prove pascals rule in two ways as follows, although i don't think we need to know this (it helps for understanding though):

**Algebraic proof:**
$$
\begin{align*}
    \binom{n}{r}+\binom{n}{r+1}&=\frac{n!}{r! \times (n-r)!}+\frac{n!}{(r+1)!(n-r-1)!}\\
    &=\frac{n! \times (r+1)}{(r+1)! \times (n-r)!} + \frac{n! \times (n-r)}{(r+1)! \times (n-r)!}\\
    &=\frac{n! \times (r+1) + n! \times (n-r)}{(r+1)!\times (n-r)!}\\
    &=\frac{n! \times (n+1)}{(r+1)! \times (n-r)!}\\
    &=\frac{(n+1)!}{(r+1)! \times (n-r)!}\\
    &=\binom{n+1}{r+1}
\end{align*}
$$
If you wish to remember this, the best way to do it is to read through it, understand the idea behind it, and then try to derive it yourself with no notes.
**Combinatorial Proof:**

Note that $\binom{n+1}{r+1}$ is the number of ways to choose $n+1$ objects from $r+1$.
So, lets count the number of ways to select $n+1$ objects from $r+1$ objects. Suppose for example we have $n+1$ marbles and we want to select $r+1$ marbles. Lets paint 1 marble red. Then, we can either select this red marble or not select it.
* If we do choose the red marble, then we need to select $r$ more marbles from the remaining $n$, which we have $\binom{n}{r}$ ways of doing.
* If we don't select the red marble, we need to choose $r+1$, from the remaining $n$, which we have $\binom{n}{r+1}$ ways of doing. 
So, adding up the cases where we select the red and don't select the red marble, we have $\binom{n}{r}+\binom{n}{r+1}$ ways of selecting the $r+1$ objects in total, so $\binom{n}{r}+\binom{n}{r+1}=\binom{n+1}{r+1}$.
### Pigeonhole Principle
What is pigeonhole principle?
> If $n+1$ pigeons are placed into $n$ pigeonholes, then 1 pigeonhole must contain at least 2 pigeons.

This principle is easy to prove: assume for a contradiction that each pigeonhole contains at most 1 pigeon - then there are at most $n$ pigeons, a contradiction. This principle is also quite intuitive - how are you giving each pigeon its own pigeonhole if there are more pigeons than pigeonholes?  
This principle can be extended as well as follows:
> If $an+1$ pigeons are placed into $n$ pigeonholes, 1 pigeonhole must contain at least $a+1$ pigeons.

Again, a similar proof by contradiction works for this - if each pigeonhole contains at most $a$ pigeons, then theres at most $an$ pigeons, a contradiction.  
Although this principle is rather easy to understand, the difficult part is finding out what should be our pigeons and what should be our pigeon holes.

Here are two examples to illustrate how i would approached these problems and my thought process. With practice, you can spot the idea immediately. 

**Problem 1:**  
 There are 35 players on a football team and each player has a different number chosen from 1 to 100. Prove that there are at least four pairs of players whose numbers have the same sum. 

 Here, we want to show that there are pairs of players with the same sum. So, if our pigeonholes are the number of sums, and the number of pairs of players as our pigeons, then by pigeonhole principle we can probably find pairs of players in the with the same sum (i.e. in the same pigeonhole). Therefore, all that is left is to calculate the numbers. Here is how I would write it:

 Let the pairs of players be our pigeons, and the possible sums of the players numbers be our pigeonholes. Therefore, we have $\binom{35}{2}=595$ pigeons. Since the smallest sum is 3 and the largest 199, there are 197 different sums, so 197 pigeonholes. Therefore, since $197 \times 3 + 1= 592 < 595$, one of the pigeonholes has to have at least 4 pigeons, so there do exist 4 pairs with the same sum.

 **Problem 2**  
Seven boys and five girls sit evenly spaced at a round table. Prove that some pair of
boys are sitting opposite each other.  
What does it mean for two boys to be sitting opposite to to each other? Well, it means that if i take two people opposite each other they contain two boys. So, having our pigeons be boys at the table and pigeonholes be the 6 groups of opposite chairs seems like it could work. To clarify, suppose that each person is sitting on a number on a clock face. Our pigeonholes would be seats (12 and 6), (1 and 7), (2 and 8), and so on, where each pigeonhole has two seats opposite each other. Then, since there are 7 pigeons (boys) and 6 pigeonholes (groups of seats), 2 boys must be in the same group of seats, so there must be two boys sitting opposite each other. 

### Selections
### How to use case bash
Some combinatorics problems you just have to break into cases
## Vectors
### Definition
For our purposes, a vector is a line segment with direction and magnitude. We can represent a vector this way, listing its magnitude and direction as such: $3$  $\angle 135^\circ$ (polar form). However, we can also represent a vector as its vertical part and its horizontal part, which we call component form, like $\binom{a}{b} = ai + bj$. Here,     
### Addition
### Proofs
**Problem 1:**
Show that the diagonals of a parallelogram bisect each other.  

As always, we draw a diagram first. Note that i dunno how to place the little squiggly line under variables in the diagrams, so they are omitted (pretend they have squiggly lines underneath them).
![](VectorDiagrams/ParallelogramBisect1.png)
Since we are dealing with a parallelogram, the red vectors are the same, and the blue vectors are the same. Furthermore, we are dealing with diagonals, so lets draw those in.  
![](VectorDiagrams/ParallelogramBisect2.png)
Now, a useful approach to this question is to show that the two midpoints of the purple and green vectors are the same point. So, lets define the midpoints of $AC$ and $BD$ as $M_1$ and $M_2$. Furthermore, lets represent them in terms of $\underset{\tilde{}}{a}$ and $\underset{\tilde{}}{a}$.  
![](VectorDiagrams/ParallelogramBisect3.png)
Here, we have $\vec{AM_1}=\frac{1}{2}\vec{AC}=\frac{{\underset{\tilde{}}{a}+\underset{\tilde{}}{b}}}{2}$.  
Furthermore, $\vec{AM_2}=\vec{AB}+\vec{BM_2}=\underset{\tilde{}}{b}+\frac{{\underset{\tilde{}}{a}}-\underset{\tilde{}}{b}}{2}=\frac{\underset{\tilde{}}{a}+\underset{\tilde{}}{b}}{2}$.  
Therefore, $\vec{AM_1}=\vec{AM_2}$, so $M_1$ is the same point as $M_2$ and therefore the intersection of the lines is a midpoint to both lines, so the diagonals bisect each other.
### Sin + Cos with vectors
### || and perp vectors
### CAS tutorial
Main website [here](_index.md).
<!---
needs fixing
-->