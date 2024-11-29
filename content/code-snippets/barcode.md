---
title: Barcode
date: 2024-11-28
author: Your Name
cell_count: 7
score: 5
---

```python
pip install python-barcode

```

    Collecting python-barcode
      Downloading python_barcode-0.15.1-py3-none-any.whl.metadata (2.3 kB)
    Downloading python_barcode-0.15.1-py3-none-any.whl (212 kB)
    Installing collected packages: python-barcode
    Successfully installed python-barcode-0.15.1
    Note: you may need to restart the kernel to use updated packages.



```python
from barcode import EAN13
```


```python
from barcode.writer import ImageWriter
```


```python
def generate_ean13_barcode(number, filename):
    """
    Generates an EAN-13 barcode and saves it as an image.
    :param number: 12-digit string for the barcode.
    :param filename: Name of the output file (without extension).
    """
    if len(number) != 12 or not number.isdigit():
        raise ValueError("EAN-13 requires a 12-digit input.")

    # Create an EAN-13 barcode
    ean = EAN13(number, writer=ImageWriter())

    # Save the barcode as an image
    ean.save(filename)
    print(f"Barcode saved as {filename}.png")

def validate_ean13(number):
    """
    Validates an EAN-13 barcode by calculating its checksum.
    :param number: 13-digit string for the barcode.
    :return: True if valid, False otherwise.
    """
    if len(number) != 13 or not number.isdigit():
        return False

    # Calculate checksum
    digits = list(map(int, number))
    checksum = sum(digits[i] if i % 2 == 0 else digits[i] * 3 for i in range(12))
    check_digit = (10 - (checksum % 10)) % 10

    return check_digit == digits[-1]

if __name__ == "__main__":
    try:
        # Example barcode number (12 digits for generation, 13 digits for validation)
        barcode_number = "123456789012"  # Must be 12 digits for generation
        validate_number = "1234567890128"  # Full 13 digits for validation

        # Generate an EAN-13 barcode
        generate_ean13_barcode(barcode_number, "ean13_barcode")

        # Validate the EAN-13 barcode
        is_valid = validate_ean13(validate_number)
        print(f"The barcode {validate_number} is {'valid' if is_valid else 'invalid'}.")
    except Exception as e:
        print(f"Error: {e}")

```

    Barcode saved as ean13_barcode.png
    The barcode 1234567890128 is valid.



```python

```


```python

            
```


```python

```


---
**Score: 5**
