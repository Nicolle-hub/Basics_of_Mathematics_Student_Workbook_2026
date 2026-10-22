## Exercise 13. A Recurrence Written in Matrix Form



### Problem Statement

Let
F = [ 1  1 ]
[ 1  0 ]

Compute F^2, F^3, F^4, and F^5. Compare the numbers obtained with the sequence
0, 1, 1, 2, 3, 5, 8, ...

and describe the relationship you observe. Then compute
F [ a ]
[ b ]

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

---

### Solution

#### 1. Computing Matrix Powers

Given the matrix F = [ 1 1 / 1 0 ]:

* **Compute F^2:**
F^2 = [ 1  1 ] * [ 1  1 ] = [ (1*1 + 1*1)  (1*1 + 1*0) ] = [ 2  1 ]
[ 1  0 ]   [ 1  0 ]   [ (1*1 + 0*1)  (1*1 + 0*0) ]   [ 1  1 ]
* **Compute F^3:**
F^3 = F^2 * F = [ 2  1 ] * [ 1  1 ] = [ (2*1 + 1*1)  (2*1 + 1*0) ] = [ 3  2 ]
[ 1  1 ]   [ 1  0 ]   [ (1*1 + 1*1)  (1*1 + 1*0) ]   [ 2  1 ]
* **Compute F^4:**
F^4 = F^3 * F = [ 3  2 ] * [ 1  1 ] = [ (3*1 + 2*1)  (3*1 + 2*0) ] = [ 5  3 ]
[ 2  1 ]   [ 1  0 ]   [ (2*1 + 1*1)  (2*1 + 1*0) ]   [ 3  2 ]
* **Compute F^5:**
F^5 = F^4 * F = [ 5  3 ] * [ 1  1 ] = [ (5*1 + 3*1)  (5*1 + 3*0) ] = [ 8  5 ]
[ 3  2 ]   [ 1  0 ]   [ (3*1 + 2*1)  (3*1 + 2*0) ]   [ 5  3 ]

---

#### 2. Comparing with the Fibonacci Sequence

The given sequence is the Fibonacci sequence:
F_0 = 0,  F_1 = 1,  F_2 = 1,  F_3 = 2,  F_4 = 3,  F_5 = 5,  F_6 = 8, ...

Observing the powers of matrix F, we notice that general powers of F contain consecutive Fibonacci numbers:
F^n = [ F_{n+1}   F_n   ]
[   F_n    F_{n-1} ]

Specifically:

* F^2 = [ 2  1 ] = [ F_3  F_2 ]
[ 1  1 ]   [ F_2  F_1 ]
* F^3 = [ 3  2 ] = [ F_4  F_3 ]
[ 2  1 ]   [ F_3  F_2 ]
* F^4 = [ 5  3 ] = [ F_5  F_4 ]
[ 3  2 ]   [ F_4  F_3 ]
* F^5 = [ 8  5 ] = [ F_6  F_5 ]
[ 5  3 ]   [ F_5  F_4 ]

---

#### 3. Matrix-Vector Multiplication and Recurrence Step

Computing the product of F with a column vector [ a / b ]:

F * [ a ] = [ 1  1 ] * [ a ] = [ 1*a + 1*b ] = [ a + b ]
[ b ]   [ 1  0 ]   [ b ]   [ 1*a + 0*b ]   [   a   ]

**Explanation:**

* **The top entry (a + b):** Creates the sum of the two consecutive terms (a and b), representing the next term in the recurrence sequence.


* **The bottom entry (a):** Keeps the previous term (a) so it can move down to become the secondary term in the subsequent recurrence step.