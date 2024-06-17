# Lego on Sale


## Overview

This project is a simple web scraping and notification system designed to monitor the price of a specific LEGO set and send an email alert if the price drops below a specified threshold. The system is implemented in Python and utilizes several libraries to accomplish its tasks.

## Components

### 1. Web Scraping

The script uses the `requests` library to send an HTTP GET request to the LEGO product page and fetch its HTML content. The `BeautifulSoup` library is then used to parse the HTML and extract the price of the LEGO set. The price is retrieved from an HTML element identified by a specific attribute (`data-test="product-price"`).

### 2. Email Notification

If the price of the LEGO set is found to be below $200, an email notification is sent. The script uses the `smtplib` library to send an email via the SMTP server of the user's email provider. The email content is created using the `email.mime.text.MIMEText` class. The email includes a subject and a body, informing the recipient about the current price of the LEGO set and asking if they want to purchase it.

### 3. Automation

The script is designed to run in an infinite loop, checking the price of the LEGO set once every 24 hours (86400 seconds). This ensures that the user is kept up-to-date with the latest price information.

