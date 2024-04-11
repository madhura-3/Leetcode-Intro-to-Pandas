# Intuition
The company wants to give employees a bonus, which is simply double their salary. To achieve this in a DataFrame, we can create a new column named "bonus" and populate it with the doubled salary values.

# Approach
1. **Import pandas:** We'll import pandas to work with DataFrames.
2. **Define the function:** We'll create a function named `createBonusColumn` that takes an employee DataFrame as input.
3. **Create the bonus column:** We'll add a new column named `"bonus"` to the DataFrame. We'll assign the doubled salary values from the `"salary"` column to this new column.
4. **Return the modified DataFrame:** We'll return the DataFrame with the added bonus column.

# Complexity
- Time complexity: `O(n)` (linear time) as we iterate through each row in the DataFrame to create the bonus column.

- Space complexity: `O(n)` proportional to the number of rows in the worst case, as a new DataFrame with an additional column is created.

# Code
``` python
import pandas as pd

def createBonusColumn(employees: pd.DataFrame) -> pd.DataFrame:
    employees['bonus'] = employees['salary'] * 2
    return employees
    
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/create-a-new-column/solutions/5009273/simple-solution)

![image.png](https://assets.leetcode.com/users/images/97ef23c2-0319-4137-9554-fb2e17b9b6ee_1712860484.8236983.png)
