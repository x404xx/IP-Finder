<div align="center">

# IPFinder <img src="https://github.com/x404xx/Sub-finder/assets/114883816/54d26b01-0480-48fa-b188-c12088108111" width="25">

**IPFinder** is a Rest-API that helps you quickly discover the `REAL IP` of a website with lightning-fast speed and precision, especially for Cloudflare websites. It's the fastest on GitHub. 

</div>

> **Note**
> For the first request, it may take some time to respond due to spin down or inactivity. Remember not all the results are positive.

## Made With

-   [Quart](https://quart.palletsprojects.com/en/latest/index.html)

## Methods

-   CrimeFlare (Real IP) - **_True_** by default
-   ZoomEye (Real IP) - **_False_** by default
-   SubWhois (Subdomains) - **_False_** by default
-   DNS Dumpster (DNS Info) - **_False_** by default
-   Port Scanner (Scanning port on Real IP) - **_False_** by default

## Endpoint (Click this url first to check the server is UP or NOT)

-   [https://async-quart.onrender.com](https://async-quart.onrender.com)

## Parameter

```
domain_info
ip_info (Bonus)
```

## Required (as JSON data)

```python
'query_domain': 'TARGET DOMAIN'
```

## Modes

```python
'zoomeye': False
'subwhois': False
'dumpster': False
'port_scan': False
```

## Usage

-   ### Single Run (CrimeFlare)

```python
import requests

domain = 'streak.com'

url = 'https://async-quart.onrender.com/domain_info'
json_data = {'query_domain': domain}
response = requests.post(url, json=json_data)

print(response.text)
```

-   ### Custom Switch (CrimeFlare and ZoomEye)

```python
import requests

domain = 'streak.com'

url = 'https://async-quart.onrender.com/domain_info'
json_data = {
    'query_domain': domain,
    'zoomeye': True,
}
response = requests.post(url, json=json_data)

print(response.text)
```

-   ### All Modes (CrimeFlare, ZoomEye, SubWhois, DNSDumpster) + Port Scanner

```python
import requests

domain = 'streak.com'

url = 'https://async-quart.onrender.com/domain_info'
json_data = {
    'query_domain': domain,
    'zoomeye': True,
    'dumpster': True,
    'subwhois': True,
    'port_scan': True
}
response = requests.post(url, json=json_data)

print(response.text)
```

## IP Checker (Bonus)

> To check your current IP

```python
import requests

url = 'https://async-quart.onrender.com/ip_info'
response = requests.get(url)

print(response.text)
```

> To check with custom IP

```python
import requests

custom_ip = '37.19.205.147'
params = {'ip': custom_ip}

url = 'https://async-quart.onrender.com/ip_info'
response = requests.get(url, params=params)

print(response.text)
```

## JSON Output

-   Single run results ([singlerun](https://github.com/x404xx/IP-Finder/blob/main/singlerun.json))
-   Custom switch results ([customswitch](https://github.com/x404xx/IP-Finder/blob/main/customswitch.json))
-   All modes results ([allmodes](https://github.com/x404xx/IP-Finder/blob/main/allmodes.json))
-   Current IP results ([currentip](https://github.com/x404xx/IP-Finder/blob/main/currentip.json))
-   Custom IP results ([customip](https://github.com/x404xx/IP-Finder/blob/main/customip.json))

## Test Found IP

![Screenshot (20231025-032657)](https://github.com/x404xx/Sub-finder/assets/114883816/a0f64677-8279-4d91-8ebd-462f06a75136)

## Legal Disclaimer

> **Note**
> This was made for educational purposes only, nobody which directly involved in this project is responsible for any damages caused. **_You are responsible for your actions._**
