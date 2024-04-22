# Woocommerce Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Woocommerce Scraper](https://oxylabs.io/products/scraper-api/ecommerce/woocommerce?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Woocommerce website effortlessly. This brief guide showcases how Woocommerce Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Woocommerce results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Woocommerce page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://augustapparel.com/product-category/mto/mens/mens-boots/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/woocommerce-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en-US\" dir=\"ltr\">\n<head>\n\t<meta charset=\"UTF-8\">\n\t<meta name=\"viewport\"  ... </html>",
      "created_at": "2024-01-10 09:36:05",
      "updated_at": "2024-01-10 09:36:08",
      "page": 1,
      "url": "https://augustapparel.com/product-category/mto/mens/mens-boots/",
      "job_id": "7150782343123360769",
      "status_code": 200
    }
  ]
}
```
With our Woocommerce Scraper, you can effortlessly extract key business data from any Woocommerce web page. Gather crucial product specifics, including price, customer feedback, as well as detailed product descriptions to gain a complete understanding of the market and outperform your competitors. If further assistance is required, connect with our readily available support team via live chat or send us a note at hello@oxylabs.io.
