\documentclass{article}
\usepackage{graphicx} % Required for inserting images
\usepackage{geometry}
\usepackage{uwamaths,xcolor,wasysym,framed}
\geometry{a4paper, left=20mm, right=20mm, top=20mm}
\title{meth test wk2 notes}
\author{jole + yap formatting lol}
\date{April 2023}

\begin{document}

\maketitle
\section*{Introduction}
Hello! Here are some notes that I have written up based on the chapters for 3, 4, and 7. The size of this document may be intimidating, but these notes are intended to be understood and explanatory rather than something to be memorized. I'm not in any year 11 methods classes, so these notes aim to explain the Cambridge chapters that i believe are in the test in maybe a more accessible way. 
\section*{Graphing}
This is a general statement about graphing - here are my tips and tricks:
\begin{itemize}
    \item Draw graphs by plotting important/random points and drawing an appropriate shape through the points.
    \item When graphing, the most important thing to do is to LABEL IMPORTANT POINTS (and asymptotes for hyperbolas). Important points include x-intercepts, y-intercepts, turning points for quadratics, and equations of asymptotes.
    \item When reading graphs, use information they give to you clearly to substitute into a form you know. For example, if there are clear x-intercepts given for a quadratic, use those to fill in information about the quadratic in factored form. Don't go looking for a turning point if it isn't given to you!
    \item If you have some variables left that you need to solve for, find some points and substitute the x, y values into the equation. This will give you an equation or simultaneous equations that will let you solve for these variables. For example, suppose that I know my graph is $y=a(x-1)(x+3)$. I would then find a point, which could be for example $(0,8)$, to substitute in to solve for $a$.
\end{itemize}
\section{Quadratics}
\subsection{Forms of a quadratic}
There are 3 forms of a quadratic. (Please note that the following values of $a,b$ and $c$ are usually not equal between forms, and I just only want to use 3 letters.)
\begin{itemize}
    \item Standard form: $ax^2+bx+c=0$\\
    Standard form is not particularly useful, but you will often get questions with quadratics in standard form and have to convert them to another form. However, $(0,c)$ is the y-intercept.
    \item Factored form: $a(x-b)(x-c)=0$\\
    Factored form is especially useful for solving quadratics. Note that simply substituting b and c both give 0 on the left hand side, as it is multiplied by 0, so this quadratic has solutions $x=b$ and $x=c$. Therefore, the x-intercepts are $(b,0)$ and $(c,0)$.
    \item Vertex form: $a(x-b)^2+c=0$\\
    This form is special as it helps us find the \textbf{maximum or minimum} (which is also the turning point or vertex). This is due to $(x-b)^2$ always being positive, and therefore $a(x-b)^2$ having the same sign as $a$. Therefore, the extreme cases, where the minimum or maximum is reached, occurs when $(x-b)^2$ is 0, or when $x=b$. The turning point here is therefore $(b,c)$.
\end{itemize}

\subsection{Factorising Quadratics}
Why do we even want to factorise anyways? Well, suppose we want to solve the equation $x^2+11x+24=0$. Lets expand a seemingly unrelated factored quadratic like $(x+3)(x+8)$.
\begin{align*}
(x+3)(x+8)&=x^2+3x+8x+3 \times 8 \\
&= x^2 + (3+8)x + 3 \times 8 \\
&= x^2 + 11x + 24
\end{align*}
Therefore, we have that $(x+3)(x+8)=x^2+11x+24$. Shockingly, they are the same! So, we can solve this quadratic as follows:
\begin{align*}
    0&=x^2+11x+24\\
    &=x^2+3x+8x+3\times 8\\
    &=(x+3)(x+8)
