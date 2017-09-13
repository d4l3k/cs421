# CPSC 421 - Homework 1
Tristan Rice, 25886145, q7w9a

## A.1(3,4,6)

### A.1.3

Fibonacci:

| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10| 11| 12| 13| 14| 15|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 1 | 2 | 3 | 5 | 8 | 13| 21| 34| 55| 89|144|233|377|610|

$F_nF_{n+3}-F_{n+1}F_{n+2}$
1. $1*3-1*2 = 1$
2. $1*5-2*3 = -1$
3. $2*8-3*5 = 1$
4. $3*13-5*8 = -1$
5. $5*21-8*13 = 1$

Theorem: The output of $f(n) = F_nF_{n+3}-F_{n+1}F_{n+2}$ is $1$ when $n$ is even and $-1$ when
$n$ is odd.

Proof by induction.

Case: $n$ is odd.

Base cases:
- $n=1$: $1*3-1*2 = 1$
- $n=2$: $1*5-2*3 = -1$

Induction step ($n \geq 3)$:

$f(n) = f(n+2)$

$F_nF_{n+3}-F_{n+1}F_{n+2}=F_{n+2}F_{n+5}-F_{n+3}F_{n+4}$

$= F_{n+2}(F_{n+1}+F_{n+5})$

$= (F_{n+1}+F_{n})(F_{n+3}+F_{n+2}+F_{n+3}) - (F_{n+2} + F_{n+1})(F_{n+3}+F_{n+2})$

$$
= 2*F_{n+1}F_{n+3}+F_{n+1}F_{n+2}+2*F_nF_{n+3} + F_nF_{n+2}
- F_{n+2}F_{n+3} - F_{n+2}F_{n+2} - F_{n+1}F_{n+3}-F_{n+1}F_{n+2}
$$

$$
= F_{n+1}F_{n+3}+2*F_nF_{n+3} + F_nF_{n+2}
- F_{n+2}F_{n+3} - F_{n+2}F_{n+2}
$$

$$
= F_{n+1}F_{n+3}+2*F_nF_{n+3} + F_nF_{n+2}
- F_{n+1}F_{n+3}- F_nF_{n+3} - F_{n+1}F_{n+2} - F_nF_{n+2}
$$
$$
= F_nF_{n+3} - F_{n+1}F_{n+2}
$$

Thus, since $f(n) = f(n+2)$ we prove via induction that the output will be $1$
for all odd values of $n$ and $-1$ for all even values of $n$.

### A.1.4

```py
In [15]: def F(n):
    ...:         return int(0.5+((1+sqrt(5))**n-(1-sqrt(5))**n)/(2**n*sqrt(5)))
In [16]: [(n, F(n) * F(n+8) - F(n+1)*F(n+7)) for n in range(1,6)]
Out[16]: [(1, 13), (2, -13), (3, 13), (4, -13), (5, 13)]
```

For all even values of $n$, $f(n) = -13$. For all odd values of $n$, $f(n) =
13$.

Proof by induction.

Base cases:
* $n=1$: $f(1) = 13$
* $n=2$: $f(2) = -13$

Induction step:

We must show that for all $n>2, f(n) = f(n+2)$.

$$F_{n}F_{n+8}-F_{n+1}F_{n+7} = F_{n+2}F_{n+10}-F_{n+3}F_{n+9}$$

$$= F_{n+1}F_{n+10} + F_{n}F_{n+10} - F_{n+2}F_{n+9} - F_{n+1}F_{n+9}$$

$$= F_{n+1}F_{n+9} + F_{n+1}F_{n+8} + F_{n}F_{n+9} + F_{n}F_{n+8}
- F_{n+0}F_{n+9}- F_{n+1}F_{n+9} - F_{n+1}F_{n+9}$$

$$= F_{n+1}F_{n+8} + F_{n}F_{n+8} - F_{n+1}F_{n+9}$$

$$= F_{n+1}F_{n+8} + F_{n}F_{n+8} - F_{n+1}F_{n+8}- F_{n+1}F_{n+7}$$

$$= F_{n}F_{n+8} - F_{n+1}F_{n+7}$$

Thus, by the property of induction it holds for all $n \geq 1$, $f(n)=13$ for
odd numbers and $f(n)=-13$ for even numbers.

### A.1.6

$$x^2=x+1$$

