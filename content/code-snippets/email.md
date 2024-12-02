---
title: Email
date: 2024-12-02
author: Your Name
cell_count: 6
score: 5
---

```python
import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText


```


```python
# Sender and receiver email addresses
sender_email = 'your_email@gmail.com'
receiver_email = 'receiver_email@example.com'
password = 'your_email_password'
```


```python
# Create the MIME message
message = MIMEMultipart()
message['From'] = sender_email
message['To'] = receiver_email
message['Subject'] = 'Test Email from Python'
```


```python
# Body of the email
body = 'Hello, this is a test email sent from Python using smtplib!'
message.attach(MIMEText(body, 'plain'))
```


```python
# Connect to the Gmail SMTP server
try:
    with smtplib.SMTP('smtp.gmail.com', 587) as server:
        server.starttls()  # Start TLS encryption
        server.login(sender_email, password)  # Login to the server
        
        # Send the email
        text = message.as_string()
        server.sendmail(sender_email, receiver_email, text)
        
        print("Email sent successfully!")
except Exception as e:
    print(f"Error: {e}")

```

    Error: (535, b'5.7.8 Username and Password not accepted. For more information, go to\n5.7.8  https://support.google.com/mail/?p=BadCredentials 6a1803df08f44-6d451a83a97sm12404156d6.7 - gsmtp')



```python

```


---
**Score: 5**
