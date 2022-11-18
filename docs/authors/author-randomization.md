---
title: Randomization
authors:
    - Rémi Poirier
date: 2022-11-17
tags:
    - authors
    - pg
    - perl
    - randomization
---

# Tips for WeBWorK Authors: Randomization

Producing random quantities in a WeBWorK problem.

## The Basic Method

Pick a random integer between 2 and 5 (inclusive),
and put it in the variable `#!pg $a1`:

``` pg title="An integer between 2 and 5"
$a1 = random(2,5);
```

Pick a random number between 2 and 5 using steps of 0.1,
and put it in the variable `#!pg $a2`:

``` pg title="A number between 2 and 5, step size of 0.1"
$a2 = random(2, 5, 0.1);
```

Pick a random integer between -2 and 5,
but exclude zero (which might cause errors in the problem):

``` pg title="A non-zero integer between -2 and 5"
$a3 = non_zero_random(-2,5);
```

## Fancier Randomization

Suppose we have already picked one number, `#!pg $a`,
and now we want to pick `#!pg $b` so that it is between 1 to 10 but not equal to `#!pg $a`.
The basic form is:

``` pg
do { $b = random(1, 10); } until ($b != $a);
```

This will keep picking random numbers until we have one we like.
The condition in the `#!pg until` clause can contain more than one comparison.

``` pg title="Pick $c different from both $a and $b"
do { $b = random(1, 10); } until (($c != $a) and ($c != $b));
```

### Picking from a list

Sometimes, you might want to pick from a list of numbers.

``` pg
$a = list_random(3, 4, 6, 9, 15, 18);
```

## Connected variables

It may happen that, in a problem, several variables are connected.
Using a single random parameter, the values of several variables can be selected.
Here is an example where three variables, _element_, _atomic weight - mantissa_, and _atomic weight - exponent_ are linked.

``` pg title="Using lists to select connected variables"
@element = ('Carbon','Silicon','Phosphorous','Sulfur','Gallium','Germanium','Arsenic','Gold');
@ma = ('2.00','4.68','5.18','5.34','1.17','1.22','1.25','3.29');
@mb = ('-26','-26','-26','-26','-25','-25','-25','-25',);
$n = random(0,7,1)
```

Now `#!pg $n` can be used as an index for the arrays
and we can write problem statements such as:

``` pg
BEGIN_PGML
Assume that for your experiment,
you inject *singly charged negative [$element[$n]] ions,
that become positively charged [$nplus] times in the center of the accelerator*.
The mass of a [$element[$n]] ion is [`m = [$ma[$n]] \times 10^{[$mb[$n]]}`] kg.
END_PGML
```

!!! note "Credits"

    This page on randomization is based on a presentation by Rémi Poirier of Champlain College Saint-Lambert.
    The starting point for Rémi's presentation was a note written by
    [John Jones](https://hobbes.la.asu.edu/), School of Mathematical and Statistical Sciences, Arizona State University.

    [Randomizing parameters in a WeBWorK Problem](https://hobbes.la.asu.edu/courses/webwork-help/randomizers.html)
