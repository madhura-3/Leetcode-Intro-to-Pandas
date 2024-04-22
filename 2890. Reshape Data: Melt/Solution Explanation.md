# Intuition
Imagine our DataFrame as a deck of cards, with each column representing a quarter of the year and each row representing a product. To reshuffle the deck and reveal the sales data in a more manageable format, we need to perform a trick known as "melting" the DataFrame.

# Approach
Just like melting ice cream on a sunny day, we can use pandas' melt function to transform our wide-format DataFrame into a long-format one. We specify the 'product' column as our identifier, while the quarters become our variables to melt. Then, we name the new columns 'quarter' and 'sales', creating a delightful mixture of product sales data.

# Complexity
- **Time complexity:** The melt function smoothly handles the reshuffling process by iterating over each element of the DataFrame once. Therefore, the time complexity is linearly proportional to the number of elements in the DataFrame, represented as O(n), where n is the total number of elements.
- **Space complexity:** As we reshape our DataFrame, the space complexity depends on the size of our melted DataFrame. Since the melted DataFrame retains the same number of elements as the original DataFrame, the space complexity is also linear, represented as O(n), where n is the total number of elements in the melted DataFrame.

# Code
```python
import pandas as pd

def meltTable(report: pd.DataFrame) -> pd.DataFrame:
    return (pd.melt(report, id_vars=['product'], var_name = 'quarter', value_name = 'sales'))
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/reshape-data-melt/solutions/4822612/sales-shuffle-melting-quarter-reports)


![image](https://github.com/madhura-3/Leetcode-Intro-to-Pandas/assets/42023529/3fade5c4-fe07-4c34-97d2-e129cb80f33f)
