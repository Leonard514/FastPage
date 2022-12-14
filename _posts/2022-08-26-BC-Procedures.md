---
toc: true
layout: post
description: The show your work guides are here
categories: [Calc BC]
title: BC Procedures
permalink: /classes/BC/procedures
comments: true
---

### Gotta Knows

(Know them.)[https://leonard514.github.io/FastPage/classes/BC/gotta_know]

### Writing your work: Arrows

When showing work, minimize arrows. Instead attempt to stick to a up to down model, then left to right.

### Using methods taught in class

When solving a problem, you are only allowed to use methods taught in class. This is likely to avoid any misconceptions about those methods not covered yet, although this does turn many of the problems into a game of whether the concept is prohibited since it wasn't covered or if it should be used since it's being introduced.

### Writing the domain

Write the domain in interval notation. So instead of using -1 < x < 1, use (-1,1). Do this even if a single value is excluded from the domain. For example, if x=1 is excluded from the domain, write as (-∞,1)u(1,∞). Also, you have to use the u. Writing (-∞,1),(1,∞) is incorrect notation... since that's the way it was written.

### Limits and grouping symbols

If there is addition/subtraction going on in the rule of the limit which is not modified by multiplication/division, there must be grouping symbols (parenthesis) around the entire rule. This is to ensure clarity of what function is taken to the limit. Outside of this, grouping symbols are optional.

### Limits and known rules

If the rule of a limit is known, it should be written out in full form (ex: x+1) rather than in f(x) form. f(x) form is usually only OK when given a graph of that function.

### One-sided limits

One sided limits should always have the +/- superscripts of whatever value x is approaching.

### Direct Substitution fails due to division by zero: not indeterminate

If a direct substitution fails due to division by zero, and the numerator is not zero, **do not** skip ahead to Does not Exist (infinity or negative infinity). You must first take the left and right limits, and if the infinities have the opposite signs (like in 1/x), then the Does not Exist reasoning is actually that the left limit is not equal to the right limit.

### Direct Substitution: infinity

If there is a limit as x approaches infinity, **do not** directly substitute infinity like it is a variable or a number, because it is neither of those.

### Piecewise Functions: Conventions

When listing a piecewise function, the piece with the least domain is listed first, and the piece with the greatest domain last. As for the domains, there will always be a greater than/equal to, and never a less than/equal to. That is, the lower bound of the domain (if not negative infinity) is included, and the upper bound is excluded. Also, when stating the domain, x always has to be listed first if it is strictly less than a value or strictly greater than a value (ex: x < 4, NOT 4 > x). This is likely in place to establish consistency in defining piecewise functions.

### Squeeze Theorem: Sign of appended functions

When using the squeeze theorem on a limit, any appended functions/actions (like x+1, or taking the reciprocal of all terms) must have their signs checked for the x being approached. 
- If the sign is negative, the inequality signs must be flipped in the first step, and in the second step the terms must be re-ordered from least to greatest. 
- Taking the reciprocal of all terms flips the inequality signs since the least term becomes the greatest (since it has the least denominator) and the greatest term becomes the least (with the greatest denominator).
- If the sign of an appended function is zero, there must be two squeeze theorem sequences performed for approaching x from the left and right sides to account for the two sides of a limit (and the effect of signs on the inequality signs).

### Using a creative one

When there is two of the same term on the denominator, there is a creative one. The term functions as a 1 within the function and has a singular effect: creating a removeable discontinuity (hole) where x causes a 0/0. There is no "canceling" of terms since the terms still play a role. When the terms become one, write ones on them.

### Using a unique creative one as part of a limit to infinity/negative infinity

When taking a limit to infinity/negative infinity and an indeterminate result is yielded(infinity over infinity... and the like), it is possible to multiply the entire rule by a unique creative one. Typically, this will involve multiplying both sides of the fraction by something like (1/x^2). There are special parameters, however. The denominator must not equal zero, and its limit must also exist. This essentially means in general cases, we multiply by (1/x^a), where a is the greatest power an x in the denominator is raised to. Occasionally, both sides of the fraction will be multiplied by (1/sqrt(x^2)) or some other root of a polynomial. This can happen if one side of the fraction is under a root (and the other isn't). In this case, the side under the root can have x^2 divided as normal, but the other side of the fraction must take into account that sqrt(x^2) is the absolute value of x, which is a piecewise function. Any roots which start out being even roots but having odd powers at the end will deal with absolute value. The sign of that part of the creative one then depends on what x is approaching (can be positive/negative depending on which piece's domain the value x is approaching falls on).

**Now,** what I haven't seen yet is the x approaching the value of the piecewise function where x=0. It is very difficult to guess how I would be expected to react to this. It is likely I will be asked to go with the piece where the non-opposite function in the absolute value is so that I can follow conventions.

### Limit of a composite function

There are times when you are asked to take the limit of f(g(x)) as x approaches c. There are two approaches you can take for this limit

1. Limit inside composite function: to use this strategy, you must **first** verify that g(x) is continuous at x=c, and that f(x) is continuous at x=g(c). If this works, then f(g(x)) is continuous and lim(f(g(x))) = f(lim(g(x))). If this is not the case, you must use a different method. The use of this different method is likely to prevent writing infinity/negative infinity as a number/variable, and/or to circumvent complications if there is a hole or if the function's output at a certain point is not equal to the limit (in which case f may be undefined or output the wrong value, since this is a limit we're taking (not where the function f is defined))
1. Input-output method: this accounts for the fact that as the definition of a composite function f(g(x)), x serves as the input to g(x), and the output serves as the input to f(x), which then gives the final input. To do this, show a separate step where the limit of the inside function is taken (as x approaches c, g(x) approaches [value]). Then, take the limit as the inside function approaches the limit you calculated, and write out f(g(x)) as usual. That inside function is your input to f. Then, get your solution.

### Definition of differentiability

Differentiability is not the same thing as continuity. Differentiability is defined as when the limit that serves as the definition of the derivative exists. Nothing more.