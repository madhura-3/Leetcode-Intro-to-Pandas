# Intuition
Concatenating two DataFrames vertically means stacking them on top of each other. 
This operation is commonly performed in data manipulation tasks, and there are specific tools available in libraries like pandas for such operations.

# Approach
The word Concatenated tables gave direct hint for using pandas concat. 
This function efficiently combines the DataFrames along the specified axis, allowing for vertical stacking in this case.

# Complexity

- Time complexity: `O(n)`
- Space complexity: `O(n)`

# Code
```python
import pandas as pd

def concatenateTables(df1: pd.DataFrame, df2: pd.DataFrame) -> pd.DataFrame:
    return pd.concat([df1, df2])
```

# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/reshape-data-concatenate/solutions/4791046/easyto-understand)
