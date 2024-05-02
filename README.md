[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/8KYthzwp)
# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Runtime: $\Theta (\log n)$

Calculations:

$$ T(n) = T(\frac_{n}{13}) + 5 $$

$= 1(T(\frac_{n}{13^2}) + 5) + 5$

$= T(\frac_{n}{13^2} + 10$

$= T(\frac_{n}{13^3} + 15$

$ ... $

$= T(\frac_{n}{13^i}) + 5i$

for $i = \log n$

$= T(1) + 5\log n = \log n \in \Theta(\log n)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Runtime:  $\Theta (n)$

Calculations:

$T(n) = 13T(\frac_{n}{13}) + 5$

$= 13(13T(\frac_{n}{13^2}) + 5) + 5$

$= 13^2T(\frac_{n}{13^2} + 10$

$= 13^3T(\frac_{n}{13^3} + 15$

$ ... $

$= 13^iT(\frac_{n}{13^i}) + 5i$

for $i = \log n$

$= nT(1) + 5\log n = n + \log n \in \Theta(n)$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

Runtime: $\Theta (n^2)$

Calculations:

$T(n) = 13T(\frac_{n}{13}) + 2n$

$= 13(13T(\frac_{n}{13^2}) + 2(\frac_{n}{13}) + 2n$

$= 13^2T(\frac_{n}{13^2} + 2(\frac_{n}{13^2}) + 2(\frac_{n}{13}) + 2n$

$ ... $

$= 13^iT(\frac_{n}{13^i}) + 2n \cdot \sum_{k = 0}^{i} (\frac_{1}{13})^k$

for $i = \log n$

$= nT(1) + 2n^2 = n + n^2 \in \Theta(n^2)$