$$x=\{\frac12(1-\sqrt 5), \frac12(1+\sqrt 5)\}$$

TODO(d4l3k): Finish this!

## A.2(1,2)

### A.2.1

Prove $\sum_{m=1}^n m = \binom{n+1}{2}$ for any $n \in \mathbb{N}$.

Proof via induction.

Base case $n=1$.

$\sum_{m=1}^1 m = \binom{2}{2}$

$1 = 1$

Identity.

Induction step.

Must prove that:
$$\sum_{m=1}^{n+1} m - \sum_{m=1}^{n} = \binom{n+2}{2} -
\binom{n+1}{2}$$

$$n = \binom{n+2}{2} - \binom{n+1}{2}$$

$$n = \frac{(n+2)!}{2!(n+2-2)!} - \frac{(n+1)!}{2!(n+1-2)!}$$

$$n = \frac{(n+2)!}{2n!} - \frac{(n+1)!}{2(n-1)!}$$

$$n = \frac{(n+2)(n+1)}{2} - \frac{(n+1)n}{2}$$

$$2n = (n+2)(n+1) - (n+1)n$$
$$2n = n^2+3n+2 - n^2-n$$
$$2n = 2n+2 $$
$$n = n+1$$

Since $\lim_{n\to\infty} \frac{n+1}{n} = 1$ we can ignore the $1$ term.

TODO(d4l3k): Verify this.

### A.2.2

Prove $\sum_{m=1}^n \binom{m}{k} = \binom{n+1}{k+1}$.

Proof by induction.

Let $k\in\mathbb{N}$ be fixed and arbitrary.

Base case $n=1$:
$$\binom{1}{k} = \binom{1+1}{k+1}$$

If $k=1$, $\binom{1}{1} = \binom{2}{2} = 1$.
If $k>1$, $\binom{1}{k} = \binom{2}{1+k} = 0$.

Inductive step:

We must show that $\binom{n+1}{k} = \binom{n+2}{k+1} - \binom{n+1}{k+1}$.

$$\frac{(n+1)!}{k!(n+1-k)!} =
\frac{(n+2)!}{(k+1)!(n+2-k-1)!} - \frac{(n+1)!}{(k+1)!(n+1-k+1)!}$$

$$\frac{(n+1)!}{k!(n-k+1)!} =
\frac{(n+2)!}{(k+1)!(n-k+1)!} - \frac{(n+1)!}{(k+1)!(n-k)!}$$

$$\frac{(n+1)!(k+1)!}{k!} =
\frac{(n+2)!(n-k+1)!}{(n-k+1)!} - \frac{(n+1)!(n-k+1)!}{(n-k)!}$$

$$(n+1)!(k+1) = (n+2)! - (n+1)!(n-k+1)$$

$$(k+1) = \frac{(n+2)!}{(n+1)!} - (n-k+1)$$
$$k+1 = n+2 - n+k-1$$
$$k+1 = k+1$$
Identity.

Thus, $\sum_{m=1}^n \binom{m}{k} = \binom{n+1}{k+1}$ holds for all $n \geq 1$.


## A.3(1)

We aim to show $|A_1 \cup A_2| = |A_1|+|A_2|-|A_1 \cap A_2|$.

Proof by induction.

Base case:

$$A_1 = A_2 = \varnothing$$

$$|\varnothing \cup \varnothing| = |\varnothing| + |\varnothing| - |\varnothing \cap \varnothing|$$

Inductive step:

Consider adding an element $a$ to $A_1$.

Assume
$|A_1 \cup A_2| = |A_1|+|A_2|-|A_1 \cap A_2|$ for $A_1, A_2$.

Since $a$ only occurs in $A_1$, only the $|A_1|$ term changes, and the union is
maintained. This holds for adding $a$ only to $A_2$ since set addition, union
and intersection are symmetric operations.

Consider adding an element $a$ to $A_1$ and $A_2$.

Since $a$ occurs in $A_1$ and $A_2$, the right side becomes
$|A_1|+a + |A_2| + a - |A_1 \cap A_2| - a$. Since $a$ is in both, it is included
in the intersection and cancels out. Thus, it is only added once.

Thus, $|A_1 \cup A_2| = |A_1|+|A_2|-|A_1 \cap A_2|$ holds for all $A_1, A_2$.


