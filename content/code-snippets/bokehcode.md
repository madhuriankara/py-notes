---
title: Bokehcode
date: 2024-11-28
author: Your Name
cell_count: 9
score: 5
---

```python

```


```python
!pip install bokeh
```

    Collecting bokeh
      Downloading bokeh-3.6.1-py3-none-any.whl.metadata (12 kB)
    Requirement already satisfied: Jinja2>=2.9 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (3.1.4)
    Requirement already satisfied: contourpy>=1.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (1.3.1)
    Requirement already satisfied: numpy>=1.16 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (1.26.4)
    Requirement already satisfied: packaging>=16.8 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (24.1)
    Requirement already satisfied: pandas>=1.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (2.2.3)
    Requirement already satisfied: pillow>=7.1.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (11.0.0)
    Requirement already satisfied: PyYAML>=3.10 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (6.0.2)
    Requirement already satisfied: tornado>=6.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from bokeh) (6.4.1)
    Collecting xyzservices>=2021.09.1 (from bokeh)
      Downloading xyzservices-2024.9.0-py3-none-any.whl.metadata (4.1 kB)
    Requirement already satisfied: MarkupSafe>=2.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from Jinja2>=2.9->bokeh) (3.0.2)
    Requirement already satisfied: python-dateutil>=2.8.2 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pandas>=1.2->bokeh) (2.9.0.post0)
    Requirement already satisfied: pytz>=2020.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pandas>=1.2->bokeh) (2024.2)
    Requirement already satisfied: tzdata>=2022.7 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from pandas>=1.2->bokeh) (2024.2)
    Requirement already satisfied: six>=1.5 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from python-dateutil>=2.8.2->pandas>=1.2->bokeh) (1.16.0)
    Downloading bokeh-3.6.1-py3-none-any.whl (6.9 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m6.9/6.9 MB[0m [31m33.3 MB/s[0m eta [36m0:00:00[0m MB/s[0m eta [36m0:00:01[0m
    [?25hDownloading xyzservices-2024.9.0-py3-none-any.whl (85 kB)
    Installing collected packages: xyzservices, bokeh
    Successfully installed bokeh-3.6.1 xyzservices-2024.9.0



```python
from bokeh.plotting import figure, show
from bokeh.io import output_file
```


```python

# Output to an HTML file
output_file("bokeh_line_plot.html")

# Data for the plot
x = [1, 2, 3, 4, 5]
y = [6, 7, 2, 4, 5]
```


```python
# Create a figure object
p = figure(
    title="Simple Bokeh Line Plot",
    x_axis_label="X-Axis",
    y_axis_label="Y-Axis",
    width=700,  # Use 'width' instead of 'plot_width'
    height=400,  # Use 'height' instead of 'plot_height'
)
```


```python
# Add a line to the figure
p.line(x, y, legend_label="Line", line_width=2, color="blue")

# Add points using scatter (replaces circle)
p.scatter(x, y, size=8, color="red", legend_label="Points")
```




<div style="display: table;"><div style="display: table-row;"><div style="display: table-cell;"><b title="bokeh.models.renderers.glyph_renderer.GlyphRenderer">GlyphRenderer</b>(</div><div style="display: table-cell;">id&nbsp;=&nbsp;'p1287', <span id="p1292" style="cursor: pointer;">&hellip;)</span></div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">context_menu&nbsp;=&nbsp;None,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">coordinates&nbsp;=&nbsp;None,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">css_classes&nbsp;=&nbsp;[],</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">css_variables&nbsp;=&nbsp;{},</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">data_source&nbsp;=&nbsp;ColumnDataSource(id='p1281', ...),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">glyph&nbsp;=&nbsp;Scatter(id='p1284', ...),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">group&nbsp;=&nbsp;None,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">hover_glyph&nbsp;=&nbsp;None,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_event_callbacks&nbsp;=&nbsp;{},</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_property_callbacks&nbsp;=&nbsp;{},</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">level&nbsp;=&nbsp;'glyph',</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted&nbsp;=&nbsp;False,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted_glyph&nbsp;=&nbsp;Scatter(id='p1286', ...),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">name&nbsp;=&nbsp;None,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">nonselection_glyph&nbsp;=&nbsp;Scatter(id='p1285', ...),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">propagate_hover&nbsp;=&nbsp;False,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">selection_glyph&nbsp;=&nbsp;'auto',</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">styles&nbsp;=&nbsp;{},</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">stylesheets&nbsp;=&nbsp;[],</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">subscribed_events&nbsp;=&nbsp;PropertyValueSet(),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">syncable&nbsp;=&nbsp;True,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">tags&nbsp;=&nbsp;[],</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">view&nbsp;=&nbsp;CDSView(id='p1288', ...),</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">visible&nbsp;=&nbsp;True,</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">x_range_name&nbsp;=&nbsp;'default',</div></div><div class="p1291" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">y_range_name&nbsp;=&nbsp;'default')</div></div></div>
<script>
(function() {
  let expanded = false;
  const ellipsis = document.getElementById("p1292");
  ellipsis.addEventListener("click", function() {
    const rows = document.getElementsByClassName("p1291");
    for (let i = 0; i < rows.length; i++) {
      const el = rows[i];
      el.style.display = expanded ? "none" : "table-row";
    }
    ellipsis.innerHTML = expanded ? "&hellip;)" : "&lsaquo;&lsaquo;&lsaquo;";
    expanded = !expanded;
  });
})();
</script>





```python
# Customize legend
p.legend.title = "Legend"
p.legend.label_text_font_size = "10pt"
```


```python
# Show the plot
show(p)
```


```python

```


---
**Score: 5**
