

## Midterm practice

### 1.

a. T
b. F
c. T
d. F
e. T
f. F
g. T
h. F
i. F
j. T
k. T
l. F
m. T
n. T
o. F
p. F


### 2.

Myhill-nerode DFA construction

### 3.

Turing machine.

Make sure you remember that you need to go to the blank and then make your
decision.

Regular and turing machine decidable.

Know DFA, NFA and turing machine notation.

### 4.

a. Turing machine
b. Pumping lemma/Myhill-Nerode questions

### 5.

Three ways to show a language isn't regular.

#### a.

length(xy^2z) = length(xyz) + length(y)

The gap between 1^(2^k), 1^(2^(k+1)) = 1^(2*2^k)= 2^k

choose k such that 2^k is bigger than p.


#### b.

Using walk counting:

If DFA/directed graph has <= p states/verticies, then
$$f(n) = c_1 f(n-1)+c_2f(n-2)+\ldots+c_p(f(n-p)$$

$f(n)$ = # strings in $L$ length $n$.

$f(n)=1$ on powers of 2, $=0$ else

Thus, no asymptotic ratio. Thus not a regular language.

Violates the DFA recurrence definition.

#### c.

Myhill-Nerode accepting futures.

Second elements are all different for each power. Thus, can't be regular.

### 6.

DFA to regular expression. GNFA reduction

