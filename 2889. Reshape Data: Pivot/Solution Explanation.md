# Intuition
When we look at the problem, we see that we need to transform the data from a long format to a wide format, 
where each city becomes a separate column and each row represents temperatures for a specific month. This transformation is commonly known as pivoting.

# Approach
To pivot the data, we use pandas' pivot_table function. We set the index to be the 'month' column, the columns to 
be the 'city' column, and the values to be the 'temperature' column. Additionally, we use the 'max' aggregation function to handle duplicate entries, 
ensuring that we have the maximum temperature for each city in case there are multiple temperature records for the same month.

# Complexity

- **Time complexity:** The time complexity of the pivot_table function largely depends on the size of the DataFrame.
  In this case, it's relatively efficient as it's based on hash tables, giving it an average time complexity of O(n).
- **Space complexity:** The space complexity is also dependent on the size of the resulting pivoted DataFrame.
  It's O(m * n), where m is the number of unique months and n is the number of unique cities.

# Code
```python
import pandas as pd

def pivotTable(weather: pd.DataFrame) -> pd.DataFrame:
    return (weather.pivot_table(index = 'month', columns = 'city', values = 'temperature', aggfunc = 'max'))
```
# My Solution

You can find my solution posted on Leetcode [here](https://leetcode.com/problems/reshape-data-pivot/solutions/4818717/weather-waves-pivoting-city-temperatures)

![image](https://github.com/madhura-3/Leetcode-Intro-to-Pandas/assets/42023529/8f8c2320-9c7c-4d4a-b3a5-d46d834eb8d5)
