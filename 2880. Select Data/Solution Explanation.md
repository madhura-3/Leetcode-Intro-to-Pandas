# Intuition
We want to retrieve the name and age of a particular student identified by their student ID. We can filter the DataFrame based on the ID and then select the desired columns.

# Approach
1. **Import pandas:** We'll import the pandas library for DataFrame operations.
2. **Define the function:** We'll create a function named `selectData` that takes a student DataFrame as input.
3. **Filter by ID:** We'll use boolean indexing to filter the DataFrame, keeping only rows where `student_id` equals 101.
4. **Select name and age:** We'll select the specific columns `'name'` and `'age'` from the filtered DataFrame.

# Complexity
- Time complexity: `O(n)` (worst case) for iterating through the DataFrame. In practice, with efficient indexing, it's often much faster.

- Space complexity: `O(n)` in the worst case for creating a new DataFrame.

# Code
``` python
import pandas as pd

def selectData(students: pd.DataFrame) -> pd.DataFrame:
    return students[students['student_id']== 101][['name', 'age']]
    
```
# My Solution
You can find my solution posted on Leetcode [here](https://leetcode.com/problems/select-data/solutions/5009142/simple-solution)

![image.png](https://assets.leetcode.com/users/images/d1562a75-917d-4f73-ab99-0f70f1e98718_1712858942.712688.png)
