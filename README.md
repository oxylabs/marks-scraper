# Marks Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Marks Scraper](https://oxylabs.io/products/scraper-api/ecommerce/marks?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Marks website effortlessly. This brief guide showcases how Marks Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Marks results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Marks page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.marksandspencer.com/l/women/all-new-in#intid=ww_dlp_logo-nav_08022024_txt_1_new_in'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/marks-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-GB\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width= ... </html>",
      "created_at": "2024-02-20 12:45:17",
      "updated_at": "2024-02-20 12:45:19",
      "page": 1,
      "url": "https://www.marksandspencer.com/l/women/all-new-in#intid=ww_dlp_logo-nav_08022024_txt_1_new_in",
      "job_id": "7165687858743778305",
      "status_code": 200
    }
  ]
}
```
With our Marks Scraper, you can seamlessly gather personalized data from any Marks web page. Accumulate necessary information, such as personal records, academic degrees, or work experience, to fortify your knowledge base and stay ahead in your field of study or work. If you face any troubles or need guidance, our support team is readily available through live chat or feel free to email us at hello@oxylabs.io.