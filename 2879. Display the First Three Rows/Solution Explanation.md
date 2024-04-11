# Intuition
We want to efficiently display the first 3 rows of an employee DataFrame. Pandas offers a built-in method specifically designed for this task.

# Approach
1. **Import pandas:** We'll import the pandas library to work with DataFrames.
2. **Define the function:** We'll create a function `selectFirstRows` that takes an employee DataFrame as input.
3.**Utilize head method:** Inside the function, we'll use the `head` method of the DataFrame. This method conveniently retrieves the first `n` rows from the DataFrame.

# Complexity
- Time complexity: `O(1)` constant time, independent of DataFrame size.

- Space complexity: `O(n)` proportional to the number of rows returned.

# Code
``` python
import pandas as pd

def selectFirstRows(employees: pd.DataFrame) -> pd.DataFrame:
    return employees.head(3)
```
# My Solution
You can find my solution posted on Leetcode [here](https://leetcode.com/problems/display-the-first-three-rows/solutions/5009081/simple-solution)

![image.png](https://assets.leetcode.com/users/images/b8bd6d11-c756-4b83-b91c-e606940060f4_1712858249.9922154.png)
