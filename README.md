## Remember how to connect to an sqlite database?


```python
#connect to the db 'parlgov-development' in the data folder
```


```python
#__SOLUTION__

import sqlite3

conn = sqlite3.connect('data/parlgov-development.sqlite')
```

### And select data from the table `view_election`?


```python
#your code here
```


```python
#__SOLUTION__

import pandas as pd

elections = pd.read_sql("select * from view_election", conn)
elections.head()
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
      <th>country_name_short</th>
      <th>country_name</th>
      <th>election_type</th>
      <th>election_date</th>
      <th>vote_share</th>
      <th>seats</th>
      <th>seats_total</th>
      <th>party_name_short</th>
      <th>party_name</th>
      <th>party_name_english</th>
      <th>left_right</th>
      <th>country_id</th>
      <th>election_id</th>
      <th>previous_parliament_election_id</th>
      <th>previous_cabinet_id</th>
      <th>party_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>AUS</td>
      <td>Australia</td>
      <td>parliament</td>
      <td>1901-03-30</td>
      <td>44.4</td>
      <td>32.0</td>
      <td>75</td>
      <td>PP</td>
      <td>Protectionist Party</td>
      <td>Protectionist Party</td>
      <td>7.4000</td>
      <td>33</td>
      <td>731</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1898</td>
    </tr>
    <tr>
      <td>1</td>
      <td>AUS</td>
      <td>Australia</td>
      <td>parliament</td>
      <td>1901-03-30</td>
      <td>34.2</td>
      <td>26.0</td>
      <td>75</td>
      <td>FTP</td>
      <td>Free Trade Party</td>
      <td>Free Trade Party</td>
      <td>6.0000</td>
      <td>33</td>
      <td>731</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1938</td>
    </tr>
    <tr>
      <td>2</td>
      <td>AUS</td>
      <td>Australia</td>
      <td>parliament</td>
      <td>1901-03-30</td>
      <td>19.4</td>
      <td>15.0</td>
      <td>75</td>
      <td>ALP</td>
      <td>Australian Labor Party</td>
      <td>Australian Labor Party</td>
      <td>3.8833</td>
      <td>33</td>
      <td>731</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1253</td>
    </tr>
    <tr>
      <td>3</td>
      <td>AUS</td>
      <td>Australia</td>
      <td>parliament</td>
      <td>1901-03-30</td>
      <td>1.4</td>
      <td>1.0</td>
      <td>75</td>
      <td>none</td>
      <td>no party affiliation</td>
      <td>no party affiliation</td>
      <td>NaN</td>
      <td>33</td>
      <td>731</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1396</td>
    </tr>
    <tr>
      <td>4</td>
      <td>AUS</td>
      <td>Australia</td>
      <td>parliament</td>
      <td>1901-03-30</td>
      <td>0.6</td>
      <td>1.0</td>
      <td>75</td>
      <td>one-seat</td>
      <td>one seat</td>
      <td>one seat</td>
      <td>NaN</td>
      <td>33</td>
      <td>731</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2299</td>
    </tr>
  </tbody>
</table>
</div>



# DON'T FORGET TO CLOSE THE DB CONNECTION WHEN YOU'RE DONE QUERYING!!!!!


```python
#your code to close the connection here
```


```python
#__SOLUTION__

conn.close()
```

Good luck on the code challenge, you'll all do fine


```python

```
