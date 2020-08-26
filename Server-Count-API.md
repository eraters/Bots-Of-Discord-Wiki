# Getting your Authorization Token

To start using server counts on a bot, go to your bot edit page, and click the `Authorization Token` link at the bottom of the page. This will generate an auth token.

# Posting Stats

NodeJS
```js
var myHeaders = new Headers();
myHeaders.append("authorization", "YOUR_AUTH_TOKEN");
myHeaders.append("Content-Type", "application/json");

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: JSON.stringify({"server_count": 1500}); // Replace this number with the server count
};

fetch("/api/auth/stats/:botid", requestOptions) // Make sure you include the domain
  .then(response => response.text())
  .then(console.log)
  .catch(console.error);
```
Python
```py
url = "/api/auth/stats/:botid" # Make sure you include the domain

payload = "{\"server_count\": 1500}" # Replace this number with the server count
headers = {
  'authorization': 'YOUR_AUTH_TOKEN',
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data = payload)
print(response.text.encode('utf8'))
```