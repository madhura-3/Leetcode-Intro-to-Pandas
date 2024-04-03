# Intuition
Solving this problem is as easy as scoring a goal in a game of soccer! We just need to use pandas, our trusty teammate, and its built-in attribute called `shape` to find out how many players (rows) and attributes (columns) we have in our team DataFrame.

# Approach
We'll craft a function called `getDataframeSize`, acting as the coach's playbook. This function will accept our team `DataFrame players`. Inside, we'll execute calling `players.shape`, which returns a tuple with the number of rows and columns. We'll then convert this tuple to a list and deliver it as our result!

# Complexity
- Time complexity: `O(1)`

- Space complexity: `O(1)`

# Code
``` python
import pandas as pd

def getDataframeSize(players: pd.DataFrame) -> List[int]:
    return list(players.shape)
```

# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/get-the-size-of-a-dataframe/solutions/4967867/simple-solution)

![image.png](https://assets.leetcode.com/users/images/47d8bdb3-da5f-456e-bc0f-eae556235103_1712155765.365919.png)
