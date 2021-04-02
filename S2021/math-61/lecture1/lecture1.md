# Math 61: Lecture 1

(dated: 3/29/21)

## Notation

- Let $\N = \{1, 2, 3, 4, ... \}$ (natural numbers)
- For $n \in \N$ means that $n$ is a natural number
- More formalization to happen in lec 2

## Theory

### Principal of Mathematical Induction

What is it?

- A proof technique that is used to show that an infinite 'family' of statements holds.
- Domino effect:
  - We visualize it as a bunch of dominos that become true
  - For example
    1. First, we show that statement #1 is true
    2. Then, we show that *if* statement #n is true, *then* #(n+1) statement must be true
  - Essentially, if the nth domino falls, the (n+1)th domino also falls.
  - Thus for $n \in \N$ , the nth statement is true

Let's try to find a formal definition now:

> **Definition**
>
> Suppose that we have a collection of statements:
> $$
> S(1), S(2), S(3), ..., S(n),...
> $$
> indexed by $\N$
>
> Supposing that:
>
> - $S(1)$ is true (base case)
> - For each $n \geq 1$, if $S(n)$ is true, then $S(n+1)$ is true.
>
> Then, $S(n)$ is true for each $n \in \N$ (for every positive integer $n$)

### Applications of Mathematical Induction

#### Proposition 1: 

Prove for each $n \in \N$, we have that:
$$
1+2+...+n =\frac{n(n+1)}{2}\\
\text{or}\\
1\sum_{i=1}^{n}i=\frac{n(n+1)}{2}
$$
**Proof**: Prove this statement via mathematical induction. Let:
$$
S(n) = 1 + 2 + ... + n =\frac{n(n+1)}{2}
$$
**Base case**: WTS that S(1) is true
$$
S(1) = 1 =\frac{1(1 + 1)}{2}
$$
This is obviously true. Now we move on to the:

**Inductive Step**:

WTS that **if** $S(n)$ is true (for $n \geq 1$), **then** $S(n+1)$.

**How?**

We assume $S(n)$ and try to prove $S(n+1)$.

Assume $S(n)$ is true, ie $S(n) = 1+2+...+n =\frac{n(n+1)}{2}$. 

We want to prove that: $S(n) = 1+2+...+n+(n+1) =\frac{(n+1)((n+1)+1)}{2}$. 

To prove this:
$$
\begin{align} 
1+2+...+n+(n+1)&=(1+2+...+n)+(n+1)\\
&=(1+2+...+n)+(n+1)\\
&=\frac{n(n+1)}{2}+(n+1)\\
&=\frac{(n+1)((n+1)+1)}{2}
\end{align}
$$
Thus, if $S(n)$ is true, then $S(n+1)$ is true. Thus, we conclude that for all $n \in \N$ we have:
$$
1+2+...+n =\frac{n(n+1)}{2}\\
$$

#### Proposition 2:

Given:
$$
n! = 
	\begin{cases}
	1 & n = 0 \\
	n(n-1)(n-2)...(2)(1) & n \geq 1
	\end{cases}
$$
Prove that for each $n \in \N$:
$$
n! \geq 2^{n-1}
$$

**Best case**: 

For $n = 1$:
$$
\begin{align}
1! &= 1\\
2^{1-1} &= 1 \space \checkmark
\end{align}
$$


**Inductive Step:**

For (some) $n \geq 1$, assume $S(n)$ holds. WTS that $S(n+1)$ holds.

We assume that $n! \geq 2^{n-1}$, WTS $(n+1)! \geq 2^{((n+1)-1)}$. So:
$$
\begin{align}
(n+1)! &=(n+1)(n)(n-1)...(2)(1)\\
&=(n+1)(n!)\\
&\geq (n+1)2^{n-1}\\
&\geq 2 \cdot 2^{n-1} = 2^{(n+1)-1} \checkmark
\end{align}
$$
Now that we have shown base case and inductive step, we have proved that $n! \geq 2^{n-1}$ for each $n \in \N$.

#### Proposition 3:

For each $n \in \N$, $5^n-1$ is divisible by 4 (for each $n \in \N$, there exists some $k \in \N$ s.t. $k\cdot 4 = 5^n-1$).

**Proof:**

Let $S(n):= ``5^n-1 \text{ is divisible by } 4"$.

**Best Case**:

WTS $ S(1)$ holds.
$$
S(1):=``5^1-1 \text{ is divisible by } 4"\\
5^1-1=4 \text{ } \checkmark
$$
**Inductive Step:**

We assume that $5^n -1$ is divisible by $4$.

WTS $5^{n+1}-1$ is divisible by 4. Since $5^n-1$ is divisible by 4, there exists $k \in \N$ s.t.  $k\cdot 4 = 5^n-1$.

Now we prove:
$$
\begin{align}
5^{n+1}-1 &= (5\cdot 5^n)-1 \\
&=(4\cdot5^n+5^n)-1\\
&=4\cdot5^n+(5^n-1)\\
&=4\cdot5^n+4*k\\
&=4(5^n+k)\\
\end{align}\\
$$
Thus $4\cdot(5^n+k)=5^{n+1}-1$. Hence, $5^{n+1}-1$ is divisible by 4.

By the principle of mathematical induction, we conclude that $5^n-1$ is divisible by 4 for each $n \in \N$ $\checkmark$.

