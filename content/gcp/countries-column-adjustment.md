---
title: Countries-Column-Adjustment
date: 2025-01-22
author: Your Name
cell_count: 21
score: 20
---

```python
import pandas as pd
```


```python
FILEPATH = "../countries-of-the-world-cleaned.csv"
```


```python
df = pd.read_csv(FILEPATH)
```


```python

```


```python
df
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
      <th>Unnamed: 0</th>
      <th>country</th>
      <th>region</th>
      <th>population</th>
      <th>area_sq_mi</th>
      <th>pop_density_per_sq_mi</th>
      <th>coastline_coastarea_ratio</th>
      <th>net_migration</th>
      <th>infant_mortality_per_1000_births</th>
      <th>gdp_$_per_capita</th>
      <th>...</th>
      <th>phones_per_1000</th>
      <th>arable_</th>
      <th>crops_</th>
      <th>other_</th>
      <th>climate</th>
      <th>birthrate</th>
      <th>deathrate</th>
      <th>agriculture</th>
      <th>industry</th>
      <th>service</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>Afghanistan</td>
      <td>ASIA (EX. NEAR EAST)</td>
      <td>31056997</td>
      <td>647500</td>
      <td>48,0</td>
      <td>0,00</td>
      <td>23,06</td>
      <td>163,07</td>
      <td>700.0</td>
      <td>...</td>
      <td>3,2</td>
      <td>12,13</td>
      <td>0,22</td>
      <td>87,65</td>
      <td>1</td>
      <td>46,6</td>
      <td>20,34</td>
      <td>0,38</td>
      <td>0,24</td>
      <td>0,38</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>Albania</td>
      <td>EASTERN EUROPE</td>
      <td>3581655</td>
      <td>28748</td>
      <td>124,6</td>
      <td>1,26</td>
      <td>-4,93</td>
      <td>21,52</td>
      <td>4500.0</td>
      <td>...</td>
      <td>71,2</td>
      <td>21,09</td>
      <td>4,42</td>
      <td>74,49</td>
      <td>3</td>
      <td>15,11</td>
      <td>5,22</td>
      <td>0,232</td>
      <td>0,188</td>
      <td>0,579</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>Algeria</td>
      <td>NORTHERN AFRICA</td>
      <td>32930091</td>
      <td>2381740</td>
      <td>13,8</td>
      <td>0,04</td>
      <td>-0,39</td>
      <td>31</td>
      <td>6000.0</td>
      <td>...</td>
      <td>78,1</td>
      <td>3,22</td>
      <td>0,25</td>
      <td>96,53</td>
      <td>1</td>
      <td>17,14</td>
      <td>4,61</td>
      <td>0,101</td>
      <td>0,6</td>
      <td>0,298</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>American Samoa</td>
      <td>OCEANIA</td>
      <td>57794</td>
      <td>199</td>
      <td>290,4</td>
      <td>58,29</td>
      <td>-20,71</td>
      <td>9,27</td>
      <td>8000.0</td>
      <td>...</td>
      <td>259,5</td>
      <td>10</td>
      <td>15</td>
      <td>75</td>
      <td>2</td>
      <td>22,46</td>
      <td>3,27</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>Andorra</td>
      <td>WESTERN EUROPE</td>
      <td>71201</td>
      <td>468</td>
      <td>152,1</td>
      <td>0,00</td>
      <td>6,6</td>
      <td>4,05</td>
      <td>19000.0</td>
      <td>...</td>
      <td>497,2</td>
      <td>2,22</td>
      <td>0</td>
      <td>97,78</td>
      <td>3</td>
      <td>8,71</td>
      <td>6,25</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>222</th>
      <td>222</td>
      <td>West Bank</td>
      <td>NEAR EAST</td>
      <td>2460492</td>
      <td>5860</td>
      <td>419,9</td>
      <td>0,00</td>
      <td>2,98</td>
      <td>19,62</td>
      <td>800.0</td>
      <td>...</td>
      <td>145,2</td>
      <td>16,9</td>
      <td>18,97</td>
      <td>64,13</td>
      <td>3</td>
      <td>31,67</td>
      <td>3,92</td>
      <td>0,09</td>
      <td>0,28</td>
      <td>0,63</td>
    </tr>
    <tr>
      <th>223</th>
      <td>223</td>
      <td>Western Sahara</td>
      <td>NORTHERN AFRICA</td>
      <td>273008</td>
      <td>266000</td>
      <td>1,0</td>
      <td>0,42</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>NaN</td>
      <td>0,02</td>
      <td>0</td>
      <td>99,98</td>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0,4</td>
    </tr>
    <tr>
      <th>224</th>
      <td>224</td>
      <td>Yemen</td>
      <td>NEAR EAST</td>
      <td>21456188</td>
      <td>527970</td>
      <td>40,6</td>
      <td>0,36</td>
      <td>0</td>
      <td>61,5</td>
      <td>800.0</td>
      <td>...</td>
      <td>37,2</td>
      <td>2,78</td>
      <td>0,24</td>
      <td>96,98</td>
      <td>1</td>
      <td>42,89</td>
      <td>8,3</td>
      <td>0,135</td>
      <td>0,472</td>
      <td>0,393</td>
    </tr>
    <tr>
      <th>225</th>
      <td>225</td>
      <td>Zambia</td>
      <td>SUB-SAHARAN AFRICA</td>
      <td>11502010</td>
      <td>752614</td>
      <td>15,3</td>
      <td>0,00</td>
      <td>0</td>
      <td>88,29</td>
      <td>800.0</td>
      <td>...</td>
      <td>8,2</td>
      <td>7,08</td>
      <td>0,03</td>
      <td>92,9</td>
      <td>2</td>
      <td>41</td>
      <td>19,93</td>
      <td>0,22</td>
      <td>0,29</td>
      <td>0,489</td>
    </tr>
    <tr>
      <th>226</th>
      <td>226</td>
      <td>Zimbabwe</td>
      <td>SUB-SAHARAN AFRICA</td>
      <td>12236805</td>
      <td>390580</td>
      <td>31,3</td>
      <td>0,00</td>
      <td>0</td>
      <td>67,69</td>
      <td>1900.0</td>
      <td>...</td>
      <td>26,8</td>
      <td>8,32</td>
      <td>0,34</td>
      <td>91,34</td>
      <td>2</td>
      <td>28,01</td>
      <td>21,84</td>
      <td>0,179</td>
      <td>0,243</td>
      <td>0,579</td>
    </tr>
  </tbody>
</table>
<p>227 rows × 21 columns</p>
</div>




```python
df.columns 
```




    Index(['Country', 'Region', 'Population', 'Area (sq. mi.)',
           'Pop. Density (per sq. mi.)', 'Coastline (coast/area ratio)',
           'Net migration', 'Infant mortality (per 1000 births)',
           'GDP ($ per capita)', 'Literacy (%)', 'Phones (per 1000)', 'Arable (%)',
           'Crops (%)', 'Other (%)', 'Climate', 'Birthrate', 'Deathrate',
           'Agriculture', 'Industry', 'Service'],
          dtype='object')




```python
for col in li
```


```python

        
```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python
df_population = df[df['Population'] > 60000]
```


