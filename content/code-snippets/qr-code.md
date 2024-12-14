---
title: Qr-Code
date: 2024-12-13
author: Your Name
cell_count: 27
score: 25
---

```python

```


```python
!pip install qrcode
```

    Requirement already satisfied: qrcode in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (8.0)



```python
import qrcode
```


```python
def main():    
    
    qr = qrcode.QRCode(
        version=1,
        error_correction=qrcode.constants.ERROR_CORRECT_L,
        box_size=10,
        border=4,
    )
    qr.add_data('http://talentaccurate.com')
    qr.make(fit=True)

    img = qr.make_image(fill_color="black", back_color="white")    
    
    print(type(img))
    
    img.save("img.png","PNG")
```


```python
if __name__ == '__main__':
    main()

```

    <class 'qrcode.image.pil.PilImage'>



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


---
**Score: 25**
