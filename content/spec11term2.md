## Combinatorics
### Inclusion Exclusion
What is Inclusion 
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
* Given that 


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
### Selections
### How to use case bash
## Vectors
### Addition
### Proofs
### Sin + Cos with vectors
### || and perp vectors
### CAS tutorial
Main website [here](_index.md).
<!---
needs fixing
-->