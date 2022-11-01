---
title: Entering Answers
authors:
    - Michèle Titcombe
---
# Entering Answers into WeBWorK

## How do I enter square roots or cube roots?

For square roots, you can use `sqrt()` or the exponent `1/2`.
For example, the square root of two in WeBWorK is either `sqrt(2)` or `2^(1/2)`.
For cube roots, use the exponent `1/3`.
The cube root of 7 is then `7^(1/3)`.

## How do I enter the number $\pi$ in my answer?

Enter `pi` for the number $\pi$ in WeBWorK.

## WeBWorK says my answer is incorrect but I can't see what is wrong. What can I try?

- Use the Preview button to see that WeBWorK understands what you have entered.
- See if there are any ways to simplify your answer.
For example, simplify $e^0$ to 1, simplify $1^{5/2}$ to 1,
simplify $\sin\pi$ to 0, simplify $\cos(\pi)$ to -1, and so on.
- Do you expect your answer to be positive or negative?
- Check for bracket errors, especially with negative numbers.
For example, `(-3)^2` is not the same as `-3^2`.
- Check how you are entering exponents.
For example, `e^3^x` is not the same as `e^(3x)`.
- Check that you are using the correct brackets for intervals (see [below](#how-do-i-enter-intervals-in-webwork)).
- Check that you are using a dot for a decimal point and not a comma.

## How many decimal places do I need to have my answer scored correctly?

For most numerical problems,
WeBWorK counts an answer within .01 percent of the right answer as correct.
So, if the right answer is 12345, anything between 12343.765 and 12346.235 counts as correct.
If the correct answer is smaller, \(\pi / 2 \) for example,
an answer would need to be within about 0.0001570796 of \(\pi / 2 \) to be considered correct.

## The answer box is too small. How do I enter my answer?

WeBWorK will accept hundreds of characters in an answer box,
even if the box size on the screen is smaller.
When you enter a long answer in a short answer box,
the text scrolls to the left as you continue to type characters.

## How do I enter intervals in WeBWorK?

Use a round bracket, that is, "`(`" or "`)`", if the endpoint of the interval is not included.
Use a square bracket, that is, "`[`" or "`]`", if the endpoint of the interval is included.
For example, enter `(-4,3)` to indicate the interval $-4<x<3$.
WeBWorK will not accept `]-4,3[` as a correct answer for that interval.

## Do I use a comma or a dot for the decimal point?

Use a dot for the decimal point.
For example, enter 0.625 not 0,625.
