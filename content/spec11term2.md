## Combinatorics
### Inclusion Exclusion

### Pascal's Rule
Pascals Rule states that $\binom{n}{r}+\binom{n}{r+1}=\binom{n+1}{r+1}$. Right now, this doesn't seem particularly, important, but this gives us reasoning as to why the numbers in pascals triangle are actually binomial coefficients $\binom{n}{r}$. For example, we know that the third row of pascals triangle (1 3 3 1) can be represented in binomial coeffecients as follows:  
$$\binom{3}{0}$$ $$\binom{3}{1}$$ $$\binom{3}{2}$$ $$\binom{3}{3}$$



We can prove this in two ways as follows, although i don't think we need to know this (it helps for understanding imo):

Algebraic proof:
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
Combinatorial Proof:

Note that $\binom{n+1}{r+1}$ is the number of ways to choose $n+1$ objects from $r+1$.\\
So, lets count the number of ways to select $n+1$ objects from $r+1$ objects. Suppose for example we have $n+1$ marbles and we want to select $r+1$ marbles. Lets paint 1 marble red. Then, we can either select this red marble or not select it.
* If we do choose the red marble, then we need to select $r$ more marbles from the remaining $n$, which we have $\binom{n}{r}$ ways of doing.
* If we don't select the red marble, we need to choose $r+1$, from the remaining $n$, which we have $\binom{n}{r+1}$ ways of doing. 
So, adding up the cases where we select the red and don't select the red marble, we have $\binom{n}{r}+\binom{n}{r+1}$ ways of selecting the $r+1$ objects in total, so \\$\binom{n}{r}+\binom{n}{r+1}=\binom{n+1}{r+1}$.
### Pigeonhole Principle
### Selections
### How to use case bash
## Vectors
### Addition
### Proofs
### Sin + Cos with vectors
### || and perp vectors
### CAS tutorial

Main website [here](_index.md). 