\end{align*}
Notice we have $(x+3)$ and $(x+8)$ multiplying to 0. If neither are 0, their product wouldn't be 0, so one of the factors must be 0 (this is otherwise known as null factor law).  Therefore, either $x+3=0$ or $x+8=0$, so $x=3$ or $x=8$ and the equation is solved. Here, we saw that by rewriting the quadratic as two factors that multiplied to 0, the equation magically solved itself! However, how do we find these two factors?\\ \\
\noindent \textbf{How to Factorise:}
If we take a monic factorised quadratic in a general form, we can expand it to get \\
$(x-a)(x-b)=x^2-(a+b)x+ab$.
Therefore, for \textbf{monic} quadratics $x^2+px+q$ if we can find $a$ and $b$ such that $a+b=-p$ and $ab=q$, we have 
$$x^2+px+q=x^2-(a+b)x+ab=(x-a)(x-b)$$
which factorises the quadratic. Unfortunately, we have to use intuition and trial and error to find these two numbers. What I like to do is list the pairs of factors in my head that multiply to the last number, and use trial and error adding them up until I find a pair that works. With practice it becomes much easier, so do some practice questions. 
\begin{framed}
\noindent \textbf{Example 1.} Find the solutions of $x^2+2x-15=0$.
\end{framed}
\begin{proof}
We want to find $a+b=-2$ and $ab=-15$. Now we go through all the factors that multiply to $-15$ (be careful with negatives!)\\
We have $(1,-15)$ and $(-1,15)$, $(3,-5)$, $(-3,5)$ are all the pairs with two integers that multiply to $-15$. The corresponding sums of each pair are $-14,14,-2,$ and $2$. Note that we are looking for $a+b=-2$ and $ab=-15$, and our search shows that the third pair $(3,-5)$ fills this condition. 
\begin{align*}
    \therefore \text{ Since } 3-5=-2, 3 \times -5 = -15&, x^2+2x-15=(x-3)(x-(-5))=(x-3)(x+5).\\
    \therefore x-3=0 &\text{ or } x+5=0\\
    \therefore x=3 &\text{ or } x=-5
\end{align*}
\end{proof}
For non-monic quadratics, the process is quite similar. If u can, try and take a common factor out. For example, $2x^2+4x-6=2(x^2+2x-3)$, which can then be factorised similar to before. If this is not possible to do without creating fractions, then we have to take a slightly different approach. \\
Note that $(ax-b)(cx-d)=acx^2-(ad+bc)x+bd$. So, for monic quadratics, $a=c=1$. However, for non-monic quadratics, we have to take these into consideration when doing trial and error. Again, practice is the best way to get better at this, but I will work through an example below:
\begin{framed}
    \textbf{Example 2:} Solve $2 x^2 + 5 x - 12=0$
\end{framed}
Since 2 can only be described as a product of 2 and 1, we aim to factorise this quadratic as:\\
$2x^2+5x-12=(2x-a)(x-b)$. \\
Therefore, we are looking for $a,b$ such that $a+2b=-5$, $ab=-12$. Looking at the second condition first, we find that there are the following pairs $(a,b)$ that satisfy this condition:\\
$(1,-12),(2,-6),(3,-4),(4,-3),(6,-2),(12,-1)$,\\ and inspecting each we find that $a+2b=-5$ occurs when $a=3, b=-4$, which is the third pair. Therefore, 
\begin{align*}
2x^2+5x-12&=(2x-3)(x+4)\\
\therefore 0&=(2x-3)(x+4)\\
2x-3=0 &\text{ or }x+4=0\\
x=\frac{3}{2} &\text{ or }x=-4
\end{align*}
This is a similar process, just accounting for some extra multiplication.
\subsection{Completing the Square}
For this chapter, I will first provide a little bit of motivation behind why we complete the square. 
First, lets solve a simple quadratic, $x^2=9$.\\
\begin{align*}
x^2&=9\\
\sqrt{x^2}&=\pm \sqrt{9}\\
x=3 &\text{ or } x=-3
\end{align*}
Here the process was quite simple - we just square rooted both sides (and accounted for the negative solution as well!)
Now, notice that if we have any square in place of $x^2$, we can do the same thing. For example, lets solve what seems to be a more complicated quadratic, $x^2+2x+1=9$. However, this is not very difficult at all once we realise that $(x+1)^2=x^2+2x+1$.
\begin{align*}
    x^2+2x+1&=9\\
    (x+1)^2&=9\\
    x+1=3 &\text{ or } x+1=-3\\
    x=2 &\text{ or } x=-4\\
