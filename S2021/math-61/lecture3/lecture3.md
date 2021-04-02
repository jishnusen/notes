# Math 61: Lecture 3

## Sets (cont.)

Two constructions left.

* Sometimes we want to study subsets of some fixed set $u$.
* (we think of $u$ as a fixed <u>universe</u> or <u>universal set</u>)

### Compliment

#### Definition

Given a universe $U$ and a subset $X \subseteq U$. The set $U - X$ is called the <u>compliment</u> of $X$. We denote the compliment of $X$ as $\overline{X}$.

#### Example

Let $U = \Z$

let $A = \{X \mid x\in \Z\:\text{and}\: x \:\text{is even}\}$

Then clearly, $A \subseteq Z$.

What is $\overline{A}$?
$$
\begin{align}
\overline{A} = U - A &= \{x \mid x \in U \:\text{and}\: x \notin A\}\\
&= \{x \mid x \in U \:\text{and $x$ is not even}\}\\
&= \{x \mid x \in \Z \:\text{and $x$ is odd}\}
\end{align}
$$


### Cartesian Product

Recall that by convention, a set is not ordered. Sometimes, we want to discuss ordering.

#### Definition

An <u>ordered pair</u> of elements (objects) $a$ and $b$ is $(a, b)$.

> **Note**
>
> $(a, b)$ is distinct from $(b, a)$ unless $a = b$

Let $X$ and $Y$ be sets. Then the Cartesian product of $X$ and $Y$ is denoted $X \times Y$:
$$
X \times Y = \{(a, b) \mid x \in \:\text{and}\: b \in Y\}
$$
We have seen this in $\R^2$ when we "graph a function".

#### Example:

Let $X = \{5, 6, 7\}$, $Y = \{U, V\}$.
$$
\begin{align}
X \times Y &= \{(5, u), (5, v), (6, u), (6, v), (7, v), (7, u)\}.\\
Y \times X &= \{(u,5), (v, 5), (u, 6), (v, 6), (u, 7), (v, 7)\}.
\end{align}
$$
We must now show that $X \times Y \neq Y \times X$:
$$
(5, u) \in X \times Y\\
(5, y) \notin X \times Y
$$
For a Cartesian product with itself, we have:
$$
\begin{align}
Y\times Y &= \{(u, u), (u, v), (v, u), (v, v)\}\\
|Y \times Y| &= 4.
\end{align}
$$

## Functions

Intuitively, a "function" can be thought of as a little machine:

* Takes in inputs
* Returns outputs.

  :star: If we give a function the same input multiple times, we always get the same output.

### Example

For example, $f(x) = x^2$ takes in $\R$ and returns elements in $\R$.

- $f(2) = 4$
- $f(3) = 9$
- $f(-\pi) = \pi^2$.

### Definition

Let $X$ and $Y$ be sets. A function $f$ from $X$ to $Y$ is a subset of the Cartesian product $X \times Y$ ($f \subseteq X\times Y$) such that :star: for each $a \in X$ there exists exactly one $b \in Y$ such that $(a, b) \in f$.

> **Notes**
>
> * We sometimes denote '$f$ is a function from $X$ to $Y$' as $f: x \rightarrow y$.
> * If $f: x \rightarrow y$
>   1. $x$ is called the <u>domain</u>
>   2. $y$ is called the <u>co-domain</u>
>   3. $\{y \mid (x, y) \in f\}$ is called the range. In English, this is the elements in $Y$ so that there exists some $x \in X$ so that $f(x) = y$.
>   4. We usually write $f(x) = y$ to mean $(x, y) \in f$.

### Examples

#### Example 1

Let $x = \{1, 2, 3\}$, $Y = \{a, b, c\}$, $f = \{(1, a), (2, b), (3, b)\}$.

- $f$ is a function. For every element in $X$ there is a single corresponding element in $Y$. 

- Domain: $\{1, 2, 3\}$.
- Co-domain: $\{a, b, c\}$.
- Range: $\{a, b\}$.

#### Example 2

Let $g \subseteq X \times Y$, $g = \{(1, a), (2, b), (2, v)\}$. $g$ is not a function:

​	For $2 \in X$, there exists $y_1, y_2 \in Y$ such that $(2, y_1), (2, y_2) \in g$.

By definition, this cannot happen, so $g$ is not a function.

### Properties

#### Definitions

Let $f: X \rightarrow Y$.

1. We say $f$ is <u>injective</u> (one-to-one) if for every $X_1, X_2 \in X$ if $f(X_1) = f(X_2)$ then $X_1 = X_2$.
2. We say $f$ is <u>surjective</u> (onto) if for every $y \in Y$, there exists some $x \in X$ so that $f(x) = y$.
3. We say $f$ is <u>bijective</u> if $f$ is both injective and surjective

#### Examples

##### Example 1

Let $X = \{1, 2, 3\},\: Y = \{a, b, c\}$. $f = \{(1, a), (2, a), (3, c)\}$. We want to prove that $f$ is not injective or surjective.

$f$ is not injective: $1, 2 \in X$ gives $a \in Y$ and $1 \neq 2$.

$f$ is not surjective: for $b \in Y$, there is no $X_1 \in X$ such that $f(X_1) = b$.

##### Example 2

Let $f: \N \rightarrow \Z$ where $f(n) = 2n + 1$. $f = \{(n + 2n + 1) \mid n \in \N\} \subseteq \N \times \Z$.

We want to show that $f$ is injective, but not surjective.

Injective:

​	Let $n_1, n_2 \in \N$:

​	Assume $f(n_1) = f(n_2)$, WTS that $n_1 = n_2$.

​	Then,
$$
\begin{align}
2n_1 + 1 &= 2n_2 + 1\\
2n_1 &= 2n_2\\
n_1 &= n_2
\end{align}
$$
​	So, $f$ is injective.



Not surjective:

Find $x \in \Z$ such that for any $n \in \N$, $f(n) \neq x$.

Consider $-1 \in \Z$.

Assume there exists $n \in \N$ such that $f(n) = -1$:
$$
\begin{align}
2n + 1 &= -1\\
2n &= -2\\
n &= -1
\end{align}
$$
But, $-1 \notin \N$, so we have a contradiction.

##### Example 3

Consider the map: $f: \Z \rightarrow \N$ where $f(x) = |x|$.

##### Example 4

$x = \{1,2,3\}$, $y=\{a,b,c\}$, $f=\{(1,a),(2,b),(3,c)\}$.

