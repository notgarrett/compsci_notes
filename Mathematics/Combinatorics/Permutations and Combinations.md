# Rules and Principles

## Sum and Product rules

**Product rule:** n(A) ways to do sub task A. n(B) ways to do sub task B.
Do A and B: n(A)n(B) ways. 

$|A \times B| = |A| \times |B|$, A and B are sets. 
$A\times{B} = \{(a,b) : a \in A, b \in B\}$

**Sum Rule:** distinct sub tasks A and B. n(A) + n(B) ways. 
$A\cap{B} = \{x:x\in{A} \text{ or } x\in{B}\}$
If $A\cap B = \emptyset \implies |A\cup{B}|= |A|+|B|$

## Inclusion-Exclusion Principle
$$|A\cup{B}| = |A| + |B| - |A\cap B|$$

![[AnBExampleChart.excalidraw | center]]

$$(A-B)\cup (A\cap B) = A$$
$$(A-B)\cap (A\cap B) = \emptyset$$
$$\begin{align*}
|A| &= |A-B| + |A\cap B|\\
|B| &= |B-A| + |A\cap B|
\end{align*}$$

$$\begin{align*}
|A\cup B| &= |(A-B)\cup (B-A)\cup(A\cap B)|\\
&= |(A-B)\cup B|\\
&= |A-B| + |B|\\
&= |A| - |A\cap B|+|B|
\end{align*}$$

$$\begin{align*}
|A\cup B \cup C| &= |(A\cup B) \cup C|\\
&= |A\cup B| + |C| - |(A\cup B) \cap C|\\
&= |A| + |B| - |A\cap B| + |C| - (|A\cap C| + |B\cap C| - |(A\cap C)\cap (B\cap C|))\\
&= |A|+|B|+|C| - |A\cap B| - |A\cap C| - |B\cap C| + |A\cap B \cap C|\\ 
\end{align*}$$

### Examples

```ad-question
title: Example 1
Let S = {1,2,...,100}, how many integers in S are multiples of 2 and 3, 2 or 3, 4 or 5 or 6?
```

First we will define that $D_{n} = \{\text{integers in s that are divisible by n}\}$ 

$$|D_{2}\cap D_{3}| = |D_{6}| = \lfloor{\frac{100}{6}\rfloor} = 16$$
$$\begin{align*}
|D_{2}\cup D_{3}| &=  |D_{2}| + |D_{3}| - |D_{2}\cap D_{3}|\\ 
&= \lfloor{\frac{100}{2}}\rfloor + \lfloor \frac{100}{3} \rfloor - 16\\ 
&= 50 + 33 - 16\\ 
&= 67
\end{align*}$$

$$\begin{align*}
|D_{4}\cup D_{6}\cup D_{5}| &=  \lfloor \frac{100}{4} \rfloor + \lfloor \frac{100}{5}\rfloor + \lfloor \frac{100}{8} \rfloor - \lfloor \frac{100}{20} \rfloor - \lfloor \frac{100}{12} \rfloor - \lfloor \frac{100}{30} \rfloor + \lfloor \frac{100}{60} \rfloor\\
&= 25 + 20 + 16 - 5 - 8 - 3 + 1\\
&= 46
\end{align*}
$$

# Permutations and Combinations

**Permutation:** A selection of k elements from n things where order matters.

$$nPk = \frac{n!}{(n-k)!}$$

**Combination:** A selection of k elements from n things where order does 
not matter.

$$nCk =\frac{n!}{k!(n-k)!}$$


### Examples 

```ad-question
title: Example 1
S = {1,2,3,4}
How many 4 digit integers can you make from the elements in S? 
```
$$\begin{align*}
\frac{n!}{(n-k)!} &= \frac{4!}{(4-4)!}\\
&= \frac{4!}{0!}\\
&= 4!\\
&= 24  
\end{align*}$$

```ad-question
title: Example 2
S = {1,2,3,4,5}
How many 3 digit combinations can you make from s?
```

$$\begin{align*}
\frac{n!}{k!(n-k)!}&=  \frac{5!}{3!(5-3)!}\\
&= \frac{5!}{3!2!}\\
&= \frac{5\times4}{2}\\
&= 10
\end{align*}$$


```ad-question
title: Exammple 3
A store sells apples, bananas and pears. How many different ways do you have for a bag of 6 fruits of those 3 kinds? (Repition is allowed, order does not matter.)
```

The number of different multisets of k elements from n categories is:

$$\pmatrix{n + k - 1 \\ n - 1} = \pmatrix{n + k - 1 \\ k}$$

Thus, our answer looks like:
$$\begin{align*}
\begin{pmatrix}3 + 6 - 1\\
3 - 1\end{pmatrix} &= \begin{pmatrix}8 \\ 6\end{pmatrix}\\
&= \frac{8\times7}{2}\\
&= 28
\end{align*}$$



```ad-question
title: Example 4
I need to buy 100 fruits from 3 kinds of fruits: Apple, Banana, and Pears. However, there must be at least 10 apples, 20 bananas, and 30 pears.
```

$$x_{1}+ x_{2}+ x_{3}= 100$$

$$\begin{align*}
x_{1}&\ge 10\\
x_{2}&\ge 20\\
x_{3}&\ge 30
\end{align*}$$

$$\begin{align*}
y_{1}&= x_{1}-10 \ge 0\\
y_{2}&= x_{2} - 20 \ge 0\\
y_{3}&= x_{3}-30 \ge 0
\end{align*}$$

$$\begin{align*}
x_{1}&= y_{1}+ 10\\
x_{2}&= y_{2}+ 20\\
x_{3}&= y_{3}+ 30
\end{align*}$$

$$\begin{align*}
(y_{1}+ 10) + (y_{2}+ 20) + (y_{3}+ 30) &=  100\\
y_{1}+ y_{2}+ y_{3} &= 40
\end{align*}$$

$$\begin{pmatrix}40 + 3 - 1 \\ 40\end{pmatrix} = \begin{pmatrix}42 \\ 40\end{pmatrix}$$

```ad-note
title: Combination notation
Note that a combination can be written like so: 
$$\begin{pmatrix}n \\ k\end{pmatrix}$$
Where n is our number of things, and k is our number of items selected from n.
```



