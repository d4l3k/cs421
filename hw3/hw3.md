# CPSC 421 - Homework 3

Tristan Rice, 25886145, q7w9a

## 1. Problem 7.1.1

### 7.1.1.1

Proof by induction.

Every positive integer is the "meaning" of some sentence with words from W.

Base case: $n=1$.

"one" means $1$.

Induction step:

Assume that $n-1$ is the meaning of some sentence with words from W.

One can get $n$ by adding "plus one" to the sentence that means $n-1$.

Thus, every positive integer is the meaning of some sentence with words from W.

### 7.1.1.2

No, you can't construct a paradox similar to Paradox 3 since this language isn't
self referential. There's no way to have a sentence that describes itself.

## 2. Problem 7.1.2

#### 7.1.2.1

The meaning of "moo one" is "the smallest positive integer not described by a
sentence of one word or fewer". E.g. smallest positive integer that has to be
described by at least two words.

#### 7.1.2.2

You get a paradox with "moo two" since it describes the smallest positive
integer that has to be described by at least three words. Since "moo two" is
only two words it becomes a paradox.

#### 7.1.2.3

This paradox is similar to Paradox 3 since it's using set theory to contruct an
impossible set.

#### 7.1.2.4

You can resolve this paradox by ignoring it.

## 3. Problem 7.1.4

Argue informally that one can conclude that S is true but there is no proof S is
true.

Under assumption 1, the statement holds since S is either true or false.

Under assumption 2, the statment holds since it doesn't claim it's both true and
false.

Under assumption 3, the statement holds since the assumption only deals with the
case there is a proof S is true and the statement doesn't assert that.

Thus, one can conclude S is true but there is no proof that S is true.

## 4. Problem 7.2.1

Proof by contradiction.

Assume that both $C_1,C_2$ are countable sets and that $C_1 \cup C_2$ is
uncountable.

Pick $C_1$ such that it is the larger or equal of $C_1,C_2$.

Create a set $C_3$ such that it has an element for every element in set $C_1$.

Since $|C_3| = |C_1|$, $|C_1 \cup C_3| = 2*|C_1|$.

Since $C_1$ is bigger than $C_2$, $|C_1 \cup C_3| \geq |C_1 \cup C_2|$.

Contradicton. Thus, $C_1 \cup C_2$ must be countable since it is shown to be less than
some other set.

## 5. Problem 7.2.2

You can construct a table with the X axis being the elements of A and the Y axis
being the elements of B.

You can then iterate over all elements in the diagonal order
$$(a_0, b_0),  (a_0, b_1), (b_1, a_0), (a_0, b_2), (a_1, b_1), (a_2, b_0),
\ldots$$

Since all elements will be iterated over, you can assign each element a specific
index. Thus, there is an injective map $A \times B \to \mathbb{N}$ and thus is
countable.

## 6. Problem 7.2.8

Consider the set of all functions $\mathbb{N} \to \{1,2,3\}$.

This set is uncountable since there's an arbitrarily infinite number of
functions that can map to $\{1,2,3\}$. Since you can come up with new arbitrary
functions there's no simple way to enumerate all possible functions.

## 7. Which of the following sets are countable and which aren't?

### 7.1 $\mathbb{N}$

The natural numbers are countable since they fall under a "sequence of elements
of S such that each elment of S appears at least once in this sequence" as
specified by Definition 4.1.

The sequence, $S =  \{1,2,3,\ldots,i,\ldots\}$ satisfies this. Thus, it must be
countable.

### 7.2 $\mathbb{Z}$

You can construct a sequence
$$\mathbb{Z} = \{0, -1, 1, -2, 2, \ldots, -1^{i}*ceil(\frac{i}{2})\}$$.

Thus the set of all integers must be countable.

### 7.3 $\mathbb{Q}$

Given a constant $n$, there can be a max of $n^2$ distinct rationals since there
are $n$ possible values of the numerator and $n$ possible values of the
denominator. Since it's possible to map integers to each one of those rationals
$\mathbb{Q}$ is countable.

### 7.4 $A^*$ over an alphabet $A$

Every time you add 1 to the length of $A^*$ the number of sets increases by
$|A|$ times.

Thus, the number of sets is $|A|^n$. This means you can assign an index to each
set and thus is countable.

### 7.5 the set of languages over an alphabet $A$.

Since the set of languages over an alphabet A is equivalent to a power set over
$A*$ this means this is uncountable since $A*$ is infinite.