\end{align*}
Furthermore, if we take another quadratic like $x^2+2x+5=13$, we can break it up into $(x^2+2x+1)+4=13$, so $x^2+2x+1=9$ as before. As we can see, the constant term doesn't matter at all as we can just separate it out to leave a square behind (9 is not important, we can use any other number). Furthermore, this doesn't just apply to $(x+1)^2$ and applies to any square, since we know that 
$(x+a)^2=x^2+2ax+a^2$.\\
Therefore, to complete the square on $x^2+bx+c$, since we know $(x+\frac{b}{2})^2=x^2+bx+\frac{b^2}{4}$,
\begin{align*}
    x^2+bx+c&=(x^2+bx+\frac{b^2}{4})-\frac{b^2}{4}+ c\\
    &=(x+\frac{b}{2})^2+c-\frac{b^2}{4}
\end{align*}
For example,
\begin{framed}
    \textbf{Example 3:} Solve $x^2+3x-6=0$.
\end{framed}
We are going to complete the square. Note that $(x+\frac{3}{2})^2=x^2+3x+\frac{9}{4}$.
\begin{align*}
    0&=x^2+3x-6\\
    &=(x+\frac{3}{2})^2-6-\frac{9}{4}\\
    &=(x+\frac{3}{2})^2-\frac{33}{4}\\
    \frac{33}{4}&=(x+\frac{3}{2})^2\\
    \pm\frac{\sqrt{33}}{2}&=x+\frac{3}{2}\\
    \frac{-3\pm\sqrt{33}}{2}&=x
\end{align*}
\subsection{Quadratic Formula}
The quadratic formula is the result of the general case of completing the square. Suppose we have $ax^2+bx+c=0$. Therefore,
\begin{align*}
    0&=x^2+\frac{b}{a}x+\frac{c}{a}\\
    &=(x+\frac{b}{2a})^2-\frac{b^2}{4a^2}+\frac{c}{a}\\
    &=(x+\frac{b}{2a})^2-\frac{b^2-4ac}{4a^2}\\
    \frac{b^2-4ac}{4a^2}&=(x+\frac{b}{2a})^2\\
    \pm\sqrt{\frac{b^2-4ac}{4a^2}}&=x+\frac{b}{2a}\\
    \pm\frac{\sqrt{b^2-4ac}}{2a}&=x+\frac{b}{2a}\\
    \frac{-b\pm\sqrt{b^2-4ac}}{2a}=x
\end{align*}
Which is the quadratic formula. This means that completing the square is essentially the same process as using the quadratic formula.
\subsection{Discriminant}
You may have noticed the term $\pm\sqrt{b^2-4ac}$ in the quadratic formula. We call the term $b^2-4ac$ the discriminant since it tells us how many solutions a quadratic has.
\begin{itemize}
    \item if $b^2-4ac<0$, then $\sqrt{b^2-4ac}$ is not a real number, so there are no solutions for $x$.
    \item if $b^2-4ac=0$, then $\pm\sqrt{b^2-4ac}=0$, so there is exactly 1 solution for $x$.
    \item if $b^2-4ac>0$, then $\pm \sqrt{b^2-4ac}$ has two values, positive and negative, and therefore there are two solutions for $x$.
\end{itemize}
\section{Graphs of relations}
\subsection{Transformations}
Lets talk about transformations, as we can apply these ideas to any graph. There are 3 types of transformations that we care about:
\begin{itemize}
    \item Translations - the graph moving around without the shape changing or stretching.
    \item Dilation - Stretching the graph around horizontally or vertically
    \item Reflection - the graph is flipped in some way horizontally or vertically
