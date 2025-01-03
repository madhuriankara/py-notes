---
title: Langchain-Basics
date: 2025-01-03
author: Your Name
cell_count: 12
score: 10
---

```python
#!pip install openai
```


```python
#!pip install langchain_openai
```


```python
#!pip install python-dotenv==0.21.0
```


```python
from langchain_core.output_parsers import StrOutputParser
from langchain_core.prompts import ChatPromptTemplate
from langchain_openai import ChatOpenAI
from constant import OPENAI_API_KEY
import os
```


```python
os.environ["OPENAI_API_KEY"] = OPENAI_API_KEY
```


```python


model = ChatOpenAI(model="gpt-4o-mini")

prompt = ChatPromptTemplate.from_template("tell me a joke about {topic}")

chain = prompt | model | StrOutputParser()
```


```python
chain.invoke({"topic": "bears"})
```




    'Why do bears have hairy coats?\n\nBecause they look silly in sweaters!'




```python
chain.invoke({"topic": "Developer"})
```




    'Why do developers prefer dark mode?\n\nBecause light attracts bugs!'




```python

```


```python

```


```python

```


```python

```


---
**Score: 10**
