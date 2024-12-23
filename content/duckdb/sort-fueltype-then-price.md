---
title: Sort-Fueltype-Then-Price
date: 2024-12-23
author: Your Name
cell_count: 7
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE automobile AS SELECT * FROM 'automobile_data.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x107a918b0>




```python
#Sort the dataset first by fuel-type and then by price.
```


```python
result = con.execute("""SELECT make,"fuel-type",price
                       FROM automobile
                    WHERE price != '?'
                    ORDER BY "fuel-type",price ASC """).fetchall()
```


```python
result
```




    [('toyota', 'diesel', '10698'),
     ('mazda', 'diesel', '10795'),
     ('peugot', 'diesel', '13200'),
     ('volkswagen', 'diesel', '13845'),
     ('peugot', 'diesel', '13860'),
     ('peugot', 'diesel', '16900'),
     ('peugot', 'diesel', '17075'),
     ('peugot', 'diesel', '17950'),
     ('mazda', 'diesel', '18344'),
     ('volvo', 'diesel', '22470'),
     ('mercedes-benz', 'diesel', '25552'),
     ('mercedes-benz', 'diesel', '28176'),
     ('mercedes-benz', 'diesel', '28248'),
     ('mercedes-benz', 'diesel', '31600'),
     ('nissan', 'diesel', '7099'),
     ('volkswagen', 'diesel', '7775'),
     ('toyota', 'diesel', '7788'),
     ('toyota', 'diesel', '7898'),
     ('volkswagen', 'diesel', '7995'),
     ('volkswagen', 'diesel', '9495'),
     ('subaru', 'gas', '10198'),
     ('mazda', 'gas', '10245'),
     ('honda', 'gas', '10295'),
     ('honda', 'gas', '10345'),
     ('mazda', 'gas', '10595'),
     ('toyota', 'gas', '10898'),
     ('mazda', 'gas', '10945'),
     ('isuzu', 'gas', '11048'),
     ('toyota', 'gas', '11199'),
     ('mazda', 'gas', '11245'),
     ('toyota', 'gas', '11248'),
     ('subaru', 'gas', '11259'),
     ('toyota', 'gas', '11549'),
     ('volkswagen', 'gas', '11595'),
     ('subaru', 'gas', '11694'),
     ('mazda', 'gas', '11845'),
     ('saab', 'gas', '11850'),
     ('peugot', 'gas', '11900'),
     ('saab', 'gas', '12170'),
     ('volkswagen', 'gas', '12290'),
     ('peugot', 'gas', '12440'),
     ('mitsubishi', 'gas', '12629'),
     ('plymouth', 'gas', '12764'),
     ('volvo', 'gas', '12940'),
     ('honda', 'gas', '12945'),
     ('dodge', 'gas', '12964'),
     ('volkswagen', 'gas', '13295'),
     ('volvo', 'gas', '13415'),
     ('alfa-romero', 'gas', '13495'),
     ('nissan', 'gas', '13499'),
     ('nissan', 'gas', '13499'),
     ('mazda', 'gas', '13645'),
     ('audi', 'gas', '13950'),
     ('nissan', 'gas', '14399'),
     ('mitsubishi', 'gas', '14489'),
     ('mitsubishi', 'gas', '14869'),
     ('saab', 'gas', '15040'),
     ('audi', 'gas', '15250'),
     ('saab', 'gas', '15510'),
     ('peugot', 'gas', '15580'),
     ('mazda', 'gas', '15645'),
     ('toyota', 'gas', '15690'),
     ('toyota', 'gas', '15750'),
     ('volvo', 'gas', '15985'),
     ('toyota', 'gas', '15998'),
     ('bmw', 'gas', '16430'),
     ('alfa-romero', 'gas', '16500'),
     ('alfa-romero', 'gas', '16500'),
     ('mercury', 'gas', '16503'),
     ('volvo', 'gas', '16515'),
     ('toyota', 'gas', '16558'),
     ('peugot', 'gas', '16630'),
     ('peugot', 'gas', '16695'),
     ('volvo', 'gas', '16845'),
     ('bmw', 'gas', '16925'),
     ('nissan', 'gas', '17199'),
     ('audi', 'gas', '17450'),
     ('toyota', 'gas', '17669'),
     ('audi', 'gas', '17710'),
     ('peugot', 'gas', '18150'),
     ('saab', 'gas', '18150'),
     ('mazda', 'gas', '18280'),
     ('nissan', 'gas', '18399'),
     ('volvo', 'gas', '18420'),
     ('saab', 'gas', '18620'),
     ('audi', 'gas', '18920'),
     ('volvo', 'gas', '18950'),
     ('volvo', 'gas', '19045'),
     ('nissan', 'gas', '19699'),
     ('bmw', 'gas', '20970'),
     ('bmw', 'gas', '21105'),
     ('volvo', 'gas', '21485'),
     ('porsche', 'gas', '22018'),
     ('volvo', 'gas', '22625'),
     ('audi', 'gas', '23875'),
     ('bmw', 'gas', '24565'),
     ('bmw', 'gas', '30760'),
     ('jaguar', 'gas', '32250'),
     ('porsche', 'gas', '32528'),
     ('porsche', 'gas', '34028'),
     ('mercedes-benz', 'gas', '34184'),
     ('mercedes-benz', 'gas', '35056'),
     ('jaguar', 'gas', '35550'),
     ('jaguar', 'gas', '36000'),
     ('bmw', 'gas', '36880'),
     ('porsche', 'gas', '37028'),
     ('mercedes-benz', 'gas', '40960'),
     ('bmw', 'gas', '41315'),
     ('mercedes-benz', 'gas', '45400'),
     ('subaru', 'gas', '5118'),
     ('chevrolet', 'gas', '5151'),
     ('mazda', 'gas', '5195'),
     ('toyota', 'gas', '5348'),
     ('mitsubishi', 'gas', '5389'),
     ('honda', 'gas', '5399'),
     ('nissan', 'gas', '5499'),
     ('dodge', 'gas', '5572'),
     ('plymouth', 'gas', '5572'),
     ('mazda', 'gas', '6095'),
     ('mitsubishi', 'gas', '6189'),
     ('dodge', 'gas', '6229'),
     ('plymouth', 'gas', '6229'),
     ('chevrolet', 'gas', '6295'),
     ('toyota', 'gas', '6338'),
     ('dodge', 'gas', '6377'),
     ('honda', 'gas', '6479'),
     ('toyota', 'gas', '6488'),
     ('honda', 'gas', '6529'),
     ('chevrolet', 'gas', '6575'),
     ('nissan', 'gas', '6649'),
     ('mitsubishi', 'gas', '6669'),
     ('dodge', 'gas', '6692'),
     ('plymouth', 'gas', '6692'),
     ('mazda', 'gas', '6695'),
     ('isuzu', 'gas', '6785'),
     ('mazda', 'gas', '6795'),
     ('nissan', 'gas', '6849'),
     ('honda', 'gas', '6855'),
     ('toyota', 'gas', '6918'),
     ('toyota', 'gas', '6938'),
     ('mitsubishi', 'gas', '6989'),
     ('subaru', 'gas', '7053'),
     ('subaru', 'gas', '7126'),
     ('honda', 'gas', '7129'),
     ('toyota', 'gas', '7198'),
     ('honda', 'gas', '7295'),
     ('honda', 'gas', '7295'),
     ('nissan', 'gas', '7299'),
     ('nissan', 'gas', '7349'),
     ('mazda', 'gas', '7395'),
     ('subaru', 'gas', '7463'),
     ('nissan', 'gas', '7499'),
     ('subaru', 'gas', '7603'),
     ('dodge', 'gas', '7609'),
     ('plymouth', 'gas', '7609'),
     ('mitsubishi', 'gas', '7689'),
     ('toyota', 'gas', '7738'),
     ('subaru', 'gas', '7775'),
     ('nissan', 'gas', '7799'),
     ('honda', 'gas', '7895'),
     ('toyota', 'gas', '7898'),
     ('dodge', 'gas', '7957'),
     ('plymouth', 'gas', '7957'),
     ('volkswagen', 'gas', '7975'),
     ('nissan', 'gas', '7999'),
     ('subaru', 'gas', '8013'),
     ('toyota', 'gas', '8058'),
     ('mitsubishi', 'gas', '8189'),
     ('volkswagen', 'gas', '8195'),
     ('toyota', 'gas', '8238'),
     ('nissan', 'gas', '8249'),
     ('toyota', 'gas', '8358'),
     ('toyota', 'gas', '8449'),
     ('mazda', 'gas', '8495'),
     ('volkswagen', 'gas', '8495'),
     ('mitsubishi', 'gas', '8499'),
     ('dodge', 'gas', '8558'),
     ('toyota', 'gas', '8778'),
     ('honda', 'gas', '8845'),
     ('mazda', 'gas', '8845'),
     ('dodge', 'gas', '8921'),
     ('plymouth', 'gas', '8921'),
     ('toyota', 'gas', '8948'),
     ('nissan', 'gas', '8949'),
     ('honda', 'gas', '9095'),
     ('subaru', 'gas', '9233'),
     ('toyota', 'gas', '9258'),
     ('mitsubishi', 'gas', '9279'),
     ('mitsubishi', 'gas', '9279'),
     ('renault', 'gas', '9295'),
     ('toyota', 'gas', '9298'),
     ('toyota', 'gas', '9538'),
     ('nissan', 'gas', '9549'),
     ('toyota', 'gas', '9639'),
     ('renault', 'gas', '9895'),
     ('mitsubishi', 'gas', '9959'),
     ('subaru', 'gas', '9960'),
     ('volkswagen', 'gas', '9980'),
     ('toyota', 'gas', '9988'),
     ('toyota', 'gas', '9989'),
     ('volkswagen', 'gas', '9995')]




```python

```


---
**Score: 5**
