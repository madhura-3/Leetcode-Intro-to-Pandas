# Intuition
The `grade` column in the student DataFrame is currently stored as floats, even though grades are typically integers. We need to convert the data type of this column to integers.

# Approach
1. **Import pandas:** We'll import pandas for DataFrame operations.
2. **Define the function:** We'll create a function named `changeDatatype` that takes a student DataFrame as input.
3. **Convert grade to integer:** We'll use the `astype` method on a subset of the DataFrame containing only the 'grade' column. We'll specify `int` as the target data type.
4. **Return the modified DataFrame:** We'll return the DataFrame with the grade column converted to integers.
# Complexity
- Time complexity:`O(n)` linear time as we iterate through each row in the 'grade' column to convert the data type.

- Space complexity: `O(n)` proportional to the number of rows in the worst case, as a new DataFrame might be created.

# Code
```
import pandas as pd

def changeDatatype(students: pd.DataFrame) -> pd.DataFrame:
    students['grade'] = students[['grade']].astype(int)
    return students
```

# My Solution
You can find my solution posted on Leetcode [here](https://leetcode.com/problems/change-data-type/solutions/5014197/simple-solution)

![image.png](https://assets.leetcode.com/users/images/b82f4d94-0297-49ba-b3ea-92338e039fb7_1712959910.004877.png)
