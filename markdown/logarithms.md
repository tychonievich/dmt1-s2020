---
title: On logarithms
...

Logarithms are pervasive in computing.
They are not strictly a discrete mathematics topic, being continuous in form,
and were once taught extensively in pre-college algebra courses;
however, we have observed that fewer and fewer students come in to UVA already knowing them each year,
and thus have decided to cover them in this course.

# Definitions

The **log base $b$ of $x$** is written $\log_b(x)$ and means "the power to which $b$ must be raised to result in $x$".

{.example} $\log_3(81) = 4$ because $3^4 = 81$

The **log base 10 of $x$** is a continuous parallel to the number of digits needed to write $x$ as a decimal (base-10) integer.

{.example} $\log_{10}(81) = 1.908405\dots$, a number a bit smaller than 2 because $81$ is a bit smaller than the largest 2-digit number.

{.example} $\log_{10}(99.999999\dots) = 2$ because it is as big as 2-digit numbers can be. This also means that $\log_{10}(100.0000\dots) = 2$ because $100.000\dots - 99.999\dots = 0$.

The **log base 2 of $x$** is a continuous parallel to the number of digits needed to write $x$ as a binary (base-2) integer.

{.example} $\log_{2}(81) = 6.3395\dots$ because the binary for 81 is 1010001, more than you can fit in 6 bits but less than you can fit in 7.

$\ln(x)$ means $\log_e(x)$, where $e$ is a [universal constant](https://oeis.org/A001113) sometimes called Euler's number of Napier's constant.

$\lg(x)$ means $\log_2(x)$

$\log(x)$ means either $\log_2(x)$ (common in computing) or $\log_{10}(x)$ (common in engineering) or $\log_e(x)$ (common in mathematics).

# Defining properties

## Change of base

How important is the base used in a logarithm? It matters... but only by a fixed constant factor.

{.example} $\log_3(81) = 4$ because $3^4 = 81$; $3^4 = (3^2)^2 = 9^2$ so $\log_9(81) = 2$. But the same reasoning works for other values: if $\log_3(x) = y$ then $3^y = x$, meaning $(3^2)^{y\div 2} = x$, meaning $\log_9(x) = \frac{y}{2}$.

{.example ...} Suppose a number used 24 digits to write in base 10. How many digits does it take to write in base 1000? 8: each cluster of 3 digits in base 10 turns into one digit in base 1000, so $\log_{1000}(x) = \frac{1}{3}\log_{10}(x)$.

Arguably, this is what the thousands separators do: they take a too-big-to-read decimal numbers like 23276820784381 and re-write them as more readable milial numbers like 23,276,820,784,381
{/}

This leads to the change of base identity: $$\forall a,b,x > 0 \;.\; \log_b(x) = {\log_a(x) \over \log_a(b)}$$ This identity shows up often enough in computing that it is worth memorizing.

{.example} $\log_2(x) = \log_2(10) \log_{10}(x)$, and $\log_2(10) = 3.321928\dots$. Thus, a 10-digit number is a $33.21928\dots$-bit number.

{.example} The most common representation of non-integer numbers in computers is the IEEE-754 double-precision floating-point number, which is represented with 53 bits of precision. Dividing by $\log_2(10) = 3.321928\dots$, we find this is $15.95\dots$ digits of precision.

:::corollary
$\displaystyle \log_a(b) = \frac{1}{\log_b(a)}$
:::

:::proof
$\displaystyle \log_a(b) = \frac{\log_b(b)}{\log_b(a)}$; since $b^1 = b$, $\log_b(b) = 1$ meaning $\displaystyle \log_a(b) = \frac{1}{\log_b(a)}$
:::

## Logs of multiples


