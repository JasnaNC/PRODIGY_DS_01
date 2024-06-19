# TASK 1

# Importing and checking dataset



```python
import pandas as pd
import matplotlib.pyplot as plt
import os
```


```python
data=pd.read_csv("C:\\Users\\LENOVO\\OneDrive\\Desktop\\MY personal\\New folder\\titanic csv.csv")
data
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
      <th>Passenger_No</th>
      <th>first_name</th>
      <th>last_name</th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
      <th>DECK_NUMBER</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Steven</td>
      <td>King</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22</td>
      <td>0</td>
      <td>24000</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>A</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>90</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Ross</td>
      <td>Kochhar</td>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38</td>
      <td>0</td>
      <td>50806</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>90</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Alex</td>
      <td>Urman</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26</td>
      <td>0</td>
      <td>54071</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>90</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Bruce</td>
      <td>Popp</td>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35</td>
      <td>0</td>
      <td>26969</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>60</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>David</td>
      <td>Raphaely</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35</td>
      <td>0</td>
      <td>34048</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>60</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>Nancy</td>
      <td>Khoo</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>27</td>
      <td>0</td>
      <td>46206</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
      <td>70</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>John</td>
      <td>Baida</td>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54</td>
      <td>0</td>
      <td>63090</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>70</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>Daniel</td>
      <td>Weiss</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2</td>
      <td>1</td>
      <td>56356</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>70</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>Sigal</td>
      <td>Kaufling</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27</td>
      <td>2</td>
      <td>23488</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>A</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>60</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>Adam</td>
      <td>Vollman</td>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14</td>
      <td>0</td>
      <td>29047</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>B</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>90</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11</td>
      <td>Mathew</td>
      <td>Himuro</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4</td>
      <td>1</td>
      <td>51428</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>100</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12</td>
      <td>Harvey</td>
      <td>Mikkilineni</td>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>58</td>
      <td>0</td>
      <td>61770</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>100</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13</td>
      <td>Kevin</td>
      <td>Rogers</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>20</td>
      <td>0</td>
      <td>30897</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>70</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14</td>
      <td>Julia</td>
      <td>Patel</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>39</td>
      <td>5</td>
      <td>59197</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>80</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15</td>
      <td>Irene</td>
      <td>Davies</td>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>14</td>
      <td>0</td>
      <td>61211</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>80</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>James</td>
      <td>Zlotkey</td>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>55</td>
      <td>0</td>
      <td>43386</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>D</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>80</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17</td>
      <td>Jason</td>
      <td>Bernstein</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2</td>
      <td>1</td>
      <td>27978</td>
      <td>Q</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
      <td>100</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18</td>
      <td>Peter</td>
      <td>Hall</td>
      <td>1</td>
      <td>2</td>
      <td>male</td>
      <td>34</td>
      <td>0</td>
      <td>46632</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>80</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19</td>
      <td>Sartha</td>
      <td>Sully</td>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>31</td>
      <td>0</td>
      <td>66662</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>D</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>60</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20</td>
      <td>William</td>
      <td>Smith</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>29</td>
      <td>0</td>
      <td>38628</td>
      <td>C</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>D</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
      <td>70</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21</td>
      <td>Jack</td>
      <td>Greene</td>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>35</td>
      <td>0</td>
      <td>20068</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>G</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 21 entries, 0 to 20
    Data columns (total 18 columns):
     #   Column        Non-Null Count  Dtype 
    ---  ------        --------------  ----- 
     0   Passenger_No  21 non-null     int64 
     1   first_name    21 non-null     object
     2   last_name     21 non-null     object
     3   survived      21 non-null     int64 
     4   pclass        21 non-null     int64 
     5   sex           21 non-null     object
     6   age           21 non-null     int64 
     7   parch         21 non-null     int64 
     8   fare          21 non-null     int64 
     9   embarked      21 non-null     object
     10  class         21 non-null     object
     11  who           21 non-null     object
     12  adult_male    21 non-null     bool  
     13  deck          21 non-null     object
     14  embark_town   21 non-null     object
     15  alive         21 non-null     object
     16  alone         21 non-null     bool  
     17  DECK_NUMBER   21 non-null     int64 
    dtypes: bool(2), int64(7), object(9)
    memory usage: 2.8+ KB
    


```python
data.describe()
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
      <th>Passenger_No</th>
      <th>survived</th>
      <th>pclass</th>
      <th>age</th>
      <th>parch</th>
      <th>fare</th>
      <th>DECK_NUMBER</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>21.000000</td>
      <td>21.000000</td>
      <td>21.000000</td>
      <td>21.000000</td>
      <td>21.000000</td>
      <td>21.000000</td>
      <td>21.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>11.000000</td>
      <td>0.476190</td>
      <td>2.428571</td>
      <td>28.619048</td>
      <td>0.476190</td>
      <td>43616.095238</td>
      <td>79.047619</td>
    </tr>
    <tr>
      <th>std</th>
      <td>6.204837</td>
      <td>0.511766</td>
      <td>0.810643</td>
      <td>16.026466</td>
      <td>1.167007</td>
      <td>15081.489823</td>
      <td>13.749459</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>20068.000000</td>
      <td>60.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>6.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
      <td>29047.000000</td>
      <td>70.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>11.000000</td>
      <td>0.000000</td>
      <td>3.000000</td>
      <td>29.000000</td>
      <td>0.000000</td>
      <td>46206.000000</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>16.000000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>35.000000</td>
      <td>0.000000</td>
      <td>56356.000000</td>
      <td>90.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>21.000000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>58.000000</td>
      <td>5.000000</td>
      <td>66662.000000</td>
      <td>100.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.isna().sum()
