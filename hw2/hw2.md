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

$$\lim_{n\to\infty} \frac{2^{(n+1)^2}}{2^{n^2}}
= $$
TODO(d4l3k): finish this

## A.9

$$\frac{a_{n+1}}{a_n} = ρ$$

### A.9.1

$$b_n = 3a_n$$

$$\lim_{n\to\infty} \frac{b_{n+1}}{\frac{b_n}} =
\lim_{n\to\infty} \frac{3a_{n+1}}{3a_n} = \frac{a_{n+1}}{a_n} = ρ$$

### A.9.2

### A.9.3

## A.11

## Bonus: A.12

## Bonus: A.14
