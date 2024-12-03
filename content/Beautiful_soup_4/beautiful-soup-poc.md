---
title: Beautiful-Soup-Poc
date: 2024-12-03
author: Your Name
cell_count: 86
score: 85
---

```python
from bs4 import BeautifulSoup
import requests


```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"



```


```python
response = requests.get(url)



```


```python
if response.status_code == 200:
    soup = BeautifulSoup(response.content, 'html.parser')
    
    title = soup.find('h1').text
    print("Title tag:", title )
    
else:
    print("Failed to get the page.", response.status_code)
```

    Title tag: Sharp Objects



```python
from bs4 import BeautifulSoup
import requests

url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"

response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')



#Extact list items
list_items = soup.find_all('p')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")


```

    List item 1 : <p class="price_color">£47.82</p>
    List item 2 : <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock (20 available)
        
    </p>
    List item 3 : <p class="star-rating Four">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <!-- <small><a href="/catalogue/sharp-objects_997/reviews/">
            
                    
                        0 customer reviews
                    
            </a></small>
             --> 
    
    
    <!-- 
        <a id="write_review" href="/catalogue/sharp-objects_997/reviews/add/#addreview" class="btn btn-success btn-sm">
            Write a review
        </a>
    
     --></p>
    List item 4 : <p>WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since she left town eight years ago, Camille has hardly spoken to her neurotic, hypochondriac mother or to the half-sister she barely knows: a beautiful thirteen-year-old with an eerie grip on the town. Now, installed again in her family’s Victorian mansion, Camille is haunted by the childhood tragedy she has spent her whole life trying to cut from her memory. HARMFUL on her wrist, WHORE on her ankle As Camille works to uncover the truth about these violent crimes, she finds herself identifying with the young victims—a bit too strongly. Clues keep leading to dead ends, forcing Camille to unravel the psychological puzzle of her own past to get at the story. Dogged by her own demons, Camille will have to confront what happened to her years before if she wants to survive this homecoming.With its taut, crafted writing, Sharp Objects is addictive, haunting, and unforgettable. ...more</p>
    List item 5 : <p class="star-rating One">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    List item 6 : <p class="price_color">£50.10</p>
    List item 7 : <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>
    List item 8 : <p class="star-rating One">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    List item 9 : <p class="price_color">£53.74</p>
    List item 10 : <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>
    List item 11 : <p class="star-rating Three">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    List item 12 : <p class="price_color">£51.77</p>
    List item 13 : <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>



```python
def tags_iterater():
    result = []
    for i in range(1,7):
        print(f'h{i}')
        result.append(f'h{i}')
    return result
    
tags_iterater()  
```

    h1
    h2
    h3
    h4
    h5
    h6





    ['h1', 'h2', 'h3', 'h4', 'h5', 'h6']




```python
from bs4 import BeautifulSoup
import requests

```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
```


```python
soup = BeautifulSoup(response.content,'html.parser')
```


```python

for idx, item in tags_iterater():
    list_items = soup.find_all(f'{idx}{item}')
    for idx, item in enumerate(list_items, start=1):    
        print(f"List item {idx} : {item}")
    
    

```

    h1
    h2
    h3
    h4
    h5
    h6
    List item 1 : <h1>Sharp Objects</h1>
    List item 1 : <h2>Product Description</h2>
    List item 2 : <h2>Product Information</h2>
    List item 3 : <h2>Products you recently viewed</h2>
    List item 1 : <h3><a href="../soumission_998/index.html" title="Soumission">Soumission</a></h3>
    List item 2 : <h3><a href="../tipping-the-velvet_999/index.html" title="Tipping the Velvet">Tipping the Velvet</a></h3>
    List item 3 : <h3><a href="../a-light-in-the-attic_1000/index.html" title="A Light in the Attic">A Light in the ...</a></h3>



