# CMPS 2200 Reciation 5
## Answers

**Name:** Christopher Yarbro


Place all written answers from `recitation-05.md` here for easier grading.







- **1b.**
Quicksort with a fixed pivot seems to perform badly on sorted lists, giving a worst case time complexity of O(n^2) as lists get longer and longer due to using the first element to pivot.

Quicksort with a random pivot seems to work better as the list gets longer, giving a time complexity of O(nlogn). At n = 10,000, it performs better than the fixed pivot version.

With its best-case complexity nearing O(n) and generally operating at O(nlogn), TimSort works extremely well across all lists






Sorted List:
|      n |qsort-fixed-pivot(ms)|qsort-random-pivot(ms)|timsort(ms)|
|--------|---------------------|----------------------|-----------|
|    100 |               0.017 |                0.198 |     0.004 |
|    200 |               0.023 |                0.321 |     0.003 |
|    500 |               0.053 |                1.141 |     0.005 |
|   1000 |               0.101 |               42.823 |     0.026 |
|   2000 |               0.218 |                4.635 |     0.025 |
|   5000 |               0.519 |               22.494 |     0.057 |
|  10000 |               1.085 |               78.248 |     0.111 |
|  20000 |               2.230 |              114.529 |     0.271 |
|  50000 |               5.930 |              374.854 |     0.814 |
| 100000 |              11.693 |              985.747 |     1.438 |



Random List:
|      n |qsort-fixed-pivot(ms)|qsort-random-pivot(ms)|timsort(ms)|
|--------|---------------------|----------------------|-----------|
|    100 |               0.174 |                0.203 |     0.013 |
|    200 |               0.597 |                0.436 |     0.023 |
|    500 |               1.029 |                1.388 |     0.059 |
|   1000 |               2.009 |                2.193 |     0.125 |
|   2000 |               4.642 |                4.497 |     0.271 |
|   5000 |              10.933 |               70.263 |     0.836 |
|  10000 |              23.925 |               94.382 |     1.942 |
|  20000 |             130.447 |              190.134 |     4.321 |
|  50000 |             406.280 |              473.475 |    11.756 |
| 100000 |            1005.367 |              992.023 |    82.661 |

- **1c.**

On shuffled lists, both quicksort and timsort both try for O(nlogn), but timsort outperforms quicksort as n increases.

On sorted lists, timsort probably has built-in code that allows it to exploit ordered lists, performing exponentially better than quicksort.