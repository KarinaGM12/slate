---
title: Facebook API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="facebook-api">Facebook API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is the entropy facebook api

Base URLs:

* <a href="https://pending.entropy.tech/v1">https://pending.entropy.tech/v1</a>

Email: <a href="mailto:karina@entropy.tech">Support</a> 

<h1 id="facebook-api-organizations">organizations</h1>

Entropy organizations resource

## post__organizations

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://pending.entropy.tech/v1/organizations HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "name": "Fake organization",
  "currency": "MXN",
  "domain": "http://fake.fake"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://pending.entropy.tech/v1/organizations', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations`

*Create organization*

> Body parameter

```json
{
  "name": "Fake organization",
  "currency": "MXN",
  "domain": "http://fake.fake"
}
```

<h3 id="post__organizations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» name|body|string|false|none|
|» currency|body|string|false|none|
|» domain|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "id": "00000000-0000-0000-000a-000a000000aa"
}
```

<h3 id="post__organizations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created organizationId|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="post__organizations-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## get__organizations

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations \
  -H 'Accept: application/json'

```

```http
GET https://pending.entropy.tech/v1/organizations HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://pending.entropy.tech/v1/organizations', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations`

*Get organizations for current user*

> Example responses

> 200 Response

```json
[
  {
    "id": "00000000-0000-0000-000a-000a000000aa",
    "name": "My fake organization"
  }
]
```

<h3 id="get__organizations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="get__organizations-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|
|» name|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## put__organizations_{organizationId}

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId} \
  -H 'Accept: application/json'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}',
{
  method: 'PUT',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}`

*Update organization name*

<h3 id="put__organizations_{organizationid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|

> Example responses

> 401 Response

```json
{
  "message": "string"
}
```

<h3 id="put__organizations_{organizationid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="put__organizations_{organizationid}-responseschema">Response Schema</h3>

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## get__organizations_{organizationId}

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId} \
  -H 'Accept: application/json'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}`

*Get organization by id*

<h3 id="get__organizations_{organizationid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|

> Example responses

> 200 Response

```json
{
  "id": "00000000-0000-0000-000a-000a000000aa",
  "name": "My fake organization"
}
```

<h3 id="get__organizations_{organizationid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|organization|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="get__organizations_{organizationid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|string|false|none|none|
|» name|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## get__organizations_{organizationId}_members

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/members \
  -H 'Accept: application/json'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/members HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/members',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/members',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/members',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/members', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/members");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/members", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/members`

*Get organization members*

<h3 id="get__organizations_{organizationid}_members-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|

> Example responses

> 200 Response

```json
[
  {
    "id": 1,
    "name": "Test User",
    "email": "fake@fake.com"
  }
]
```

<h3 id="get__organizations_{organizationid}_members-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="get__organizations_{organizationid}_members-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|none|
|» name|string|false|none|none|
|» email|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="facebook-api-credentials">credentials</h1>

Entropy Facebook credentials resource

## post__organizations_{organizationId}_credentials

> Code samples

```shell
# You can also use wget
curl -X POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://pending.entropy.tech/v1/organizations/{organizationId}/credentials HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "code": "string",
  "state": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /organizations/{organizationId}/credentials`

*Add a new credential to organization*

> Body parameter

```json
{
  "code": "string",
  "state": "string"
}
```

<h3 id="post__organizations_{organizationid}_credentials-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|body|body|object|true|none|
|» code|body|string|false|none|
|» state|body|string|false|none|

> Example responses

> 201 Response

```json
{
  "id": 1,
  "name": "Generic credential"
}
```

<h3 id="post__organizations_{organizationid}_credentials-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="post__organizations_{organizationid}_credentials-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## get__organizations_{organizationId}_credentials

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials \
  -H 'Accept: appplication/json'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials HTTP/1.1
Host: pending.entropy.tech
Accept: appplication/json

```

```javascript
var headers = {
  'Accept':'appplication/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'appplication/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'appplication/json'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'appplication/json'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"appplication/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/credentials`

*Get credentials by organization*

<h3 id="get__organizations_{organizationid}_credentials-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|

> Example responses

> 200 Response

> 401 Response

```json
{
  "message": "string"
}
```

<h3 id="get__organizations_{organizationid}_credentials-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|

<h3 id="get__organizations_{organizationid}_credentials-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## get__organizations_{organizationId}_credentials_{credentialId}

> Code samples

```shell
# You can also use wget
curl -X GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} \
  -H 'Accept: application/json'

```

```http
GET https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /organizations/{organizationId}/credentials/{credentialId}`

*Get credential by credential id*

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|credentialId|path|integer|true|none|

> Example responses

> 201 Response

```json
{
  "id": 1,
  "name": "Generic credential"
}
```

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="get__organizations_{organizationid}_credentials_{credentialid}-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## delete__organizations_{organizationId}_credentials_{credentialId}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} \
  -H 'Accept: application/json'

```

```http
DELETE https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} HTTP/1.1
Host: pending.entropy.tech
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /organizations/{organizationId}/credentials/{credentialId}`

*Delete credential by id*

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|credentialId|path|integer|true|none|

> Example responses

> 400 Response

```json
{
  "message": "string"
}
```

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="delete__organizations_{organizationid}_credentials_{credentialid}-responseschema">Response Schema</h3>

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## put__organizations_{organizationId}_credentials_{credentialId}

> Code samples

```shell
# You can also use wget
curl -X PUT https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId} HTTP/1.1
Host: pending.entropy.tech
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "code": "string",
  "state": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put 'https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://pending.entropy.tech/v1/organizations/{organizationId}/credentials/{credentialId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /organizations/{organizationId}/credentials/{credentialId}`

*Update organization credential*

> Body parameter

```json
{
  "code": "string",
  "state": "string"
}
```

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|The organization Id|
|credentialId|path|integer|true|none|
|body|body|object|true|none|
|» code|body|string|false|none|
|» state|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "id": 1,
  "name": "Generic credential"
}
```

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|Inline|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Unknown error|Inline|

<h3 id="put__organizations_{organizationid}_credentials_{credentialid}-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» id|integer|false|none|The credential ID.|
|» name|string|false|none|The credential name.|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

Status Code **500**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