```python

```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('a')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <a href="../../index.html">Books to Scrape</a>
    List item 2 : <a href="../../index.html">Home</a>
    List item 3 : <a href="../category/books_1/index.html">Books</a>
    List item 4 : <a href="../category/books/mystery_3/index.html">Mystery</a>
    List item 5 : <a href="../soumission_998/index.html"><img alt="Soumission" class="thumbnail" src="../../media/cache/3e/ef/3eef99c9d9adef34639f510662022830.jpg"/></a>
    List item 6 : <a href="../soumission_998/index.html" title="Soumission">Soumission</a>
    List item 7 : <a href="../tipping-the-velvet_999/index.html"><img alt="Tipping the Velvet" class="thumbnail" src="../../media/cache/26/0c/260c6ae16bce31c8f8c95daddd9f4a1c.jpg"/></a>
    List item 8 : <a href="../tipping-the-velvet_999/index.html" title="Tipping the Velvet">Tipping the Velvet</a>
    List item 9 : <a href="../a-light-in-the-attic_1000/index.html"><img alt="A Light in the Attic" class="thumbnail" src="../../media/cache/2c/da/2cdad67c44b002e7ead0cc35693c0e8b.jpg"/></a>
    List item 10 : <a href="../a-light-in-the-attic_1000/index.html" title="A Light in the Attic">A Light in the ...</a>



```python
#image sourcing
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('img')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <img alt="Sharp Objects" src="../../media/cache/c0/59/c05972805aa7201171b8fc71a5b00292.jpg"/>
    List item 2 : <img alt="Soumission" class="thumbnail" src="../../media/cache/3e/ef/3eef99c9d9adef34639f510662022830.jpg"/>
    List item 3 : <img alt="Tipping the Velvet" class="thumbnail" src="../../media/cache/26/0c/260c6ae16bce31c8f8c95daddd9f4a1c.jpg"/>
    List item 4 : <img alt="A Light in the Attic" class="thumbnail" src="../../media/cache/2c/da/2cdad67c44b002e7ead0cc35693c0e8b.jpg"/>



```python
#metadata scraping
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('meta')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <meta content="text/html; charset=utf-8" http-equiv="content-type"/>
    List item 2 : <meta content="24th Jun 2016 09:29" name="created"/>
    List item 3 : <meta content="
        WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since she left town eight years ago, Camille has hardly spoken to her neurotic, hypochondriac mother or to the half-sister she barely knows: a beautiful thirteen-year-old with an eerie grip on the town. Now, installed again in her family’s Victorian mansion, Camille is haunted by the childhood tragedy she has spent her whole life trying to cut from her memory. HARMFUL on her wrist, WHORE on her ankle As Camille works to uncover the truth about these violent crimes, she finds herself identifying with the young victims—a bit too strongly. Clues keep leading to dead ends, forcing Camille to unravel the psychological puzzle of her own past to get at the story. Dogged by her own demons, Camille will have to confront what happened to her years before if she wants to survive this homecoming.With its taut, crafted writing, Sharp Objects is addictive, haunting, and unforgettable. ...more
    " name="description"/>
    List item 4 : <meta content="width=device-width" name="viewport"/>
    List item 5 : <meta content="NOARCHIVE,NOCACHE" name="robots"/>



```python
#Webpage table contents
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('table')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <table class="table table-striped">
    <tr>
    <th>UPC</th><td>e00eb4fd7b871a48</td>
    </tr>
    <tr>
    <th>Product Type</th><td>Books</td>
    </tr>
    <tr>
    <th>Price (excl. tax)</th><td>£47.82</td>
    </tr>
    <tr>
    <th>Price (incl. tax)</th><td>£47.82</td>
    </tr>
    <tr>
    <th>Tax</th><td>£0.00</td>
    </tr>
    <tr>
    <th>Availability</th>
    <td>In stock (20 available)</td>
    </tr>
    <tr>
    <th>Number of reviews</th>
    <td>0</td>
    </tr>
    </table>



```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
#There is no span tags present in the url
list_items = soup.find_all('span')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```


```python

```


```python
#Class and ID-Based Selection
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
#product_gallery
```


```python
items = soup.find('div' ,class_='col-sm-6 product_main').text
```


```python
#items_id = items.get('id')
```


```python
#items_text = items.text
```


```python
#items_id
```


```python
#content_inner > article > div.row > div.col-sm-6.product_main
```


```python
items
```




    '\nSharp Objects\n£47.82\n\n\n    \n        In stock (20 available)\n    \n\n\n\n\n\n\n\n\xa0\n\n\n\n\nWarning! This is a demo website for web scraping purposes. Prices and ratings here were randomly assigned and have no real meaning.\n'




```python

