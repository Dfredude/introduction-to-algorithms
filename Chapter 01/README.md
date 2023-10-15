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