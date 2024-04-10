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

$$|D_{2}\cap D_{3}| = |D_{6}| = {}$$
