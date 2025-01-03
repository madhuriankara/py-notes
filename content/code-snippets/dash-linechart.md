---
title: Dash-Linechart
date: 2025-01-03
author: Your Name
cell_count: 8
score: 5
---

```python

```


```python
!pip install dash
```

    Requirement already satisfied: dash in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (2.18.2)
    Requirement already satisfied: Flask<3.1,>=1.0.4 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (3.0.3)
    Requirement already satisfied: Werkzeug<3.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (3.0.6)
    Requirement already satisfied: plotly>=5.0.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (5.24.1)
    Requirement already satisfied: dash-html-components==2.0.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (2.0.0)
    Requirement already satisfied: dash-core-components==2.0.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (2.0.0)
    Requirement already satisfied: dash-table==5.0.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (5.0.0)
    Requirement already satisfied: importlib-metadata in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (8.5.0)
    Requirement already satisfied: typing-extensions>=4.1.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (4.12.2)
    Requirement already satisfied: requests in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (2.32.3)
    Requirement already satisfied: retrying in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (1.3.4)
    Requirement already satisfied: nest-asyncio in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (1.6.0)
    Requirement already satisfied: setuptools in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from dash) (75.1.0)
    Requirement already satisfied: Jinja2>=3.1.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Flask<3.1,>=1.0.4->dash) (3.1.4)
    Requirement already satisfied: itsdangerous>=2.1.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Flask<3.1,>=1.0.4->dash) (2.2.0)
    Requirement already satisfied: click>=8.1.3 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Flask<3.1,>=1.0.4->dash) (8.1.7)
    Requirement already satisfied: blinker>=1.6.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Flask<3.1,>=1.0.4->dash) (1.9.0)
    Requirement already satisfied: tenacity>=6.2.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from plotly>=5.0.0->dash) (9.0.0)
    Requirement already satisfied: packaging in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from plotly>=5.0.0->dash) (24.1)
    Requirement already satisfied: MarkupSafe>=2.1.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Werkzeug<3.1->dash) (3.0.2)
    Requirement already satisfied: zipp>=3.20 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from importlib-metadata->dash) (3.21.0)
    Requirement already satisfied: charset-normalizer<4,>=2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests->dash) (3.4.0)
    Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests->dash) (3.10)
    Requirement already satisfied: urllib3<3,>=1.21.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests->dash) (2.2.3)
    Requirement already satisfied: certifi>=2017.4.17 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from requests->dash) (2024.8.30)
    Requirement already satisfied: six>=1.7.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from retrying->dash) (1.16.0)



```python
import dash
from dash import dcc, html
from dash.dependencies import Input, Output
import plotly.express as px
import pandas as pd
```


```python
app = dash.Dash(__name__)
```


```python
df = pd.DataFrame({
    'X': [1, 2, 3, 4, 5],
    'Y': [2, 4, 6, 8, 10]
})
```


```python
app.layout = html.Div([
    # Title of the app
    html.H1("Simple Line Chart in Dash"),
    
    # Dropdown for selecting a color for the line
    dcc.Dropdown(
        id='color-dropdown',
        options=[
            {'label': 'Blue', 'value': 'blue'},
            {'label': 'Red', 'value': 'red'},
            {'label': 'Green', 'value': 'green'}
        ],
        value='blue',  # Default value
        style={'width': '50%'}
    ),
    
    # Graph to display the line chart
    dcc.Graph(id='line-chart')
])

```


```python
def update_chart(selected_color):
    fig = px.line(df, x='X', y='Y', title="Line Chart Example")
    fig.update_traces(line=dict(color=selected_color))  # Update the line color based on the dropdown
    return fig

# Run the app
if __name__ == '__main__':
    app.run_server(debug=True)

```



<iframe
    width="100%"
    height="650"
    src="http://127.0.0.1:8050/"
    frameborder="0"
    allowfullscreen

></iframe>




```python

```


---
**Score: 5**
