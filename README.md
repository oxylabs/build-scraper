# Build Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Build Scraper](https://oxylabs.io/products/scraper-api/ecommerce/build?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Build website effortlessly. This brief guide showcases how Build Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Build results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Build page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.build.com/bathroom/c108412'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/build-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n    <!doctype html>\n    <html>\n    <head>\r\n<script>(function(){ window.SS = window.SS || {}; SS.Req ... </html>",
      "created_at": "2024-02-20 12:38:30",
      "updated_at": "2024-02-20 12:38:40",
      "page": 1,
      "url": "https://www.build.com/bathroom/c108412",
      "job_id": "7165686150831547393",
      "status_code": 200
    }
  ]
}
```
With our Build Scraper, you can seamlessly harvest public data from any Build web page. Gather necessary project data, including blueprints, estimates, or specs, to have a profound understanding of the market and get a leg up on your competition. Should you have any inquiries, reach out to our support staff through live chat or shoot us an email at hello@oxylabs.io.