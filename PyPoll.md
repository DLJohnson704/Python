```python
import pandas as pd
from pathlib import Path
```


```python
election_data = Path("election_data.csv")
election_data_df = pd.read_csv(election_data)
election_data_df.head()

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
      <th>Ballot ID</th>
      <th>County</th>
      <th>Candidate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1323913</td>
      <td>Jefferson</td>
      <td>Charles Casper Stockham</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1005842</td>
      <td>Jefferson</td>
      <td>Charles Casper Stockham</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1880345</td>
      <td>Jefferson</td>
      <td>Charles Casper Stockham</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1600337</td>
      <td>Jefferson</td>
      <td>Charles Casper Stockham</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1835994</td>
      <td>Jefferson</td>
      <td>Charles Casper Stockham</td>
    </tr>
  </tbody>
</table>
</div>




```python
total_votes = int()
results = pd.read_csv(election_data)
print("Total Votes:",
      len(results))
election_data = election_data_df.groupby("Candidate")["Candidate"].count() 
election_data
   

```

    Total Votes: 369711
    




    Candidate
    Charles Casper Stockham     85213
    Diana DeGette              272892
    Raymon Anthony Doane        11606
    Name: Candidate, dtype: int64




```python
winner = 
```


```python
print("Winner : Diana Degette") 

	
```

    Winner : Diana Degette
    


```python
	
```


```python
#
```


```python

```
