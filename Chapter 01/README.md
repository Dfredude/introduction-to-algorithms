# The role of algorithms in computing

An algorithm is any well-defined computational procedure that takes some vale, or set of values, as input and produces some value, or set of values as output.

> 🎯 An algorithm is a computational process that takes a value as an input and produces a value as output. (My own definition)

# Exercises 1.1

## 1.1 - 1
Give a real-world example in which one of the following computational problems appears: sorting, determining the best order for multiplying matrices, or finding the convex hull.

- **Sorting:** Sorting a library catalog
- **Matrix multiplication:** 3D computer graphics rotations

## 1.1 - 2

Other than speed, what other measures of efficiency might one use in a real-world setting?

- The space taken in **memory**

## 1.1 - 3

Select a data structure that you have seen previously, and discuss its strengths and limitations.

### Linked List

#### Strengths
___
- Quick deletion of nodes
- Quick addition of nodes 

#### Limitations
___
- It may take longer to access a node, since you may need to traverse the entire Linked List until reaching the desired node.

## 1.1 - 4 

How are the shortest-path and traveling-salesman problems given above similar? How are they different?

### Shortest path
- Finding she shortest distance from A to B through the available edges and nodes
- Feels simpler, since you just want to arrive to your destination asap

### Traveling Salesman

- Finding the shortest distance possible by traversing every node
- Sounds simple, and with so many approaches to tackle this problem, none seem to be the best solution

### Similarites

- Both problems are trying to travel the shortest distance
- Permutations is a way to approach both problems incorrectly

### Differences

- The problem complexity grows way faster for the **Traveling salesman** problem as *n* grows
- More permutations available in the **Traveling salesman** problem for the same number of nodes
- **Shortest path** is polynomially solvable but the **Travelling Salesman** is an NP-Complete

## 1.1 - 5

Come up with a real-world problem in which only the best solution will do. Then come up with one in which a solution that is "approximately" the best is good enough.

- Calculating the factorial of a number n!. In this case dynamic programming is the way to go.
- Predicting the price of house based on certain parameters.

## 1.2 - 1
Give an example of an application that requires algorithmic content at the application level, and discuss the function of the algorithms involved.

A browser requires a Linked List structure to store the history of sites visited. So when the user clicks go back it simply goes to previous node in O(1) time complexity.

## 1.2 - 2
Suppose we are comparing implementations of insertion sort and merge sort on the same machine. For inputs of size n, insertion sort runs in ![](http://latex.codecogs.com/gif.latex?8n^2)
 steps, while merge sort runs in ![](http://latex.codecogs.com/gif.latex?64nlg{n})
 steps. For which values of n does insertion sort beat merge sort?
```
1 < n < 44
```
## 1.3 - 3
What is the smallest value of n such that an algorithm whose running time is ![](http://latex.codecogs.com/gif.latex?100n^2) runs faster
than an algorithm whose running time is ![](http://latex.codecogs.com/gif.latex?2^n) on the same machine?

```
n = 15
```

# Problems

## Comparison of running times

For each function **f**(n) and time t in the following table, determine the largest size n of a problem that can be solved in time t, assuming that the algorithm to solve the problem takes **f**(n) microseconds.



Item | 1 second | 1 minute | 1 hour | 1 day | 1 month | 1 year | 1 century
:----:|----:|----:|----:|----:|----:|----:|----:
$\lg n$ | $2^{10^6}$ | $2^{60 \times 10^6}$ | $2^{36 \times 10^8}$ | $2^{864 \times 10^8}$ | $2^{2592 \times 10^9}$ | $2^{31.104 \times 10^{12}}$ | $2^{3.1104 \times 10^{15}}$ | 
$\sqrt{n}$ | $10^{12}$ | $36 \times 10^{14}$| $1296 \times 10^{16}$ | $7465 \times 10^{18}$ | $6.7185 \times 10^{24}$ | $967.458 \times 10^{24}$ | $967.458 \times 10^{28}$ |
$n$ | $10^6$ | $60 \times 10^6$ | $3.6 \times 10^{12}$ | $86.4 \times 10^{12}$ | $2592 \times 10^{12}$ | $31.104 \times 10^{17}$ | $31.104 \times 10^{19}$ |
$n \lg n$ | $62747$ | $2801418$ | $ 133378059 $ | $2cl.755147514e+09$ |
$n^2$ | $1000$ | $7746$ | $60000$ | $293939$ | $1609969$ | $ 5577097 $ | $55770961$ |
$n^3$ | $100$ | $392$ | $1533$ | $4421$ | $13737$ | $31449$ | $145973$ |
$2^n$ | $20$ | $26$ | $32$ | $37$ | $42$ | $45$ | $52$ |
$n!$ | $10$ | $12$ | $13$ | $14$ | $16$ | $17$ | $18$ |