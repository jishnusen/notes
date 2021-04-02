# Math 61: Lecture 2

Date: 03/31/2021

## Sets

"Sets are the building blocks of all mathematical structures"

### Definition

A set is is simply a collection of objects (usually denoted by capital letters)

- An <u>element</u> of a set $A$ is the same as an object in $A$
- If $x$ is an element of a set $A$, we write this as $x \in A$

### Examples

1. $A = \{1, 2, 3, 4\}$, $A$ is a set:

   e.g, $1 \in A, 2\in A, 3\in A, 4\in A$

2. $B = \{x \mid x\text{ is a positive integer strictly greater than 0}\}$

   reads: "B is a set of all $x$ where $x$ is a positive integer strictly greater than 0"

   $B = \{1, 2, 3, 4, 5, ...\}$

3. $C_1 = \{\text{Chicago, 26, my computer, } \pi, 0\}$

   $C_2 = \{x \mid x \:\text{is an elephant in New Jersey}\}$

4. $D = \{x \mid x\:\text{is a real number and}\:x^2-1 = 0\} = \{x \mid x^2-1 = 0\} = \{-1, 1\}$

5. The set with <u>no elements</u> is called the empty set, and is denoted: $\emptyset = \{\}$

6. Sets can contain other sets: $E = \{A, B, C_1, C_2, D, \emptyset\}$

### Conventions

1. Sets are <u>not</u> ordered, and elements are assumed to be unique: $\{1, 2, 2, 2, 3, 3\} = \{3, 2, 1\}$
2. Important Sets:
   1. The integers: $\{..., -3, -2, -1, 0, 1, 2, 3, ...\} = \Z$
   2. The natural numbers: $\{1, 2, 3, ...\} = \N$
   3. Rational number: $\{\frac{m}{n}\mid m\in\Z,n\in\Z\}=\Q$
   4. Real number: $\R = \text{the real number line}$

## Cardinality and Equality

### Cardinality

Sets have a notion of size.

If $X$ is a finite set, then $|X| = $ the number of elements in $X$

$X$ is called the <u>cardinality</u> of $X$.

#### Examples

$$
X = \{2, 8, 192\}\\
|X| = 3
$$

$$
\newcommand{\set}[1]{\left\lbrace#1\right\rbrace}
Y = \{\Z, \R\}\\
|Y| = 2
$$

 Not necessary for class: Infinite sets also have well-defined cardinality:
$$
|\Z| = |\N| = |\Q| = \aleph_0 \\
|\R| > \aleph_0, |\R| = 2^{\aleph_0}
$$

### Equality

Let $X, Y$ be two sets, we say that $X=Y$ if $X$ and $Y$ contain the same elements:

- How do we do this? $X = Y$ if and only if the following conditions hold:

  1. ​	For every $x$, if $x \in X$, then $x \in Y$:
     - "every element of $X$ is an element of $Y$"
     - In this case, "$X$ is a subset of $Y$, so $X \subseteq Y$"
  2. For every $x$, if $x \in Y$, then $x \in X$
     - $Y$ is a subset of $X$, or $Y \subseteq X$

- Notice that 

  1. ensures every element of $X$ is an element of $Y$.
  2. ensures every element of $Y$ is an element of $X$

  $\therefore X = Y$

**Thus** we have: $X = Y$ if and only if $X \subseteq Y$ and $Y \subseteq X$

#### Examples

Let:
$$
\begin{align}
A &= \{x \mid x^2 + x - 6 = 0\}\\
B &= \{2, -3\}
\end{align}
$$
Let's show that $A = B$

WTS if $x \in A$, then $x \in B$ and if $x \in B$ then $x \in A$

First, Suppose $x \in A$:
$$
\begin{align}
x^2+x-6&=0\\
(x-2)(x+3)&=0\\
x=2 \qquad &\text{or} \qquad x=-3 \qquad \checkmark\\
\end{align}\\
\therefore \:A\subseteq B
$$
Second, suppose if $x \in B$:
$$
x = 2\\
x^2 + x - 6 = 4 + 2 - 6 = 0 \qquad \checkmark\\
$$

$$
x = -3\\
x^2 + x - 6 = 9-3-6 = 0 \qquad \checkmark\\
\therefore \: B\subseteq A
$$

Hence, $A = B$.

### Inequality

We write $A \neq B$ if equality conditions are not met. At least of the following must be true:

- There exists some $x \in A$ s.t. $x \notin b$
- There exists some $x \in B$ s.t. $x \notin b$

#### Examples

$$
A = \{1, 3, 5\} \qquad B = \{1, 3, 5, 8\}
$$

Notice: $8 \in B$ and $8 \notin A$ so, $A \neq B$.

Notice: every element of $A$ is an element of $B$, so we have: $A \subseteq B$

## Set Operations

How to build new sets from old ones.

If $A$ and $B$ are sets then:

- <u>Union</u>, $A \cup B = \{x \mid x\in A \:\text{or}\: x\in B\}$
- <u>Intersection</u>, $A \cap B = \{x \mid x \in A \:\text{and}\: x \in B\}$
- <u>Difference</u>, $A - B = \{x \mid x\in A \:\text{and}\: x\notin B\}$

#### Examples

$$
\begin{align}
A = \{2, 4, 6\} &\qquad B = \{4, 7, 8\}\\
A\cup B &= {2, 4, 6, 7, 8}\\
A\cap B &= {4}\\
A - B &= \{2, 6\}\\
B - A &= \{7, 8\}
\end{align}
$$

