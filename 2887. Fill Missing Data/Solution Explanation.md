# Intuition
The `quantity` column has missing values (denoted as `None` in this case). We want to replace these missing values with a specific value, in this case, 0.

# Approach
1. **Import pandas:** We'll import pandas for DataFrame manipulation.
2. **Define the function:** We'll create a function named `fillMissingValues` that takes a product DataFrame as input.
3. **Fill missing values in quantity:** We'll use the `fillna` method on the 'quantity' column. We'll specify 0 as the value to replace missing values.
4. **Return the modified DataFrame:** We'll return the DataFrame with missing quantities replaced by 0.

# Complexity
- Time complexity: `O(n)` linear time as we iterate through each row to check for missing values.

- Space complexity: `O(n)` proportional to the number of rows in the worst case, as a new DataFrame might be created.

# Code
```python
import pandas as pd

def fillMissingValues(products: pd.DataFrame) -> pd.DataFrame:
    products['quantity'] = products['quantity'].fillna(0)
    return products   
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/fill-missing-data/solutions/5014088/simple-solution)

![image.png](https://assets.leetcode.com/users/images/e71a0252-cb03-4653-a3a7-07078475436f_1712955955.1047943.png)
