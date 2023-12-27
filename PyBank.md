```python
import pandas as pd
from pathlib import Path
```


```python
# The path to our CSV file
budget_data = Path("Resources/budget_data.csv")
Budget_data_df = pd.read_csv(budget_data)
Budget_data_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Date</th>
      <th>Profit/Losses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Jan-10</td>
      <td>1088983</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Feb-10</td>
      <td>-354534</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mar-10</td>
      <td>276622</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Apr-10</td>
      <td>-728133</td>
    </tr>
    <tr>
      <th>4</th>
      <td>May-10</td>
      <td>852993</td>
    </tr>
  </tbody>
</table>
</div>




```python
results = pd.read_csv(budget_data)
print("Total Months:",
      len(results))
total = Budget_data_df['Profit/Losses'].sum()
print("Profit/Losses: $",
     total)
change = Budget_data_df
Budget_data_df['shifted_column'] = Budget_data_df['Profit/Losses'].shift(1)
Budget_data_df['difference'] = Budget_data_df['Profit/Losses'] - Budget_data_df['shifted_column']
average = Budget_data_df['difference'].mean()
maximum = Budget_data_df['difference'].max()
minimum = Budget_data_df['difference'].min()
print("Average Change: $",
       average)
print("Greatest Increase in Profits: $",
       maximum)
print("Greatet Decrease in Profits: $",
       minimum)
```

    Total Months: 86
    Profit/Losses: $ 22564198
    Average Change: $ -8311.105882352942
    Greatest Increase in Profits: $ 1862002.0
    Greatet Decrease in Profits: $ -1825558.0
    


```python

```
