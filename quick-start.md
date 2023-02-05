---
label: Quick Start
order: 99999
---


# Quick Start

## Determine your Chocolate Server IP and Port

The combination of the Chocolate Server IP and Port are essential

To get the combination, simply start the server, wait it to load, and look at the line who start with

```
*  Running on: http://ip:port
```

## Interact with Chocolate

There's no best way to interact with Chocolate, all programming language can do it!

+++ JS (Axios)
```javascript
axios.get("http://ip:port")
  .then(response => console.log(response.data))
  .catch(error => console.error(error));
```
+++ JS (fetch)
```javascript
fetch('http://ip:port')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```
+++ Python
```python
import requests

response = requests.get("http://ip:port")

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print("Request failed")
```
+++ C#
```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static async Task Main(string[] args)
    {
        var client = new HttpClient();
        var response = await client.GetAsync("http://ip:port");

        if (response.IsSuccessStatusCode)
        {
            var data = await response.Content.ReadAsStringAsync();
            Console.WriteLine(data);
        }
        else
        {
            Console.WriteLine("Request failed");
        }
    }
}
```
+++ Ruby
```ruby
require 'net/http'
require 'json'

url = URI("http://ip:port")

response = Net::HTTP.get(url)

if response.code == "200"
    data = JSON.parse(response)
    puts data
else
    puts "Request failed"
end
```
+++ Kotlin
```kotlin
import com.github.kittinunf.fuel.Fuel
import com.github.kittinunf.fuel.core.FuelManager
import com.github.kittinunf.fuel.core.Response
import com.github.kittinunf.result.Result

fun main() {
    FuelManager.instance.basePath = "http://ip:port"
    Fuel.get("").responseString { _, response, result ->
        when (result) {
            is Result.Success -> {
                val data = response.data
                println(data)
            }
            is Result.Failure -> {
                println("Request failed")
            }
        }
    }
}
```
+++ Java
```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.HttpURLConnection;
import java.net.URL;

public class Main {
    public static void main(String[] args) {
        try {
            URL url = new URL("http://ip:port");
            HttpURLConnection con = (HttpURLConnection) url.openConnection();
            con.setRequestMethod("GET");
            int responseCode = con.getResponseCode();
            if (responseCode == HttpURLConnection.HTTP_OK) {
                BufferedReader in = new BufferedReader(new InputStreamReader(con.getInputStream()));
                String inputLine;
                StringBuilder response = new StringBuilder();
                while ((inputLine = in.readLine()) != null) {
                    response.append(inputLine);
                }
                in.close();
                System.out.println(response.toString());
            } else {
                System.out.println("Request failed");
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```
+++


## Make your first request

To make your first request, send a request to /login, to authenticate

==- [!badge text="POST" variant="success"] http://ip:port/login
# Login
Login to an existing account.

All parameters need to be in a form-data.

## Parameters

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | The account username | true |
| password | string | The account password | true |

## Responses

| Status | Description |
| ------ | ----------- |
| 200: OK | Logged in |
| 400: Bad Request | Wrong username or password |

## Example

Take a look at how you might call this method using your favorite languages:

+++ JS (axios)
```javascript
const data = {
  name: name,
  password: password
};

axios.post('http://ip:port/login', data)
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error(error);
  });
```
+++ JS (fetch)
```javascript
const formData = new FormData();
formData.append('name', name);
formData.append('password', password);

fetch('http://ip:port/login', {
  method: 'POST',
  body: formData
})
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error(error));
```
+++ Python
```python
import requests

data = {
  'name': name,
  'password': password
}

response = requests.post('http://ip:port/login', data=data)

if response.status_code == 200:
  print(response.json())
else:
  print('Error: ' + str(response.status_code))
```
+++

===