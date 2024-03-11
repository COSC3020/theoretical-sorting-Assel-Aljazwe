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

1. **Generate Test Cases:** Various lists will be prepared to challenge the algorithm under varying conditions, including:
   - Randomly ordered lists to test average-case scenarios.
   - Lists sorted in ascending and descending order to test the algorithm's efficiency in best-case and worst-case scenarios.
   - Lists with all elements the same to check how it handles uniform input.
   - Lists of different sizes, from small to large, to observe scalability and performance trends.

2. **Measure Performance:** The sorting algorithm will be used to sort these lists, with the aim of measuring:
   - Time taken to sort each list, giving us insight on the algorithm's speed.
   - Number of comparisons made during sorting, if possible to understand operational efficiency.

3. **Analyze Results:** Performance across different lists and sizes will be analyzed to determine:
   - If the time complexity aligns with the $O(n)$ claim, by observing whether sorting time increases linearly with list size.
   - If there are any patterns of Performance degradation observed with larger list sizes, which would contradict the $O(n)$ complexity.

4. **Benchmarking:** The algorithm's performance will be directly compared with well-known algorithms (e.g., quicksort, mergesort), providing a context-based reference point to understand the algorithm's efficiency and effectiveness by comparing it to algorithms widely used and understood.

5. **Statistical Analysis:** We'll use a basic method called regression analysis to study how the time taken to sort a list changes with the list's size by looking at the results from our tests.

### Expected Results

- If we see Linear growth in sorting time as the list size increases, without any significant changes, then it would support the $O(n)$ claim
- On the other hand, Significant deviations (not following linear growth) would suggest the claim might not hold under all conditions.

## Theoretical Argument

- In theory, the minimum complexity for comparison-based sorting is $O(n\ log n)$, due to the many possible ways to arrange the items ($n!$ ways) and to sort them, we need to figure out the correct order. Achieving sorting in fewer steps, faster than $O(n\ logn)$, would contradict this lower bound, suggesting the algorithm either:
  - Does not rely solely on comparisons, perhaps takes advantage of specific patterns etc.
  - Or the claim is incorrect.

To summarize, while testing can give us real data on how the algorithm performs, understanding the theory behind sorting tells us there are limits to how fast comparison-based sorting can be. So, an algorithm claiming to be $O(n)$ for all kinds of data is a big claim, that needs careful examination from both practical experiments and theoretical understanding to be proven.


