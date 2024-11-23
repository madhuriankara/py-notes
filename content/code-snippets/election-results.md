---
title: Election-Results
date: 2024-11-23
author: Your Name
cell_count: 4
score: 0
---

```python


import requests
from bs4 import BeautifulSoup


```


```python

def main():
    
    #print('Main')
    
    # Collect and parse first page
    page = requests.get('https://newsinteractives.cbc.ca/elections/federal/2019/results/')
    soup = BeautifulSoup(page.text, 'html.parser')    
    
    #print(soup)    

    items = soup.select('div.party-standings__table__row span')

    item_list = ''
    for item in items:

        print(item)

        name = item.get_text().strip()

        
        print('['+str(name)+']')
        #item_list =  item_list + ',' +str(item.get_text())
    
    #print(item_list)
        

```


```python
if __name__ == '__main__':
    main()


```

    <span>170 seats to majority</span>
    [170 seats to majority]
    <span class="triangle"></span>
    []
    <span aria-label="Elected" class="elected-container"><img alt="" src="/elections/federal/2019/results/assets/images/icons/icon-check-white.svg"/></span>
    []
    <span class="party-name" v-text="formatPartyName(party.englishName)"></span>
    []
    <span class="party-code" v-text="party.englishCode"></span>
    []
    <span class="hide-sm">Vote Share</span>
    [Vote Share]
    <span class="hide-lg">Share</span>
    [Share]
    <span aria-label="Elected" class="elected-container"><img alt="" src="/elections/federal/2019/results/assets/images/icons/icon-check-white.svg"/></span>
    []
    <span class="party-name" v-text="formatPartyName(party.englishName)"></span>
    []
    <span class="party-code" v-text="party.englishCode"></span>
    []
    <span role="cell"><p v-text="party.electedSeats"></p></span>
    []
    <span role="cell"><p v-text="party.leadingSeats"></p></span>
    []
    <span role="cell"><p v-text="(parseFloat(party.totalVotesPercentage * 100) || 0).toFixed(1) + '%'"></p></span>
    []
    <span role="cell"><p v-text="party.totalVotes.toLocaleString()"></p></span>
    []
    <span class="bar loss">
    <span class="fill" v-bind:style="getPartyStyle(party.englishCode)" v-if="getPartyAttribute(party.englishCode, 'net') &lt; 0"></span>
    </span>
    []
    <span class="fill" v-bind:style="getPartyStyle(party.englishCode)" v-if="getPartyAttribute(party.englishCode, 'net') &lt; 0"></span>
    []
    <span class="bar gain">
    <span class="fill" v-bind:style="getPartyStyle(party.englishCode)" v-if="getPartyAttribute(party.englishCode, 'net') &gt; 0"></span>
    </span>
    []
    <span class="fill" v-bind:style="getPartyStyle(party.englishCode)" v-if="getPartyAttribute(party.englishCode, 'net') &gt; 0"></span>
    []



```python

```


---
**Score: 0**