## A.4(1b,1d,2d)

Show that $f(n)=O(g(n))$...

### A.4.1b

$f(n)=100*3^n, g(n) = 4^n$.

Pick $C=100, n_0 = 0$.

Proof by induction.

Base case: $n=0$

$$100*3^0 \leq 100*4^0$$
$$100 \leq 100$$

Inductive step:

Must show that
$$100*3^{n+1} - 100*3^{n} \leq 100*4^{n+1}-100*4^{n}$$
$$3^{n+1} - 3^{n} \leq 4^{n+1}-4^{n}$$

$$3^{n}(3 - 1) \leq 4^{n}(4-1)$$

$$3^{n}(2) \leq 4^{n}(3)$$

$$n*\log(3)+\log(2) \leq n*\log(4)+\log(3)$$

The left side is clearly less than the right side. Thus, via induction we show
that $f(n) = O(g(n))$ since $f(n) \leq C g(n) \forall n \geq n_0$.

### A.4.1d

Show that $f(n) = O(g(n)), f(n)=n^2+3n+1, g(n)=n(n-1)$.

$g(n) = n^2-n$

$C = 4, n_0 = 4$

Proof by induction.

Base case $n=4$:

$$4^2+3*4+1 \leq 4*4^2 - 4*4$$
$$16+12+1 \leq 64 - 16$$
$$29 \leq 48$$

Inductive step:

We must show that $(n+1)^2+3(n+1)+1 - n^2-3n-1 \leq 4(n+1)^2-4(n+1) - 4n^2 +4n$.

$$n^2+2n+1+3n+4 - n^2-3n-1 \leq 4(n^2+2n+1)-4n+4 - 4n^2 +4n$$
$$2n+4 \leq 4n^2+8n+8+4 - 4n^2$$
$$2n+4 \leq 8n+12$$
$$n+2 \leq 8n+6$$

This holds for $n \geq 0$.

Thus, by induction $f(n) = O(g(n)), f(n)=n^2+3n+1, g(n)=n(n-1)$ since
 $f(n) \leq C g(n) \forall n \geq n_0$.

### A.4.2d

Compute limit $\lim_{n\to\infty} \frac{f(n)}{g(n)}$ to show that $f(n) = o(g(n))$
for $f(n) = n^2+3n+1,g(n)=n(n-1)(n-2)$.

$$\lim_{n \to \infty} \frac{n^2+3n+1}{n(n-1)(n-2)}$$
$$=\lim_{n \to \infty} \frac{n^2+3n+1}{n(n^2-3n+6)}$$
$$=\lim_{n \to \infty} \frac{n^2+3n+1}{n^3-3n^2+6n)}$$
$$=\lim_{n \to \infty} \frac{n^2+3n+1}{n^3-3n^2+6n)}$$

Using L'Hospital's rule.

$$=\lim_{n \to \infty} \frac{2n+3}{3n^2-6n+6)}$$
$$=\lim_{n \to \infty} \frac{2}{3n-6)} = 0$$

Since the limit goes to 0 as $n\to\infty$, $f(n) = o(g(n))$.

## A.5(2)

Prove that if $f,g$ are functions $\mathbb{Z}\to\mathbb{R}^+$, then
$f(n)=o(g(n)) \iff \log g(n) -\log f(n)$ tends to infinity (as $n\to\infty$).

Definition: We know that $f(n) = o(g(n))$ iff $\lim_{n\to\infty} \frac{f(n)}{g(n)} = 0$.

$$\lim_{n\to\infty} \log g(n) - \log f(n) = \infty$$
$$=\lim_{n\to\infty} \log (\frac{g(n)}{f(n)}) = \infty$$

If $\lim_{x\to\infty} \log x = \infty$, then $\lim_{x\to\infty} x = \infty$,
since $x >> \log x$.

$$\lim_{n\to\infty} \frac{g(n)}{f(n)} = \infty$$

Taking the reciprocal of this statement gets us to the definition for $f(n) =
o(g(n))$.
$$\lim_{n\to\infty} \frac{f(n)}{g(n)} = \frac{1}{\infty} = 0$$

Thus, if $f,g$ are functions $\mathbb{Z}\to\mathbb{R}^+$, then
$f(n)=o(g(n)) \iff \log g(n) -\log f(n)$ tends to infinity (as $n\to\infty$).