```




    Passenger_No    0
    first_name      0
    last_name       0
    survived        0
    pclass          0
    sex             0
    age             0
    parch           0
    fare            0
    embarked        0
    class           0
    who             0
    adult_male      0
    deck            0
    embark_town     0
    alive           0
    alone           0
    DECK_NUMBER     0
    dtype: int64




```python
data.duplicated().sum()
```




    0



# Age Distribution: A Histogram of Passenger Ages


```python
x=data['age']
plt.xlabel("age")
plt.ylabel("frequency")
plt.hist(x, bins=20, edgecolor='black')
age_summary=x.describe()
print(age_summary)
```

    count    21.000000
    mean     28.619048
    std      16.026466
    min       2.000000
    25%      20.000000
    50%      29.000000
    75%      35.000000
    max      58.000000
    Name: age, dtype: float64
    


    
![png](output_9_1.png)
    


# Fare Distribution: A Histogram of fare paid by passengers


```python
x=data['fare']
plt.xlabel("fare")
plt.ylabel("frequency")
plt.hist(x, edgecolor='black')
age_summary=x.describe()
print(age_summary)
```

    count       21.000000
    mean     43616.095238
    std      15081.489823
    min      20068.000000
    25%      29047.000000
    50%      46206.000000
    75%      56356.000000
    max      66662.000000
    Name: fare, dtype: float64
    


    
![png](output_11_1.png)
    


# Histogram showing the distribution of embark town


```python
x=data['embark_town']
plt.xlabel("age")
plt.ylabel("frequency")
plt.hist(x, edgecolor='black')
age_summary=x.describe()
print(age_summary)
```

    count              21
    unique              3
    top       Southampton
    freq               16
    Name: embark_town, dtype: object
    


    
![png](output_13_1.png)
    


# Bar Chart of Passenger Survival Status: Alive vs Not Alive


```python
alive=data['alive']
count=alive.value_counts()
count=pd.DataFrame(count)
print(count.index,count['alive'])
plt.figure(figsize=(5,4))
plt.bar(count.index, count['alive'])
plt.xlabel('Alive or not')
plt.ylabel('Count')
plt.title('Distribution of passengers who are alive or not')
```

    Index(['no', 'yes'], dtype='object') no     11
    yes    10
    Name: alive, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of passengers are alive or not')




    
![png](output_15_2.png)
    


# Histogram shows the distribution of alive passengers in each deck


```python
alive_data = data[data['alive'] == 'yes']
print(alive_data)
deck=alive_data['deck']
count=deck.value_counts()
count=pd.DataFrame(count)
print(count.index,count['deck'])
plt.figure(figsize=(5,4))
plt.bar(count.index, count['deck'])
plt.xlabel('decks in which people are alive')
plt.ylabel('Count')
plt.title('Distribution of alive passengers in each deck')
```

        Passenger_No first_name    last_name  survived  pclass     sex  age  \
    1              2       Ross      Kochhar         1       1  female   38   
    2              3       Alex        Urman         1       3  female   26   
    3              4      Bruce         Popp         1       1  female   35   
    8              9      Sigal     Kaufling         1       3  female   27   
    9             10       Adam      Vollman         1       2  female   14   
    10            11     Mathew       Himuro         1       3  female    4   
    11            12     Harvey  Mikkilineni         1       1  female   58   
    15            16      James      Zlotkey         1       2  female   55   
    17            18      Peter         Hall         1       2    male   34   
    19            20    William        Smith         1       3  female   29   
    
        parch   fare embarked   class    who  adult_male deck  embark_town alive  \
    1       0  50806        C   First  woman       False    C    Cherbourg   yes   
    2       0  54071        S   Third  woman       False    B  Southampton   yes   
    3       0  26969        S   First  woman       False    C  Southampton   yes   
    8       2  23488        S   Third  woman       False    A  Southampton   yes   
    9       0  29047        C  Second  child       False    B    Cherbourg   yes   
    10      1  51428        S   Third  child       False    G  Southampton   yes   
    11      0  61770        S   First  woman       False    C  Southampton   yes   
    15      0  43386        S  Second  woman       False    D  Southampton   yes   
    17      0  46632        S  Second    man        True    B  Southampton   yes   
    19      0  38628        C   Third  woman       False    D    Cherbourg   yes   
    
        alone  DECK_NUMBER  
    1   False           90  
    2    True           90  
    3   False           60  
    8   False           60  
    9   False           90  
    10  False          100  
    11   True          100  
    15   True           80  
    17   True           80  
    19   True           70  
    Index(['C', 'B', 'D', 'A', 'G'], dtype='object') C    3
    B    3
    D    2
    A    1
    G    1
    Name: deck, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of alive passengers in each deck')




    
![png](output_17_2.png)
    


# Deck-wise Distribution of passengers who are not alive


```python
dead_data = data[data['alive'] == 'no']
print(dead_data)
deck=dead_data['deck']
count=deck.value_counts()
count=pd.DataFrame(count)
print(count.index,count['deck'])
plt.figure(figsize=(5,4))
plt.bar(count.index, count['deck'])
plt.xlabel('decks in which people are not alive')
plt.ylabel('Count')
plt.title('Deck-wise Distribution of passengers who are not alive')
```

        Passenger_No first_name  last_name  survived  pclass     sex  age  parch  \
    0              1     Steven       King         0       3    male   22      0   
    4              5      David   Raphaely         0       3    male   35      0   
    5              6      Nancy       Khoo         0       3    male   27      0   
    6              7       John      Baida         0       1    male   54      0   
    7              8     Daniel      Weiss         0       3    male    2      1   
    12            13      Kevin     Rogers         0       3    male   20      0   
    13            14      Julia      Patel         0       3    male   39      5   
    14            15      Irene     Davies         0       3  female   14      0   
    16            17      Jason  Bernstein         0       3    male    2      1   
    18            19     Sartha      Sully         0       3  female   31      0   
    20            21       Jack     Greene         0       2    male   35      0   
    
         fare embarked   class    who  adult_male deck  embark_town alive  alone  \
    0   24000        S   Third    man        True    A  Southampton    no  False   
    4   34048        S   Third    man        True    C  Southampton    no   True   
    5   46206        Q   Third    man        True    E   Queenstown    no   True   
    6   63090        S   First    man        True    E  Southampton    no   True   
    7   56356        S   Third  child       False    G  Southampton    no  False   
    12  30897        S   Third    man        True    C  Southampton    no   True   
    13  59197        S   Third    man        True    C  Southampton    no  False   
    14  61211        S   Third  child       False    G  Southampton    no   True   
    16  27978        Q   Third  child       False    G   Queenstown    no  False   
    18  66662        S   Third  woman       False    D  Southampton    no  False   
    20  20068        S  Second    man        True    G  Southampton    no   True   
    
        DECK_NUMBER  
    0            90  
    4            60  
    5            70  
    6            70  
    7            70  
    12           70  
    13           80  
    14           80  
    16          100  
    18           60  
    20           90  
    Index(['G', 'C', 'E', 'A', 'D'], dtype='object') G    4
    C    3
    E    2
    A    1
    D    1
    Name: deck, dtype: int64
    




    Text(0.5, 1.0, 'Deck-wise Distribution of passengers who are not alive')




    
![png](output_19_2.png)
    


# Histogram showing the distribution of gender of alive passengers


```python
alive_data = data[data['alive'] == 'yes']
sex=alive_data['sex']
count=sex.value_counts()
count=pd.DataFrame(count)
print(count.index,count['sex'])
plt.figure(figsize=(5,4))
plt.bar(count.index, count['sex'])
plt.xlabel('Gender of alive passengers')
plt.ylabel('Count')
plt.title('Distribution of gender of alive passengers')
```

    Index(['female', 'male'], dtype='object') female    9
    male      1
    Name: sex, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of gender of alive passengers')




    
![png](output_21_2.png)
    


# Histogram showing the distribution of gender of passengers who are not alive


```python
notalive_data = data[data['alive'] == 'no']
sex=notalive_data['sex']
count=sex.value_counts()
count=pd.DataFrame(count)
print(count.index,count['sex'])
plt.figure(figsize=(5,4))
plt.bar(count.index, count['sex'])
plt.xlabel('Gender of passengers who are not alive')
plt.ylabel('Count')
plt.title('Distribution of gender of passengers who are not alive')
```

    Index(['male', 'female'], dtype='object') male      9
    female    2
    Name: sex, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of gender of passengers who are not alive')




    
![png](output_23_2.png)
    


# Histogram that visualizes the distribution of deck numbers for passengers who are alive 


```python
alive_data = data[data['alive'] == 'yes']
deck_num=alive_data['DECK_NUMBER']
count=deck_num.value_counts()
count=pd.DataFrame(count)
print(count.index,count['DECK_NUMBER'])
plt.figure(figsize=(10,5))
plt.bar(count.index, count['DECK_NUMBER'])
plt.xlabel('Deck no. in which passengers are alive')
plt.ylabel('Count')
plt.title('Distribution of deck numbers for passengers who are alive')
```

    Int64Index([90, 60, 100, 80, 70], dtype='int64') 90     3
    60     2
    100    2
    80     2
    70     1
    Name: DECK_NUMBER, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of deck numbers for passengers who are alive')




    
![png](output_25_2.png)
    


# Histogram that visualizes the distribution of deck numbers for passengers who are alive


```python
notalive_data = data[data['alive'] == 'no']
deck_num=notalive_data['DECK_NUMBER']
count=deck_num.value_counts()
count=pd.DataFrame(count)
print(count.index,count['DECK_NUMBER'])
plt.figure(figsize=(10,5))
plt.bar(count.index, count['DECK_NUMBER'])
plt.xlabel('Deck no. in which passengers are not alive')
plt.ylabel('Count')
plt.title('Distribution of deck numbers for passengers who are not alive')
```

    Int64Index([70, 90, 60, 80, 100], dtype='int64') 70     4
    90     2
    60     2
    80     2
    100    1
    Name: DECK_NUMBER, dtype: int64
    




    Text(0.5, 1.0, 'Distribution of deck numbers for passengers who are not alive')




    
![png](output_27_2.png)
    



```python

```
