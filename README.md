# 🌍 Country & Language JSON Data

This repository contains two JSON files:

- **`country.json`** – ISO country codes mapped to names + flags  
  📄 [View file](https://raw.githubusercontent.com/US-USA/language/refs/heads/master/country.json)

- **`lang.json`** – ISO 639-1 language codes mapped to names  
  📄 [View file](https://raw.githubusercontent.com/US-USA/language/refs/heads/master/lang.json)

---


### python

```python
import requests

# Load country data
country_url = "https://raw.githubusercontent.com/US-USA/language/refs/heads/master/country.json"
country_data = requests.get(country_url).json()
print("Country [US]:", country_data.get("US", "Not found"))

# Load language data
lang_url = "https://raw.githubusercontent.com/US-USA/language/refs/heads/master/lang.json"
lang_data = requests.get(lang_url).json()
print("Language [en]:", lang_data.get("en", "Not found"))