```python
df_population
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
      <th>Country</th>
      <th>Region</th>
      <th>Population</th>
      <th>Area (sq. mi.)</th>
      <th>Pop. Density (per sq. mi.)</th>
      <th>Coastline (coast/area ratio)</th>
      <th>Net migration</th>
      <th>Infant mortality (per 1000 births)</th>
      <th>GDP ($ per capita)</th>
      <th>Literacy (%)</th>
      <th>Phones (per 1000)</th>
      <th>Arable (%)</th>
      <th>Crops (%)</th>
      <th>Other (%)</th>
      <th>Climate</th>
      <th>Birthrate</th>
      <th>Deathrate</th>
      <th>Agriculture</th>
      <th>Industry</th>
      <th>Service</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Afghanistan</td>
      <td>ASIA (EX. NEAR EAST)</td>
      <td>31056997</td>
      <td>647500</td>
      <td>48,0</td>
      <td>0,00</td>
      <td>23,06</td>
      <td>163,07</td>
      <td>700.0</td>
      <td>36,0</td>
      <td>3,2</td>
      <td>12,13</td>
      <td>0,22</td>
      <td>87,65</td>
      <td>1</td>
      <td>46,6</td>
      <td>20,34</td>
      <td>0,38</td>
      <td>0,24</td>
      <td>0,38</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Albania</td>
      <td>EASTERN EUROPE</td>
      <td>3581655</td>
      <td>28748</td>
      <td>124,6</td>
      <td>1,26</td>
      <td>-4,93</td>
      <td>21,52</td>
      <td>4500.0</td>
      <td>86,5</td>
      <td>71,2</td>
      <td>21,09</td>
      <td>4,42</td>
      <td>74,49</td>
      <td>3</td>
      <td>15,11</td>
      <td>5,22</td>
      <td>0,232</td>
      <td>0,188</td>
      <td>0,579</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Algeria</td>
      <td>NORTHERN AFRICA</td>
      <td>32930091</td>
      <td>2381740</td>
      <td>13,8</td>
      <td>0,04</td>
      <td>-0,39</td>
      <td>31</td>
      <td>6000.0</td>
      <td>70,0</td>
      <td>78,1</td>
      <td>3,22</td>
      <td>0,25</td>
      <td>96,53</td>
      <td>1</td>
      <td>17,14</td>
      <td>4,61</td>
      <td>0,101</td>
      <td>0,6</td>
      <td>0,298</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Andorra</td>
      <td>WESTERN EUROPE</td>
      <td>71201</td>
      <td>468</td>
      <td>152,1</td>
      <td>0,00</td>
      <td>6,6</td>
      <td>4,05</td>
      <td>19000.0</td>
      <td>100,0</td>
      <td>497,2</td>
      <td>2,22</td>
      <td>0</td>
      <td>97,78</td>
      <td>3</td>
      <td>8,71</td>
      <td>6,25</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Angola</td>
      <td>SUB-SAHARAN AFRICA</td>
      <td>12127071</td>
      <td>1246700</td>
      <td>9,7</td>
      <td>0,13</td>
      <td>0</td>
      <td>191,19</td>
      <td>1900.0</td>
      <td>42,0</td>
      <td>7,8</td>
      <td>2,41</td>
      <td>0,24</td>
      <td>97,35</td>
      <td>NaN</td>
      <td>45,11</td>
      <td>24,2</td>
      <td>0,096</td>
      <td>0,658</td>
      <td>0,246</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>222</th>
      <td>West Bank</td>
      <td>NEAR EAST</td>
      <td>2460492</td>
      <td>5860</td>
      <td>419,9</td>
      <td>0,00</td>
      <td>2,98</td>
      <td>19,62</td>
      <td>800.0</td>
      <td>NaN</td>
      <td>145,2</td>
      <td>16,9</td>
      <td>18,97</td>
      <td>64,13</td>
      <td>3</td>
      <td>31,67</td>
      <td>3,92</td>
      <td>0,09</td>
      <td>0,28</td>
      <td>0,63</td>
    </tr>
    <tr>
      <th>223</th>
      <td>Western Sahara</td>
      <td>NORTHERN AFRICA</td>
      <td>273008</td>
      <td>266000</td>
      <td>1,0</td>
      <td>0,42</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0,02</td>
      <td>0</td>
      <td>99,98</td>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0,4</td>
    </tr>
    <tr>
      <th>224</th>
      <td>Yemen</td>
      <td>NEAR EAST</td>
      <td>21456188</td>
      <td>527970</td>
      <td>40,6</td>
      <td>0,36</td>
      <td>0</td>
      <td>61,5</td>
      <td>800.0</td>
      <td>50,2</td>
      <td>37,2</td>
      <td>2,78</td>
      <td>0,24</td>
      <td>96,98</td>
      <td>1</td>
      <td>42,89</td>
      <td>8,3</td>
      <td>0,135</td>
      <td>0,472</td>
      <td>0,393</td>
    </tr>
    <tr>
      <th>225</th>
      <td>Zambia</td>
      <td>SUB-SAHARAN AFRICA</td>
      <td>11502010</td>
      <td>752614</td>
      <td>15,3</td>
      <td>0,00</td>
      <td>0</td>
      <td>88,29</td>
      <td>800.0</td>
      <td>80,6</td>
      <td>8,2</td>
      <td>7,08</td>
      <td>0,03</td>
      <td>92,9</td>
      <td>2</td>
      <td>41</td>
      <td>19,93</td>
      <td>0,22</td>
      <td>0,29</td>
      <td>0,489</td>
    </tr>
    <tr>
      <th>226</th>
      <td>Zimbabwe</td>
      <td>SUB-SAHARAN AFRICA</td>
      <td>12236805</td>
      <td>390580</td>
      <td>31,3</td>
      <td>0,00</td>
      <td>0</td>
      <td>67,69</td>
      <td>1900.0</td>
      <td>90,7</td>
      <td>26,8</td>
      <td>8,32</td>
      <td>0,34</td>
      <td>91,34</td>
      <td>2</td>
      <td>28,01</td>
      <td>21,84</td>
      <td>0,179</td>
      <td>0,243</td>
      <td>0,579</td>
    </tr>
  </tbody>
</table>
<p>207 rows × 20 columns</p>
</div>




```python
result = df[df['Country'] == 'Angola'] [['Country','Region']]
```


```python
result
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
      <th>Country</th>
      <th>Region</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df['Population']
```




    0      31056997
    1       3581655
    2      32930091
    3         57794
    4         71201
             ...   
    222     2460492
    223      273008
    224    21456188
    225    11502010
    226    12236805
    Name: Population, Length: 227, dtype: int64




```python
df.columns

```




    Index(['Unnamed: 0', 'country', 'region', 'population', 'area_sq_mi',
           'pop_density_per_sq_mi', 'coastline_coastarea_ratio', 'net_migration',
           'infant_mortality_per_1000_births', 'gdp_$_per_capita', 'literacy_',
           'phones_per_1000', 'arable_', 'crops_', 'other_', 'climate',
           'birthrate', 'deathrate', 'agriculture', 'industry', 'service'],
          dtype='object')




```python

```


---
**Score: 20**