```


```python
#Form Data Extraction
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('button')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    List item 2 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    List item 3 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>



```python

```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
tags = ['form','input','button']
```


```python
for item in tags:
    list_items = soup.find_all(item)
    for idx, item in enumerate(list_items, start=1):    
        print(f"List item {idx} : {item}")
```

    List item 1 : <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    List item 2 : <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    List item 3 : <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    List item 1 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    List item 2 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    List item 3 : <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>



```python

```


```python
#12. Scraping JSON Data Embedded in HTML
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
list_items = soup.find_all('script')
for idx, item in enumerate(list_items, start=1):    
    print(f"List item {idx} : {item}")
```

    List item 1 : <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
    List item 2 : <script>window.jQuery || document.write('<script src="../../static/oscar/js/jquery/jquery-1.9.1.min.js"><\/script>')</script>
    List item 3 : <script src="../../static/oscar/js/bootstrap3/bootstrap.min.js" type="text/javascript"></script>
    List item 4 : <script charset="utf-8" src="../../static/oscar/js/oscar/ui.js" type="text/javascript"></script>
    List item 5 : <script charset="utf-8" src="../../static/oscar/js/bootstrap-datetimepicker/bootstrap-datetimepicker.js" type="text/javascript"></script>
    List item 6 : <script charset="utf-8" src="../../static/oscar/js/bootstrap-datetimepicker/locales/bootstrap-datetimepicker.all.js" type="text/javascript"></script>
    List item 7 : <script type="text/javascript">
                $(function() {
                    
        
        oscar.init();
    
                });
            </script>



```python

```


```python

