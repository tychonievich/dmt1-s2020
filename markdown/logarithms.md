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

{.example} $\log_{10}(99.999999\dots) = 2$ because it is as big as 2-digit numbers can be. $\log_{10}(100.0000\dots) = 2$ as well, because $100.000\dots - 99.999\dots = 0$.

The **log base 2 of $x$** is a continuous parallel to the number of digits needed to write $x$ as a binary (base-2) integer.

{.example} $\log_{2}(81) = 6.3395\dots$ because the binary for 81 is 1010001, more than you can fit in 6 bits but less than you can fit in 7.

