# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

Summarize your learnings from the lab here.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?

A k-map is arranged such that traversing from one cell to another along any direction (vertical/horizontal) only differs by one bit, and each row contains a unique value. Because the values on two edges maintain these 2 properties, they behave identically to adjacent cells, thus they can be thought of adjacent, allowing them to "wrap-around."

### Why are the names Sum of Products and Products of Sums?

Each operation in boolean logic is loosely compared to a traditional math concept. The "AND" is represented by a product intuitively because the result of a product of 1's or 0's can only result in 1 if all multiplicands are also 1. An "OR" is thought of as a sum because if we sum together a collection of boolean variables, only a single variable must be 1 for the statement to evaluate to 1 (or more, but for the sake of boolean logic numbers above 1 are not possible.)

A "Sum of Products" is called such because it is a collection of AND statements that are connected to eachother via OR statements, thus a "sum" of "products".

Vice versa for the Product of Sums, it is a collection of "OR" statements (sums) connected by "AND" statements (products.)

### Open the test.v file – how are we able to check that the signals match using XOR?

"XOR" is an operator that evaluates to false if and only if the arguments it is given are the same value. In the case of 2 variables, XOR only evaluates to false if its inputs are (1, 1) or (0, 0). Thus it also evaluates to true if and only if there is a difference between its inputs. So in the test suite we can know if there is a difference between the signals whenever XOR evaluates to true.