```


```python
##default > div > div > div.content
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
```


```python
response = requests.get(url)
soup = BeautifulSoup(response.content,'html.parser')
```


```python
items = soup.find('div', class_='content')
```


```python
items
```




    <div class="content">
    <div id="promotions">
    </div>
    <div id="content_inner">
    <article class="product_page"><!-- Start of product page -->
    <div class="row">
    <div class="col-sm-6">
    <div class="carousel" id="product_gallery">
    <div class="thumbnail">
    <div class="carousel-inner">
    <div class="item active">
    <img alt="Sharp Objects" src="../../media/cache/c0/59/c05972805aa7201171b8fc71a5b00292.jpg"/>
    </div>
    </div>
    </div>
    </div>
    </div>
    <div class="col-sm-6 product_main">
    <h1>Sharp Objects</h1>
    <p class="price_color">£47.82</p>
    <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock (20 available)
        
    </p>
    <p class="star-rating Four">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <!-- <small><a href="/catalogue/sharp-objects_997/reviews/">
            
                    
                        0 customer reviews
                    
            </a></small>
             --> 
    
    
    <!-- 
        <a id="write_review" href="/catalogue/sharp-objects_997/reviews/add/#addreview" class="btn btn-success btn-sm">
            Write a review
        </a>
    
     --></p>
    <hr/>
    <div class="alert alert-warning" role="alert"><strong>Warning!</strong> This is a demo website for web scraping purposes. Prices and ratings here were randomly assigned and have no real meaning.</div>
    </div><!-- /col-sm-6 -->
    </div><!-- /row -->
    <div class="sub-header" id="product_description">
    <h2>Product Description</h2>
    </div>
    <p>WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since WICKED above her hipbone, GIRL across her heart Words are like a road map to reporter Camille Preaker’s troubled past. Fresh from a brief stay at a psych hospital, Camille’s first assignment from the second-rate daily paper where she works brings her reluctantly back to her hometown to cover the murders of two preteen girls. NASTY on her kneecap, BABYDOLL on her leg Since she left town eight years ago, Camille has hardly spoken to her neurotic, hypochondriac mother or to the half-sister she barely knows: a beautiful thirteen-year-old with an eerie grip on the town. Now, installed again in her family’s Victorian mansion, Camille is haunted by the childhood tragedy she has spent her whole life trying to cut from her memory. HARMFUL on her wrist, WHORE on her ankle As Camille works to uncover the truth about these violent crimes, she finds herself identifying with the young victims—a bit too strongly. Clues keep leading to dead ends, forcing Camille to unravel the psychological puzzle of her own past to get at the story. Dogged by her own demons, Camille will have to confront what happened to her years before if she wants to survive this homecoming.With its taut, crafted writing, Sharp Objects is addictive, haunting, and unforgettable. ...more</p>
    <div class="sub-header">
    <h2>Product Information</h2>
    </div>
    <table class="table table-striped">
    <tr>
    <th>UPC</th><td>e00eb4fd7b871a48</td>
    </tr>
    <tr>
    <th>Product Type</th><td>Books</td>
    </tr>
    <tr>
    <th>Price (excl. tax)</th><td>£47.82</td>
    </tr>
    <tr>
    <th>Price (incl. tax)</th><td>£47.82</td>
    </tr>
    <tr>
    <th>Tax</th><td>£0.00</td>
    </tr>
    <tr>
    <th>Availability</th>
    <td>In stock (20 available)</td>
    </tr>
    <tr>
    <th>Number of reviews</th>
    <td>0</td>
    </tr>
    </table>
    <section>
    <div class="sub-header" id="reviews">
    </div>
    </section>
    <div class="sub-header">
    <h2>Products you recently viewed</h2>
    </div>
    <ul class="row">
    <li class="col-xs-6 col-sm-4 col-md-3 col-lg-3">
    <article class="product_pod">
    <div class="image_container">
    <a href="../soumission_998/index.html"><img alt="Soumission" class="thumbnail" src="../../media/cache/3e/ef/3eef99c9d9adef34639f510662022830.jpg"/></a>
    </div>
    <p class="star-rating One">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    <h3><a href="../soumission_998/index.html" title="Soumission">Soumission</a></h3>
    <div class="product_price">
    <p class="price_color">£50.10</p>
    <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>
    <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    </div>
    </article>
    </li>
    <li class="col-xs-6 col-sm-4 col-md-3 col-lg-3">
    <article class="product_pod">
    <div class="image_container">
    <a href="../tipping-the-velvet_999/index.html"><img alt="Tipping the Velvet" class="thumbnail" src="../../media/cache/26/0c/260c6ae16bce31c8f8c95daddd9f4a1c.jpg"/></a>
    </div>
    <p class="star-rating One">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    <h3><a href="../tipping-the-velvet_999/index.html" title="Tipping the Velvet">Tipping the Velvet</a></h3>
    <div class="product_price">
    <p class="price_color">£53.74</p>
    <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>
    <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    </div>
    </article>
    </li>
    <li class="col-xs-6 col-sm-4 col-md-3 col-lg-3">
    <article class="product_pod">
    <div class="image_container">
    <a href="../a-light-in-the-attic_1000/index.html"><img alt="A Light in the Attic" class="thumbnail" src="../../media/cache/2c/da/2cdad67c44b002e7ead0cc35693c0e8b.jpg"/></a>
    </div>
    <p class="star-rating Three">
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    <i class="icon-star"></i>
    </p>
    <h3><a href="../a-light-in-the-attic_1000/index.html" title="A Light in the Attic">A Light in the ...</a></h3>
    <div class="product_price">
    <p class="price_color">£51.77</p>
    <p class="instock availability">
    <i class="icon-ok"></i>
        
            In stock
        
    </p>
    <form>
    <button class="btn btn-primary btn-block" data-loading-text="Adding..." type="submit">Add to basket</button>
    </form>
    </div>
    </article>
    </li>
    </ul>
    </article><!-- End of product page -->
    </div>
    </div>




```python

```


```python
#Use CSS selectors with select() to scrape specific elements.
```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
response = requests.get(url)
soup  = BeautifulSoup(response.content, 'html.parser')
links = soup.select('a.Mystery')  

for link in links:
   
    url = link.get('href')  
    print(url)  
```


```python
url
```




    'https://books.toscrape.com/catalogue/sharp-objects_997/index.html'




```python

```


```python

```


```python
from bs4 import BeautifulSoup
import requests
```


```python
url = "https://books.toscrape.com/catalogue/sharp-objects_997/index.html"
response = requests.get(url)
soup  = BeautifulSoup(response.content, 'html.parser')
custom_tags = soup.find_all('custom-tag')
for tag in custom_tags:
    paragraph = tag.find('p')
    if paragraph:
        print(paragraph.text.strip())
```


```python

```


```python

```


```python

```


```python

```


---
**Score: 85**
