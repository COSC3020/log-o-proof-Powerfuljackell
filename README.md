[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$ 
<!--
Let a, b and n be constants greater than or equal to 0
Given the Change of Base Rule of Log: $\log_{a}n = \log_{c}n / \log_{c}a$
Let a = 5 and c = 2 so that $\log_{5}n = \log_{2}n / \log_{2}5$
The properites of big O nullifies constants, thus removing $1 / \log_{2}5$-->
<!--
Commented out to return to later. This is because within the formal definition of $O$ $T(n)$ only needs to be less than or equal to $c \cdot f(n) \forall n \geq n_0$ to be included so when comparing c to that of $f(n) \forall n \geq n_0$ as $n \to \infty$ f(n) will always be larger than c
Given $T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$, 
For all f(n): $\lim_{n \to \infty}c \cdot f(n) = f(n)$-->

Plugging in $(\log_{2} n) and (\log_{5} n)$

$\log_{2} n \in O(\log n) \iff \exists c, n_0: \log_{2} n \leq c \cdot \log n \forall n \geq n_0$

$\log_{5} n \in O(\log n) \iff \exists c, n_0: \log_{5} n \leq c \cdot \log n \forall n \geq n_0$

Since $log_{2} = \frac{1}{\log 2} \cdot \log n$ via the change of base

$\log_{2} n \in O(\log n) \iff \exists c, n_0: \frac{1}{\log 2} \cdot \log n \leq c \cdot \log n \forall n \geq n_0$

Since $log_{5} = \frac{1}{\log 5} \cdot \log n$ via the change of base

$\log_{5} n \in O(\log n) \iff \exists c, n_0: \frac{1}{\log 5} \cdot \log n \leq c \cdot \log n \forall n \geq n_0$

So long as there is a c that is greater than or equal too the constant values of $\frac{1}{\log 2} and \frac{1}{\log 5}$ respectfully, then they both can be disregarded as both resulting values will be less than or equal to that of c, meaning that via $O(\log n)$; $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$



