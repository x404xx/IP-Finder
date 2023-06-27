<div align="center">

  # SubFinder <img src="https://github.com/x404xx/Sub-finder/assets/114883816/54d26b01-0480-48fa-b188-c12088108111" width="50">

**SubFinder** is a Rest-API that helps you quickly discover hidden gems with lightning-fast speed and precision.
</div>

## **Endpoint**

-   [https://subdomain-api.up.railway.app/search?](https://subdomain-api.up.railway.app/search?)

## **Parameter**

```
domain
```

## **Usage**

-   ### **_requests_**

```python
import requests

domain = 'maxis.com.my'

params = {'domain': domain}
url = 'https://subdomain-api.up.railway.app/search'
response = requests.get(url, params=params)

print(response.json())
```

-  ### **_curl_**

```
curl https://subdomain-api.up.railway.app/search?domain='YOUR_DOMAIN'
```

## **Output**
- For more details, you can find (**_subfinder.json_**) file in the repo

![Screenshot (20230627-095657)](https://github.com/x404xx/Sub-finder/assets/114883816/a98a8de5-ec69-4b4e-bcaa-1b0239699762)
