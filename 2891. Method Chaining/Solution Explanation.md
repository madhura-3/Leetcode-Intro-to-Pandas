# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
We need to find animals with weight strictly greater than 100 kg, sort them by weight in descending order, and then select only the 'name' column. Method chaining allows us to perform these operations sequentially.

# Approach
<!-- Describe your approach to solving the problem. -->
1. Import pandas: We'll import pandas for DataFrame operations.
2. Method Chaining: We'll use method chaining to perform the following steps in a single line:
    - Filter for weight > 100.
    - Sort by weight in descending order.
    - Select the 'name' column.

# Complexity
- Time complexity: `O(nlogn)` (worst case) due to sorting.
<!-- Add your time complexity here, e.g. $$O(n)$$ --> 

- Space complexity: `O(n)` (proportional to the number of rows) in the worst case, as a new DataFrame might be created.
<!-- Add your space complexity here, e.g. $$O(n)$$ -->

<img src = "https://assets.leetcode.com/users/images/61818b09-599a-4fd4-a611-349a21e2afe4_1713805519.4606636.png" width = "700"/>

# Code
``` python
import pandas as pd

def findHeavyAnimals(animals: pd.DataFrame) -> pd.DataFrame:
    return animals[animals['weight'] > 100].sort_values(['weight'], ascending = False)[['name']]
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/method-chaining/solutions/5059829/simple-solution-beats-92)

![image.png](https://assets.leetcode.com/users/images/9aa4d3bb-1d1e-4fea-bf7a-d75406c9005b_1713805423.1379483.png)