\end{itemize}
I'm going to use $f(x)$ as the base function that we are going to transform, and $g(x)$ as the transformed function.
\textbf{Vertical translations: }$g(x)=f(x)+c$\\
Here each point in the original graph $(x,f(x))$ corresponds with the point $(x,g(x)) = (x,f(x)+c)$, a translation of $c$ units up. \\
\textbf{Horizontal translations:} $g(x)=f(x-c)$\\
Again each point $(x,f(x))$ corresponds to another point $(x+c,g(x+c)) = (x+c,f(x))$ , which is a translation of c units to the right. \\
\textbf{Vertical dilation:} $g(x)=af(x)$\\
Each point $(x,f(x))$ has a corresponding point $(x,g(x))=(x,af(x))$, which is a dilation of scale factor a from the x axis (vertically).\\
\textbf{Horizontal dilation:} $g(x)=f(ax)$\\
 For each point $(x, f(x))$ there is a corresponding point $(\frac{x}{a},g(\frac{x}{a})=(\frac{x}{a},f(x))$, which is a horizontal dilation of scale factor $\frac{1}{a}$, (not $a$).\\
\textbf{Reflection}
Reflection across the x-axis occurs when $g(x)=-f(x)$, so each point $(x,f(x))$ corresponds to $(x,-f(x))$.
Reflection across the y-axis occurs when $g(x)=f(-x)$. Therefore, every point $(x,f(x))$ corresponds to $(-x,g(-x))=(-x,f(-(-x)))=(-x,f(x))$, a reflection across the y-axis. 
\subsection{Hyperbolas}
The general formula for a hyperbola is $\frac{a}{x-b}+c$. Hyperbolae have asymptotes, which are lines that the graph approaches but never actually reaches. These occur due to $x-b$ not being able to be 0, or else we divide by zero. Therefore, there is an asymptote at $x=b$. Furthermore, since $\frac{a}{x-b}$ can never equal 0, there is also an asymptote at $y=c$. 
\subsection{Parabolas... but different?}
Here, we talk about parabolas reflected. Here, we instead treat the x - axis like the y - axis and the y-axis like the x - axis, so $y^2=x$ is a parabola rotated 90 degrees. Similarly, $y=\sqrt{x}$ is the same graph, but only the positive side as $\sqrt{x}$ is always positive. The general formula for this is $y=a\sqrt{x-h}+k$, where the "starting point" is at $(h,k)$
\subsection{Circles}
Circles are represented by the formula $x^2+y^2=r^2$. A circle is defined as all the points that are a set distance away from a set point. Therefore, for a circle centered at the origin, using the distance formula we find that for any point (x,y) on the circle $\sqrt{x^2+y^2}=r$, so $x^2+y^2=r^2$. The circle can be translated using transformations to move the center around, i.e. a circle with centre $(a,b)$ and radius $r$ has formula $(x-a)^2+(y-b)^2=r^2$.
\section{Powers and Polynomials}
\subsection{What is a Polynomial}
This term sounds scary, but they are actually easy to understand. A polynomial is any expression of (positive) powers of $x$ added up, or more precisely:\\
\begin{framed}
    A polynomial is anything that can be written in the form $a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0$, where $a_n, a_{n-1},\dots a_0$ are all real numbers.
\end{framed}
For example, $x$, $x^2+x+1$ and $x^5+3x^2+100x$ are all polynomials. For convention, we will assume that $a_n$ is not 0, since if it is we can just ignore it and start with $a_{n-1}$. As Cambridge says, we say $a_nx^n$ is the leading term, $a_0$ is the constant term (unchanged by $x$) and if $a_n=1$, then the polynomial is monic. \\
We say that a polynomial written out as such has a \textbf{degree} of $n$, or in other words the highest power of $x$ in the polynomial. For example, polynomials we have seen before such as:
\begin{itemize}
    \item $x+5$ has a degree of 1
    \item $x^2+6x+7$ has a degree of 2
    \item $x^{100}+69x^{48}+3x^2$ has a degree of 100.
\end{itemize}
Linear functions have a degree of 1, quadratics 2, cubics 3, quartics 4, and quintics 5. \\
We also say that two polynomials are equal if for every value of $x$ you put in you get the same output from both. This happens if and only if their terms are equal, i.e.\\
If the two polynomials are $a_nx^n+a_{n-1}x^{n-1}+\dots+a_1x+a_0$ and $b_nx^n+b_{n-1}x^{n-1}+\dots+b_1x+b_0$, they are equal polynomials if and only if $a_0=b_0$, $a_1=b_1$, e.t.c. up to $a_n=b_n$
\subsection{Polynomial Arithmetic}
Polynomials function remarkably similar to whole numbers. For example, with 2 polynomials I can add, subtract and multiply them just like numbers. For example, suppose we have two polynomials $P(x)=x^3+2x+1$ and $Q(x)=x^2+7x+3$. 
We can add them and multiply them by just doing so algebraically:\\
$P(x)+Q(x)=x^3+x^2+9x+4$\\
$P(x)-Q(x)=x^3-x^2-5x-2$\\
$P(x) \times Q(x) = x^5+7x^4+5x^3+15x^2+13x+3$\\
So as you can see, we can add, subtract (basically adding a negative polynomial) and multiply to get another polynomial. \\
Now, we can probably guess that if we add two quadratics we are probably also going to get a quadratic, or maybe a linear function if the $x^2$ terms cancel out. We know that we can't get a cubic, as the $x^3$ term can't appear out of nowhere. This gives us some motivation for the following rule:
\begin{framed}
\textbf{Degrees of adding polynomials:} deg$(P+Q)\leq$ max$($deg$(P),$deg$(Q))$
\end{framed}
Here, I've written $P$ instead of $P(x)$ for readability. Since the equation can be a bit confusing, all it says is that if you add 2 polynomials the degree of the resulting polynomial can't get larger. \\
Furthermore, we know that multiplying a polynomial by some linear function, like $(x+2)$ increases the degree by 1, and multiplying by a quadratic increases the degree by 2. This gives some motivation for this rule:
\begin{framed}
    \textbf{Degrees of multiplying polynomials:} deg$(P \times Q)=$ deg$(P)$+deg$(Q)$
\end{framed}
For the second rule, suppose that the leading terms of $P(x)$ and $Q(x)$ are $a_nx^n$ and $b_mx^m$. This means that deg$(P)=n,$ deg$(Q)=m$. Therefore, when we multiply these together, the leading term of the resulting polynomial will be  $a_n \times b_m \times x^{n+m}$ so the resulting degree will be $m+n=$ deg$(P)+$deg$(Q)$. 
\subsection{Dividing polynomials}
Similar to whole numbers, we have a division algorithm for polynomials. Lets look at the division algorithm for whole numbers again:
\begin{framed}
    \textbf{Division algorithm for whole numbers:} For 2 positive whole numbers $a, b$, there are 2 other non-negative numbers $q, r$ such that $a=bq+r$ and $0\leq r < b$.
\end{framed}
This just describes long division, where $q$ is $a$ divided by $b$, and $r$ is the remainder. For example, we can divide 7 into 25 3 times, with a remainder of 4. Therefore, $25=7 \times 3 +4$. Note that here, we want the remainder to be less than 7. If we do end up dividing and the remainder is more than 7, we can just divide  Furthermore, note that we can do this for any 2 numbers, which describes division with whole numbers. We can do something similar with polynomials.
\begin{framed}
\textbf{Division algorithm for polynomials: }For any two polynomials $P(x)$ and $Q(x)$, there are two more polynomials $A(x)$ and $R(x)$ such that $P(x)=A(x)Q(x)+R(x)$ and deg$(R)<$ deg$(Q)$.
\end{framed}
Notice how this looks very similar to division with normal numbers. In fact, the process for long division on polynomials is very similar.
\subsection{How to do polynomial division}
\textbf{Long division for numbers:}
I'm going to start this section with dividing some numbers, as polynomial division is almost exactly the same process. Lets do long division of $23|\overline{1094}$.
\begin{align*}
    &47 \text{ r}13\\
    23|\overline{10}&\overline{94}\\
    -9&2\downarrow\\
    1&74\\
    -1&61\\
    &13
\end{align*}
\begin{itemize}
    \item 23 divides into 109 4 times, so we subtract $4 \times 23=92$ from 109 to get a remainder of 17.
    \item We bring the 4 down.
    \item 23 goes into 174 7 times so we subtract $161=23 \times 7$ from 174 to get a remainder of 13
    \item No more remaining digits, so we are done with $47 \times 23 + 13 = 1094$
\end{itemize}
\textbf{Long division for polynomials:}\\
We can do a similar thing with polynomials. There is a small difference however. Notice how at each step we always aim to have a remainder that is less than our divisor, in our case 23. The two remainders that we generate are 17 and 13, both less than 23. We aim to do the same thing with polynomials, except we aim for the remainder at each step to have a lesser degree than before. Lets divide $x+1$ into $x^3+4x^2+2x+3$.
\begin{align*}
    &x^2+3x-1 \text{ r}4\\
    x+1|\overline{x^3+4}&\overline{x^2+2x+3}\\
    - x^3 - &x^2\hspace{1em}\downarrow\hspace{1.75em}\downarrow\\
    3&x^2+2x\hspace{1em}\downarrow\\
    -3&x^2-3x\hspace{1em}\downarrow\\
    &\hspace{1.5em}-x+3\\
    &\hspace{0.25em}-(-x-1)\\
    &\hspace{4.5em} 4\\
\end{align*}
\begin{itemize}
    \item $x+1$ divides $x^2$ times into $x^3+4x^2$ with remainder $x^3+4x^2-x^3-x^2=3x^2$
    \item $x+1$ divides $3x$ times into $3x^2+2x$ with remainder $3x^2+2x-3x^2-3x=-x$ (the remainder can be negative)
    \item $x+1$ divides $-1$ times into $-x+3$ with remainder $-x+3+x+1=4$
\end{itemize}
Notice that at every step, we try to eliminate the highest power of $x$. For example, we eliminate $x^3$ by subtracting $x^3+x^2$.
\subsection{Remainder Theorem and Factor Theorem}
\begin{framed}
\textbf{Remainder Theorem:} The remainder of $P(x)$ when divided by $(x-a)$ is $P(a)$.
\end{framed}
Here we can use our division algorithm - We can express $P(x)$ as $(x-a)A(x)+R(x)$. Furthermore, we know that $R(x)$ has a degree less than 1 and must therefore be a constant, which we can denote as $r$. In other words, dividing by a linear gives a constant remainder. \\
\begin{align*}
   \therefore P(x)&=(x-a)A(x)+r\\
   P(a)&=(a-a)A(a)+r\\
   &=0 \times A(a)+r=r
\end{align*}
So the remainder is $P(a)$ as desired. In our previous example, we divided $x+1$ into $x^3+4x^2+2x+3$ to get a remainder of $4$. We could also get the same remainder by substituting $x=-1$ into $x^3+4x^2+2x+3$ to get $(-1)^+4(-1)^2+2(-1)+3=-1+4-2+3=4$. This also leads to an extremely useful \textbf{corollary} (a theorem that easily logically follows or a side case).
\begin{framed}
    \textbf{Factor Theorem:} If $P(a)=0$, then $(x-a)$ divides $P(x)$.
\end{framed}
This follows from the remainder theorem. If $P(a)=0$, then the remainder when we divide $P(x)$ by $x-a$ will be $0$, so $x-a$ divides into $P(x)$. 
\subsection{Cubics}
If you are here to deal with cubics of the form $y=a(x-b)^2+c$, this is covered in transformations, and not every cubic can be expressed in this way.
\textbf{How to solve a cubic:}\\
The first step in solving a cubic is to use trial and error to find one factor of the cubic. Suppose we have a cubic $P(x)$, and want to solve $P(x)=0$. Therefore, if we can find one factor, we can use polynomial division to find a solution and reduce it to a quadratic, which we can solve by methods outlined before. So, if we find a $k$ such that $P(k)=0$, then $x-k$ divides $P(x)$ and we can solve the cubic. For example:\\
\begin{framed}
    \textbf{Example 1:} Solve $x^3 + 2 x^2 - 21 x + 18=0$
\end{framed}
We start by using trial and error. We find rather quickly that substituting $x=1$ gives\\
$x^3 + 2 x^2 - 21 x + 18=1+2-21+18=0$. \\
Therefore, we have that $x-1$ divides the cubic. By using polynomial division, we find that $x^3 + 2 x^2 - 21 x + 18 = (x-1)(x^2+3x-18)$.\\
Therefore, $(x-1)(x^2+3x-18)=0$, so either $x=1$ or $x^2+3x-18=0$. This quadratic can be factorised into $(x-3)(x+6)=0$, so the solutions are $x=1,x=3,x=-6$.

\end{document}
