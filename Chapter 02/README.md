---
header-includes:
  - \usepackage{algorithm2e}
  - \usepackage{algpseudocode}
---

# Getting started

# Exercises 2.1

## 2.1 - 1
Using Figure 2.2 as a model, illustrate the operation of INSERTION-SORT on the array A = ⟨ 31, 41, 59, 26, 41, 58 ⟩.

![Insertion Sort](./insertion_sort.svg)

## 2.1 - 2
Rewrite the INSERTION-SORT procedure to sort into nonincreasing instead of nondecreasing order.

$$
\begin{array}{l}
\textbf{Algorithm:} \text{Insertion Sort} \\
\textbf{Input:} \text{Array size n} \\
\textbf{Output:} \text{Sorted Array size n} \\
\textbf{Steps:} \\
1. \textbf{for}\text{ j = 2 to A.length} \\
    \quad 1.1 \; \text{A[i+1] = A[i]} \\
    \quad 1.2 \; \textbf{while} \; \text{i > 0 and A[i] \textcolor{red}> key} \;\\
    \quad \quad 1.2.1 \; \text{A[i+1] = A[i]} \\
    \quad \quad 1.2.2 \; \text{i = i -1} \\
    \quad 1.3. \; \text{A[i+1] = key} \\
\end{array}
$$

## 2.1 - 3
Consider the searching problem:

$$
\textbf{Input:} \text{A sequence of n numbers A = ⧼a1, a2, . . . , an⧽ and a value \textbf{v} .}\\
\textbf{Output:} \text{An index i such that v = A[i] or the special value NIL if v does not appear in A.}\\
$$

Write pseudocode for linear search, which scans through the sequence, looking for v. Using a loop invariant, prove that your algorithm is correct. Make sure that your loop invariant fulfills the three necessary properties.

$$
\begin{array}{l}
LINEAR-SEARCH(A) \\
1 \: \textbf{for} \text{ i = 1 to A.length} \\
2 \; \quad \textbf{if} \text{A[i] = v} \\
3 \; \quad \quad \text{print i} \\
4 \; \quad \quad break
\end{array}
$$
- **Initialization**. A[1] is the first element in the array, which is true
- **Maintanence**. In each iteration ***i*** will be within the boundaries $A[1..., A.length]$
- **Termination**. In the final loop ***i*** will be $ i = A.length + 1 = n+1 $, thus at that point **v was not found** in $ A $, the loop may end sooner in which case **v was found**
## 2.1 - 4
Consider the problem of adding two $n$-bit binary integers, stored in two $n$-element arrays $A$ and $B$. The sum of the two integers should be stored in binary form in an $(n + 1)$-element array $C$. State the problem formally and write pseudocode for adding the two integers.

- ### 1. Problem Statement
$$
\textbf{Algorithm: } \text{ADD-BINARY} \\
\textbf{Input: } \text{Two } n \text{-element arrays } A \text{ and } B\\
\textbf{Output: } \text{ Sum stored in a new Array C[n+1]} \\
$$

- ### 2. Pseudocode
$$
\text{ADD-BINARY} \\
\begin{array}{l}
1 \; \text{let C[n+1] be new array} \\
2 \; carry = 0 \\
3 \; \textbf{for } i = A.length \text{ to } 1 \\
4 \; \quad sum = (A[i] + B[i] + carry) \\
5 \; \quad C[i+1] = sum \;\%\; 2 \\
6 \; \quad carry = sum / 2 \\
7 \; C[1] = carry
\end{array}

$$

