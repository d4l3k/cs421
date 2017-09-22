# CPSC 421 - HW 2
Tristan Rice, 25886145, q7w9a

## A.8

Find the asymptotic ratios, when they exist, of the following sequences:

### A.8.1

$$a_n = 5^n + 1$$

$$1 = o(5^n)$$

Thus, $5^n$ has the same asymptotic ratio as $5^n+1$.

$$\lim_{n\to\infty} \frac{5^{n+1}}{5^n} = 5$$

### A.8.2

$$a_n=3n^2-4$$

$$-4 = o(3n^2)$$

$$\lim_{n\to\infty} \frac{3(n+1)^2}{3n^2} = (\frac{n+1}{n})^2 = 1$$

### A.8.3

$$a_n=7n^6+5n^2+n$$

$$\lim_{n\to\infty} \frac{5n^2}{7n^6} = \frac{5}{7n^4} = 0$$
$$\lim_{n\to\infty} \frac{n}{7n^6} = \frac{1}{7n^5} = 0$$

$$\lim_{n\to\infty} \frac{7(n+1)^6}{7n^6} = (\frac{n+1}{n})^6 = 1$$

### A.8.4

$$a_n=2^{n^2}+2^n+n^2+3$$

$$\lim_{n\to\infty} \frac{3}{2^{n^2}} = 0$$

$$\lim_{n\to\infty} \frac{n^2}{2^{n^2}} = 0$$

$$\lim_{n\to\infty} \frac{\log(2^n)}{\log(2^{n^2})}
= \frac{n}{n^2}  = \frac{1}{n} = 0$$
Thus,
$$\lim_{n\to\infty} \frac{2^n}{2^{n^2}} = 0$$

$$\begin{split}
\lim_{n\to\infty} \frac{2^{(n+1)^2}}{2^{n^2}}
&= \lim_{n\to\infty} 2^{(n+1)^2-n^2} \\
&= \lim_{n\to\infty} 2^{2n+1} \\
&= \infty
\end{split}$$

Thus, this doesn't have an asymptotic ratio.

## A.9

$$\frac{a_{n+1}}{a_n} = \rho$$

### A.9.1

$$b_n = 3a_n$$

$$\lim_{n\to\infty} \frac{b_{n+1}}{b_n} =
\lim_{n\to\infty} \frac{3a_{n+1}}{3a_n} = \frac{a_{n+1}}{a_n} = \rho$$

### A.9.2

$$b_n = a_{n+1}$$

$$\lim_{n\to\infty} \frac{b_{n+1}}{b_n} =
\lim_{n\to\infty} \frac{a_{n+2}}{a_{n+1}} = \frac{a_{n+1}}{a_n} = \rho$$

### A.9.3

$$b_n = (a_{n})^3$$

$$\lim_{n\to\infty} \frac{b_{n+1}}{b_n} =
\lim_{n\to\infty} \frac{(a_{n+1})^3}{(a_{n})^3} = (\frac{a_{n+1}}{a_n})^3 = \rho^3$$

## A.11

### A.11.1

If $n$ is odd, $f(n) = 0$ since you start and end at the center.

When you're at an edge vertex there's only one path and when you're at the
center there's 7 paths. Thus, you're at the center every other step. Thus,
$1^{\frac n2}*7^{\frac n2} = 7^{\frac n2}$.

$$f(x) = \begin{cases}
0 & \text{if } x \text{ is odd}\\
7^{\frac{n}{2}} & \text{if } x \text{ is even}
\end{cases}$$


### A.11.2

This is similar to question 1, but there's one extra step. If $n$ is even, you
can't get to $v_1$ from $c$. Thus, $f(n)=0$.

Similarly if you go to an edge vertex you need to come back to $c$ before going
to $v_1$. Thus the number of walks is equivalent to 1 but with $n-1$.

$$f(x) = \begin{cases}
0 & \text{if } x \text{ is even}\\
7^{\frac{n-1}{2}} & \text{if } x \text{ is odd}
\end{cases}$$

### A.11.3

This is the same as (2), except in the reverse order.
$$f(x) = \begin{cases}
0 & \text{if } x \text{ is even}\\
7^{\frac{n-1}{2}} & \text{if } x \text{ is odd}
\end{cases}$$

### A.11.4

At the beginning of all walks you have to go from $v_1$ to $c$, and at the end
of all walks you have to go from $c$ to $v_1$. Thus, all that matters is the
number of walks from $c$ to $c$ that are length $n-2$.

$$f(x) = \begin{cases}
0 & \text{if } x \text{ is odd}\\
7^{\frac{n-2}{2}} & \text{if } x \text{ is even}
\end{cases}$$

### A.11.5

This is just the combination of
$$c\to c, c\to v_2, c\to v_3,
v_1 \to c, v_1 \to v_2, v_1 \to v_3,
v_2 \to c, v_2 \to v_2, v_2 \to v_3$$

This boils down to:

- 1x case 1
- 4x case 2/3
- 4x case 4

$$f(x) = \begin{cases}
4*7^{\frac{n-1}{2}} & \text{if } x \text{ is odd}\\
7^{\frac{n}{2}} + 4*7^{\frac{n-2}{2}} & \text{if } x \text{ is even}
\end{cases}$$

## Bonus: A.12

## Bonus: A.14
