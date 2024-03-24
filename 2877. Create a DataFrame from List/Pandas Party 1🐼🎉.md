# Intuition
To solve this problem, we can use the pandas library in Python, which provides an easy way to create DataFrames. We'll iterate through the given 2D list of student data and create a DataFrame with columns for student IDs and ages.

# Approach
We'll utilize the pd.DataFrame() constructor from pandas to create a DataFrame. We'll specify the column names as 'student_id' and 'age', and pass the student data to create the DataFrame. Finally, we'll return the created DataFrame.

# Complexity
- Time complexity: O(n), where n is the number of students in the input list.

- Space complexity: O(n), where n is the number of students in the input list.

# Code
```
import pandas as pd

def createDataframe(student_data: List[List[int]]) -> pd.DataFrame:
    df = pd.DataFrame(student_data, columns=['student_id','age'])
    return df
```