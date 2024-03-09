[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

# Verification of Theoretical Sorting Algorithm Claim

## Experimental/Practical Verification Method

To empirically test the claim of an $O(n)$ comparison-based sorting algorithm, the following method will be used:

1. **Generate Test Cases:** Various lists will be prepared, including:
   - Randomly ordered lists.
   - Lists sorted in ascending and descending order.
   - Lists with all elements the same.
   - Lists of different sizes, from small to large.

2. **Measure Performance:** The sorting algorithm will be used to sort these lists, measuring:
   - Time taken to sort.
   - Number of comparisons made, if possible.

3. **Analyze Results:** Performance across different lists and sizes will be analyzed to determine if:
   - Time complexity appears to be $O(n)$.
   - Performance degradation is observed with larger sizes, contradicting $O(n)$ complexity.

4. **Benchmarking:** Performance will be compared against established algorithms (e.g., quicksort, mergesort) for context.

5. **Statistical Analysis:** We'll use a basic method called regression analysis to figure out if the sorting is as quick as they say it is by looking at the results from our tests.

### Expected Results

- Linear growth in sorting time with list size increase, without significant changes, would support the $O(n)$ claim.
- Significant deviations would suggest the claim might not hold under all conditions.

## Theoretical Argument

Given the established complexity bounds for comparison-based sorting algorithms, the claim of $O(n)$ time complexity for sorting arbitrary elements is examined closely by the following:

- **Information-Based Lower Bound:** The minimum complexity for comparison-based sorting is $O(n log n)$, due to the many possible ways to arrange the items ($n!$ ways) and to sort them, we need to figure out the right way. Achieving sorting in fewer steps would contradict this lower bound, suggesting the algorithm either:
  - Does not rely solely on comparisons.
  - Or the claim is incorrect.

To summarize, while the experimental approach can provide practical insights into the algorithm's performance, the theoretical framework of algorithmic design and algorithmic theory indicate that a comparison-based sorting algorithm achieving $O(n)$ time complexity for arbitrary datasets contradicts the established principles in algorithmic theory.


