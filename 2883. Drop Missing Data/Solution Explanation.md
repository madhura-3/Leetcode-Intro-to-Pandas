# Intuition
We want to remove rows from the student DataFrame where the `'name'` column has missing values (represented as None in this case).

# Approach
1. **Import pandas:** We'll import pandas for DataFrame operations.
2. **Define the function:** We'll create a function named dropMissingData that takes a student DataFrame as input.
3. **Filter by non-null values:** We'll use boolean indexing to filter the DataFrame, keeping only rows where name is not null.
4. **Return the filtered DataFrame:** We'll return the DataFrame with rows containing missing names removed.

# Complexity
- Time complexity: `O(n)`
<!-- Add your time complexity here, e.g. $$O(n)$$ -->
(worst case) for iterating through the DataFrame. In practice, with efficient indexing, it's often much faster.

- Space complexity: `O(n)`
<!-- Add your space complexity here, e.g. $$O(n)$$ -->
(worst case) for creating a new DataFrame.

# Code
```python
import pandas as pd

def dropMissingData(students: pd.DataFrame) -> pd.DataFrame:
    return pd.DataFrame(students)[students['name'].notnull()]
```
# My Solution

You can find my solution posted on Leetcode[here](https://leetcode.com/problems/drop-missing-data/solutions/5059052/simple-solution)

![image.png](https://assets.leetcode.com/users/images/20787b99-3640-49df-ad79-1328ed532574_1713791968.8637364.png)
