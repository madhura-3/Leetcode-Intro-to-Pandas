# Intuition
We want to remove duplicate email addresses from the DataFrame while ensuring we keep at least one instance of each unique email.

# Approach
1. **Import pandas:** We'll import pandas for DataFrame operations.
2. **Define the function:** We'll create a function named `dropDuplicateEmails` that takes a customer DataFrame as input.
3. **Utilize drop_duplicates:** We'll use the `drop_duplicates` method of the DataFrame.
    - `subset` argument specifies the column(s) to consider for identifying duplicates (here, 'email').
    - `keep='first'` ensures we keep the first occurrence of each unique email address.
    - `inplace=True` modifies the original DataFrame directly (optional, but efficient).
4. **Return the modified DataFrame:** We'll return the DataFrame with duplicates removed.

# Complexity
- Time complexity: `O(nlogn)` (worst case) due to sorting involved in duplicate removal.

- Space complexity: `O(n)` in the worst case for modifying the DataFrame in-place.

# Code
```python
import pandas as pd

def dropDuplicateEmails(customers: pd.DataFrame) -> pd.DataFrame:
   customers.drop_duplicates(subset = ['email'], keep = 'first', inplace = True)
   return customers  
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/drop-duplicate-rows/solutions/5009478/simple-solution)

<img src = "https://assets.leetcode.com/users/images/988c1916-f0fa-48b7-a5bb-9a89f7431d3f_1712863372.661613.png" width = "500">
