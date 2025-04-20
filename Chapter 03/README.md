# 3.1 Exercises

## 3.1-1

Let $ f(n) $ and $ g(n) $ be asymptotically nonnegative functions. Using the basic definition of $Θ$-notation, prove that $max(f(n), g(n)) = Θ(f(n) + g(n))$.

> ### Intuition.  
> Adding $ f(n) + g(n) $ results in a new function $ h(n) $. $ Θ(h(n)) $ yields the upper bound of the new function which would be the max higher term of both functions.

### Proof.
Let's start by trying to prove that $ max(f(n), g(n)) $ is indeed between some boundaries defined by $ C_1 $ and $ C_2 $.  

$ 0 <= C_1\bigl(f(n) + g(n)\bigr) <= max\bigl(f(n), g(n)\bigr) <= C_2\bigl(f(n) + g(n)\bigr) $

- $ max\bigl(f(n), g(n)\bigr) <= \bigl(f(n) + g(n)\bigr) $. In fact $ max\bigl(f(n), g(n)\bigr) $ will at most be equal to the sum of the functions. 
- $ \frac12\bigl(f(n) + g(n)\bigr) <=  max\bigl(f(n), g(n)\bigr) $ . This holds because the max of two functions will at least equal to half the sum of the functions.
- $ 0 <= \frac12(f(n) + g(n)) $ is trivial.

Thus this proves so because there exist constants $ C_1 = 1/2 $ and $ C_2 = 1 $.

## 3.1-2
Show that for any real constants $ a $ and $ b $, where $ b > 0 $,
$(n+a)^b =Θ(nb)$

We have to find $ C_1 $ and $ C_2 $ such that:

$$
0 \le C_1n^b \le \bigl(n+a\bigr)^b \le C_2n^b 
$$
- $ n $ should be at least equal to $ a $, thus

$ n + a \le 2n $, when $ |a| \le n $

- Since $ a $ could be negative,  

$ n - |a| \ge n/2 $

$ n + |a|  \ge n/2 $

So the previous statements hold true when $ n_0 $ = 2|a|

$$
0 \le C_1n^b \le \bigl(n+a\bigr)^b \le C_2n^b 
$$

## 3.1-3
Explain why the statement, "The running time of algorithm *A* is at least $ O(n^2)$," is meaningless.

Because Big O denotes an upper bound not a lower bound.

## 3.1-4
Is $2^{n+1}=O(2^n)$? Is $2^{2n}=O(2^n)$?

## 3.1-5
Prove Theorem 3.1
## 3.1-6
Prove that the running time of an algorithm is $Θ(g(n))$ if and only if its worst-case running time is $ O(g(n)) $ and its best-case running time is $ Ω(g(n)) $.

## 3.1-7 

Prove that $ o(g(n)) ∩ ω(g(n))$ is the empty set.

## 3.1-8
We can extend our notation to the case of two parameters n and m that can go to infinity independently at different rates. For a given function $ g(n, m) $, we denote by $ O(g(n, m)) $ the set of functions

$ O(g(n, m)) = {f(n, m): there exist positive constants c, n0, and m0 such that 0 ≤ f(n, m) ≤ cg(n, m)for all n≥n0 and m≥m0} $.

Give corresponding definitions for $ Ω(g(n, m)) and Θ(g(n, m)) $.

