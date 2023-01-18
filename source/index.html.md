---
title: jungle-nft-marketplace v1.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="jungle-nft-marketplace">jungle-nft-marketplace v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

jungle nft marketplace various functions

Base URLs:

# Authentication

- HTTP Authentication, scheme: bearer 

- oAuth2 authentication. 

<h1 id="jungle-nft-marketplace-default">Default</h1>

## ReportController_findAllReportedCollections

<a id="opIdReportController_findAllReportedCollections"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/report/allReportedCollections \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/report/allReportedCollections HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/report/allReportedCollections',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/report/allReportedCollections',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/report/allReportedCollections', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/report/allReportedCollections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/report/allReportedCollections");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/report/allReportedCollections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/report/allReportedCollections`

*Find All Reported collections*

<h3 id="reportcontroller_findallreportedcollections-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|time|query|string|false|none|
|reason|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|alltime|
|time|1|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|
|reason|Spam|
|reason|Explicit and sensitive content|
|reason|Fake collection or possible scam|
|reason|Might be stolen|
|reason|Other|

<h3 id="reportcontroller_findallreportedcollections-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Reported Collections|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ReportController_findAllReportedItems

<a id="opIdReportController_findAllReportedItems"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/report/allReportedItems \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/report/allReportedItems HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/report/allReportedItems',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/report/allReportedItems',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/report/allReportedItems', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/report/allReportedItems', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/report/allReportedItems");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/report/allReportedItems", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/report/allReportedItems`

*Find All Reported Items*

<h3 id="reportcontroller_findallreporteditems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|time|query|string|false|none|
|reason|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|alltime|
|time|1|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|
|reason|Spam|
|reason|Explicit and sensitive content|
|reason|Fake collection or possible scam|
|reason|Might be stolen|
|reason|Other|

<h3 id="reportcontroller_findallreporteditems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Reported Items|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ReportController_findAllReportedUsers

<a id="opIdReportController_findAllReportedUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/report/allReportedUsers \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/report/allReportedUsers HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/report/allReportedUsers',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/report/allReportedUsers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/report/allReportedUsers', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/report/allReportedUsers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/report/allReportedUsers");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/report/allReportedUsers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/report/allReportedUsers`

*Find All Reported Users*

<h3 id="reportcontroller_findallreportedusers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Reported Users|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-dashboard">Dashboard</h1>

## AppController_healthCheck

<a id="opIdAppController_healthCheck"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1

```

```http
GET /api/v1 HTTP/1.1

```

```javascript

fetch('/api/v1',
{
  method: 'GET'

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

result = RestClient.get '/api/v1',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1`

<h3 id="appcontroller_healthcheck-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|checks health of app|None|

<aside class="success">
This operation does not require authentication
</aside>

## AppController_csrfCheck

<a id="opIdAppController_csrfCheck"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/jungle_check

```

```http
POST /api/v1/jungle_check HTTP/1.1

```

```javascript

fetch('/api/v1/jungle_check',
{
  method: 'POST'

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

result = RestClient.post '/api/v1/jungle_check',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.post('/api/v1/jungle_check')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/jungle_check', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/jungle_check");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/jungle_check", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/jungle_check`

<h3 id="appcontroller_csrfcheck-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## AppController_testAuth0

<a id="opIdAppController_testAuth0"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/testAuth0 \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/testAuth0 HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/testAuth0',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/testAuth0',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/testAuth0', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/testAuth0', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/testAuth0");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/testAuth0", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/testAuth0`

<h3 id="appcontroller_testauth0-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AppController_testAuth1

<a id="opIdAppController_testAuth1"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/testAuth0Open

```

```http
GET /api/v1/testAuth0Open HTTP/1.1

```

```javascript

fetch('/api/v1/testAuth0Open',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/testAuth0Open',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/testAuth0Open')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/testAuth0Open', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/testAuth0Open");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/testAuth0Open", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/testAuth0Open`

<h3 id="appcontroller_testauth1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-user-module">User Module</h1>

## UserController_createUser

<a id="opIdUserController_createUser"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/user \
  -H 'Content-Type: application/json'

```

```http
POST /api/v1/user HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "walletAddress": "string",
  "signature": "string",
  "signature_message": "string",
  "loginWallet": "string",
  "referralSource": "string"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('/api/v1/user',
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
  'Content-Type' => 'application/json'
}

result = RestClient.post '/api/v1/user',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('/api/v1/user', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/user', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/user", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/user`

*Login User with given Wallet Address or Create new Account with given Wallet Address*

> Body parameter

```json
{
  "walletAddress": "string",
  "signature": "string",
  "signature_message": "string",
  "loginWallet": "string",
  "referralSource": "string"
}
```

<h3 id="usercontroller_createuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateUserLoginDto](#schemacreateuserlogindto)|true|none|

<h3 id="usercontroller_createuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User has been Logged In|None|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|User has been created|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_updateUser

<a id="opIdUserController_updateUser"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/user \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/user HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "firstName": "string",
  "lastName": "string",
  "userName": "string",
  "email": "string",
  "imageUrl": "string",
  "bannerUrl": "string",
  "bio": "string",
  "twitterHandle": "string",
  "instagramHandle": "string",
  "website": "string",
  "instagramToken": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/user',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/user', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/user', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/user", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/user`

*Update User Details who is currenlty Logged In*

> Body parameter

```json
{
  "firstName": "string",
  "lastName": "string",
  "userName": "string",
  "email": "string",
  "imageUrl": "string",
  "bannerUrl": "string",
  "bio": "string",
  "twitterHandle": "string",
  "instagramHandle": "string",
  "website": "string",
  "instagramToken": "string"
}
```

<h3 id="usercontroller_updateuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateUserDto](#schemaupdateuserdto)|true|none|

<h3 id="usercontroller_updateuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User with given wallet Address doesn't exists|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|User with given email address already exists|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_logOut

<a id="opIdUserController_logOut"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/user/logout \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/user/logout HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/logout',
{
  method: 'POST',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/user/logout',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/user/logout', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/user/logout', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/logout");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/user/logout", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/user/logout`

<h3 id="usercontroller_logout-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getUserDetailsByUserName

<a id="opIdUserController_getUserDetailsByUserName"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/userdetails/username/{userName} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/userdetails/username/{userName} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/userdetails/username/{userName}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/userdetails/username/{userName}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/userdetails/username/{userName}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/userdetails/username/{userName}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/userdetails/username/{userName}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/userdetails/username/{userName}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/userdetails/username/{userName}`

*Get User Details with given User Name*

<h3 id="usercontroller_getuserdetailsbyusername-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userName|path|string|true|none|

<h3 id="usercontroller_getuserdetailsbyusername-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User with given username doesn't exists|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getUserDetailsByWalletAddress

<a id="opIdUserController_getUserDetailsByWalletAddress"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/userdetails/walletaddress/{walletAddress} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/userdetails/walletaddress/{walletAddress} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/userdetails/walletaddress/{walletAddress}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/userdetails/walletaddress/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/userdetails/walletaddress/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/userdetails/walletaddress/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/userdetails/walletaddress/{walletAddress}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/userdetails/walletaddress/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/userdetails/walletaddress/{walletAddress}`

*Get User Details with given Wallet Address*

<h3 id="usercontroller_getuserdetailsbywalletaddress-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_getuserdetailsbywalletaddress-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User with given wallet Address doesn't exists|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getPresignedURL

<a id="opIdUserController_getPresignedURL"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/user/getPresignedURL \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/user/getPresignedURL HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileName": "string",
  "fileType": "string",
  "filePath": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getPresignedURL',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/user/getPresignedURL',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/user/getPresignedURL', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/user/getPresignedURL', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getPresignedURL");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/user/getPresignedURL", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/user/getPresignedURL`

*Get pre-signed url with given filename and filetype*

> Body parameter

```json
{
  "fileName": "string",
  "fileType": "string",
  "filePath": "string"
}
```

<h3 id="usercontroller_getpresignedurl-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SignedUrlDto](#schemasignedurldto)|true|none|

<h3 id="usercontroller_getpresignedurl-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Pre-Signed Url|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getAllCategories

<a id="opIdUserController_getAllCategories"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getAllCategories

```

```http
GET /api/v1/user/getAllCategories HTTP/1.1

```

```javascript

fetch('/api/v1/user/getAllCategories',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/getAllCategories',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/getAllCategories')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getAllCategories', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getAllCategories");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getAllCategories", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getAllCategories`

*Api request to fetch all categories*

<h3 id="usercontroller_getallcategories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|Array of all categories|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_updateOneTimeFees

<a id="opIdUserController_updateOneTimeFees"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/user/feesPaid \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/user/feesPaid HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isOneTimeFees": true,
  "oneTimeFees": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/feesPaid',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/user/feesPaid',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/user/feesPaid', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/user/feesPaid', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/feesPaid");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/user/feesPaid", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/user/feesPaid`

*Api request to update feespaid *

> Body parameter

```json
{
  "isOneTimeFees": true,
  "oneTimeFees": "string"
}
```

<h3 id="usercontroller_updateonetimefees-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FeesPaidDto](#schemafeespaiddto)|true|none|

<h3 id="usercontroller_updateonetimefees-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|object with success response|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_profileCountStats

<a id="opIdUserController_profileCountStats"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getProfileCountStats/{walletAddress}

```

```http
GET /api/v1/user/getProfileCountStats/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/user/getProfileCountStats/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/getProfileCountStats/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/getProfileCountStats/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getProfileCountStats/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getProfileCountStats/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getProfileCountStats/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getProfileCountStats/{walletAddress}`

*Returns count of diff fields for user profile*

<h3 id="usercontroller_profilecountstats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_profilecountstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Items Favourite Count|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_creatsubscribeNewslettereUser

<a id="opIdUserController_creatsubscribeNewslettereUser"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/user/subscribeNewsletter \
  -H 'Content-Type: application/json'

```

```http
POST /api/v1/user/subscribeNewsletter HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "userEmail": "abc@gmail.com"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('/api/v1/user/subscribeNewsletter',
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
  'Content-Type' => 'application/json'
}

result = RestClient.post '/api/v1/user/subscribeNewsletter',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('/api/v1/user/subscribeNewsletter', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/user/subscribeNewsletter', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/subscribeNewsletter");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/user/subscribeNewsletter", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/user/subscribeNewsletter`

*subscribe to newsletter and add to sendgrid*

> Body parameter

```json
{
  "userEmail": "abc@gmail.com"
}
```

<h3 id="usercontroller_creatsubscribenewslettereuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SubscribeNewsletterDto](#schemasubscribenewsletterdto)|true|none|

<h3 id="usercontroller_creatsubscribenewslettereuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|User has been created|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_getallUsersSubscribedForNewsletter

<a id="opIdUserController_getallUsersSubscribedForNewsletter"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getAllSubscribedForNewsletter

```

```http
GET /api/v1/user/getAllSubscribedForNewsletter HTTP/1.1

```

```javascript

fetch('/api/v1/user/getAllSubscribedForNewsletter',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/getAllSubscribedForNewsletter',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/getAllSubscribedForNewsletter')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getAllSubscribedForNewsletter', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getAllSubscribedForNewsletter");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getAllSubscribedForNewsletter", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getAllSubscribedForNewsletter`

*get all newsletter users*

<h3 id="usercontroller_getalluserssubscribedfornewsletter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_setNftAsProfilePic

<a id="opIdUserController_setNftAsProfilePic"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/user/setNftAsProfilePic?nftItemId=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/user/setNftAsProfilePic?nftItemId=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/setNftAsProfilePic?nftItemId=string',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/user/setNftAsProfilePic',
  params: {
  'nftItemId' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/user/setNftAsProfilePic', params={
  'nftItemId': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/user/setNftAsProfilePic', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/setNftAsProfilePic?nftItemId=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/user/setNftAsProfilePic", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/user/setNftAsProfilePic`

*Set an nft item as users profile picture*

<h3 id="usercontroller_setnftasprofilepic-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|nftItemId|query|string|true|nft item id|

<h3 id="usercontroller_setnftasprofilepic-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|User with given wallet Address doesn't exists|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_instagram

<a id="opIdUserController_instagram"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/instagram/{code}

```

```http
GET /api/v1/user/instagram/{code} HTTP/1.1

```

```javascript

fetch('/api/v1/user/instagram/{code}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/instagram/{code}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/instagram/{code}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/instagram/{code}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/instagram/{code}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/instagram/{code}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/instagram/{code}`

*Get instagram userId and token*

<h3 id="usercontroller_instagram-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|path|string|true|none|

<h3 id="usercontroller_instagram-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Instagram_UserId_And_Token|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_resendEmailForVerification

<a id="opIdUserController_resendEmailForVerification"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/resendEmailForVerification \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/resendEmailForVerification HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/resendEmailForVerification',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/resendEmailForVerification',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/resendEmailForVerification', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/resendEmailForVerification', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/resendEmailForVerification");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/resendEmailForVerification", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/resendEmailForVerification`

*Resend an Email for Verification*

<h3 id="usercontroller_resendemailforverification-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_verifyEmail

<a id="opIdUserController_verifyEmail"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/verifyEmail/{accessToken} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/verifyEmail/{accessToken} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/verifyEmail/{accessToken}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/verifyEmail/{accessToken}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/verifyEmail/{accessToken}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/verifyEmail/{accessToken}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/verifyEmail/{accessToken}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/verifyEmail/{accessToken}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/verifyEmail/{accessToken}`

*Verify the Email*

<h3 id="usercontroller_verifyemail-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|accessToken|path|string|true|none|

<h3 id="usercontroller_verifyemail-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Email has been Verified|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Email cannot be verified|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_uniqueUser

<a id="opIdUserController_uniqueUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/uniqueUser \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/uniqueUser HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/uniqueUser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/uniqueUser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/uniqueUser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/uniqueUser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/uniqueUser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/uniqueUser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/uniqueUser`

*To fetch if username or email already exist*

<h3 id="usercontroller_uniqueuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userName|query|string|false|none|
|email|query|string|false|none|

<h3 id="usercontroller_uniqueuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_checkIsUserBlocked

<a id="opIdUserController_checkIsUserBlocked"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/checkisuserblocked/{walletAddress}

```

```http
GET /api/v1/user/checkisuserblocked/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/user/checkisuserblocked/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/checkisuserblocked/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/checkisuserblocked/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/checkisuserblocked/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/checkisuserblocked/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/checkisuserblocked/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/checkisuserblocked/{walletAddress}`

*To check is User Blocked*

<h3 id="usercontroller_checkisuserblocked-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_checkisuserblocked-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_getCashbacksForUser

<a id="opIdUserController_getCashbacksForUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getcashbackforuser \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/getcashbackforuser HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getcashbackforuser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/getcashbackforuser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/getcashbackforuser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getcashbackforuser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getcashbackforuser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getcashbackforuser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getcashbackforuser`

*To get cashback for user*

<h3 id="usercontroller_getcashbacksforuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getCashbacksAmountForUser

<a id="opIdUserController_getCashbacksAmountForUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getcashbackamountforuser \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/getcashbackamountforuser HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getcashbackamountforuser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/getcashbackamountforuser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/getcashbackamountforuser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getcashbackamountforuser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getcashbackamountforuser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getcashbackamountforuser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getcashbackamountforuser`

*To get cashback amount for user*

<h3 id="usercontroller_getcashbacksamountforuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getUserWalletBalance

<a id="opIdUserController_getUserWalletBalance"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getuserwalletbalance \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/getuserwalletbalance HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getuserwalletbalance',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/getuserwalletbalance',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/getuserwalletbalance', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getuserwalletbalance', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getuserwalletbalance");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getuserwalletbalance", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getuserwalletbalance`

*To get user wallet balance*

<h3 id="usercontroller_getuserwalletbalance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getUserDetailsByMultipleWalletAddress

<a id="opIdUserController_getUserDetailsByMultipleWalletAddress"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/user/userdetails \
  -H 'Content-Type: application/json'

```

```http
PUT /api/v1/user/userdetails HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "walletAddress": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('/api/v1/user/userdetails',
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
  'Content-Type' => 'application/json'
}

result = RestClient.put '/api/v1/user/userdetails',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('/api/v1/user/userdetails', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/user/userdetails', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/userdetails");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/user/userdetails", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/user/userdetails`

*To get user details of all the users with given wallet Address*

> Body parameter

```json
{
  "walletAddress": [
    "string"
  ]
}
```

<h3 id="usercontroller_getuserdetailsbymultiplewalletaddress-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UsersWalletAddressDto](#schemauserswalletaddressdto)|true|none|

<h3 id="usercontroller_getuserdetailsbymultiplewalletaddress-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_fetchingNftOfWalletAddressFromMoralis

<a id="opIdUserController_fetchingNftOfWalletAddressFromMoralis"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/syncProfileNFT \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/syncProfileNFT HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/syncProfileNFT',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/syncProfileNFT',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/syncProfileNFT', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/syncProfileNFT', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/syncProfileNFT");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/syncProfileNFT", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/syncProfileNFT`

*api to sync nfts of given wallet address*

<h3 id="usercontroller_fetchingnftofwalletaddressfrommoralis-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getAllFollowers

<a id="opIdUserController_getAllFollowers"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getAllFollowers/{walletAddress} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/getAllFollowers/{walletAddress} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getAllFollowers/{walletAddress}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/getAllFollowers/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/getAllFollowers/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getAllFollowers/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getAllFollowers/{walletAddress}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getAllFollowers/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getAllFollowers/{walletAddress}`

*To get all followers*

<h3 id="usercontroller_getallfollowers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_getallfollowers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getAllFollowings

<a id="opIdUserController_getAllFollowings"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getAllFollowings/{walletAddress} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/getAllFollowings/{walletAddress} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/getAllFollowings/{walletAddress}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/getAllFollowings/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/getAllFollowings/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getAllFollowings/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getAllFollowings/{walletAddress}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getAllFollowings/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getAllFollowings/{walletAddress}`

*To get all followings*

<h3 id="usercontroller_getallfollowings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_getallfollowings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_follow

<a id="opIdUserController_follow"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/user/followUnfollow \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/user/followUnfollow HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "toFollow": "string",
  "status": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/followUnfollow',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/user/followUnfollow',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/user/followUnfollow', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/user/followUnfollow', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/followUnfollow");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/user/followUnfollow", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/user/followUnfollow`

*Follow and Unfollow User*

> Body parameter

```json
{
  "toFollow": "string",
  "status": true
}
```

<h3 id="usercontroller_follow-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FollowUser](#schemafollowuser)|true|none|

<h3 id="usercontroller_follow-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_countFollowerFollowed

<a id="opIdUserController_countFollowerFollowed"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/countFollowerFollowed/{walletAddress}

```

```http
GET /api/v1/user/countFollowerFollowed/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/user/countFollowerFollowed/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/countFollowerFollowed/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/countFollowerFollowed/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/countFollowerFollowed/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/countFollowerFollowed/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/countFollowerFollowed/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/countFollowerFollowed/{walletAddress}`

*Get count of followers and followed*

<h3 id="usercontroller_countfollowerfollowed-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_countfollowerfollowed-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_followersSearch

<a id="opIdUserController_followersSearch"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/followersSearch?walletAddress=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/followersSearch?walletAddress=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/followersSearch?walletAddress=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/followersSearch',
  params: {
  'walletAddress' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/followersSearch', params={
  'walletAddress': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/followersSearch', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/followersSearch?walletAddress=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/followersSearch", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/followersSearch`

*To search followers*

<h3 id="usercontroller_followerssearch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|none|
|walletAddress|query|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="usercontroller_followerssearch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_checkFollowUnFollow

<a id="opIdUserController_checkFollowUnFollow"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/checkFollowUnFollow?walletAddress=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/checkFollowUnFollow?walletAddress=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/checkFollowUnFollow?walletAddress=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/checkFollowUnFollow',
  params: {
  'walletAddress' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/checkFollowUnFollow', params={
  'walletAddress': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/checkFollowUnFollow', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/checkFollowUnFollow?walletAddress=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/checkFollowUnFollow", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/checkFollowUnFollow`

*To check Follower*

<h3 id="usercontroller_checkfollowunfollow-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|query|string|true|none|

<h3 id="usercontroller_checkfollowunfollow-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_followingsSearch

<a id="opIdUserController_followingsSearch"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/followingsSearch?walletAddress=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/followingsSearch?walletAddress=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/followingsSearch?walletAddress=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/followingsSearch',
  params: {
  'walletAddress' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/followingsSearch', params={
  'walletAddress': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/followingsSearch', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/followingsSearch?walletAddress=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/followingsSearch", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/followingsSearch`

*To search followings*

<h3 id="usercontroller_followingssearch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|search|query|string|false|none|
|walletAddress|query|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="usercontroller_followingssearch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_creators

<a id="opIdUserController_creators"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/creators

```

```http
GET /api/v1/user/creators HTTP/1.1

```

```javascript

fetch('/api/v1/user/creators',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/creators',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/creators')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/creators', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/creators");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/creators", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/creators`

*Creators*

<h3 id="usercontroller_creators-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|filterPage|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|filterPage|all|
|filterPage|top|
|filterPage|trending|

<h3 id="usercontroller_creators-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_favourites

<a id="opIdUserController_favourites"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/user/addOrRemoveFavourites \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/user/addOrRemoveFavourites HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isFavourite": true,
  "creatorWalletAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/addOrRemoveFavourites',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/user/addOrRemoveFavourites',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/user/addOrRemoveFavourites', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/user/addOrRemoveFavourites', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/addOrRemoveFavourites");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/user/addOrRemoveFavourites", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/user/addOrRemoveFavourites`

*Add and Removes user wallet address from favourites of a creator*

> Body parameter

```json
{
  "isFavourite": true,
  "creatorWalletAddress": "string"
}
```

<h3 id="usercontroller_favourites-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreatorFavouritesDto](#schemacreatorfavouritesdto)|true|none|

<h3 id="usercontroller_favourites-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User has been added in Favourites|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_getCreatorForUserFavourites

<a id="opIdUserController_getCreatorForUserFavourites"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getFavouriteCreator/{walletAddress}?walletAddress=string

```

```http
GET /api/v1/user/getFavouriteCreator/{walletAddress}?walletAddress=string HTTP/1.1

```

```javascript

fetch('/api/v1/user/getFavouriteCreator/{walletAddress}?walletAddress=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/getFavouriteCreator/{walletAddress}',
  params: {
  'walletAddress' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/getFavouriteCreator/{walletAddress}', params={
  'walletAddress': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getFavouriteCreator/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getFavouriteCreator/{walletAddress}?walletAddress=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getFavouriteCreator/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getFavouriteCreator/{walletAddress}`

*Returns Current User favourite creators*

<h3 id="usercontroller_getcreatorforuserfavourites-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|query|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="usercontroller_getcreatorforuserfavourites-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Creators|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## UserController_getCreatorFavouritesCount

<a id="opIdUserController_getCreatorFavouritesCount"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}

```

```http
GET /api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/getCreatorFavouritesCount/{creatorWalletAddress}`

*Returns Number of Favourites for a creator*

<h3 id="usercontroller_getcreatorfavouritescount-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|creatorWalletAddress|path|string|true|none|

<h3 id="usercontroller_getcreatorfavouritescount-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Creator Favourite Count|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-admin">admin</h1>

## UserController_BlockUser

<a id="opIdUserController_BlockUser"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/user/blockUser \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/user/blockUser HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "walletAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/blockUser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/user/blockUser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/user/blockUser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/user/blockUser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/blockUser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/user/blockUser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/user/blockUser`

> Body parameter

```json
{
  "walletAddress": "string"
}
```

<h3 id="usercontroller_blockuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[BlockUserDto](#schemablockuserdto)|true|none|

<h3 id="usercontroller_blockuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## UserController_ViewUserProfileByAdmin

<a id="opIdUserController_ViewUserProfileByAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/user/viewUserProfilebyAdmin/{walletAddress} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/user/viewUserProfilebyAdmin/{walletAddress} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/user/viewUserProfilebyAdmin/{walletAddress}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/user/viewUserProfilebyAdmin/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/user/viewUserProfilebyAdmin/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/user/viewUserProfilebyAdmin/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/user/viewUserProfilebyAdmin/{walletAddress}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/user/viewUserProfilebyAdmin/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/user/viewUserProfilebyAdmin/{walletAddress}`

<h3 id="usercontroller_viewuserprofilebyadmin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="usercontroller_viewuserprofilebyadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_login

<a id="opIdAdminController_login"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/login \
  -H 'Content-Type: application/json'

```

```http
POST /api/v1/admin/login HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "username": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('/api/v1/admin/login',
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
  'Content-Type' => 'application/json'
}

result = RestClient.post '/api/v1/admin/login',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('/api/v1/admin/login', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/login', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/login");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/login`

*Admin api for login*

> Body parameter

```json
{
  "username": "string",
  "password": "string"
}
```

<h3 id="admincontroller_login-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LoginAdminDto](#schemaloginadmindto)|true|none|

<h3 id="admincontroller_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|login as admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Invalid credentials|None|

<aside class="success">
This operation does not require authentication
</aside>

## AdminController_create

<a id="opIdAdminController_create"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin`

*Api to create an Admin*

> Body parameter

```json
{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}
```

<h3 id="admincontroller_create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateAdminDto](#schemacreateadmindto)|true|none|

<h3 id="admincontroller_create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|creates the account and returns created admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Email already exists|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_findAll

<a id="opIdAdminController_findAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin`

*Api request to fetch all Admins*

<h3 id="admincontroller_findall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|get all Admins|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_update

<a id="opIdAdminController_update"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/updateAdmin/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/updateAdmin/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/updateAdmin/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/updateAdmin/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/updateAdmin/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/updateAdmin/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/updateAdmin/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/updateAdmin/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/updateAdmin/{id}`

*Update Admin by id*

> Body parameter

```json
{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}
```

<h3 id="admincontroller_update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateAdminDto](#schemaupdateadmindto)|true|none|

<h3 id="admincontroller_update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update Admin Data|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getAdminProfile

<a id="opIdAdminController_getAdminProfile"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/me \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/me HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/me',
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
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/me',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/me', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/me', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/me");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/me", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/me`

*Admin api to fetch details.*

> Example responses

> 200 Response

```json
{
  "id": "string",
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string",
  "active": true,
  "createdAt": "2019-08-24T14:15:22Z",
  "updatedAt": "2019-08-24T14:15:22Z"
}
```

<h3 id="admincontroller_getadminprofile-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get data about current logged in admin|[Admin](#schemaadmin)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_createCategory

<a id="opIdAdminController_createCategory"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/createCategory \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/createCategory HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "categoryName": "string",
  "categoryImageUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/createCategory',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/createCategory',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/createCategory', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/createCategory', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/createCategory");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/createCategory", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/createCategory`

*create category*

> Body parameter

```json
{
  "categoryName": "string",
  "categoryImageUrl": "string"
}
```

<h3 id="admincontroller_createcategory-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateCategoryDto](#schemacreatecategorydto)|true|none|

<h3 id="admincontroller_createcategory-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|creates the category and returns created category|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|category already exists|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_deleteCategory

<a id="opIdAdminController_deleteCategory"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/admin/deleteCategory/{categoryId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/admin/deleteCategory/{categoryId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/deleteCategory/{categoryId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/admin/deleteCategory/{categoryId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/admin/deleteCategory/{categoryId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/admin/deleteCategory/{categoryId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/deleteCategory/{categoryId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/admin/deleteCategory/{categoryId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/admin/deleteCategory/{categoryId}`

*Delete category by ID*

<h3 id="admincontroller_deletecategory-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categoryId|path|string|true|none|

<h3 id="admincontroller_deletecategory-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|delete Category|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_updateCategory

<a id="opIdAdminController_updateCategory"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/updateCategory/admin/{categoryId} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/updateCategory/admin/{categoryId} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "categoryName": "string",
  "categoryImageUrl": "string",
  "categoryStatus": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/updateCategory/admin/{categoryId}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/updateCategory/admin/{categoryId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/updateCategory/admin/{categoryId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/updateCategory/admin/{categoryId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/updateCategory/admin/{categoryId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/updateCategory/admin/{categoryId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/updateCategory/admin/{categoryId}`

*update category using category id.*

> Body parameter

```json
{
  "categoryName": "string",
  "categoryImageUrl": "string",
  "categoryStatus": true
}
```

<h3 id="admincontroller_updatecategory-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categoryId|path|string|true|none|
|body|body|[UpdateCategoryDto](#schemaupdatecategorydto)|true|none|

<h3 id="admincontroller_updatecategory-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update Category Data|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_findAllCategories

<a id="opIdAdminController_findAllCategories"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/allCategories \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/allCategories HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/allCategories',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/allCategories',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/allCategories', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/allCategories', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/allCategories");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/allCategories", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/allCategories`

*Find All categories*

<h3 id="admincontroller_findallcategories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|get all categories|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getCategoryById

<a id="opIdAdminController_getCategoryById"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/category/{categoryId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/category/{categoryId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/category/{categoryId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/category/{categoryId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/category/{categoryId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/category/{categoryId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/category/{categoryId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/category/{categoryId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/category/{categoryId}`

*Get category details by Id*

<h3 id="admincontroller_getcategorybyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categoryId|path|string|true|none|

<h3 id="admincontroller_getcategorybyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get category by CategoryId|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_collections

<a id="opIdAdminController_collections"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/collections \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/collections HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/collections',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/collections',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/collections', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/collections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/collections");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/collections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/collections`

*Fetch collection stats for admin dashboard*

<h3 id="admincontroller_collections-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|blockchainId|query|string|false|A parameter blockchainId. Optional|

<h3 id="admincontroller_collections-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_nfts

<a id="opIdAdminController_nfts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/nfts \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/nfts HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/nfts',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/nfts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/nfts', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/nfts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/nfts");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/nfts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/nfts`

*Fetch nfts count stats for admin dashboard*

<h3 id="admincontroller_nfts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|blockchainId|query|string|false|A parameter blockchainId. Optional|

<h3 id="admincontroller_nfts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_collectionNftStats

<a id="opIdAdminController_collectionNftStats"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/collectionNftStats \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/collectionNftStats HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/collectionNftStats',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/collectionNftStats',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/collectionNftStats', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/collectionNftStats', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/collectionNftStats");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/collectionNftStats", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/collectionNftStats`

*Fetch nfts count stats for admin dashboard*

<h3 id="admincontroller_collectionnftstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_findWalletBalance

<a id="opIdAdminController_findWalletBalance"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/findWalletBalance/{walletAddress} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/findWalletBalance/{walletAddress} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/findWalletBalance/{walletAddress}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/findWalletBalance/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/findWalletBalance/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/findWalletBalance/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/findWalletBalance/{walletAddress}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/findWalletBalance/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/findWalletBalance/{walletAddress}`

*Fetch walletbalance stats for admin dashboard*

<h3 id="admincontroller_findwalletbalance-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="admincontroller_findwalletbalance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_userStats

<a id="opIdAdminController_userStats"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/userStats \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/userStats HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/userStats',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/userStats',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/userStats', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/userStats', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/userStats");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/userStats", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/userStats`

*Fetch users stats for admin dashboard*

<h3 id="admincontroller_userstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_revenueGraph

<a id="opIdAdminController_revenueGraph"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/revenueGraph?fromDate=2023-01-18T13%3A47%3A16.887Z&toDate=2023-01-11T13%3A47%3A16.887Z \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/revenueGraph?fromDate=2023-01-18T13%3A47%3A16.887Z&toDate=2023-01-11T13%3A47%3A16.887Z HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/revenueGraph?fromDate=2023-01-18T13%3A47%3A16.887Z&toDate=2023-01-11T13%3A47%3A16.887Z',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/revenueGraph',
  params: {
  'fromDate' => 'string',
'toDate' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/revenueGraph', params={
  'fromDate': '2023-01-18T13:47:16.887Z',  'toDate': '2023-01-11T13:47:16.887Z'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/revenueGraph', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/revenueGraph?fromDate=2023-01-18T13%3A47%3A16.887Z&toDate=2023-01-11T13%3A47%3A16.887Z");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/revenueGraph", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/revenueGraph`

*Fetch revenue graph stats for admin dashboard*

<h3 id="admincontroller_revenuegraph-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|tokenId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|string|true|from date :format(2022-04-30)|
|toDate|query|string|true|till date :format(2022-05-30)|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_revenuegraph-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_salesGraph

<a id="opIdAdminController_salesGraph"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/stats/salesGraph?fromDate=2023-01-18T13%3A47%3A17.345Z&toDate=2023-01-11T13%3A47%3A17.345Z \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/stats/salesGraph?fromDate=2023-01-18T13%3A47%3A17.345Z&toDate=2023-01-11T13%3A47%3A17.345Z HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/stats/salesGraph?fromDate=2023-01-18T13%3A47%3A17.345Z&toDate=2023-01-11T13%3A47%3A17.345Z',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/stats/salesGraph',
  params: {
  'fromDate' => 'string',
'toDate' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/stats/salesGraph', params={
  'fromDate': '2023-01-18T13:47:17.345Z',  'toDate': '2023-01-11T13:47:17.345Z'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/stats/salesGraph', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/stats/salesGraph?fromDate=2023-01-18T13%3A47%3A17.345Z&toDate=2023-01-11T13%3A47%3A17.345Z");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/stats/salesGraph", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/stats/salesGraph`

*Fetch revenue graph stats for admin dashboard*

<h3 id="admincontroller_salesgraph-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|tokenId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|string|true|from date :format(2022-04-30)|
|toDate|query|string|true|till date :format(2022-05-30)|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_salesgraph-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetched stats for admin|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_ExecuteMetaTrasaction

<a id="opIdAdminController_ExecuteMetaTrasaction"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/executeMetaTransaction \
  -H 'Content-Type: application/json'

```

```http
POST /api/v1/admin/executeMetaTransaction HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "contractAddress": "string",
  "userAddress": "string",
  "functionSignature": "string",
  "sigR": "string",
  "sigS": "string",
  "sigV": "string",
  "value": 0
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('/api/v1/admin/executeMetaTransaction',
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
  'Content-Type' => 'application/json'
}

result = RestClient.post '/api/v1/admin/executeMetaTransaction',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('/api/v1/admin/executeMetaTransaction', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/executeMetaTransaction', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/executeMetaTransaction");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/executeMetaTransaction", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/executeMetaTransaction`

*Execute meta Trasactions*

> Body parameter

```json
{
  "contractAddress": "string",
  "userAddress": "string",
  "functionSignature": "string",
  "sigR": "string",
  "sigS": "string",
  "sigV": "string",
  "value": 0
}
```

<h3 id="admincontroller_executemetatrasaction-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ExecuteMetaTrasactionDto](#schemaexecutemetatrasactiondto)|true|none|

<h3 id="admincontroller_executemetatrasaction-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Track meta Tractions|None|

<aside class="success">
This operation does not require authentication
</aside>

## AdminController_blockUser

<a id="opIdAdminController_blockUser"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/block/{walletAddress} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/block/{walletAddress} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isBlocked": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/block/{walletAddress}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/block/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/block/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/block/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/block/{walletAddress}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/block/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/block/{walletAddress}`

*Block User*

> Body parameter

```json
{
  "isBlocked": true
}
```

<h3 id="admincontroller_blockuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|
|body|body|[UserBlockDto](#schemauserblockdto)|true|none|

<h3 id="admincontroller_blockuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_UpdateCashbackPlatformfee

<a id="opIdAdminController_UpdateCashbackPlatformfee"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/updateCashbackPlateformfee \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/updateCashbackPlateformfee HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "platformfee": 0,
  "cashback": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/updateCashbackPlateformfee',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/updateCashbackPlateformfee',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/updateCashbackPlateformfee', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/updateCashbackPlateformfee', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/updateCashbackPlateformfee");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/updateCashbackPlateformfee", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/updateCashbackPlateformfee`

> Body parameter

```json
{
  "platformfee": 0,
  "cashback": 0
}
```

<h3 id="admincontroller_updatecashbackplatformfee-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CashbackPlatformFeeDTO](#schemacashbackplatformfeedto)|true|none|

<h3 id="admincontroller_updatecashbackplatformfee-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|for cashback platformfee updations|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_banUser

<a id="opIdAdminController_banUser"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/ban/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/ban/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isBanned": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/ban/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/ban/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/ban/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/ban/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/ban/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/ban/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/ban/{id}`

*Ban User*

> Body parameter

```json
{
  "isBanned": true
}
```

<h3 id="admincontroller_banuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UserBanDto](#schemauserbandto)|true|none|

<h3 id="admincontroller_banuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_GetDefaultCashbackPlateformfee

<a id="opIdAdminController_GetDefaultCashbackPlateformfee"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getCashbackPlatformfee

```

```http
GET /api/v1/admin/getCashbackPlatformfee HTTP/1.1

```

```javascript

fetch('/api/v1/admin/getCashbackPlatformfee',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/admin/getCashbackPlatformfee',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/admin/getCashbackPlatformfee')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getCashbackPlatformfee', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getCashbackPlatformfee");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getCashbackPlatformfee", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getCashbackPlatformfee`

*Fatch cashback Amount and PlatformFee*

<h3 id="admincontroller_getdefaultcashbackplateformfee-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get default cashback and Platformfee|None|

<aside class="success">
This operation does not require authentication
</aside>

## AdminController_deleteItem

<a id="opIdAdminController_deleteItem"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/admin/delete/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/admin/delete/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/delete/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/admin/delete/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/admin/delete/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/admin/delete/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/delete/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/admin/delete/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/admin/delete/{id}`

*it will delete nft item*

<h3 id="admincontroller_deleteitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="admincontroller_deleteitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getAllItems1

<a id="opIdAdminController_getAllItems1"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/allItems

```

```http
GET /api/v1/admin/allItems HTTP/1.1

```

```javascript

fetch('/api/v1/admin/allItems',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/admin/allItems',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/admin/allItems')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/allItems', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/allItems");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/allItems", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/allItems`

*it will fetch nft items according to filters*

<h3 id="admincontroller_getallitems1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|status|query|string|false|give single or multiple input from 'new', 'buynow', 'onAuction', 'hasOffer', 'hasCashback' seprated by ' , '|
|priceType|query|string|false|give price type eg. usd, eth, weth|
|priceRange|query|string|false|give price value range separated by ' , '  eg.(1, 10) |
|paymentTokens|query|string|false|give patmentToken  separated by ' , '  eg.(Eth, MATIC) |
|collectionsId|query|string|false|give single collection id or multiple separated by ' , '|
|onSale|query|string|false|give single token id or multiple seprated by ' , '|
|chainsId|query|string|false|give single chain id or multiple separated by ' , '|
|categories|query|string|false|give single categoryId id or multiple separated by |
|isBundle|query|boolean|false|none|
|isOpenseaNft|query|boolean|false|none|
|search|query|string|false|search by name of item|
|order|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|propertyType|query|string|false|none|
|PropertyName|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|priceType|usd|
|priceType|eth|
|priceType|weth|
|order|recentlyCreated|
|order|oldest|
|order|endingSoon|
|order|endDate|
|order|recentlyListed|
|order|HighestLastSale|
|order|priceH2L|
|order|priceL2H|
|order|recentlyReceived|
|order|mostFavourited|
|order|recentlySold|

<h3 id="admincontroller_getallitems1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## AdminController_createNftItem

<a id="opIdAdminController_createNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/item/create \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/item/create HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/item/create',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/item/create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/item/create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/item/create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/item/create");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/item/create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/item/create`

*it will create new nft item*

> Body parameter

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}
```

<h3 id="admincontroller_createnftitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateNftItemDto](#schemacreatenftitemdto)|true|none|

<h3 id="admincontroller_createnftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_updateNftItem

<a id="opIdAdminController_updateNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/admin/item/update/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/admin/item/update/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/item/update/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/admin/item/update/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/admin/item/update/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/admin/item/update/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/item/update/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/admin/item/update/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/admin/item/update/{id}`

*it will update nft item*

> Body parameter

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true
}
```

<h3 id="admincontroller_updatenftitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateNftItemDto](#schemaupdatenftitemdto)|true|none|

<h3 id="admincontroller_updatenftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_createCollection

<a id="opIdAdminController_createCollection"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/createCollectionAdmin \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/createCollectionAdmin HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "blockchain": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/createCollectionAdmin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/createCollectionAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/createCollectionAdmin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/createCollectionAdmin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/createCollectionAdmin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/createCollectionAdmin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/createCollectionAdmin`

*Creates a new Collection owned by admin*

> Body parameter

```json
{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "blockchain": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}
```

<h3 id="admincontroller_createcollection-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateCollectionsDto](#schemacreatecollectionsdto)|true|none|

<h3 id="admincontroller_createcollection-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Collection Created|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getPresignedURL

<a id="opIdAdminController_getPresignedURL"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/getPresignedURLForAdmin \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/getPresignedURLForAdmin HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileName": "string",
  "fileType": "string",
  "filePath": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getPresignedURLForAdmin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/getPresignedURLForAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/getPresignedURLForAdmin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/getPresignedURLForAdmin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getPresignedURLForAdmin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/getPresignedURLForAdmin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/getPresignedURLForAdmin`

*Get pre-signed url with given filename and filetype*

> Body parameter

```json
{
  "fileName": "string",
  "fileType": "string",
  "filePath": "string"
}
```

<h3 id="admincontroller_getpresignedurl-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SignedUrlDto](#schemasignedurldto)|true|none|

<h3 id="admincontroller_getpresignedurl-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Pre-Signed Url|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_countOfTransaction

<a id="opIdAdminController_countOfTransaction"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/admin/countOfTransaction \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/admin/countOfTransaction HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/countOfTransaction',
{
  method: 'POST',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/admin/countOfTransaction',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/admin/countOfTransaction', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/admin/countOfTransaction', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/countOfTransaction");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/admin/countOfTransaction", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/admin/countOfTransaction`

*Get count of total trasaction done in different tokens*

<h3 id="admincontroller_countoftransaction-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|count|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getAllCollectionsAdmin

<a id="opIdAdminController_getAllCollectionsAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getAllCollectionsAdmin \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getAllCollectionsAdmin HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getAllCollectionsAdmin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getAllCollectionsAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getAllCollectionsAdmin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getAllCollectionsAdmin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getAllCollectionsAdmin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getAllCollectionsAdmin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getAllCollectionsAdmin`

*Get all collections*

<h3 id="admincontroller_getallcollectionsadmin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|Number of items per page|
|skip|query|number|false|Skip items for page number|
|earningWalletAddress|query|string|false|Earning Wallet id of the collection|
|slug|query|string|false|search by collection slug|
|time|query|string|false|none|
|isVerified|query|boolean|false|isVerified value for collection|
|search|query|string|false|search by collection name|
|name|query|string|false|order by collection name eg. DESC or ASC|
|createdAt|query|string|false|order by createdAt eg. DESC or ASC|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|
|time|alltime|

<h3 id="admincontroller_getallcollectionsadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|all collections|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getAllCollectionsNames

<a id="opIdAdminController_getAllCollectionsNames"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getAllCollectionsNames \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getAllCollectionsNames HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getAllCollectionsNames',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getAllCollectionsNames',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getAllCollectionsNames', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getAllCollectionsNames', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getAllCollectionsNames");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getAllCollectionsNames", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getAllCollectionsNames`

*Get all collections*

<h3 id="admincontroller_getallcollectionsnames-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|Number of items per page|
|skip|query|number|false|Skip items for page number|
|earningWalletAddress|query|string|false|Earning Wallet id of the collection|
|slug|query|string|false|search by collection slug|
|time|query|string|false|none|
|isVerified|query|boolean|false|isVerified value for collection|
|search|query|string|false|search by collection name|
|name|query|string|false|order by collection name eg. DESC or ASC|
|createdAt|query|string|false|order by createdAt eg. DESC or ASC|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|
|time|alltime|

<h3 id="admincontroller_getallcollectionsnames-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|all collections|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getCollectionById

<a id="opIdAdminController_getCollectionById"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getCollectionForAdmin/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getCollectionForAdmin/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getCollectionForAdmin/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getCollectionForAdmin/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getCollectionForAdmin/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getCollectionForAdmin/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getCollectionForAdmin/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getCollectionForAdmin/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getCollectionForAdmin/{id}`

*Find one collection*

<h3 id="admincontroller_getcollectionbyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="admincontroller_getcollectionbyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Single Collection|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getAdminWalletBalance

<a id="opIdAdminController_getAdminWalletBalance"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/admin/getAdminWalletBalance \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/admin/getAdminWalletBalance HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getAdminWalletBalance',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/admin/getAdminWalletBalance',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/admin/getAdminWalletBalance', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/admin/getAdminWalletBalance', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getAdminWalletBalance");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/admin/getAdminWalletBalance", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/admin/getAdminWalletBalance`

*Get balance of admin wallet*

<h3 id="admincontroller_getadminwalletbalance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Balance|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_verifyUserUpdate

<a id="opIdAdminController_verifyUserUpdate"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/verifyUserUpdate/{walletAddress} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/verifyUserUpdate/{walletAddress} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "verifiedUser": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/verifyUserUpdate/{walletAddress}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/verifyUserUpdate/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/verifyUserUpdate/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/verifyUserUpdate/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/verifyUserUpdate/{walletAddress}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/verifyUserUpdate/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/verifyUserUpdate/{walletAddress}`

*verify User*

> Body parameter

```json
{
  "verifiedUser": true
}
```

<h3 id="admincontroller_verifyuserupdate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|
|body|body|[UserVerifyDto](#schemauserverifydto)|true|none|

<h3 id="admincontroller_verifyuserupdate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_verifyCollectionUpdate

<a id="opIdAdminController_verifyCollectionUpdate"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/verifyCollectionUpdate/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/verifyCollectionUpdate/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isVerified": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/verifyCollectionUpdate/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/verifyCollectionUpdate/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/verifyCollectionUpdate/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/verifyCollectionUpdate/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/verifyCollectionUpdate/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/verifyCollectionUpdate/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/verifyCollectionUpdate/{id}`

*verify collection*

> Body parameter

```json
{
  "isVerified": true
}
```

<h3 id="admincontroller_verifycollectionupdate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[CollectionVerifyDto](#schemacollectionverifydto)|true|none|

<h3 id="admincontroller_verifycollectionupdate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_updateNotableDrop

<a id="opIdAdminController_updateNotableDrop"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/updateNotableDrop/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/updateNotableDrop/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isNotableDrop": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/updateNotableDrop/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/updateNotableDrop/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/updateNotableDrop/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/updateNotableDrop/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/updateNotableDrop/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/updateNotableDrop/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/updateNotableDrop/{id}`

*Updates whether a collection is a notable drop or not*

> Body parameter

```json
{
  "isNotableDrop": true
}
```

<h3 id="admincontroller_updatenotabledrop-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[NotableDrop](#schemanotabledrop)|true|none|

<h3 id="admincontroller_updatenotabledrop-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_cashbackGiven

<a id="opIdAdminController_cashbackGiven"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/cashbackGiven \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/cashbackGiven HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/cashbackGiven',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/cashbackGiven',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/cashbackGiven', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/cashbackGiven', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/cashbackGiven");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/cashbackGiven", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/cashbackGiven`

*To fetch total cashback given on platform*

<h3 id="admincontroller_cashbackgiven-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|tokenId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_cashbackgiven-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_cashbackPaidOut

<a id="opIdAdminController_cashbackPaidOut"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/cashbackpaidout \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/cashbackpaidout HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/cashbackpaidout',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/cashbackpaidout',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/cashbackpaidout', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/cashbackpaidout', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/cashbackpaidout");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/cashbackpaidout", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/cashbackpaidout`

*To fetch cashback paid out based on filters*

<h3 id="admincontroller_cashbackpaidout-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|tokenId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_cashbackpaidout-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|In case admin is not logged in|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_fatchNftItemByID

<a id="opIdAdminController_fatchNftItemByID"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getNftItemByIDForAdmin/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getNftItemByIDForAdmin/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getNftItemByIDForAdmin/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getNftItemByIDForAdmin/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getNftItemByIDForAdmin/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getNftItemByIDForAdmin/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getNftItemByIDForAdmin/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getNftItemByIDForAdmin/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getNftItemByIDForAdmin/{id}`

*get item by its its ID*

<h3 id="admincontroller_fatchnftitembyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="admincontroller_fatchnftitembyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET ITEM DATA BY ITEM ID|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_fetchKycLogs

<a id="opIdAdminController_fetchKycLogs"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/kyc_logs \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/kyc_logs HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/kyc_logs',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/kyc_logs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/kyc_logs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/kyc_logs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/kyc_logs");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/kyc_logs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/kyc_logs`

*Fetching the kyc logs*

<h3 id="admincontroller_fetchkyclogs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|search|query|string|false|none|

<h3 id="admincontroller_fetchkyclogs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Kyc Logs fetched successfully|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_resetKycLimit

<a id="opIdAdminController_resetKycLimit"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/reset_user_kyc_limit?wallet_address=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/reset_user_kyc_limit?wallet_address=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/reset_user_kyc_limit?wallet_address=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/reset_user_kyc_limit',
  params: {
  'wallet_address' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/reset_user_kyc_limit', params={
  'wallet_address': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/reset_user_kyc_limit', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/reset_user_kyc_limit?wallet_address=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/reset_user_kyc_limit", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/reset_user_kyc_limit`

*Used to reset the user kyc limit*

<h3 id="admincontroller_resetkyclimit-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|wallet_address|query|string|true|none|

<h3 id="admincontroller_resetkyclimit-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Kyc limit resetted successfully|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_verifyKyc

<a id="opIdAdminController_verifyKyc"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/verifykyc/{walletAddress} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/verifykyc/{walletAddress} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "status": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/verifykyc/{walletAddress}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/verifykyc/{walletAddress}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/verifykyc/{walletAddress}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/verifykyc/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/verifykyc/{walletAddress}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/verifykyc/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/verifykyc/{walletAddress}`

*Used to verify the kyc*

> Body parameter

```json
{
  "status": true
}
```

<h3 id="admincontroller_verifykyc-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|
|body|body|[KycVerificationDto](#schemakycverificationdto)|true|none|

<h3 id="admincontroller_verifykyc-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Kyc verified successfully|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_setExtraCharges

<a id="opIdAdminController_setExtraCharges"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/setExtraCharges \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/setExtraCharges HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "extraCharges": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/setExtraCharges',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/setExtraCharges',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/setExtraCharges', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/setExtraCharges', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/setExtraCharges");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/setExtraCharges", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/setExtraCharges`

*Set extra charges on plaform*

> Body parameter

```json
{
  "id": "string",
  "extraCharges": "string"
}
```

<h3 id="admincontroller_setextracharges-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SetChargesDto](#schemasetchargesdto)|true|none|

<h3 id="admincontroller_setextracharges-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|extra charges|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_setPlatformFees

<a id="opIdAdminController_setPlatformFees"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/setPlatformMintingFees \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/setPlatformMintingFees HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "platformFees": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/setPlatformMintingFees',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/setPlatformMintingFees',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/setPlatformMintingFees', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/setPlatformMintingFees', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/setPlatformMintingFees");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/setPlatformMintingFees", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/setPlatformMintingFees`

*set Platform fees charges on plaform*

> Body parameter

```json
{
  "id": "string",
  "platformFees": "string"
}
```

<h3 id="admincontroller_setplatformfees-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PlatformFeesDto](#schemaplatformfeesdto)|true|none|

<h3 id="admincontroller_setplatformfees-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Platform fees|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_setRelayerCashback

<a id="opIdAdminController_setRelayerCashback"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/setRelayerCashback \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/setRelayerCashback HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "setCashback": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/setRelayerCashback',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/setRelayerCashback',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/setRelayerCashback', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/setRelayerCashback', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/setRelayerCashback");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/setRelayerCashback", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/setRelayerCashback`

*Set Cashback percentage on plaform*

> Body parameter

```json
{
  "id": "string",
  "setCashback": "string"
}
```

<h3 id="admincontroller_setrelayercashback-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SetCashbackDto](#schemasetcashbackdto)|true|none|

<h3 id="admincontroller_setrelayercashback-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Cashback percentage|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getFeeDetails

<a id="opIdAdminController_getFeeDetails"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getFeeDetails/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getFeeDetails/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getFeeDetails/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getFeeDetails/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getFeeDetails/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getFeeDetails/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getFeeDetails/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getFeeDetails/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getFeeDetails/{id}`

*Get fees on plaform*

<h3 id="admincontroller_getfeedetails-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="admincontroller_getfeedetails-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Cashback percentage|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_GetAllUserByAdmin

<a id="opIdAdminController_GetAllUserByAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getAllUserbyAdmin \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getAllUserbyAdmin HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getAllUserbyAdmin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getAllUserbyAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getAllUserbyAdmin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getAllUserbyAdmin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getAllUserbyAdmin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getAllUserbyAdmin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getAllUserbyAdmin`

<h3 id="admincontroller_getalluserbyadmin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|isBlocked|query|boolean|false|none|
|kyc_verified|query|boolean|false|none|
|username|query|string|false|none|
|walletAddress|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|search|query|string|false|none|
|verifiedUser|query|boolean|false|none|
|walletType|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

<h3 id="admincontroller_getalluserbyadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_findAllByOwnerOrCollaborator

<a id="opIdAdminController_findAllByOwnerOrCollaborator"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getAdminCollections \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/getAdminCollections HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/getAdminCollections',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/getAdminCollections',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/getAdminCollections', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getAdminCollections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getAdminCollections");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getAdminCollections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getAdminCollections`

*Find All Collections of Admin*

<h3 id="admincontroller_findallbyownerorcollaborator-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

<h3 id="admincontroller_findallbyownerorcollaborator-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns All Collections that are owned by admin|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collections do not exist|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getUsersWithTransactions

<a id="opIdAdminController_getUsersWithTransactions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/userswithtransactions \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/userswithtransactions HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/userswithtransactions',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/userswithtransactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/userswithtransactions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/userswithtransactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/userswithtransactions");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/userswithtransactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/userswithtransactions`

*Find All Users with Transactions*

<h3 id="admincontroller_getuserswithtransactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_getuserswithtransactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getUsersWithNoTransactions

<a id="opIdAdminController_getUsersWithNoTransactions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/userswithnotransactions \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/userswithnotransactions HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/userswithnotransactions',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/userswithnotransactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/userswithnotransactions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/userswithnotransactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/userswithnotransactions");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/userswithnotransactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/userswithnotransactions`

*Find All Users with No Transactions*

<h3 id="admincontroller_getuserswithnotransactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_getuserswithnotransactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_averageVolumePerTrade

<a id="opIdAdminController_averageVolumePerTrade"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/averagevolumepertrade \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/averagevolumepertrade HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/averagevolumepertrade',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/averagevolumepertrade',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/averagevolumepertrade', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/averagevolumepertrade', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/averagevolumepertrade");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/averagevolumepertrade", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/averagevolumepertrade`

<h3 id="admincontroller_averagevolumepertrade-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|skip|query|number|false|none|
|take|query|number|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_averagevolumepertrade-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_averageVolumePerUser

<a id="opIdAdminController_averageVolumePerUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/averagevolumeperuser \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/averagevolumeperuser HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/averagevolumeperuser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/averagevolumeperuser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/averagevolumeperuser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/averagevolumeperuser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/averagevolumeperuser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/averagevolumeperuser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/averagevolumeperuser`

<h3 id="admincontroller_averagevolumeperuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|skip|query|number|false|none|
|take|query|number|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_averagevolumeperuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_averageTradePerUser

<a id="opIdAdminController_averageTradePerUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/averagetradeperuser \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/averagetradeperuser HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/averagetradeperuser',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/averagetradeperuser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/averagetradeperuser', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/averagetradeperuser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/averagetradeperuser");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/averagetradeperuser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/averagetradeperuser`

<h3 id="admincontroller_averagetradeperuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|skip|query|number|false|none|
|take|query|number|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_averagetradeperuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getGeneratedFees

<a id="opIdAdminController_getGeneratedFees"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/generatedfees \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/generatedfees HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/generatedfees',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/generatedfees',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/generatedfees', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/generatedfees', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/generatedfees");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/generatedfees", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/generatedfees`

<h3 id="admincontroller_getgeneratedfees-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|query|string|false|none|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|categoryId|query|string|false|none|
|chainId|query|string|false|none|
|tokenId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|skip|query|number|false|none|
|take|query|number|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_getgeneratedfees-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_topCollectionsByRevenue

<a id="opIdAdminController_topCollectionsByRevenue"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/topcollectionsbyrevenue \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/topcollectionsbyrevenue HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/topcollectionsbyrevenue',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/topcollectionsbyrevenue',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/topcollectionsbyrevenue', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/topcollectionsbyrevenue', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/topcollectionsbyrevenue");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/topcollectionsbyrevenue", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/topcollectionsbyrevenue`

<h3 id="admincontroller_topcollectionsbyrevenue-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|query|string|false|none|
|walletAddress|query|string|false|none|
|chainId|query|string|false|none|
|categoryId|query|string|false|none|
|mintingPlatform|query|string|false|none|
|nftPurchaseMethod|query|string|false|none|
|skip|query|number|false|none|
|take|query|number|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nftPurchaseMethod|BUY_NOW|
|nftPurchaseMethod|ACCEPT_OFFER|

<h3 id="admincontroller_topcollectionsbyrevenue-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_listAllMintingPlatformNfts

<a id="opIdAdminController_listAllMintingPlatformNfts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/listAllMintingPlatformNfts?identifier=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/listAllMintingPlatformNfts?identifier=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/listAllMintingPlatformNfts?identifier=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/listAllMintingPlatformNfts',
  params: {
  'identifier' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/listAllMintingPlatformNfts', params={
  'identifier': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/listAllMintingPlatformNfts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/listAllMintingPlatformNfts?identifier=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/listAllMintingPlatformNfts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/listAllMintingPlatformNfts`

<h3 id="admincontroller_listallmintingplatformnfts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|identifier|query|string|true|none|

<h3 id="admincontroller_listallmintingplatformnfts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_updateFeaturedVideo

<a id="opIdAdminController_updateFeaturedVideo"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/admin/updateFeaturedVideo \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/admin/updateFeaturedVideo HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/updateFeaturedVideo',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/admin/updateFeaturedVideo',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/admin/updateFeaturedVideo', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/admin/updateFeaturedVideo', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/updateFeaturedVideo");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/admin/updateFeaturedVideo", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/admin/updateFeaturedVideo`

<h3 id="admincontroller_updatefeaturedvideo-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|videoUrl|query|string|false|Link of video|
|gifUrl|query|string|false|Link of gif|

<h3 id="admincontroller_updatefeaturedvideo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_setCollectionAsFeatured

<a id="opIdAdminController_setCollectionAsFeatured"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/admin/setCollectionAsFeatured \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/admin/setCollectionAsFeatured HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "collectionId": "string",
  "isFeatured": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/setCollectionAsFeatured',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/admin/setCollectionAsFeatured',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/admin/setCollectionAsFeatured', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/admin/setCollectionAsFeatured', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/setCollectionAsFeatured");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/admin/setCollectionAsFeatured", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/admin/setCollectionAsFeatured`

> Body parameter

```json
{
  "collectionId": "string",
  "isFeatured": true
}
```

<h3 id="admincontroller_setcollectionasfeatured-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SetFeaturedCollectionDto](#schemasetfeaturedcollectiondto)|true|none|

<h3 id="admincontroller_setcollectionasfeatured-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_getFeaturedCollectionsAndVideo

<a id="opIdAdminController_getFeaturedCollectionsAndVideo"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/getFeaturedCollectionsAndVideo

```

```http
GET /api/v1/admin/getFeaturedCollectionsAndVideo HTTP/1.1

```

```javascript

fetch('/api/v1/admin/getFeaturedCollectionsAndVideo',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/admin/getFeaturedCollectionsAndVideo',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/admin/getFeaturedCollectionsAndVideo')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/getFeaturedCollectionsAndVideo', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/getFeaturedCollectionsAndVideo");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/getFeaturedCollectionsAndVideo", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/getFeaturedCollectionsAndVideo`

<h3 id="admincontroller_getfeaturedcollectionsandvideo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## AdminController_getWalletDetails

<a id="opIdAdminController_getWalletDetails"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/walletDetails \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/walletDetails HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/walletDetails',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/walletDetails',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/walletDetails', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/walletDetails', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/walletDetails");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/walletDetails", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/walletDetails`

<h3 id="admincontroller_getwalletdetails-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_enableGiveAway

<a id="opIdAdminController_enableGiveAway"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/admin/giveaway \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/admin/giveaway HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "status": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/giveaway',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/admin/giveaway',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/admin/giveaway', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/admin/giveaway', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/giveaway");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/admin/giveaway", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/admin/giveaway`

> Body parameter

```json
{
  "status": true
}
```

<h3 id="admincontroller_enablegiveaway-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[GiveawayDto](#schemagiveawaydto)|true|none|

<h3 id="admincontroller_enablegiveaway-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AdminController_fetchGiveAwayStatus

<a id="opIdAdminController_fetchGiveAwayStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/admin/giveaway \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/admin/giveaway HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/admin/giveaway',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/admin/giveaway',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/admin/giveaway', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/admin/giveaway', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/admin/giveaway");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/admin/giveaway", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/admin/giveaway`

<h3 id="admincontroller_fetchgiveawaystatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_BlockCollection

<a id="opIdCollectionsController_BlockCollection"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/collection/blockCollection \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/collection/blockCollection HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "collectionId": "string",
  "blockOrUnblock": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/collection/blockCollection',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/collection/blockCollection',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/collection/blockCollection', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/collection/blockCollection', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collection/blockCollection");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/collection/blockCollection", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/collection/blockCollection`

> Body parameter

```json
{
  "collectionId": "string",
  "blockOrUnblock": true
}
```

<h3 id="collectionscontroller_blockcollection-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[BlockCollectionDto](#schemablockcollectiondto)|true|none|

<h3 id="collectionscontroller_blockcollection-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection is updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_updateCashbackByCollectionID

<a id="opIdCollectionsController_updateCashbackByCollectionID"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/collection/updateCashbackByCollectionId \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/collection/updateCashbackByCollectionId HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "collectionId": "string",
  "cashback": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/collection/updateCashbackByCollectionId',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/collection/updateCashbackByCollectionId',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/collection/updateCashbackByCollectionId', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/collection/updateCashbackByCollectionId', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collection/updateCashbackByCollectionId");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/collection/updateCashbackByCollectionId", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/collection/updateCashbackByCollectionId`

> Body parameter

```json
{
  "collectionId": "string",
  "cashback": 0
}
```

<h3 id="collectionscontroller_updatecashbackbycollectionid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateCashbackByCollectionIdDto](#schemaupdatecashbackbycollectioniddto)|true|none|

<h3 id="collectionscontroller_updatecashbackbycollectionid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_deleteCollectionByAdmin

<a id="opIdCollectionsController_deleteCollectionByAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/collections/deleteCollectionByAdmin/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/collections/deleteCollectionByAdmin/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/deleteCollectionByAdmin/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/collections/deleteCollectionByAdmin/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/collections/deleteCollectionByAdmin/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/collections/deleteCollectionByAdmin/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/deleteCollectionByAdmin/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/collections/deleteCollectionByAdmin/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/collections/deleteCollectionByAdmin/{id}`

*Removed a Collection by Admin*

<h3 id="collectionscontroller_deletecollectionbyadmin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="collectionscontroller_deletecollectionbyadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer, bearer
</aside>

## ActivityController_FilterSalesActivities

<a id="opIdActivityController_FilterSalesActivities"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/admin/fetchSalesActivity \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/activity/admin/fetchSalesActivity HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/activity/admin/fetchSalesActivity',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/activity/admin/fetchSalesActivity',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/activity/admin/fetchSalesActivity', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/admin/fetchSalesActivity', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/admin/fetchSalesActivity");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/admin/fetchSalesActivity", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/admin/fetchSalesActivity`

*Find activities related to sales activity by ADMIN*

<h3 id="activitycontroller_filtersalesactivities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|chain|query|string|false|chain must be comma seperated|
|category|query|string|false|none|
|time|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|1|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_filtersalesactivities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ActivityController_filterTransactions

<a id="opIdActivityController_filterTransactions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/admin/transactions \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/activity/admin/transactions HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/activity/admin/transactions',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/activity/admin/transactions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/activity/admin/transactions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/admin/transactions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/admin/transactions");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/admin/transactions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/admin/transactions`

*Find transactions by ADMIN*

<h3 id="activitycontroller_filtertransactions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|event|query|string|false|none|
|chain|query|string|false|chain must be comma seperated|
|category|query|string|false|none|
|time|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|event|Listed|
|event|Minted|
|event|Sales|
|event|Successful|
|event|Cancelled|
|event|BidEntered|
|event|BidWithdrawn|
|event|Transfer|
|event|OfferEntered|
|event|OfferWithdrawn|
|event|Approve|
|time|1|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_filtertransactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_updateCashback

<a id="opIdNftItemController_updateCashback"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/updatecashback \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/updatecashback HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "itemID": "string",
  "cashback": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/updatecashback',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/updatecashback',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/updatecashback', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/updatecashback', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/updatecashback");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/updatecashback", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/updatecashback`

> Body parameter

```json
{
  "itemID": "string",
  "cashback": 0
}
```

<h3 id="nftitemcontroller_updatecashback-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateCashbackDto](#schemaupdatecashbackdto)|true|none|

<h3 id="nftitemcontroller_updatecashback-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_BlockItem

<a id="opIdNftItemController_BlockItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/blockitem \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/blockitem HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "ItemId": "string",
  "isBlocked": true,
  "isblockedByAI": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/blockitem',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/blockitem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/blockitem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/blockitem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/blockitem");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/blockitem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/blockitem`

> Body parameter

```json
{
  "ItemId": "string",
  "isBlocked": true,
  "isblockedByAI": true
}
```

<h3 id="nftitemcontroller_blockitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[BlockItemDto](#schemablockitemdto)|true|none|

<h3 id="nftitemcontroller_blockitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-notification-module">Notification Module</h1>

## NotificationController_update

<a id="opIdNotificationController_update"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/notification/me \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/notification/me HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "itemSold": true,
  "bidActivity": true,
  "priceChange": true,
  "auctionExpiration": true,
  "outBid": true,
  "ownedItemUpdates": true,
  "successfulPurchase": true,
  "jungleNewsletter": true,
  "minimumBidThreshold": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/notification/me',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/notification/me',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/notification/me', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/notification/me', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/notification/me");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/notification/me", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/notification/me`

*update user notification settings*

> Body parameter

```json
{
  "itemSold": true,
  "bidActivity": true,
  "priceChange": true,
  "auctionExpiration": true,
  "outBid": true,
  "ownedItemUpdates": true,
  "successfulPurchase": true,
  "jungleNewsletter": true,
  "minimumBidThreshold": 0
}
```

<h3 id="notificationcontroller_update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[NotificationDto](#schemanotificationdto)|true|none|

<h3 id="notificationcontroller_update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|notification setting of current user updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NotificationController_getNotification

<a id="opIdNotificationController_getNotification"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/notification/me \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/notification/me HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/notification/me',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/notification/me',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/notification/me', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/notification/me', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/notification/me");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/notification/me", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/notification/me`

*get all notification settings of login user*

<h3 id="notificationcontroller_getnotification-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns all notification settings of user|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-chains">Chains</h1>

## ChainsController_createChain

<a id="opIdChainsController_createChain"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/chains/chains \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/chains/chains HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "name": "string",
  "symbol": "string",
  "chainId": "string",
  "imageUrl": "string",
  "baseUrl": "string",
  "tokenId": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/chains/chains',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/chains/chains',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/chains/chains', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/chains/chains', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/chains/chains");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/chains/chains", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/chains/chains`

*Create new Chains*

> Body parameter

```json
{
  "name": "string",
  "symbol": "string",
  "chainId": "string",
  "imageUrl": "string",
  "baseUrl": "string",
  "tokenId": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0
}
```

<h3 id="chainscontroller_createchain-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateChainsDto](#schemacreatechainsdto)|true|none|

<h3 id="chainscontroller_createchain-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ChainsController_updateChain

<a id="opIdChainsController_updateChain"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/chains/chains \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/chains/chains HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "name": "string",
  "chainId": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "baseUrl": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/chains/chains',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/chains/chains',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/chains/chains', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/chains/chains', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/chains/chains");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/chains/chains", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/chains/chains`

*Update the Existing Chains*

> Body parameter

```json
{
  "id": "string",
  "name": "string",
  "chainId": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "baseUrl": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true
}
```

<h3 id="chainscontroller_updatechain-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateChainsDto](#schemaupdatechainsdto)|true|none|

<h3 id="chainscontroller_updatechain-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ChainsController_getChainsForAdmin

<a id="opIdChainsController_getChainsForAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/chains/admin \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/chains/admin HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/chains/admin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/chains/admin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/chains/admin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/chains/admin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/chains/admin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/chains/admin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/chains/admin`

*Get all the Chain and their details*

<h3 id="chainscontroller_getchainsforadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## ChainsController_getChainsForUser

<a id="opIdChainsController_getChainsForUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/chains/user

```

```http
GET /api/v1/chains/user HTTP/1.1

```

```javascript

fetch('/api/v1/chains/user',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/chains/user',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/chains/user')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/chains/user', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/chains/user");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/chains/user", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/chains/user`

*Get all the chains and their details*

<h3 id="chainscontroller_getchainsforuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## ChainsController_deleteChain

<a id="opIdChainsController_deleteChain"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/chains/deleteChain/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/chains/deleteChain/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/chains/deleteChain/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/chains/deleteChain/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/chains/deleteChain/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/chains/deleteChain/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/chains/deleteChain/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/chains/deleteChain/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/chains/deleteChain/{id}`

*Deleting chain*

<h3 id="chainscontroller_deletechain-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="chainscontroller_deletechain-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-tokens">Tokens</h1>

## TokenController_createToken

<a id="opIdTokenController_createToken"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/tokens \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/tokens HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "chainId": "string",
  "chainName": "string",
  "name": "string",
  "symbol": "string",
  "tokenId": "string",
  "imageUrl": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/tokens',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/tokens`

*Create new Tokens*

> Body parameter

```json
{
  "chainId": "string",
  "chainName": "string",
  "name": "string",
  "symbol": "string",
  "tokenId": "string",
  "imageUrl": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}
```

<h3 id="tokencontroller_createtoken-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateTokensDto](#schemacreatetokensdto)|true|none|

<h3 id="tokencontroller_createtoken-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## TokenController_updateToken

<a id="opIdTokenController_updateToken"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/tokens \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/tokens HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "chainId": "string",
  "name": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/tokens',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/tokens',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/tokens', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/tokens`

*Update the Existing Tokens*

> Body parameter

```json
{
  "id": "string",
  "chainId": "string",
  "name": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}
```

<h3 id="tokencontroller_updatetoken-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateTokensDto](#schemaupdatetokensdto)|true|none|

<h3 id="tokencontroller_updatetoken-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## TokenController_getAllActiveTokens

<a id="opIdTokenController_getAllActiveTokens"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/tokens

```

```http
GET /api/v1/tokens HTTP/1.1

```

```javascript

fetch('/api/v1/tokens',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/tokens',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/tokens')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/tokens', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/tokens", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/tokens`

*Fetches all active tokens*

<h3 id="tokencontroller_getallactivetokens-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Tokens not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## TokenController_getTokensForAdmin

<a id="opIdTokenController_getTokensForAdmin"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/tokens/admin/{chainId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/tokens/admin/{chainId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/tokens/admin/{chainId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/tokens/admin/{chainId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/tokens/admin/{chainId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/tokens/admin/{chainId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens/admin/{chainId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/tokens/admin/{chainId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/tokens/admin/{chainId}`

*Get all the Token and their details*

<h3 id="tokencontroller_gettokensforadmin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|chainId|path|string|true|none|

<h3 id="tokencontroller_gettokensforadmin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## TokenController_getTokensForUser

<a id="opIdTokenController_getTokensForUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/tokens/user/{chainId}

```

```http
GET /api/v1/tokens/user/{chainId} HTTP/1.1

```

```javascript

fetch('/api/v1/tokens/user/{chainId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/tokens/user/{chainId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/tokens/user/{chainId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/tokens/user/{chainId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens/user/{chainId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/tokens/user/{chainId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/tokens/user/{chainId}`

*Get all the Tokens and their details*

<h3 id="tokencontroller_gettokensforuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|chainId|path|string|true|none|

<h3 id="tokencontroller_gettokensforuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## TokenController_getTokensById

<a id="opIdTokenController_getTokensById"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/tokens/user?tokenIds=string

```

```http
GET /api/v1/tokens/user?tokenIds=string HTTP/1.1

```

```javascript

fetch('/api/v1/tokens/user?tokenIds=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/tokens/user',
  params: {
  'tokenIds' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/tokens/user', params={
  'tokenIds': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/tokens/user', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens/user?tokenIds=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/tokens/user", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/tokens/user`

*Get all the Tokens with given tokenId and their details*

<h3 id="tokencontroller_gettokensbyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tokenIds|query|string|true|none|

<h3 id="tokencontroller_gettokensbyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## TokenController_deleteToken

<a id="opIdTokenController_deleteToken"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/tokens/deleteToken/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/tokens/deleteToken/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/tokens/deleteToken/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/tokens/deleteToken/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/tokens/deleteToken/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/tokens/deleteToken/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens/deleteToken/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/tokens/deleteToken/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/tokens/deleteToken/{id}`

*Deleting Token*

<h3 id="tokencontroller_deletetoken-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="tokencontroller_deletetoken-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Chain Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## TokenController_getAllTokenIds

<a id="opIdTokenController_getAllTokenIds"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/tokens/getalltokenids

```

```http
GET /api/v1/tokens/getalltokenids HTTP/1.1

```

```javascript

fetch('/api/v1/tokens/getalltokenids',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/tokens/getalltokenids',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/tokens/getalltokenids')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/tokens/getalltokenids', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/tokens/getalltokenids");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/tokens/getalltokenids", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/tokens/getalltokenids`

*Fetches all active tokens*

<h3 id="tokencontroller_getalltokenids-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-collection-module">Collection Module</h1>

## CollectionsController_create

<a id="opIdCollectionsController_create"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/collections/create \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/collections/create HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "blockchain": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/create',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/collections/create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/collections/create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/collections/create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/create");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/collections/create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/collections/create`

*Creates a new Collection owned by user who is logged in*

> Body parameter

```json
{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "blockchain": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}
```

<h3 id="collectionscontroller_create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateCollectionsDto](#schemacreatecollectionsdto)|true|none|

<h3 id="collectionscontroller_create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Collection Created|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Collection creation failed|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_findAll

<a id="opIdCollectionsController_findAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections

```

```http
GET /api/v1/collections HTTP/1.1

```

```javascript

fetch('/api/v1/collections',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections`

*Find All Collections*

<h3 id="collectionscontroller_findall-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|Number of items per page|
|skip|query|number|false|Skip items for page number|
|earningWalletAddress|query|string|false|Earning Wallet id of the collection|
|slug|query|string|false|search by collection slug|
|time|query|string|false|none|
|isVerified|query|boolean|false|isVerified value for collection|
|search|query|string|false|search by collection name|
|name|query|string|false|order by collection name eg. DESC or ASC|
|createdAt|query|string|false|order by createdAt eg. DESC or ASC|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|
|time|alltime|

<h3 id="collectionscontroller_findall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns All Collections|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collections do not exist|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_findAllByOwnerOrCollaborator

<a id="opIdCollectionsController_findAllByOwnerOrCollaborator"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getByUserId/{walletAddress}

```

```http
GET /api/v1/collections/getByUserId/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/getByUserId/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/getByUserId/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/getByUserId/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getByUserId/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getByUserId/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getByUserId/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getByUserId/{walletAddress}`

*Find All Collections by owner*

<h3 id="collectionscontroller_findallbyownerorcollaborator-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="collectionscontroller_findallbyownerorcollaborator-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns All Collections that have user either as owner or as collaborator|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collections do not exist|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_findAllCollectionOfUser

<a id="opIdCollectionsController_findAllCollectionOfUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getByWalletAddress?walletAddress=string

```

```http
GET /api/v1/collections/getByWalletAddress?walletAddress=string HTTP/1.1

```

```javascript

fetch('/api/v1/collections/getByWalletAddress?walletAddress=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/getByWalletAddress',
  params: {
  'walletAddress' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/getByWalletAddress', params={
  'walletAddress': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getByWalletAddress', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getByWalletAddress?walletAddress=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getByWalletAddress", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getByWalletAddress`

*Find All Collections by owner*

<h3 id="collectionscontroller_findallcollectionofuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|Number of items per page|
|skip|query|number|false|Skip items for page number|
|walletAddress|query|string|true|user wallet address creator of collection|
|search|query|string|false|search by collection name|
|nameOrder|query|string|false|none|
|dateOrder|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|nameOrder|ASC|
|nameOrder|DESC|
|dateOrder|ASC|
|dateOrder|DESC|

<h3 id="collectionscontroller_findallcollectionofuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns All Collections that user have created|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collections do not exist|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_findCollectionDetails

<a id="opIdCollectionsController_findCollectionDetails"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/{id}

```

```http
GET /api/v1/collections/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/{id}`

*Find one collection*

<h3 id="collectionscontroller_findcollectiondetails-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="collectionscontroller_findcollectiondetails-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Single Collection|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_deleteCollection

<a id="opIdCollectionsController_deleteCollection"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/collections/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/collections/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/collections/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/collections/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/collections/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/collections/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/collections/{id}`

*Soft deletes the Collection owned by user who is currenlty Logged In*

<h3 id="collectionscontroller_deletecollection-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="collectionscontroller_deletecollection-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection deleted|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|User does not own the collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_findOne

<a id="opIdCollectionsController_findOne"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/details/{id}

```

```http
GET /api/v1/collections/details/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/details/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/details/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/details/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/details/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/details/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/details/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/details/{id}`

*Find one collection*

<h3 id="collectionscontroller_findone-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="collectionscontroller_findone-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Single Collection|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_findByCategoryId

<a id="opIdCollectionsController_findByCategoryId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getByCategory/{categorySlug}

```

```http
GET /api/v1/collections/getByCategory/{categorySlug} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/getByCategory/{categorySlug}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/getByCategory/{categorySlug}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/getByCategory/{categorySlug}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getByCategory/{categorySlug}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getByCategory/{categorySlug}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getByCategory/{categorySlug}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getByCategory/{categorySlug}`

*Find collections based on category slug*

<h3 id="collectionscontroller_findbycategoryid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categorySlug|path|string|true|none|

<h3 id="collectionscontroller_findbycategoryid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collections based on category slug|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collections do not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_update

<a id="opIdCollectionsController_update"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/collections/update/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/collections/update/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/update/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/collections/update/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/collections/update/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/collections/update/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/update/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/collections/update/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/collections/update/{id}`

*Update Collection Details owned by user who is currenlty Logged In*

> Body parameter

```json
{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}
```

<h3 id="collectionscontroller_update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateCollectionsDto](#schemaupdatecollectionsdto)|true|none|

<h3 id="collectionscontroller_update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection Details|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Collection does not exist|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|User does not own the collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_getWatchCollections

<a id="opIdCollectionsController_getWatchCollections"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getFollowed/collections?walletAddress=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/collections/getFollowed/collections?walletAddress=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/getFollowed/collections?walletAddress=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/collections/getFollowed/collections',
  params: {
  'walletAddress' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/collections/getFollowed/collections', params={
  'walletAddress': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getFollowed/collections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getFollowed/collections?walletAddress=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getFollowed/collections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getFollowed/collections`

*Returns Current User Watchlist Collection*

<h3 id="collectionscontroller_getwatchcollections-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|time|query|string|false|none|
|categoryId|query|string|false|none|
|chainId|query|string|false|none|
|walletAddress|query|string|true|none|
|search|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|allTime|
|time|last24hours|
|time|last7days|
|time|last30days|

<h3 id="collectionscontroller_getwatchcollections-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Collections|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_watchlist

<a id="opIdCollectionsController_watchlist"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/watchlistFollowUnfollow \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/watchlistFollowUnfollow HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isWatched": true,
  "collectionId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/watchlistFollowUnfollow',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/watchlistFollowUnfollow',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/watchlistFollowUnfollow', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/watchlistFollowUnfollow', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/watchlistFollowUnfollow");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/watchlistFollowUnfollow", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/watchlistFollowUnfollow`

*Add and Removes user wallet address from watchlist of a collection*

> Body parameter

```json
{
  "isWatched": true,
  "collectionId": "string"
}
```

<h3 id="collectionscontroller_watchlist-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserWatchlistDto](#schemauserwatchlistdto)|true|none|

<h3 id="collectionscontroller_watchlist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User has been added in Watchlist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_updateCollaborator

<a id="opIdCollectionsController_updateCollaborator"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/collaborators \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/collaborators HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "collectionId": "string",
  "updateType": "string",
  "walletAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/collaborators',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/collaborators',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/collaborators', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/collaborators', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collaborators");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/collaborators", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/collaborators`

*Add and Removes user wallet address from Collaborators of a collection*

> Body parameter

```json
{
  "collectionId": "string",
  "updateType": "string",
  "walletAddress": "string"
}
```

<h3 id="collectionscontroller_updatecollaborator-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateCollaboratorDto](#schemaupdatecollaboratordto)|true|none|

<h3 id="collectionscontroller_updatecollaborator-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collaborator added|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_checkUniqueCollection

<a id="opIdCollectionsController_checkUniqueCollection"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/checkUniqueCollection \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/checkUniqueCollection HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/checkUniqueCollection',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/checkUniqueCollection',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/checkUniqueCollection', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/checkUniqueCollection', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/checkUniqueCollection");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/checkUniqueCollection", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/checkUniqueCollection`

*Boolean Values for Collection Name and Url*

<h3 id="collectionscontroller_checkuniquecollection-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|none|
|slug|query|string|false|none|

<h3 id="collectionscontroller_checkuniquecollection-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Boolean Values for Collection Name and url|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_findStatsByCollectionId

<a id="opIdCollectionsController_findStatsByCollectionId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/stats/{collectionId}

```

```http
GET /api/v1/collections/stats/{collectionId} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/stats/{collectionId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/stats/{collectionId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/stats/{collectionId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/stats/{collectionId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/stats/{collectionId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/stats/{collectionId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/stats/{collectionId}`

*Find collections stats for collectionId*

<h3 id="collectionscontroller_findstatsbycollectionid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|path|string|true|none|

<h3 id="collectionscontroller_findstatsbycollectionid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collections stats for collectionId|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_fetchRankings

<a id="opIdCollectionsController_fetchRankings"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collection/fetchRankings

```

```http
GET /api/v1/collections/collection/fetchRankings HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collection/fetchRankings',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collection/fetchRankings',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collection/fetchRankings')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collection/fetchRankings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collection/fetchRankings");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collection/fetchRankings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collection/fetchRankings`

<h3 id="collectionscontroller_fetchrankings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Time|query|string|false|none|
|categoryId|query|string|false|none|
|chainId|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|hasCashback|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|Time|allTime|
|Time|last24hours|
|Time|last7days|
|Time|last30days|

<h3 id="collectionscontroller_fetchrankings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_getTopCollections

<a id="opIdCollectionsController_getTopCollections"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collections/topCollections

```

```http
GET /api/v1/collections/collections/topCollections HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collections/topCollections',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collections/topCollections',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collections/topCollections')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collections/topCollections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collections/topCollections");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collections/topCollections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collections/topCollections`

*Find top collections*

<h3 id="collectionscontroller_gettopcollections-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|time|query|string|false|none|
|categoryId|query|string|false|none|
|chainId|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|allTime|
|time|last24hours|
|time|last7days|
|time|last30days|

<h3 id="collectionscontroller_gettopcollections-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Top Collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_findTrendingCollectionsForStats

<a id="opIdCollectionsController_findTrendingCollectionsForStats"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collections/trendingCollections

```

```http
GET /api/v1/collections/collections/trendingCollections HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collections/trendingCollections',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collections/trendingCollections',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collections/trendingCollections')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collections/trendingCollections', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collections/trendingCollections");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collections/trendingCollections", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collections/trendingCollections`

*Find trending collections*

<h3 id="collectionscontroller_findtrendingcollectionsforstats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categoryId|query|string|false|none|
|chainId|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="collectionscontroller_findtrendingcollectionsforstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Trending Collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_getCategoryByCategorySlug

<a id="opIdCollectionsController_getCategoryByCategorySlug"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/categorydetails/{categorySlug}

```

```http
GET /api/v1/collections/categorydetails/{categorySlug} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/categorydetails/{categorySlug}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/categorydetails/{categorySlug}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/categorydetails/{categorySlug}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/categorydetails/{categorySlug}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/categorydetails/{categorySlug}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/categorydetails/{categorySlug}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/categorydetails/{categorySlug}`

*Get Category Details*

<h3 id="collectionscontroller_getcategorybycategoryslug-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|categorySlug|path|string|true|none|

<h3 id="collectionscontroller_getcategorybycategoryslug-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Category Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_creatorEarning

<a id="opIdCollectionsController_creatorEarning"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/creatorEarning/{collectionSlugOrId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/collections/creatorEarning/{collectionSlugOrId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/creatorEarning/{collectionSlugOrId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/collections/creatorEarning/{collectionSlugOrId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/collections/creatorEarning/{collectionSlugOrId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/creatorEarning/{collectionSlugOrId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/creatorEarning/{collectionSlugOrId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/creatorEarning/{collectionSlugOrId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/creatorEarning/{collectionSlugOrId}`

*Find trending collections*

<h3 id="collectionscontroller_creatorearning-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionSlugOrId|path|string|true|none|

<h3 id="collectionscontroller_creatorearning-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Creator Earning|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_activityGraphCollection

<a id="opIdCollectionsController_activityGraphCollection"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collectionActivity/{collectionSlugOrId}

```

```http
GET /api/v1/collections/collectionActivity/{collectionSlugOrId} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collectionActivity/{collectionSlugOrId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collectionActivity/{collectionSlugOrId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collectionActivity/{collectionSlugOrId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collectionActivity/{collectionSlugOrId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collectionActivity/{collectionSlugOrId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collectionActivity/{collectionSlugOrId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collectionActivity/{collectionSlugOrId}`

*Collection Activity*

<h3 id="collectionscontroller_activitygraphcollection-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionSlugOrId|path|string|true|none|
|date|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|date|7|
|date|14|
|date|30|
|date|60|
|date|90|
|date|365|
|date|allTime|

<h3 id="collectionscontroller_activitygraphcollection-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection Activity Data|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_importFromContract

<a id="opIdCollectionsController_importFromContract"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/importContract/address?chainId=mumbai&contractAddress=string

```

```http
GET /api/v1/collections/importContract/address?chainId=mumbai&contractAddress=string HTTP/1.1

```

```javascript

fetch('/api/v1/collections/importContract/address?chainId=mumbai&contractAddress=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/importContract/address',
  params: {
  'chainId' => 'string',
'contractAddress' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/importContract/address', params={
  'chainId': 'mumbai',  'contractAddress': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/importContract/address', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/importContract/address?chainId=mumbai&contractAddress=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/importContract/address", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/importContract/address`

*To fetch collection from contract address*

<h3 id="collectionscontroller_importfromcontract-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|chainId|query|string|true|fetch items in collected or created|
|contractAddress|query|string|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|chainId|mumbai|
|chainId|eth|
|chainId|polygon|
|chainId|goerli|

<h3 id="collectionscontroller_importfromcontract-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_uniqueCollectionFromCollectedNft

<a id="opIdCollectionsController_uniqueCollectionFromCollectedNft"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}

```

```http
GET /api/v1/collections/collectionListfromCollectedItem/{userWalletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collectionListfromCollectedItem/{userWalletAddress}`

*List of collections from user collected items*

<h3 id="collectionscontroller_uniquecollectionfromcollectednft-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userWalletAddress|path|string|true|none|

<h3 id="collectionscontroller_uniquecollectionfromcollectednft-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_getCreatorEarnings

<a id="opIdCollectionsController_getCreatorEarnings"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collection/fetchCreatorEarnings?slug=string \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/collections/collection/fetchCreatorEarnings?slug=string HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/collection/fetchCreatorEarnings?slug=string',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/collections/collection/fetchCreatorEarnings',
  params: {
  'slug' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/collections/collection/fetchCreatorEarnings', params={
  'slug': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collection/fetchCreatorEarnings', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collection/fetchCreatorEarnings?slug=string");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collection/fetchCreatorEarnings", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collection/fetchCreatorEarnings`

<h3 id="collectionscontroller_getcreatorearnings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|slug|query|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="collectionscontroller_getcreatorearnings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_getNotableDrops

<a id="opIdCollectionsController_getNotableDrops"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/collection/fetchNotableDrops

```

```http
GET /api/v1/collections/collection/fetchNotableDrops HTTP/1.1

```

```javascript

fetch('/api/v1/collections/collection/fetchNotableDrops',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/collection/fetchNotableDrops',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/collection/fetchNotableDrops')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/collection/fetchNotableDrops', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/collection/fetchNotableDrops");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/collection/fetchNotableDrops", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/collection/fetchNotableDrops`

<h3 id="collectionscontroller_getnotabledrops-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="collectionscontroller_getnotabledrops-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Notable Drops|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_claimCreatorEarning

<a id="opIdCollectionsController_claimCreatorEarning"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/claimCreatorEarning/{collectionSlugOrId}/{tokenId}`

*Processes all pending creator earning transactions for a collection*

<h3 id="collectionscontroller_claimcreatorearning-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionSlugOrId|path|string|true|none|
|tokenId|path|string|true|none|

<h3 id="collectionscontroller_claimcreatorearning-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Processed Creator Earning|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_getCreatorEarningStats

<a id="opIdCollectionsController_getCreatorEarningStats"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/creatorEarningStats/{collectionSlugOrId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/collections/creatorEarningStats/{collectionSlugOrId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/creatorEarningStats/{collectionSlugOrId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/collections/creatorEarningStats/{collectionSlugOrId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/collections/creatorEarningStats/{collectionSlugOrId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/creatorEarningStats/{collectionSlugOrId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/creatorEarningStats/{collectionSlugOrId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/creatorEarningStats/{collectionSlugOrId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/creatorEarningStats/{collectionSlugOrId}`

*Fetches stats for creator earning of a collection*

<h3 id="collectionscontroller_getcreatorearningstats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionSlugOrId|path|string|true|none|

<h3 id="collectionscontroller_getcreatorearningstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Creator Earning Stats|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_favourites

<a id="opIdCollectionsController_favourites"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/collections/favourites \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/collections/favourites HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isFavourite": true,
  "collectionId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/collections/favourites',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/collections/favourites',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/collections/favourites', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/collections/favourites', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/favourites");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/collections/favourites", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/collections/favourites`

*Add and Removes user wallet address from favourites of a collection*

> Body parameter

```json
{
  "isFavourite": true,
  "collectionId": "string"
}
```

<h3 id="collectionscontroller_favourites-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CollectionFavouritesDto](#schemacollectionfavouritesdto)|true|none|

<h3 id="collectionscontroller_favourites-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User has been added in Favourites|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## CollectionsController_getFavouriteCollections

<a id="opIdCollectionsController_getFavouriteCollections"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getFavouriteCollection/{walletAddress}

```

```http
GET /api/v1/collections/getFavouriteCollection/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/getFavouriteCollection/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/getFavouriteCollection/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/getFavouriteCollection/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getFavouriteCollection/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getFavouriteCollection/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getFavouriteCollection/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getFavouriteCollection/{walletAddress}`

*Returns Current User favourite collection*

<h3 id="collectionscontroller_getfavouritecollections-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="collectionscontroller_getfavouritecollections-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## CollectionsController_getCollectionFavouritesCount

<a id="opIdCollectionsController_getCollectionFavouritesCount"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/collections/getCollectionFavouritesCount/{collectionId}

```

```http
GET /api/v1/collections/getCollectionFavouritesCount/{collectionId} HTTP/1.1

```

```javascript

fetch('/api/v1/collections/getCollectionFavouritesCount/{collectionId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/collections/getCollectionFavouritesCount/{collectionId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/collections/getCollectionFavouritesCount/{collectionId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/collections/getCollectionFavouritesCount/{collectionId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/collections/getCollectionFavouritesCount/{collectionId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/collections/getCollectionFavouritesCount/{collectionId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/collections/getCollectionFavouritesCount/{collectionId}`

*Returns Number of Favourites for a collection*

<h3 id="collectionscontroller_getcollectionfavouritescount-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|collectionId|path|string|true|none|

<h3 id="collectionscontroller_getcollectionfavouritescount-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection Favourite Count|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-offer-module">Offer Module</h1>

## OfferController_create

<a id="opIdOfferController_create"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/offer \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/offer HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "price": 0,
  "paymentToken": "string",
  "quantity": 0,
  "item": "string",
  "Expires": 0,
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/offer',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/offer', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/offer', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/offer", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/offer`

*Creates a new offer on an item by logged in user*

> Body parameter

```json
{
  "price": 0,
  "paymentToken": "string",
  "quantity": 0,
  "item": "string",
  "Expires": 0,
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}
```

<h3 id="offercontroller_create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateOfferDto](#schemacreateofferdto)|true|none|

<h3 id="offercontroller_create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Offer created|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Bad request for offer creation|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_update

<a id="opIdOfferController_update"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/offer/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/offer/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "price": 0,
  "paymentToken": "string",
  "Expires": 0,
  "quantity": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/offer/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/offer/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/offer/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/offer/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/offer/{id}`

*Update Offer Details on an item by user who is currenlty Logged In*

> Body parameter

```json
{
  "price": 0,
  "paymentToken": "string",
  "Expires": 0,
  "quantity": 0
}
```

<h3 id="offercontroller_update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateOfferDto](#schemaupdateofferdto)|true|none|

<h3 id="offercontroller_update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Offer Details|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Bad request for offer update|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_delete

<a id="opIdOfferController_delete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/offer/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/offer/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/offer/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/offer/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/offer/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/offer/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/offer/{id}`

*Api to delete an offer using id.*

<h3 id="offercontroller_delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="offercontroller_delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|User who sent the request doesnt own the offer|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_getOffers

<a id="opIdOfferController_getOffers"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/offer/getOffers

```

```http
GET /api/v1/offer/getOffers HTTP/1.1

```

```javascript

fetch('/api/v1/offer/getOffers',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/offer/getOffers',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/offer/getOffers')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/offer/getOffers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/getOffers");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/offer/getOffers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/offer/getOffers`

*Api to fetch offers based on current filter.*

<h3 id="offercontroller_getoffers-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|item|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="offercontroller_getoffers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Offer Details|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Offers do not exist|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## OfferController_getOffersByUser

<a id="opIdOfferController_getOffersByUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/offer/getOffersByUser?walletAddress=string&recievedOrSent=string

```

```http
GET /api/v1/offer/getOffersByUser?walletAddress=string&recievedOrSent=string HTTP/1.1

```

```javascript

fetch('/api/v1/offer/getOffersByUser?walletAddress=string&recievedOrSent=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/offer/getOffersByUser',
  params: {
  'walletAddress' => 'string',
'recievedOrSent' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/offer/getOffersByUser', params={
  'walletAddress': 'string',  'recievedOrSent': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/offer/getOffersByUser', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/getOffersByUser?walletAddress=string&recievedOrSent=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/offer/getOffersByUser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/offer/getOffersByUser`

*Api to fetch offers based on user sent and recieved.*

<h3 id="offercontroller_getoffersbyuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|query|string|true|none|
|recievedOrSent|query|string|true|none|
|collectionId|query|string|false|collectionId must be comma seperated|

<h3 id="offercontroller_getoffersbyuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Offer Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## OfferController_AcceptOffer

<a id="opIdOfferController_AcceptOffer"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/offer/acceptOffer \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/offer/acceptOffer HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "offerID": "string",
  "transactionHash": "string",
  "url": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/acceptOffer',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/offer/acceptOffer',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/offer/acceptOffer', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/offer/acceptOffer', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/acceptOffer");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/offer/acceptOffer", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/offer/acceptOffer`

> Body parameter

```json
{
  "offerID": "string",
  "transactionHash": "string",
  "url": "string"
}
```

<h3 id="offercontroller_acceptoffer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AcceptOfferDto](#schemaacceptofferdto)|true|none|

<h3 id="offercontroller_acceptoffer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_updateAuctionSignature

<a id="opIdOfferController_updateAuctionSignature"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/offer/updatesignature \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/offer/updatesignature HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "offerId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/updatesignature',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/offer/updatesignature',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/offer/updatesignature', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/offer/updatesignature', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/updatesignature");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/offer/updatesignature", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/offer/updatesignature`

*Update the Signature of Offer with given Offer Id*

> Body parameter

```json
{
  "offerId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}
```

<h3 id="offercontroller_updateauctionsignature-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateOfferSignatureDto](#schemacreateoffersignaturedto)|true|none|

<h3 id="offercontroller_updateauctionsignature-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Offer Signature has been updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_updateCollectionOfferPrice

<a id="opIdOfferController_updateCollectionOfferPrice"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/offer/updateCollectionOfferPrice \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/offer/updateCollectionOfferPrice HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "collectionsMinimumOfferPrice": [
    {
      "collectionId": "string",
      "price": 0
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/updateCollectionOfferPrice',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/offer/updateCollectionOfferPrice',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/offer/updateCollectionOfferPrice', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/offer/updateCollectionOfferPrice', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/updateCollectionOfferPrice");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/offer/updateCollectionOfferPrice", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/offer/updateCollectionOfferPrice`

*Update the OfferPrice of the Collection*

> Body parameter

```json
{
  "collectionsMinimumOfferPrice": [
    {
      "collectionId": "string",
      "price": 0
    }
  ]
}
```

<h3 id="offercontroller_updatecollectionofferprice-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateCollectionOfferPriceDto](#schemaupdatecollectionofferpricedto)|true|none|

<h3 id="offercontroller_updatecollectionofferprice-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Collection Offer Price Updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## OfferController_cancelAllOffers

<a id="opIdOfferController_cancelAllOffers"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/offer/cancelalloffers \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/offer/cancelalloffers HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/offer/cancelalloffers',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/offer/cancelalloffers',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/offer/cancelalloffers', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/offer/cancelalloffers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/offer/cancelalloffers");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/offer/cancelalloffers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/offer/cancelalloffers`

*Update the OfferPrice of the Collection*

<h3 id="offercontroller_cancelalloffers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Offers Cancelled|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-activity-module">Activity Module</h1>

## ActivityController_findAll

<a id="opIdActivityController_findAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity

```

```http
GET /api/v1/activity HTTP/1.1

```

```javascript

fetch('/api/v1/activity',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/activity',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/activity')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity`

*Find All Activities*

<h3 id="activitycontroller_findall-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|eventType|query|string|false|eventType must be comma seperated. Event Type: Listing, Sales, Bids, Transfers|
|collectionId|query|string|false|collectionId must be comma seperated|
|chain|query|string|false|chain must be comma seperated|
|time|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_findall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Activities|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Activities do not exist|None|

<aside class="success">
This operation does not require authentication
</aside>

## ActivityController_fetchActivities

<a id="opIdActivityController_fetchActivities"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/nft/{id}

```

```http
GET /api/v1/activity/nft/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/activity/nft/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/activity/nft/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/activity/nft/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/nft/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/nft/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/nft/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/nft/{id}`

*Find All Activities by pagination from view*

<h3 id="activitycontroller_fetchactivities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|eventType|query|string|false|eventType must be comma seperated. Event Type: Listing, Sales, Bids, Transfers|
|collectionId|query|string|false|collectionId must be comma seperated|
|chain|query|string|false|chain must be comma seperated|
|time|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_fetchactivities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Activities|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Activities do not exist|None|

<aside class="success">
This operation does not require authentication
</aside>

## ActivityController_findActivityByItemId

<a id="opIdActivityController_findActivityByItemId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/{id}

```

```http
GET /api/v1/activity/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/activity/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/activity/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/activity/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/{id}`

*Find activity for a partiular item*

<h3 id="activitycontroller_findactivitybyitemid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|eventType|query|string|false|eventType must be comma seperated. Event Type: Listing, Sales, Bids, Transfers|

<h3 id="activitycontroller_findactivitybyitemid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Item Activities|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## ActivityController_findActivitiesForUser

<a id="opIdActivityController_findActivitiesForUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/user/{walletAddress}

```

```http
GET /api/v1/activity/user/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/activity/user/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/activity/user/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/activity/user/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/user/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/user/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/user/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/user/{walletAddress}`

*Find activities for a partiular User*

<h3 id="activitycontroller_findactivitiesforuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|eventType|query|string|false|eventType must be comma seperated. Event Type: Listing, Sales, Bids, Transfers|
|collectionId|query|string|false|collectionId must be comma seperated|
|chain|query|string|false|chain must be comma seperated|
|time|query|string|false|none|
|walletAddress|path|string|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|1|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_findactivitiesforuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Activities|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## ActivityController_getAllActivityOfFollowedNft

<a id="opIdActivityController_getAllActivityOfFollowedNft"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/activity/getAllActivity/followedItems \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/activity/getAllActivity/followedItems HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/activity/getAllActivity/followedItems',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/activity/getAllActivity/followedItems',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/activity/getAllActivity/followedItems', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/activity/getAllActivity/followedItems', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/activity/getAllActivity/followedItems");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/activity/getAllActivity/followedItems", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/activity/getAllActivity/followedItems`

*Find All Activities of followed nfts*

<h3 id="activitycontroller_getallactivityoffollowednft-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|take|query|number|false|none|
|skip|query|number|false|none|
|eventType|query|string|false|eventType must be comma seperated. Event Type: Listing, Sales, Bids, Transfers|
|collectionId|query|string|false|collectionId must be comma seperated|
|chain|query|string|false|chain must be comma seperated|
|time|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|time|7|
|time|14|
|time|30|
|time|60|
|time|90|
|time|365|

<h3 id="activitycontroller_getallactivityoffollowednft-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Activities|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Activities do not exist|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-nft-item">Nft Item</h1>

## NftItemController_createNftItem

<a id="opIdNftItemController_createNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/nft-item/create \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/nft-item/create HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/create',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/nft-item/create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/nft-item/create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/nft-item/create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/create");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/nft-item/create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/nft-item/create`

*it will create new nft item*

> Body parameter

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}
```

<h3 id="nftitemcontroller_createnftitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateNftItemDto](#schemacreatenftitemdto)|true|none|

<h3 id="nftitemcontroller_createnftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft Created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_updateNFTFileUrl

<a id="opIdNftItemController_updateNFTFileUrl"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item

```

```http
PATCH /api/v1/nft-item HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item',
{
  method: 'PATCH'

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

result = RestClient.patch '/api/v1/nft-item',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.patch('/api/v1/nft-item')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item`

<h3 id="nftitemcontroller_updatenftfileurl-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_fetchNftItems

<a id="opIdNftItemController_fetchNftItems"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item?walletAddress=string&dataType=collected

```

```http
GET /api/v1/nft-item?walletAddress=string&dataType=collected HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item?walletAddress=string&dataType=collected',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item',
  params: {
  'walletAddress' => 'string',
'dataType' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item', params={
  'walletAddress': 'string',  'dataType': 'collected'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item?walletAddress=string&dataType=collected");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item`

*it will fetch nft item of a user with filters*

<h3 id="nftitemcontroller_fetchnftitems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|query|string|true|none|
|dataType|query|string|true|fetch items in collected or created|
|status|query|string|false|give single or multiple input from 'new', 'buynow', 'onAuction', 'hasOffer', 'hasCashback' seprated by ' , '|
|priceType|query|string|false|give price type eg. usd, eth, weth|
|priceRange|query|string|false|give price value range seprated by ' , '  eg.(1, 10) |
|collectionsId|query|string|false|give single collection id or multiple seprated by ' , '|
|chainsId|query|string|false|give single chain id or multiple seprated by ' , '|
|categories|query|string|false|give categories id|
|onSale|query|string|false|give single token id or multiple seprated by ' , '|
|isBundle|query|boolean|false|give a boolean value for whether the item is bundle or not(single item), true for bundle, false for single item|
|isOpenseaNft|query|boolean|false|give a boolean value for whether the item is from opensea|
|search|query|string|false|search by name of item|
|order|query|string|false|none|
|limit|query|number|false|no. of records per page|
|page|query|number|false|page no. to view|

#### Enumerated Values

|Parameter|Value|
|---|---|
|dataType|collected|
|dataType|created|
|priceType|usd|
|priceType|eth|
|priceType|weth|
|order|recentlyCreated|
|order|oldest|
|order|endingSoon|
|order|endDate|
|order|recentlyListed|
|order|HighestLastSale|
|order|priceH2L|
|order|priceL2H|
|order|recentlyReceived|
|order|mostFavourited|
|order|recentlySold|

<h3 id="nftitemcontroller_fetchnftitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft Fetch|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_updateNftItems

<a id="opIdNftItemController_updateNftItems"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/nft-item/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/nft-item/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/nft-item/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item/{id}`

*it will update nft item*

> Body parameter

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true
}
```

<h3 id="nftitemcontroller_updatenftitems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateNftItemDto](#schemaupdatenftitemdto)|true|none|

<h3 id="nftitemcontroller_updatenftitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft updated|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the item|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_favourites

<a id="opIdNftItemController_favourites"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/favourites \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/favourites HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "isFavourite": true,
  "itemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/favourites',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/favourites',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/favourites', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/favourites', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/favourites");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/favourites", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/favourites`

*Add and Removes user wallet address from favourites of a item*

> Body parameter

```json
{
  "isFavourite": true,
  "itemId": "string"
}
```

<h3 id="nftitemcontroller_favourites-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserFavouritesDto](#schemauserfavouritesdto)|true|none|

<h3 id="nftitemcontroller_favourites-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User has been added in Favourites|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getFavouriteItems

<a id="opIdNftItemController_getFavouriteItems"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getFavouriteItems/{walletAddress}

```

```http
GET /api/v1/nft-item/getFavouriteItems/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/getFavouriteItems/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/getFavouriteItems/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/getFavouriteItems/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getFavouriteItems/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getFavouriteItems/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getFavouriteItems/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getFavouriteItems/{walletAddress}`

*Returns Current User Watchlist Items*

<h3 id="nftitemcontroller_getfavouriteitems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|

<h3 id="nftitemcontroller_getfavouriteitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Items|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_getItemFavouritesCount

<a id="opIdNftItemController_getItemFavouritesCount"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getFavouriteItemsCount/{itemId}

```

```http
GET /api/v1/nft-item/getFavouriteItemsCount/{itemId} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/getFavouriteItemsCount/{itemId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/getFavouriteItemsCount/{itemId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/getFavouriteItemsCount/{itemId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getFavouriteItemsCount/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getFavouriteItemsCount/{itemId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getFavouriteItemsCount/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getFavouriteItemsCount/{itemId}`

*Returns Number of Favourites for an Item*

<h3 id="nftitemcontroller_getitemfavouritescount-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|path|string|true|none|

<h3 id="nftitemcontroller_getitemfavouritescount-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Items Favourite Count|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_hiddItem

<a id="opIdNftItemController_hiddItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/hideitem \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/hideitem HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "itemId": "string",
  "isHidden": true
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/hideitem',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/hideitem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/hideitem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/hideitem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/hideitem");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/hideitem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/hideitem`

*Add and Removes items from Users Hidden Items*

> Body parameter

```json
{
  "itemId": "string",
  "isHidden": true
}
```

<h3 id="nftitemcontroller_hidditem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[HideItemDto](#schemahideitemdto)|true|none|

<h3 id="nftitemcontroller_hidditem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Item has been Hidden|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getHiddenItems

<a id="opIdNftItemController_getHiddenItems"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getHiddenItems \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/nft-item/getHiddenItems HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/getHiddenItems',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/nft-item/getHiddenItems',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/nft-item/getHiddenItems', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getHiddenItems', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getHiddenItems");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getHiddenItems", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getHiddenItems`

*Returns Hidden Items for Current User*

<h3 id="nftitemcontroller_gethiddenitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Items|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_fatchNftItemByID

<a id="opIdNftItemController_fatchNftItemByID"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getNftItemByID/{id}

```

```http
GET /api/v1/nft-item/getNftItemByID/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/getNftItemByID/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/getNftItemByID/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/getNftItemByID/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getNftItemByID/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getNftItemByID/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getNftItemByID/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getNftItemByID/{id}`

<h3 id="nftitemcontroller_fatchnftitembyid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_fatchnftitembyid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET ITEM DATA BY ITEM ID|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_fatchNftItemByTokenID

<a id="opIdNftItemController_fatchNftItemByTokenID"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getNftItemByTokenID/{tokenId}

```

```http
GET /api/v1/nft-item/getNftItemByTokenID/{tokenId} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/getNftItemByTokenID/{tokenId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/getNftItemByTokenID/{tokenId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/getNftItemByTokenID/{tokenId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getNftItemByTokenID/{tokenId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getNftItemByTokenID/{tokenId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getNftItemByTokenID/{tokenId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getNftItemByTokenID/{tokenId}`

*it will fetch nft item with given tokenId*

<h3 id="nftitemcontroller_fatchnftitembytokenid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tokenId|path|string|true|none|

<h3 id="nftitemcontroller_fatchnftitembytokenid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET ITEM DATA BY ITEM TokenID|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_updateViewerCount

<a id="opIdNftItemController_updateViewerCount"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/updateViewer/{id}

```

```http
PUT /api/v1/nft-item/updateViewer/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/updateViewer/{id}',
{
  method: 'PUT'

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

result = RestClient.put '/api/v1/nft-item/updateViewer/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.put('/api/v1/nft-item/updateViewer/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/updateViewer/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/updateViewer/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/updateViewer/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/updateViewer/{id}`

<h3 id="nftitemcontroller_updateviewercount-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_updateviewercount-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update VIEWER COUNT on a  ITEM|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_findAllItemExceptOne

<a id="opIdNftItemController_findAllItemExceptOne"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/fetchFromCollection/{id}

```

```http
GET /api/v1/nft-item/fetchFromCollection/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/fetchFromCollection/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/fetchFromCollection/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/fetchFromCollection/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/fetchFromCollection/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/fetchFromCollection/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/fetchFromCollection/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/fetchFromCollection/{id}`

*it will fetch nft item from a collection except one*

<h3 id="nftitemcontroller_findallitemexceptone-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="nftitemcontroller_findallitemexceptone-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft Fetch all from a collection|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_findAllItemExceptOneForSpecificUser

<a id="opIdNftItemController_findAllItemExceptOneForSpecificUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/fetchFromCollectionForUser/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/nft-item/fetchFromCollectionForUser/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/fetchFromCollectionForUser/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/nft-item/fetchFromCollectionForUser/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/nft-item/fetchFromCollectionForUser/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/fetchFromCollectionForUser/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/fetchFromCollectionForUser/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/fetchFromCollectionForUser/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/fetchFromCollectionForUser/{id}`

*it will fetch nft item from a collection except one*

<h3 id="nftitemcontroller_findallitemexceptoneforspecificuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_findallitemexceptoneforspecificuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft Fetch all from a collection|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_deleteItem

<a id="opIdNftItemController_deleteItem"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/nft-item/delete/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/nft-item/delete/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/delete/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/nft-item/delete/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/nft-item/delete/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/nft-item/delete/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/delete/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/nft-item/delete/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/nft-item/delete/{id}`

*it will delete nft item*

<h3 id="nftitemcontroller_deleteitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_deleteitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Item is deleted|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the item|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_transferItem

<a id="opIdNftItemController_transferItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item/transfer/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/nft-item/transfer/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "userWalletAddress": "string",
  "supply": 0,
  "hash": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/transfer/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/nft-item/transfer/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/nft-item/transfer/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item/transfer/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/transfer/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item/transfer/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item/transfer/{id}`

*it will transfer nft item*

> Body parameter

```json
{
  "userWalletAddress": "string",
  "supply": 0,
  "hash": "string"
}
```

<h3 id="nftitemcontroller_transferitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[TransferItemDto](#schematransferitemdto)|true|none|

<h3 id="nftitemcontroller_transferitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Item transfered|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|User does not own the item|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_buyItem

<a id="opIdNftItemController_buyItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/buyItem \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/buyItem HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "auctionId": "string",
  "soldPrice": 0,
  "itemId": "string",
  "transactionHash": "string",
  "transactionUrl": "string",
  "isDirectPurchase": false
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/buyItem',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/buyItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/buyItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/buyItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/buyItem");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/buyItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/buyItem`

*Use this api to directly buy a auction that is under fixed price or reserved buyer auction type.*

> Body parameter

```json
{
  "auctionId": "string",
  "soldPrice": 0,
  "itemId": "string",
  "transactionHash": "string",
  "transactionUrl": "string",
  "isDirectPurchase": false
}
```

<h3 id="nftitemcontroller_buyitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[BuyItemDto](#schemabuyitemdto)|true|none|

<h3 id="nftitemcontroller_buyitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Item Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getPurchasedNftItem

<a id="opIdNftItemController_getPurchasedNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getpurchasednftitem \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/nft-item/getpurchasednftitem HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/getpurchasednftitem',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/nft-item/getpurchasednftitem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/nft-item/getpurchasednftitem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getpurchasednftitem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getpurchasednftitem");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getpurchasednftitem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getpurchasednftitem`

*it will fetch purchased nft item details*

<h3 id="nftitemcontroller_getpurchasednftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_updatePurchasedNftItem

<a id="opIdNftItemController_updatePurchasedNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item/updatepurchasednftitem/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/nft-item/updatepurchasednftitem/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/updatepurchasednftitem/{id}',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/nft-item/updatepurchasednftitem/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/nft-item/updatepurchasednftitem/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item/updatepurchasednftitem/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/updatepurchasednftitem/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item/updatepurchasednftitem/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item/updatepurchasednftitem/{id}`

*it will update purchased nft item details*

<h3 id="nftitemcontroller_updatepurchasednftitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_updatepurchasednftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getAllItems1

<a id="opIdNftItemController_getAllItems1"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/allItems

```

```http
GET /api/v1/nft-item/allItems HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/allItems',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/allItems',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/allItems')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/allItems', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/allItems");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/allItems", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/allItems`

*it will fetch nft items according to filters*

<h3 id="nftitemcontroller_getallitems1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|status|query|string|false|give single or multiple input from 'new', 'buynow', 'onAuction', 'hasOffer', 'hasCashback' seprated by ' , '|
|priceType|query|string|false|give price type eg. usd, eth, weth|
|priceRange|query|string|false|give price value range separated by ' , '  eg.(1, 10) |
|paymentTokens|query|string|false|give patmentToken  separated by ' , '  eg.(Eth, MATIC) |
|collectionsId|query|string|false|give single collection id or multiple separated by ' , '|
|onSale|query|string|false|give single token id or multiple seprated by ' , '|
|chainsId|query|string|false|give single chain id or multiple separated by ' , '|
|categories|query|string|false|give single categoryId id or multiple separated by |
|isBundle|query|boolean|false|none|
|isOpenseaNft|query|boolean|false|none|
|search|query|string|false|search by name of item|
|order|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|propertyType|query|string|false|none|
|PropertyName|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|priceType|usd|
|priceType|eth|
|priceType|weth|
|order|recentlyCreated|
|order|oldest|
|order|endingSoon|
|order|endDate|
|order|recentlyListed|
|order|HighestLastSale|
|order|priceH2L|
|order|priceL2H|
|order|recentlyReceived|
|order|mostFavourited|
|order|recentlySold|

<h3 id="nftitemcontroller_getallitems1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Nft Fetch all from a collection|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_getAllNFTs

<a id="opIdNftItemController_getAllNFTs"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/allNFTs

```

```http
GET /api/v1/nft-item/allNFTs HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/allNFTs',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/allNFTs',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/allNFTs')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/allNFTs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/allNFTs");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/allNFTs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/allNFTs`

*it will fetch nft items according to filters*

<h3 id="nftitemcontroller_getallnfts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|status|query|string|false|give single or multiple input from 'new', 'buynow', 'onAuction', 'hasOffer', 'hasCashback' seprated by ' , '|
|priceType|query|string|false|give price type eg. usd, eth, weth|
|priceRange|query|string|false|give price value range separated by ' , '  eg.(1, 10) |
|paymentTokens|query|string|false|give patmentToken  separated by ' , '  eg.(Eth, MATIC) |
|collectionsId|query|string|false|give single collection id or multiple separated by ' , '|
|onSale|query|string|false|give single token id or multiple seprated by ' , '|
|chainsId|query|string|false|give single chain id or multiple separated by ' , '|
|categories|query|string|false|give single categoryId id or multiple separated by |
|isBundle|query|boolean|false|none|
|isOpenseaNft|query|boolean|false|none|
|search|query|string|false|search by name of item|
|order|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|
|propertyType|query|string|false|none|
|PropertyName|query|string|false|none|
|fromDate|query|number|false|none|
|toDate|query|number|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|priceType|usd|
|priceType|eth|
|priceType|weth|
|order|recentlyCreated|
|order|oldest|
|order|endingSoon|
|order|endDate|
|order|recentlyListed|
|order|HighestLastSale|
|order|priceH2L|
|order|priceL2H|
|order|recentlyReceived|
|order|mostFavourited|
|order|recentlySold|

<h3 id="nftitemcontroller_getallnfts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|NFT Item Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_getPricesForItem

<a id="opIdNftItemController_getPricesForItem"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/priceHistory/{id}?id=string

```

```http
GET /api/v1/nft-item/priceHistory/{id}?id=string HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/priceHistory/{id}?id=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/priceHistory/{id}',
  params: {
  'id' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/priceHistory/{id}', params={
  'id': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/priceHistory/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/priceHistory/{id}?id=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/priceHistory/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/priceHistory/{id}`

*it will fetch all auctions for an item*

<h3 id="nftitemcontroller_getpricesforitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|string|true|none|
|time|query|string|false|none|

<h3 id="nftitemcontroller_getpricesforitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|fetch all auctions for an item|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_pinNftItem

<a id="opIdNftItemController_pinNftItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item/pinNftItem/{nftItemId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/nft-item/pinNftItem/{nftItemId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/pinNftItem/{nftItemId}',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/nft-item/pinNftItem/{nftItemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/nft-item/pinNftItem/{nftItemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item/pinNftItem/{nftItemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/pinNftItem/{nftItemId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item/pinNftItem/{nftItemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item/pinNftItem/{nftItemId}`

<h3 id="nftitemcontroller_pinnftitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|nftItemId|path|string|true|none|

<h3 id="nftitemcontroller_pinnftitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_updateFreezeItem

<a id="opIdNftItemController_updateFreezeItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/nft-item/updateFreezeItem/{nftItemId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/nft-item/updateFreezeItem/{nftItemId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/updateFreezeItem/{nftItemId}',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/nft-item/updateFreezeItem/{nftItemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/nft-item/updateFreezeItem/{nftItemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/nft-item/updateFreezeItem/{nftItemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/updateFreezeItem/{nftItemId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/nft-item/updateFreezeItem/{nftItemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/nft-item/updateFreezeItem/{nftItemId}`

<h3 id="nftitemcontroller_updatefreezeitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|nftItemId|path|string|true|none|

<h3 id="nftitemcontroller_updatefreezeitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_freezeMetadata

<a id="opIdNftItemController_freezeMetadata"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/freezeMetadata \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/freezeMetadata HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "itemId": "string",
  "nftItemUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/freezeMetadata',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/freezeMetadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/freezeMetadata', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/freezeMetadata', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/freezeMetadata");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/freezeMetadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/freezeMetadata`

> Body parameter

```json
{
  "itemId": "string",
  "nftItemUrl": "string"
}
```

<h3 id="nftitemcontroller_freezemetadata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FreezeMetaDataDto](#schemafreezemetadatadto)|true|none|

<h3 id="nftitemcontroller_freezemetadata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_metadata

<a id="opIdNftItemController_metadata"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/metadata?itemId=string

```

```http
GET /api/v1/nft-item/metadata?itemId=string HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/metadata?itemId=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/metadata',
  params: {
  'itemId' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/metadata', params={
  'itemId': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/metadata', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/metadata?itemId=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/metadata`

<h3 id="nftitemcontroller_metadata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|query|string|true|A parameter itemId|

<h3 id="nftitemcontroller_metadata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_CreateBatchNftItems

<a id="opIdNftItemController_CreateBatchNftItems"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/nft-item/createBatchNftItem \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/nft-item/createBatchNftItem HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "fileUrl": [
    "string"
  ],
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/createBatchNftItem',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/nft-item/createBatchNftItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/nft-item/createBatchNftItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/nft-item/createBatchNftItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/createBatchNftItem");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/nft-item/createBatchNftItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/nft-item/createBatchNftItem`

*it will create a batch of new nft item*

> Body parameter

```json
{
  "fileUrl": [
    "string"
  ],
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}
```

<h3 id="nftitemcontroller_createbatchnftitems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateBatchNftDto](#schemacreatebatchnftdto)|true|none|

<h3 id="nftitemcontroller_createbatchnftitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getUnlockableContent

<a id="opIdNftItemController_getUnlockableContent"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getUnlockableContent/{nftItemId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/nft-item/getUnlockableContent/{nftItemId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/getUnlockableContent/{nftItemId}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/nft-item/getUnlockableContent/{nftItemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/nft-item/getUnlockableContent/{nftItemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getUnlockableContent/{nftItemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getUnlockableContent/{nftItemId}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getUnlockableContent/{nftItemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getUnlockableContent/{nftItemId}`

<h3 id="nftitemcontroller_getunlockablecontent-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|nftItemId|path|string|true|none|

<h3 id="nftitemcontroller_getunlockablecontent-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET UNLOCKABLE DATA|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_fatchNftItemByTokenIDChainIdContractAddress

<a id="opIdNftItemController_fatchNftItemByTokenIDChainIdContractAddress"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}

```

```http
GET /api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/assets/{chain}/{contractAddress}/{tokenId}`

*it will fetch nft item with given tokenId, contract address and ChainId*

<h3 id="nftitemcontroller_fatchnftitembytokenidchainidcontractaddress-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tokenId|path|string|true|none|
|chain|path|string|true|none|
|contractAddress|path|string|true|none|

<h3 id="nftitemcontroller_fatchnftitembytokenidchainidcontractaddress-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET ITEM DATA BY ITEM TokenID|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_fatchNftItemStandardFormat

<a id="opIdNftItemController_fatchNftItemStandardFormat"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}

```

```http
GET /api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/asset/{chain}/{contractAddress}/{tokenId}`

*it will fetch nft item with given tokenId, contract address and ChainId*

<h3 id="nftitemcontroller_fatchnftitemstandardformat-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|tokenId|path|string|true|none|
|chain|path|string|true|none|
|contractAddress|path|string|true|none|

<h3 id="nftitemcontroller_fatchnftitemstandardformat-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GET ITEM DATA BY ITEM TokenID|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_updateAuctionsAndOffersStatusForNFT

<a id="opIdNftItemController_updateAuctionsAndOffersStatusForNFT"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/updatenftstatus/{id}

```

```http
GET /api/v1/nft-item/updatenftstatus/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/updatenftstatus/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/updatenftstatus/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/updatenftstatus/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/updatenftstatus/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/updatenftstatus/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/updatenftstatus/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/updatenftstatus/{id}`

*It will update the auction and offer status of a NFT*

<h3 id="nftitemcontroller_updateauctionsandoffersstatusfornft-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="nftitemcontroller_updateauctionsandoffersstatusfornft-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OnAuction and HasOffers Status Updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_trackPurchaseDropOff

<a id="opIdNftItemController_trackPurchaseDropOff"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/nft-item/purchaseDropoff \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/nft-item/purchaseDropoff HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "nftId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/purchaseDropoff',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/nft-item/purchaseDropoff',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/nft-item/purchaseDropoff', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/nft-item/purchaseDropoff', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/purchaseDropoff");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/nft-item/purchaseDropoff", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/nft-item/purchaseDropoff`

*It is used to track the purchase drop off event*

> Body parameter

```json
{
  "nftId": "string"
}
```

<h3 id="nftitemcontroller_trackpurchasedropoff-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PurchaseDropOff](#schemapurchasedropoff)|true|none|

<h3 id="nftitemcontroller_trackpurchasedropoff-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Event tracked successfully|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_trackPurchase

<a id="opIdNftItemController_trackPurchase"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/trackpurchase?itemid=string

```

```http
GET /api/v1/nft-item/trackpurchase?itemid=string HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/trackpurchase?itemid=string',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/trackpurchase',
  params: {
  'itemid' => 'string'
}

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/trackpurchase', params={
  'itemid': 'string'
})

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/trackpurchase', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/trackpurchase?itemid=string");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/trackpurchase", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/trackpurchase`

*It is used to check whether that nft is purchased by particular user or not*

<h3 id="nftitemcontroller_trackpurchase-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemid|query|string|true|none|

<h3 id="nftitemcontroller_trackpurchase-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Event tracked successfully|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## NftItemController_followUnfollowNft

<a id="opIdNftItemController_followUnfollowNft"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/nft-item/followUnfollowNft \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/nft-item/followUnfollowNft HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "toFollow": true,
  "itemId": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/nft-item/followUnfollowNft',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/nft-item/followUnfollowNft',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/nft-item/followUnfollowNft', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/nft-item/followUnfollowNft', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/followUnfollowNft");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/nft-item/followUnfollowNft", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/nft-item/followUnfollowNft`

*Add and Removes user wallet address from followNFTS of a item*

> Body parameter

```json
{
  "toFollow": true,
  "itemId": "string"
}
```

<h3 id="nftitemcontroller_followunfollownft-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FollowUnfollowDto](#schemafollowunfollowdto)|true|none|

<h3 id="nftitemcontroller_followunfollownft-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|NFT followed|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## NftItemController_getFollowNFTsList

<a id="opIdNftItemController_getFollowNFTsList"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/nft-item/getFollowNFTsList/{walletAddress}

```

```http
GET /api/v1/nft-item/getFollowNFTsList/{walletAddress} HTTP/1.1

```

```javascript

fetch('/api/v1/nft-item/getFollowNFTsList/{walletAddress}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/nft-item/getFollowNFTsList/{walletAddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/nft-item/getFollowNFTsList/{walletAddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/nft-item/getFollowNFTsList/{walletAddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/nft-item/getFollowNFTsList/{walletAddress}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/nft-item/getFollowNFTsList/{walletAddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/nft-item/getFollowNFTsList/{walletAddress}`

*Returns Current User followed Items*

<h3 id="nftitemcontroller_getfollownftslist-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|
|search|query|string|false|none|
|take|query|number|false|none|
|skip|query|number|false|none|

<h3 id="nftitemcontroller_getfollownftslist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of Items|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-auctions-module">Auctions Module</h1>

## AuctionsController_createAuction

<a id="opIdAuctionsController_createAuction"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/auctions/create \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/auctions/create HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "auction_item": "string",
  "bundle_items": [
    "string"
  ],
  "auction_collection": "string",
  "startDate": 0,
  "endDate": 0,
  "tokens": "string",
  "auctionType": "string",
  "bundle": {
    "isBundle": true,
    "name": "string",
    "description": "string"
  },
  "reservedAuction": {
    "isReservedAuction": true,
    "walletAddress": "string"
  },
  "quantity": 0,
  "startingPrice": 0,
  "endingPrice": 0,
  "reservedPrice": 0,
  "timedAuctionMethod": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/create',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/auctions/create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/auctions/create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/auctions/create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/create");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/auctions/create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/auctions/create`

*Create new Auctions*

> Body parameter

```json
{
  "auction_item": "string",
  "bundle_items": [
    "string"
  ],
  "auction_collection": "string",
  "startDate": 0,
  "endDate": 0,
  "tokens": "string",
  "auctionType": "string",
  "bundle": {
    "isBundle": true,
    "name": "string",
    "description": "string"
  },
  "reservedAuction": {
    "isReservedAuction": true,
    "walletAddress": "string"
  },
  "quantity": 0,
  "startingPrice": 0,
  "endingPrice": 0,
  "reservedPrice": 0,
  "timedAuctionMethod": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}
```

<h3 id="auctionscontroller_createauction-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateAuctionDto](#schemacreateauctiondto)|true|none|

<h3 id="auctionscontroller_createauction-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_getAuctionsByUserId

<a id="opIdAuctionsController_getAuctionsByUserId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/auctions/user/{walletAddress}/{isActive}

```

```http
GET /api/v1/auctions/user/{walletAddress}/{isActive} HTTP/1.1

```

```javascript

fetch('/api/v1/auctions/user/{walletAddress}/{isActive}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/auctions/user/{walletAddress}/{isActive}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/auctions/user/{walletAddress}/{isActive}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/auctions/user/{walletAddress}/{isActive}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/user/{walletAddress}/{isActive}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/auctions/user/{walletAddress}/{isActive}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/auctions/user/{walletAddress}/{isActive}`

*Get Auctions By User Id*

<h3 id="auctionscontroller_getauctionsbyuserid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|walletAddress|path|string|true|none|
|isActive|path|boolean|true|none|
|collectionId|query|string|false|collectionId must be comma seperated|

<h3 id="auctionscontroller_getauctionsbyuserid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## AuctionsController_getAuctionDetailsByAuctionId

<a id="opIdAuctionsController_getAuctionDetailsByAuctionId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/auctions/details/{auctionId}

```

```http
GET /api/v1/auctions/details/{auctionId} HTTP/1.1

```

```javascript

fetch('/api/v1/auctions/details/{auctionId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/auctions/details/{auctionId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/auctions/details/{auctionId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/auctions/details/{auctionId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/details/{auctionId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/auctions/details/{auctionId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/auctions/details/{auctionId}`

*Get Auctions Details By Auction Id*

<h3 id="auctionscontroller_getauctiondetailsbyauctionid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|auctionId|path|string|true|none|

<h3 id="auctionscontroller_getauctiondetailsbyauctionid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## AuctionsController_getListingByItemId

<a id="opIdAuctionsController_getListingByItemId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/auctions/item/{itemId}

```

```http
GET /api/v1/auctions/item/{itemId} HTTP/1.1

```

```javascript

fetch('/api/v1/auctions/item/{itemId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/auctions/item/{itemId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/auctions/item/{itemId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/auctions/item/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/item/{itemId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/auctions/item/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/auctions/item/{itemId}`

*Get Auctions Details By Item Id*

<h3 id="auctionscontroller_getlistingbyitemid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|path|string|true|none|

<h3 id="auctionscontroller_getlistingbyitemid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## AuctionsController_getActiveListingByItemId

<a id="opIdAuctionsController_getActiveListingByItemId"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/auctions/activelisting/{itemId}

```

```http
GET /api/v1/auctions/activelisting/{itemId} HTTP/1.1

```

```javascript

fetch('/api/v1/auctions/activelisting/{itemId}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/auctions/activelisting/{itemId}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/auctions/activelisting/{itemId}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/auctions/activelisting/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/activelisting/{itemId}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/auctions/activelisting/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/auctions/activelisting/{itemId}`

*Get Active Auctions Details By Item Id*

<h3 id="auctionscontroller_getactivelistingbyitemid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|path|string|true|none|

<h3 id="auctionscontroller_getactivelistingbyitemid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## AuctionsController_cancelListing

<a id="opIdAuctionsController_cancelListing"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/auctions/cancel \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/auctions/cancel HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "auctionId": "string",
  "transactionHash": "string",
  "transactionUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/cancel',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/auctions/cancel',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/auctions/cancel', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/auctions/cancel', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/cancel");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/auctions/cancel", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/auctions/cancel`

*Cancel the Listing*

> Body parameter

```json
{
  "auctionId": "string",
  "transactionHash": "string",
  "transactionUrl": "string"
}
```

<h3 id="auctionscontroller_cancellisting-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CancelAuctionDto](#schemacancelauctiondto)|true|none|

<h3 id="auctionscontroller_cancellisting-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_cancelAllListingOfItem

<a id="opIdAuctionsController_cancelAllListingOfItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/auctions/cancelalllistings/{itemId} \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/auctions/cancelalllistings/{itemId} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/cancelalllistings/{itemId}',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/auctions/cancelalllistings/{itemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/auctions/cancelalllistings/{itemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/auctions/cancelalllistings/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/cancelalllistings/{itemId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/auctions/cancelalllistings/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/auctions/cancelalllistings/{itemId}`

*Cancel the Listing*

<h3 id="auctionscontroller_cancelalllistingofitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|path|string|true|none|

<h3 id="auctionscontroller_cancelalllistingofitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_updatePriceAndExpirationDate

<a id="opIdAuctionsController_updatePriceAndExpirationDate"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/auctions/update \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/auctions/update HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "auctionId": "string",
  "endDate": 0,
  "price": 0,
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/update',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/auctions/update',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/auctions/update', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/auctions/update', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/update");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/auctions/update", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/auctions/update`

*Update the Auction Price and Expiration Date*

> Body parameter

```json
{
  "auctionId": "string",
  "endDate": 0,
  "price": 0,
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}
```

<h3 id="auctionscontroller_updatepriceandexpirationdate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateAuctionDto](#schemaupdateauctiondto)|true|none|

<h3 id="auctionscontroller_updatepriceandexpirationdate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Details|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_updateAuctionSignature

<a id="opIdAuctionsController_updateAuctionSignature"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/auctions/updatesignature \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/auctions/updatesignature HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/updatesignature',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/auctions/updatesignature',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/auctions/updatesignature', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/auctions/updatesignature', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/updatesignature");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/auctions/updatesignature", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/auctions/updatesignature`

*Update the Signature of Auction with given Auction Id*

> Body parameter

```json
{
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}
```

<h3 id="auctionscontroller_updateauctionsignature-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateSignatureDto](#schemacreatesignaturedto)|true|none|

<h3 id="auctionscontroller_updateauctionsignature-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auction Signature has been updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_cancelAllListing

<a id="opIdAuctionsController_cancelAllListing"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/auctions/cancelalllisting \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/auctions/cancelalllisting HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/cancelalllisting',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/auctions/cancelalllisting',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/auctions/cancelalllisting', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/auctions/cancelalllisting', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/cancelalllisting");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/auctions/cancelalllisting", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/auctions/cancelalllisting`

*Cancel all the listing of the user*

<h3 id="auctionscontroller_cancelalllisting-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Auctions Listings Cancelled|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_updateHighestBid

<a id="opIdAuctionsController_updateHighestBid"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/auctions/updatehighestbid \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/auctions/updatehighestbid HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": [
    "string"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/updatehighestbid',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/auctions/updatehighestbid',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/auctions/updatehighestbid', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/auctions/updatehighestbid', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/updatehighestbid");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/auctions/updatehighestbid", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/auctions/updatehighestbid`

*Update the Highest Bid isViewed field*

> Body parameter

```json
{
  "id": [
    "string"
  ]
}
```

<h3 id="auctionscontroller_updatehighestbid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateHighestBidDto](#schemaupdatehighestbiddto)|true|none|

<h3 id="auctionscontroller_updatehighestbid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Highest Bidder Details Updated|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## AuctionsController_getHighestBid

<a id="opIdAuctionsController_getHighestBid"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/auctions/highestbids \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/auctions/highestbids HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/auctions/highestbids',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/auctions/highestbids',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/auctions/highestbids', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/auctions/highestbids', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/auctions/highestbids");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/auctions/highestbids", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/auctions/highestbids`

*Get Highest Bids of the user*

<h3 id="auctionscontroller_gethighestbid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-report">Report</h1>

## ReportController_report

<a id="opIdReportController_report"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/report \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/report HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "message": "string",
  "originalCreatorUrl": "string",
  "reason": "string",
  "reportType": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/report',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/report',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/report', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/report', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/report");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/report", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/report`

*logged in user can report user, item and collection*

> Body parameter

```json
{
  "id": "string",
  "message": "string",
  "originalCreatorUrl": "string",
  "reason": "string",
  "reportType": 0
}
```

<h3 id="reportcontroller_report-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ReportDto](#schemareportdto)|true|none|

<h3 id="reportcontroller_report-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|request successfully reported|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|user have already reported this|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-help-centre">help-centre</h1>

## HelpCentreController_CreateAboutUs

<a id="opIdHelpCentreController_CreateAboutUs"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/help-centre/createAboutUs \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/help-centre/createAboutUs HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "description": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/createAboutUs',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/help-centre/createAboutUs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/help-centre/createAboutUs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/help-centre/createAboutUs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/createAboutUs");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/help-centre/createAboutUs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/help-centre/createAboutUs`

*it will create about us description*

> Body parameter

```json
{
  "description": "string"
}
```

<h3 id="helpcentrecontroller_createaboutus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AboutUsDto](#schemaaboutusdto)|true|none|

<h3 id="helpcentrecontroller_createaboutus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_CreateTermCondition

<a id="opIdHelpCentreController_CreateTermCondition"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/help-centre/createTermCondition \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/help-centre/createTermCondition HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "termCondition": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/createTermCondition',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/help-centre/createTermCondition',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/help-centre/createTermCondition', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/help-centre/createTermCondition', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/createTermCondition");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/help-centre/createTermCondition", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/help-centre/createTermCondition`

*it will create term and conditions by admin*

> Body parameter

```json
{
  "termCondition": "string"
}
```

<h3 id="helpcentrecontroller_createtermcondition-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TermConditionDto](#schematermconditiondto)|true|none|

<h3 id="helpcentrecontroller_createtermcondition-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_getTermCondition

<a id="opIdHelpCentreController_getTermCondition"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/help-centre/getTermCondition

```

```http
GET /api/v1/help-centre/getTermCondition HTTP/1.1

```

```javascript

fetch('/api/v1/help-centre/getTermCondition',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/help-centre/getTermCondition',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/help-centre/getTermCondition')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/help-centre/getTermCondition', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/getTermCondition");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/help-centre/getTermCondition", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/help-centre/getTermCondition`

*it will fatch term and conditions by admin*

<h3 id="helpcentrecontroller_gettermcondition-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## HelpCentreController_updateTermCondition

<a id="opIdHelpCentreController_updateTermCondition"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/help-centre/updateTermCondition \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/help-centre/updateTermCondition HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "termCondition": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/updateTermCondition',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/help-centre/updateTermCondition',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/help-centre/updateTermCondition', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/help-centre/updateTermCondition', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/updateTermCondition");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/help-centre/updateTermCondition", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/help-centre/updateTermCondition`

*it will update term and conditions*

> Body parameter

```json
{
  "termCondition": "string"
}
```

<h3 id="helpcentrecontroller_updatetermcondition-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TermConditionDto](#schematermconditiondto)|true|none|

<h3 id="helpcentrecontroller_updatetermcondition-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_CreateFrequentlyQuestion

<a id="opIdHelpCentreController_CreateFrequentlyQuestion"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/help-centre/createFQ \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/help-centre/createFQ HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "question": "string",
  "answer": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/createFQ',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/help-centre/createFQ',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/help-centre/createFQ', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/help-centre/createFQ', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/createFQ");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/help-centre/createFQ", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/help-centre/createFQ`

*it will create frequently asked question*

> Body parameter

```json
{
  "question": "string",
  "answer": "string"
}
```

<h3 id="helpcentrecontroller_createfrequentlyquestion-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FandQDto](#schemafandqdto)|true|none|

<h3 id="helpcentrecontroller_createfrequentlyquestion-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_getAboutUs

<a id="opIdHelpCentreController_getAboutUs"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/help-centre/getAboutUs

```

```http
GET /api/v1/help-centre/getAboutUs HTTP/1.1

```

```javascript

fetch('/api/v1/help-centre/getAboutUs',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/help-centre/getAboutUs',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/help-centre/getAboutUs')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/help-centre/getAboutUs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/getAboutUs");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/help-centre/getAboutUs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/help-centre/getAboutUs`

*it will fatch aboutUs*

<h3 id="helpcentrecontroller_getaboutus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## HelpCentreController_updateAboutUs

<a id="opIdHelpCentreController_updateAboutUs"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/help-centre/updateAboutUs \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/help-centre/updateAboutUs HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "description": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/updateAboutUs',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/help-centre/updateAboutUs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/help-centre/updateAboutUs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/help-centre/updateAboutUs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/updateAboutUs");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/help-centre/updateAboutUs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/help-centre/updateAboutUs`

*it will update about Us by admin*

> Body parameter

```json
{
  "description": "string"
}
```

<h3 id="helpcentrecontroller_updateaboutus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AboutUsDto](#schemaaboutusdto)|true|none|

<h3 id="helpcentrecontroller_updateaboutus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_getFrequentlyQuestion

<a id="opIdHelpCentreController_getFrequentlyQuestion"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/help-centre/getFrequentlyQuestion

```

```http
GET /api/v1/help-centre/getFrequentlyQuestion HTTP/1.1

```

```javascript

fetch('/api/v1/help-centre/getFrequentlyQuestion',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/help-centre/getFrequentlyQuestion',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/help-centre/getFrequentlyQuestion')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/help-centre/getFrequentlyQuestion', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/getFrequentlyQuestion");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/help-centre/getFrequentlyQuestion", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/help-centre/getFrequentlyQuestion`

*it will fatch F&Q*

<h3 id="helpcentrecontroller_getfrequentlyquestion-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="success">
This operation does not require authentication
</aside>

## HelpCentreController_updateFrequentlyQuestion

<a id="opIdHelpCentreController_updateFrequentlyQuestion"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /api/v1/help-centre/updateFrequentlyQuestion \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PUT /api/v1/help-centre/updateFrequentlyQuestion HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "id": "string",
  "question": "string",
  "answer": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/updateFrequentlyQuestion',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put '/api/v1/help-centre/updateFrequentlyQuestion',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('/api/v1/help-centre/updateFrequentlyQuestion', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/api/v1/help-centre/updateFrequentlyQuestion', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/updateFrequentlyQuestion");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/api/v1/help-centre/updateFrequentlyQuestion", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v1/help-centre/updateFrequentlyQuestion`

*it will update F & Q by admin*

> Body parameter

```json
{
  "id": "string",
  "question": "string",
  "answer": "string"
}
```

<h3 id="helpcentrecontroller_updatefrequentlyquestion-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UpdateFandQDto](#schemaupdatefandqdto)|true|none|

<h3 id="helpcentrecontroller_updatefrequentlyquestion-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Token Details|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_deleteFrequentlyQuestion

<a id="opIdHelpCentreController_deleteFrequentlyQuestion"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/help-centre/deleteFAQs \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/help-centre/deleteFAQs HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = 'string';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/deleteFAQs',
{
  method: 'DELETE',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/help-centre/deleteFAQs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/help-centre/deleteFAQs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/help-centre/deleteFAQs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/deleteFAQs");
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
        "Content-Type": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/help-centre/deleteFAQs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/help-centre/deleteFAQs`

*it will delete FAQs by admin*

> Body parameter

```json
"string"
```

<h3 id="helpcentrecontroller_deletefrequentlyquestion-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|string|true|none|

<h3 id="helpcentrecontroller_deletefrequentlyquestion-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_deleteAboutUs

<a id="opIdHelpCentreController_deleteAboutUs"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/help-centre/deleteAboutUs \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/help-centre/deleteAboutUs HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = 'string';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/deleteAboutUs',
{
  method: 'DELETE',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/help-centre/deleteAboutUs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/help-centre/deleteAboutUs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/help-centre/deleteAboutUs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/deleteAboutUs");
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
        "Content-Type": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/help-centre/deleteAboutUs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/help-centre/deleteAboutUs`

*it will delete AboutUs by admin*

> Body parameter

```json
"string"
```

<h3 id="helpcentrecontroller_deleteaboutus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|string|true|none|

<h3 id="helpcentrecontroller_deleteaboutus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_deleteTermsAndConditions

<a id="opIdHelpCentreController_deleteTermsAndConditions"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/help-centre/deleteT&Cs \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/help-centre/deleteT&Cs HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = 'string';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/deleteT&Cs',
{
  method: 'DELETE',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/help-centre/deleteT&Cs',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/help-centre/deleteT&Cs', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/help-centre/deleteT&Cs', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/deleteT&Cs");
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
        "Content-Type": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/help-centre/deleteT&Cs", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/help-centre/deleteT&Cs`

*it will delete T&Cs by admin*

> Body parameter

```json
"string"
```

<h3 id="helpcentrecontroller_deletetermsandconditions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|string|true|none|

<h3 id="helpcentrecontroller_deletetermsandconditions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_deletePrivacy

<a id="opIdHelpCentreController_deletePrivacy"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/help-centre/deletePrivacy/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/help-centre/deletePrivacy/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/deletePrivacy/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/help-centre/deletePrivacy/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/help-centre/deletePrivacy/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/help-centre/deletePrivacy/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/deletePrivacy/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/help-centre/deletePrivacy/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/help-centre/deletePrivacy/{id}`

*it will delete privacy by admin*

<h3 id="helpcentrecontroller_deleteprivacy-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="helpcentrecontroller_deleteprivacy-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## HelpCentreController_getPrivacy

<a id="opIdHelpCentreController_getPrivacy"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/help-centre/getPrivacy

```

```http
GET /api/v1/help-centre/getPrivacy HTTP/1.1

```

```javascript

fetch('/api/v1/help-centre/getPrivacy',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/help-centre/getPrivacy',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/help-centre/getPrivacy')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/help-centre/getPrivacy', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/getPrivacy");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/help-centre/getPrivacy", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/help-centre/getPrivacy`

*it will get privacy by admin*

<h3 id="helpcentrecontroller_getprivacy-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## HelpCentreController_createUpdatePrivacy

<a id="opIdHelpCentreController_createUpdatePrivacy"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/help-centre/createOrUpdatePrivacy \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/help-centre/createOrUpdatePrivacy HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "privacyPolicy": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/help-centre/createOrUpdatePrivacy',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/help-centre/createOrUpdatePrivacy',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/help-centre/createOrUpdatePrivacy', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/help-centre/createOrUpdatePrivacy', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/help-centre/createOrUpdatePrivacy");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/help-centre/createOrUpdatePrivacy", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/help-centre/createOrUpdatePrivacy`

*it will create/update privacy by admin*

> Body parameter

```json
{
  "privacyPolicy": "string"
}
```

<h3 id="helpcentrecontroller_createupdateprivacy-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PrivacyDto](#schemaprivacydto)|true|none|

<h3 id="helpcentrecontroller_createupdateprivacy-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

<h1 id="jungle-nft-marketplace-kyc">KYC</h1>

## KycController_createSession

<a id="opIdKycController_createSession"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/kyc/create_session \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/kyc/create_session HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "request_data": "string",
  "user_data": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/kyc/create_session',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/kyc/create_session',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/kyc/create_session', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/kyc/create_session', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/kyc/create_session");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/kyc/create_session", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/kyc/create_session`

*it will return the kyc url*

> Body parameter

```json
{
  "request_data": "string",
  "user_data": "string"
}
```

<h3 id="kyccontroller_createsession-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[KycSessionDto](#schemakycsessiondto)|true|none|

<h3 id="kyccontroller_createsession-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Kyc Session Generated Succssfully|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## KycController_fetchKycStatus

<a id="opIdKycController_fetchKycStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/kyc/kyc_status \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/kyc/kyc_status HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/kyc/kyc_status',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/kyc/kyc_status',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/kyc/kyc_status', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/kyc/kyc_status', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/kyc/kyc_status");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/kyc/kyc_status", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/kyc/kyc_status`

*it will return the kyc status of the user kyc status*

<h3 id="kyccontroller_fetchkycstatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Fetched kyc status|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## KycController_cancelKyc

<a id="opIdKycController_cancelKyc"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/kyc/cancel_kyc \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/kyc/cancel_kyc HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/kyc/cancel_kyc',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/kyc/cancel_kyc',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/kyc/cancel_kyc', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/kyc/cancel_kyc', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/kyc/cancel_kyc");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/kyc/cancel_kyc", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/kyc/cancel_kyc`

*it will remove the kyc verification*

<h3 id="kyccontroller_cancelkyc-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Kyc cancelled successfully|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## KycController_updateSessionStatus

<a id="opIdKycController_updateSessionStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/kyc/update_session/{kyc_id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/kyc/update_session/{kyc_id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/kyc/update_session/{kyc_id}',
{
  method: 'PATCH',

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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/kyc/update_session/{kyc_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/kyc/update_session/{kyc_id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/kyc/update_session/{kyc_id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/kyc/update_session/{kyc_id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/kyc/update_session/{kyc_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/kyc/update_session/{kyc_id}`

*it will update the kyc session status*

<h3 id="kyccontroller_updatesessionstatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|session updated successfully|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## KycController_clearKyc

<a id="opIdKycController_clearKyc"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/kyc/clear_kyc/{walletaddress}

```

```http
PATCH /api/v1/kyc/clear_kyc/{walletaddress} HTTP/1.1

```

```javascript

fetch('/api/v1/kyc/clear_kyc/{walletaddress}',
{
  method: 'PATCH'

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

result = RestClient.patch '/api/v1/kyc/clear_kyc/{walletaddress}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.patch('/api/v1/kyc/clear_kyc/{walletaddress}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/kyc/clear_kyc/{walletaddress}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/kyc/clear_kyc/{walletaddress}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/kyc/clear_kyc/{walletaddress}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/kyc/clear_kyc/{walletaddress}`

<h3 id="kyccontroller_clearkyc-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-health">Health</h1>

## HealthController_check

<a id="opIdHealthController_check"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/healthcheck/db \
  -H 'Accept: application/json'

```

```http
GET /api/v1/healthcheck/db HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/api/v1/healthcheck/db',
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

result = RestClient.get '/api/v1/healthcheck/db',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/api/v1/healthcheck/db', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/healthcheck/db', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/healthcheck/db");
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
    req, err := http.NewRequest("GET", "/api/v1/healthcheck/db", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/healthcheck/db`

> Example responses

> 200 Response

```json
{
  "status": "ok",
  "info": {
    "database": {
      "status": "up"
    }
  },
  "error": {},
  "details": {
    "database": {
      "status": "up"
    }
  }
}
```

<h3 id="healthcontroller_check-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|The Health Check is successful|Inline|
|503|[Service Unavailable](https://tools.ietf.org/html/rfc7231#section-6.6.4)|The Health Check is not successful|Inline|

<h3 id="healthcontroller_check-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» status|string|false|none|none|
|» info|object¦null|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|
|» error|object¦null|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|
|» details|object|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|

Status Code **503**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» status|string|false|none|none|
|» info|object¦null|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|
|» error|object¦null|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|
|» details|object|false|none|none|
|»» **additionalProperties**|object|false|none|none|
|»»» **additionalProperties**|string|false|none|none|
|»»» status|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="jungle-nft-marketplace-status">status</h1>

## StatusController_create

<a id="opIdStatusController_create"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /api/v1/status/create \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST /api/v1/status/create HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "content": "string",
  "version": 0,
  "isActive": true,
  "status": "general",
  "imageUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/status/create',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post '/api/v1/status/create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('/api/v1/status/create', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/api/v1/status/create', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/create");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/api/v1/status/create", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/status/create`

*it will create about us description*

> Body parameter

```json
{
  "content": "string",
  "version": 0,
  "isActive": true,
  "status": "general",
  "imageUrl": "string"
}
```

<h3 id="statuscontroller_create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateStatusDto](#schemacreatestatusdto)|true|none|

<h3 id="statuscontroller_create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|status created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## StatusController_findAll

<a id="opIdStatusController_findAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/status/getAllStatusByAdmin \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/status/getAllStatusByAdmin HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/status/getAllStatusByAdmin',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/status/getAllStatusByAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/status/getAllStatusByAdmin', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/status/getAllStatusByAdmin', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/getAllStatusByAdmin");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/status/getAllStatusByAdmin", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/status/getAllStatusByAdmin`

*it will get all status description*

<h3 id="statuscontroller_findall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## StatusController_findOne

<a id="opIdStatusController_findOne"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/status/getStatusById/{id}

```

```http
GET /api/v1/status/getStatusById/{id} HTTP/1.1

```

```javascript

fetch('/api/v1/status/getStatusById/{id}',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/status/getStatusById/{id}',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/status/getStatusById/{id}')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/status/getStatusById/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/getStatusById/{id}");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/status/getStatusById/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/status/getStatusById/{id}`

*it will get status description*

<h3 id="statuscontroller_findone-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="statuscontroller_findone-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## StatusController_update

<a id="opIdStatusController_update"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH /api/v1/status/updateStatus/{id} \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
PATCH /api/v1/status/updateStatus/{id} HTTP/1.1

Content-Type: application/json

```

```javascript
const inputBody = '{
  "content": "string",
  "version": 0,
  "isActive": true,
  "imageUrl": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/status/updateStatus/{id}',
{
  method: 'PATCH',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.patch '/api/v1/status/updateStatus/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.patch('/api/v1/status/updateStatus/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PATCH','/api/v1/status/updateStatus/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/updateStatus/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "/api/v1/status/updateStatus/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v1/status/updateStatus/{id}`

*it will update status description*

> Body parameter

```json
{
  "content": "string",
  "version": 0,
  "isActive": true,
  "imageUrl": "string"
}
```

<h3 id="statuscontroller_update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[UpdateStatusDto](#schemaupdatestatusdto)|true|none|

<h3 id="statuscontroller_update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|status created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## StatusController_remove

<a id="opIdStatusController_remove"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /api/v1/status/deleteStatus/{id} \
  -H 'Authorization: Bearer {access-token}'

```

```http
DELETE /api/v1/status/deleteStatus/{id} HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/status/deleteStatus/{id}',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete '/api/v1/status/deleteStatus/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('/api/v1/status/deleteStatus/{id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/api/v1/status/deleteStatus/{id}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/deleteStatus/{id}");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/api/v1/status/deleteStatus/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v1/status/deleteStatus/{id}`

*it will delete status description*

<h3 id="statuscontroller_remove-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

<h3 id="statuscontroller_remove-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|status created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

## StatusController_findAllForUsers

<a id="opIdStatusController_findAllForUsers"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/status/findAllStatusForUsers

```

```http
GET /api/v1/status/findAllStatusForUsers HTTP/1.1

```

```javascript

fetch('/api/v1/status/findAllStatusForUsers',
{
  method: 'GET'

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

result = RestClient.get '/api/v1/status/findAllStatusForUsers',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/api/v1/status/findAllStatusForUsers')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/status/findAllStatusForUsers', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/findAllStatusForUsers");
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

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/status/findAllStatusForUsers", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/status/findAllStatusForUsers`

*it will get all status description*

<h3 id="statuscontroller_findallforusers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## StatusController_fetchGiveAwayStatus

<a id="opIdStatusController_fetchGiveAwayStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /api/v1/status/giveaway \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET /api/v1/status/giveaway HTTP/1.1

```

```javascript

const headers = {
  'Authorization':'Bearer {access-token}'
};

fetch('/api/v1/status/giveaway',
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
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get '/api/v1/status/giveaway',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('/api/v1/status/giveaway', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Authorization' => 'Bearer {access-token}',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/api/v1/status/giveaway', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/api/v1/status/giveaway");
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
        "Authorization": []string{"Bearer {access-token}"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/api/v1/status/giveaway", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v1/status/giveaway`

*it will fetch the giveaway status*

<h3 id="statuscontroller_fetchgiveawaystatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|status created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad request|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal Server Error|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
bearer
</aside>

# Schemas

<h2 id="tocS_CreateUserLoginDto">CreateUserLoginDto</h2>
<!-- backwards compatibility -->
<a id="schemacreateuserlogindto"></a>
<a id="schema_CreateUserLoginDto"></a>
<a id="tocScreateuserlogindto"></a>
<a id="tocscreateuserlogindto"></a>

```json
{
  "walletAddress": "string",
  "signature": "string",
  "signature_message": "string",
  "loginWallet": "string",
  "referralSource": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|walletAddress|string|true|none|none|
|signature|string|true|none|none|
|signature_message|string|true|none|none|
|loginWallet|string|true|none|none|
|referralSource|string|true|none|none|

<h2 id="tocS_UpdateUserDto">UpdateUserDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdateuserdto"></a>
<a id="schema_UpdateUserDto"></a>
<a id="tocSupdateuserdto"></a>
<a id="tocsupdateuserdto"></a>

```json
{
  "firstName": "string",
  "lastName": "string",
  "userName": "string",
  "email": "string",
  "imageUrl": "string",
  "bannerUrl": "string",
  "bio": "string",
  "twitterHandle": "string",
  "instagramHandle": "string",
  "website": "string",
  "instagramToken": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|userName|string|true|none|none|
|email|string|true|none|none|
|imageUrl|string|false|none|none|
|bannerUrl|string|false|none|none|
|bio|string|false|none|none|
|twitterHandle|string|false|none|none|
|instagramHandle|string|false|none|none|
|website|string|false|none|none|
|instagramToken|string|false|none|none|

<h2 id="tocS_SignedUrlDto">SignedUrlDto</h2>
<!-- backwards compatibility -->
<a id="schemasignedurldto"></a>
<a id="schema_SignedUrlDto"></a>
<a id="tocSsignedurldto"></a>
<a id="tocssignedurldto"></a>

```json
{
  "fileName": "string",
  "fileType": "string",
  "filePath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fileName|string|true|none|none|
|fileType|string|true|none|none|
|filePath|string|true|none|none|

<h2 id="tocS_FeesPaidDto">FeesPaidDto</h2>
<!-- backwards compatibility -->
<a id="schemafeespaiddto"></a>
<a id="schema_FeesPaidDto"></a>
<a id="tocSfeespaiddto"></a>
<a id="tocsfeespaiddto"></a>

```json
{
  "isOneTimeFees": true,
  "oneTimeFees": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isOneTimeFees|boolean|true|none|none|
|oneTimeFees|string|true|none|none|

<h2 id="tocS_SubscribeNewsletterDto">SubscribeNewsletterDto</h2>
<!-- backwards compatibility -->
<a id="schemasubscribenewsletterdto"></a>
<a id="schema_SubscribeNewsletterDto"></a>
<a id="tocSsubscribenewsletterdto"></a>
<a id="tocssubscribenewsletterdto"></a>

```json
{
  "userEmail": "abc@gmail.com"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userEmail|string|true|none|none|

<h2 id="tocS_BlockUserDto">BlockUserDto</h2>
<!-- backwards compatibility -->
<a id="schemablockuserdto"></a>
<a id="schema_BlockUserDto"></a>
<a id="tocSblockuserdto"></a>
<a id="tocsblockuserdto"></a>

```json
{
  "walletAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|walletAddress|string|true|none|none|

<h2 id="tocS_UsersWalletAddressDto">UsersWalletAddressDto</h2>
<!-- backwards compatibility -->
<a id="schemauserswalletaddressdto"></a>
<a id="schema_UsersWalletAddressDto"></a>
<a id="tocSuserswalletaddressdto"></a>
<a id="tocsuserswalletaddressdto"></a>

```json
{
  "walletAddress": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|walletAddress|[string]|true|none|none|

<h2 id="tocS_FollowUser">FollowUser</h2>
<!-- backwards compatibility -->
<a id="schemafollowuser"></a>
<a id="schema_FollowUser"></a>
<a id="tocSfollowuser"></a>
<a id="tocsfollowuser"></a>

```json
{
  "toFollow": "string",
  "status": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|toFollow|string|true|none|none|
|status|boolean|true|none|none|

<h2 id="tocS_CreatorFavouritesDto">CreatorFavouritesDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatorfavouritesdto"></a>
<a id="schema_CreatorFavouritesDto"></a>
<a id="tocScreatorfavouritesdto"></a>
<a id="tocscreatorfavouritesdto"></a>

```json
{
  "isFavourite": true,
  "creatorWalletAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isFavourite|boolean|true|none|none|
|creatorWalletAddress|string|true|none|none|

<h2 id="tocS_LoginAdminDto">LoginAdminDto</h2>
<!-- backwards compatibility -->
<a id="schemaloginadmindto"></a>
<a id="schema_LoginAdminDto"></a>
<a id="tocSloginadmindto"></a>
<a id="tocsloginadmindto"></a>

```json
{
  "username": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|username|string|true|none|Email of user|
|password|string|true|none|Password of user|

<h2 id="tocS_CreateAdminDto">CreateAdminDto</h2>
<!-- backwards compatibility -->
<a id="schemacreateadmindto"></a>
<a id="schema_CreateAdminDto"></a>
<a id="tocScreateadmindto"></a>
<a id="tocscreateadmindto"></a>

```json
{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|firstName|string|true|none|firstname of user|
|lastName|string|true|none|lastname of user|
|username|string|true|none|Email of user|
|password|string|true|none|Password user wants provide|

<h2 id="tocS_UpdateAdminDto">UpdateAdminDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdateadmindto"></a>
<a id="schema_UpdateAdminDto"></a>
<a id="tocSupdateadmindto"></a>
<a id="tocsupdateadmindto"></a>

```json
{
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|firstName|string|true|none|firstname of user|
|lastName|string|true|none|lastname of user|
|username|string|true|none|Email of user|
|password|string|true|none|Password user wants provide|

<h2 id="tocS_Admin">Admin</h2>
<!-- backwards compatibility -->
<a id="schemaadmin"></a>
<a id="schema_Admin"></a>
<a id="tocSadmin"></a>
<a id="tocsadmin"></a>

```json
{
  "id": "string",
  "firstName": "string",
  "lastName": "string",
  "username": "string",
  "password": "string",
  "active": true,
  "createdAt": "2019-08-24T14:15:22Z",
  "updatedAt": "2019-08-24T14:15:22Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|none|
|firstName|string|true|none|none|
|lastName|string|true|none|none|
|username|string|true|none|none|
|password|string|true|none|none|
|active|boolean|true|none|none|
|createdAt|string(date-time)|true|none|none|
|updatedAt|string(date-time)|true|none|none|

<h2 id="tocS_CreateCategoryDto">CreateCategoryDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatecategorydto"></a>
<a id="schema_CreateCategoryDto"></a>
<a id="tocScreatecategorydto"></a>
<a id="tocscreatecategorydto"></a>

```json
{
  "categoryName": "string",
  "categoryImageUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|categoryName|string|true|none|New category name to be created|
|categoryImageUrl|string|true|none|category pic url|

<h2 id="tocS_UpdateCategoryDto">UpdateCategoryDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecategorydto"></a>
<a id="schema_UpdateCategoryDto"></a>
<a id="tocSupdatecategorydto"></a>
<a id="tocsupdatecategorydto"></a>

```json
{
  "categoryName": "string",
  "categoryImageUrl": "string",
  "categoryStatus": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|categoryName|string|true|none|New category name to be created|
|categoryImageUrl|string|true|none|category pic url|
|categoryStatus|boolean|true|none|none|

<h2 id="tocS_ExecuteMetaTrasactionDto">ExecuteMetaTrasactionDto</h2>
<!-- backwards compatibility -->
<a id="schemaexecutemetatrasactiondto"></a>
<a id="schema_ExecuteMetaTrasactionDto"></a>
<a id="tocSexecutemetatrasactiondto"></a>
<a id="tocsexecutemetatrasactiondto"></a>

```json
{
  "contractAddress": "string",
  "userAddress": "string",
  "functionSignature": "string",
  "sigR": "string",
  "sigS": "string",
  "sigV": "string",
  "value": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractAddress|string|true|none|none|
|userAddress|string|true|none|none|
|functionSignature|string|true|none|Encoded function abi and params|
|sigR|string|true|none|Signature parameters after signature from user|
|sigS|string|true|none|Signature parameters after signature from user|
|sigV|string|true|none|Signature parameters after signature from user|
|value|number|true|none|Ether amount if any|

<h2 id="tocS_UserBlockDto">UserBlockDto</h2>
<!-- backwards compatibility -->
<a id="schemauserblockdto"></a>
<a id="schema_UserBlockDto"></a>
<a id="tocSuserblockdto"></a>
<a id="tocsuserblockdto"></a>

```json
{
  "isBlocked": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isBlocked|boolean|true|none|Boolean value for isBlocked|

<h2 id="tocS_CashbackPlatformFeeDTO">CashbackPlatformFeeDTO</h2>
<!-- backwards compatibility -->
<a id="schemacashbackplatformfeedto"></a>
<a id="schema_CashbackPlatformFeeDTO"></a>
<a id="tocScashbackplatformfeedto"></a>
<a id="tocscashbackplatformfeedto"></a>

```json
{
  "platformfee": 0,
  "cashback": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|platformfee|number|true|none|none|
|cashback|number|true|none|none|

<h2 id="tocS_UserBanDto">UserBanDto</h2>
<!-- backwards compatibility -->
<a id="schemauserbandto"></a>
<a id="schema_UserBanDto"></a>
<a id="tocSuserbandto"></a>
<a id="tocsuserbandto"></a>

```json
{
  "isBanned": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isBanned|boolean|true|none|Boolean value for isBanned|

<h2 id="tocS_Properties">Properties</h2>
<!-- backwards compatibility -->
<a id="schemaproperties"></a>
<a id="schema_Properties"></a>
<a id="tocSproperties"></a>
<a id="tocsproperties"></a>

```json
{
  "type": "string",
  "name": "string",
  "percentage": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|none|
|name|string|true|none|none|
|percentage|number|true|none|none|

<h2 id="tocS_Levels">Levels</h2>
<!-- backwards compatibility -->
<a id="schemalevels"></a>
<a id="schema_Levels"></a>
<a id="tocSlevels"></a>
<a id="tocslevels"></a>

```json
{
  "name": "string",
  "value": 0,
  "maxValue": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|value|number|true|none|none|
|maxValue|number|true|none|none|

<h2 id="tocS_ItemStats">ItemStats</h2>
<!-- backwards compatibility -->
<a id="schemaitemstats"></a>
<a id="schema_ItemStats"></a>
<a id="tocSitemstats"></a>
<a id="tocsitemstats"></a>

```json
{
  "name": "string",
  "value": 0,
  "maxValue": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|value|number|true|none|none|
|maxValue|number|true|none|none|

<h2 id="tocS_CreateNftItemDto">CreateNftItemDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatenftitemdto"></a>
<a id="schema_CreateNftItemDto"></a>
<a id="tocScreatenftitemdto"></a>
<a id="tocscreatenftitemdto"></a>

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fileUrl|string|true|none|none|
|fileName|string|true|none|none|
|externalUrl|string|false|none|none|
|previewImage|string|false|none|none|
|description|string|false|none|none|
|collectionId|string|false|none|none|
|properties|[[Properties](#schemaproperties)]|false|none|properties|
|levels|[[Levels](#schemalevels)]|false|none|Levels|
|stats|[[ItemStats](#schemaitemstats)]|false|none|Stats|
|isLockable|boolean|false|none|none|
|lockableContent|string|false|none|none|
|isExplicit|boolean|false|none|none|
|supply|number|false|none|none|
|blockChainId|string|true|none|none|
|contractAddress|string|false|none|none|

<h2 id="tocS_UpdateNftItemDto">UpdateNftItemDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatenftitemdto"></a>
<a id="schema_UpdateNftItemDto"></a>
<a id="tocSupdatenftitemdto"></a>
<a id="tocsupdatenftitemdto"></a>

```json
{
  "fileUrl": "string",
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fileUrl|string|true|none|none|
|fileName|string|true|none|none|
|externalUrl|string|false|none|none|
|previewImage|string|false|none|none|
|description|string|false|none|none|
|collectionId|string|true|none|none|
|properties|[[Properties](#schemaproperties)]|false|none|properties|
|levels|[[Levels](#schemalevels)]|false|none|Levels|
|stats|[[ItemStats](#schemaitemstats)]|false|none|Stats|
|isLockable|boolean|false|none|none|
|lockableContent|string|false|none|none|
|isExplicit|boolean|false|none|none|

<h2 id="tocS_CreateCollectionsDto">CreateCollectionsDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatecollectionsdto"></a>
<a id="schema_CreateCollectionsDto"></a>
<a id="tocScreatecollectionsdto"></a>
<a id="tocscreatecollectionsdto"></a>

```json
{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "blockchain": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|logo|string|true|none|Logo for the collection|
|featureImage|string|false|none|Feature image for collection|
|banner|string|false|none|Banner for collection|
|name|string|true|none|Name of collection|
|slug|string|false|none|slug for this collection|
|description|string|false|none|Description about collection|
|categoryId|string|false|none|Category for this collection|
|websiteLink|string|false|none|Url of website|
|discordLink|string|false|none|Discord Link|
|instagramLink|string|false|none|Instagram Link|
|mediumLink|string|false|none|Medium Link|
|telegramLink|string|false|none|Telegram Link|
|earningFee|number|false|none|Earning fee for Creator|
|earningWalletAddress|string|false|none|Earning wallet address for the collection|
|blockchain|string|false|none|blockchain being used for this collection|
|paymentToken|[string]|false|none|Payment Token being used for this collection|
|displayTheme|string|false|none|Display Theme for collection|
|explicitOrSensitiveContent|boolean|false|none|Whether information is explicit or sensitive|

<h2 id="tocS_UserVerifyDto">UserVerifyDto</h2>
<!-- backwards compatibility -->
<a id="schemauserverifydto"></a>
<a id="schema_UserVerifyDto"></a>
<a id="tocSuserverifydto"></a>
<a id="tocsuserverifydto"></a>

```json
{
  "verifiedUser": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|verifiedUser|boolean|true|none|Boolean value for verifieduser|

<h2 id="tocS_CollectionVerifyDto">CollectionVerifyDto</h2>
<!-- backwards compatibility -->
<a id="schemacollectionverifydto"></a>
<a id="schema_CollectionVerifyDto"></a>
<a id="tocScollectionverifydto"></a>
<a id="tocscollectionverifydto"></a>

```json
{
  "isVerified": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isVerified|boolean|true|none|Boolean value for isVerified|

<h2 id="tocS_NotableDrop">NotableDrop</h2>
<!-- backwards compatibility -->
<a id="schemanotabledrop"></a>
<a id="schema_NotableDrop"></a>
<a id="tocSnotabledrop"></a>
<a id="tocsnotabledrop"></a>

```json
{
  "isNotableDrop": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isNotableDrop|boolean|true|none|Boolean value for isNotableDrop|

<h2 id="tocS_KycVerificationDto">KycVerificationDto</h2>
<!-- backwards compatibility -->
<a id="schemakycverificationdto"></a>
<a id="schema_KycVerificationDto"></a>
<a id="tocSkycverificationdto"></a>
<a id="tocskycverificationdto"></a>

```json
{
  "status": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|boolean|true|none|none|

<h2 id="tocS_SetChargesDto">SetChargesDto</h2>
<!-- backwards compatibility -->
<a id="schemasetchargesdto"></a>
<a id="schema_SetChargesDto"></a>
<a id="tocSsetchargesdto"></a>
<a id="tocssetchargesdto"></a>

```json
{
  "id": "string",
  "extraCharges": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|Chain Id|
|extraCharges|string|true|none|Extra charges|

<h2 id="tocS_PlatformFeesDto">PlatformFeesDto</h2>
<!-- backwards compatibility -->
<a id="schemaplatformfeesdto"></a>
<a id="schema_PlatformFeesDto"></a>
<a id="tocSplatformfeesdto"></a>
<a id="tocsplatformfeesdto"></a>

```json
{
  "id": "string",
  "platformFees": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|Chain Id|
|platformFees|string|true|none|Platform Fees|

<h2 id="tocS_SetCashbackDto">SetCashbackDto</h2>
<!-- backwards compatibility -->
<a id="schemasetcashbackdto"></a>
<a id="schema_SetCashbackDto"></a>
<a id="tocSsetcashbackdto"></a>
<a id="tocssetcashbackdto"></a>

```json
{
  "id": "string",
  "setCashback": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|Chain Id|
|setCashback|string|true|none|Cash back|

<h2 id="tocS_SetFeaturedCollectionDto">SetFeaturedCollectionDto</h2>
<!-- backwards compatibility -->
<a id="schemasetfeaturedcollectiondto"></a>
<a id="schema_SetFeaturedCollectionDto"></a>
<a id="tocSsetfeaturedcollectiondto"></a>
<a id="tocssetfeaturedcollectiondto"></a>

```json
{
  "collectionId": "string",
  "isFeatured": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionId|string|true|none|Collection Id|
|isFeatured|boolean|true|none|none|

<h2 id="tocS_GiveawayDto">GiveawayDto</h2>
<!-- backwards compatibility -->
<a id="schemagiveawaydto"></a>
<a id="schema_GiveawayDto"></a>
<a id="tocSgiveawaydto"></a>
<a id="tocsgiveawaydto"></a>

```json
{
  "status": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|boolean|true|none|none|

<h2 id="tocS_NotificationDto">NotificationDto</h2>
<!-- backwards compatibility -->
<a id="schemanotificationdto"></a>
<a id="schema_NotificationDto"></a>
<a id="tocSnotificationdto"></a>
<a id="tocsnotificationdto"></a>

```json
{
  "itemSold": true,
  "bidActivity": true,
  "priceChange": true,
  "auctionExpiration": true,
  "outBid": true,
  "ownedItemUpdates": true,
  "successfulPurchase": true,
  "jungleNewsletter": true,
  "minimumBidThreshold": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemSold|boolean|false|none|none|
|bidActivity|boolean|false|none|none|
|priceChange|boolean|false|none|none|
|auctionExpiration|boolean|false|none|none|
|outBid|boolean|false|none|none|
|ownedItemUpdates|boolean|false|none|none|
|successfulPurchase|boolean|false|none|none|
|jungleNewsletter|boolean|false|none|none|
|minimumBidThreshold|number|false|none|none|

<h2 id="tocS_CreateChainsDto">CreateChainsDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatechainsdto"></a>
<a id="schema_CreateChainsDto"></a>
<a id="tocScreatechainsdto"></a>
<a id="tocscreatechainsdto"></a>

```json
{
  "name": "string",
  "symbol": "string",
  "chainId": "string",
  "imageUrl": "string",
  "baseUrl": "string",
  "tokenId": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|symbol|string|true|none|none|
|chainId|string|true|none|none|
|imageUrl|string|true|none|none|
|baseUrl|string|true|none|none|
|tokenId|string|true|none|none|
|description|string|true|none|none|
|address|string|true|none|none|
|decimals|number|true|none|none|
|ethPrice|number|true|none|none|
|usdPrice|number|true|none|none|

<h2 id="tocS_UpdateChainsDto">UpdateChainsDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatechainsdto"></a>
<a id="schema_UpdateChainsDto"></a>
<a id="tocSupdatechainsdto"></a>
<a id="tocsupdatechainsdto"></a>

```json
{
  "id": "string",
  "name": "string",
  "chainId": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "baseUrl": "string",
  "description": "string",
  "address": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|none|
|name|string|true|none|none|
|chainId|string|true|none|none|
|symbol|string|true|none|none|
|imageUrl|string|true|none|none|
|tokenId|string|true|none|none|
|baseUrl|string|true|none|none|
|description|string|true|none|none|
|address|string|true|none|none|
|decimals|number|true|none|none|
|ethPrice|number|true|none|none|
|usdPrice|number|true|none|none|
|active|boolean|true|none|none|

<h2 id="tocS_CreateTokensDto">CreateTokensDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatetokensdto"></a>
<a id="schema_CreateTokensDto"></a>
<a id="tocScreatetokensdto"></a>
<a id="tocscreatetokensdto"></a>

```json
{
  "chainId": "string",
  "chainName": "string",
  "name": "string",
  "symbol": "string",
  "tokenId": "string",
  "imageUrl": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|chainId|string|true|none|none|
|chainName|string|true|none|none|
|name|string|true|none|none|
|symbol|string|true|none|none|
|tokenId|string|true|none|none|
|imageUrl|string|true|none|none|
|description|string|true|none|none|
|decimals|number|true|none|none|
|ethPrice|number|true|none|none|
|usdPrice|number|true|none|none|
|defaultToken|boolean|true|none|none|
|contractAddress|string|true|none|none|
|chainBaseUrl|string|true|none|none|
|erc712_version|string|false|none|none|
|erc712_name|string|false|none|none|

<h2 id="tocS_UpdateTokensDto">UpdateTokensDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatetokensdto"></a>
<a id="schema_UpdateTokensDto"></a>
<a id="tocSupdatetokensdto"></a>
<a id="tocsupdatetokensdto"></a>

```json
{
  "id": "string",
  "chainId": "string",
  "name": "string",
  "symbol": "string",
  "imageUrl": "string",
  "tokenId": "string",
  "description": "string",
  "decimals": 0,
  "ethPrice": 0,
  "usdPrice": 0,
  "active": true,
  "defaultToken": true,
  "contractAddress": "string",
  "chainBaseUrl": "string",
  "erc712_version": "string",
  "erc712_name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|none|
|chainId|string|true|none|none|
|name|string|true|none|none|
|symbol|string|true|none|none|
|imageUrl|string|true|none|none|
|tokenId|string|true|none|none|
|description|string|true|none|none|
|decimals|number|true|none|none|
|ethPrice|number|true|none|none|
|usdPrice|number|true|none|none|
|active|boolean|true|none|none|
|defaultToken|boolean|true|none|none|
|contractAddress|string|true|none|none|
|chainBaseUrl|string|true|none|none|
|erc712_version|string|false|none|none|
|erc712_name|string|false|none|none|

<h2 id="tocS_UpdateCollectionsDto">UpdateCollectionsDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecollectionsdto"></a>
<a id="schema_UpdateCollectionsDto"></a>
<a id="tocSupdatecollectionsdto"></a>
<a id="tocsupdatecollectionsdto"></a>

```json
{
  "logo": "string",
  "featureImage": "string",
  "banner": "string",
  "name": "string",
  "slug": "string",
  "description": "string",
  "categoryId": "string",
  "websiteLink": "string",
  "discordLink": "string",
  "instagramLink": "string",
  "mediumLink": "string",
  "telegramLink": "string",
  "earningFee": 0,
  "earningWalletAddress": "string",
  "paymentToken": [
    "string"
  ],
  "displayTheme": "contained",
  "explicitOrSensitiveContent": false
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|logo|string|true|none|Logo for the collection|
|featureImage|string|false|none|Feature image for collection|
|banner|string|false|none|Banner for collection|
|name|string|true|none|Name of collection|
|slug|string|false|none|Collection url slug|
|description|string|false|none|Description about collection|
|categoryId|string|false|none|Category for this collection|
|websiteLink|string|false|none|Url of website|
|discordLink|string|false|none|Discord Link|
|instagramLink|string|false|none|Instagram Link|
|mediumLink|string|false|none|Medium Link|
|telegramLink|string|false|none|Telegram Link|
|earningFee|number|false|none|Earning fee for Creator|
|earningWalletAddress|string|false|none|Earning wallet address for the collection|
|paymentToken|[string]|false|none|Payment token to be used in the collection|
|displayTheme|string|false|none|Display theme for the collection|
|explicitOrSensitiveContent|boolean|false|none|Whether explicit or sensitive content|

<h2 id="tocS_UserWatchlistDto">UserWatchlistDto</h2>
<!-- backwards compatibility -->
<a id="schemauserwatchlistdto"></a>
<a id="schema_UserWatchlistDto"></a>
<a id="tocSuserwatchlistdto"></a>
<a id="tocsuserwatchlistdto"></a>

```json
{
  "isWatched": true,
  "collectionId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isWatched|boolean|true|none|none|
|collectionId|string|true|none|none|

<h2 id="tocS_UpdateCollaboratorDto">UpdateCollaboratorDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecollaboratordto"></a>
<a id="schema_UpdateCollaboratorDto"></a>
<a id="tocSupdatecollaboratordto"></a>
<a id="tocsupdatecollaboratordto"></a>

```json
{
  "collectionId": "string",
  "updateType": "string",
  "walletAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionId|string|true|none|Collection id of where collaborator has to be added|
|updateType|string|true|none|Update type telling whether to add or remove collaborator|
|walletAddress|string|true|none|Wallet address of the user to be added|

<h2 id="tocS_BlockCollectionDto">BlockCollectionDto</h2>
<!-- backwards compatibility -->
<a id="schemablockcollectiondto"></a>
<a id="schema_BlockCollectionDto"></a>
<a id="tocSblockcollectiondto"></a>
<a id="tocsblockcollectiondto"></a>

```json
{
  "collectionId": "string",
  "blockOrUnblock": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionId|string|true|none|none|
|blockOrUnblock|boolean|true|none|to block or unblock a collection|

<h2 id="tocS_UpdateCashbackByCollectionIdDto">UpdateCashbackByCollectionIdDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecashbackbycollectioniddto"></a>
<a id="schema_UpdateCashbackByCollectionIdDto"></a>
<a id="tocSupdatecashbackbycollectioniddto"></a>
<a id="tocsupdatecashbackbycollectioniddto"></a>

```json
{
  "collectionId": "string",
  "cashback": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionId|string|true|none|none|
|cashback|number|true|none|none|

<h2 id="tocS_CollectionFavouritesDto">CollectionFavouritesDto</h2>
<!-- backwards compatibility -->
<a id="schemacollectionfavouritesdto"></a>
<a id="schema_CollectionFavouritesDto"></a>
<a id="tocScollectionfavouritesdto"></a>
<a id="tocscollectionfavouritesdto"></a>

```json
{
  "isFavourite": true,
  "collectionId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isFavourite|boolean|true|none|none|
|collectionId|string|true|none|none|

<h2 id="tocS_Signature">Signature</h2>
<!-- backwards compatibility -->
<a id="schemasignature"></a>
<a id="schema_Signature"></a>
<a id="tocSsignature"></a>
<a id="tocssignature"></a>

```json
{
  "exchange": "string",
  "maker": "string",
  "taker": "string",
  "makerRelayerFee": 0,
  "takerRelayerFee": 0,
  "takerCashbackFee": 0,
  "feeRecipient": "string",
  "side": 0,
  "saleKind": 0,
  "target": "string",
  "howToCall": 0,
  "data": "string",
  "replacementPattern": "string",
  "royaltyData": "string",
  "staticTarget": "string",
  "staticExtradata": "string",
  "paymentToken": "string",
  "basePrice": 0,
  "extra": 0,
  "listingTime": 0,
  "expirationTime": 0,
  "salt": 0,
  "nonce": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|exchange|string|true|none|none|
|maker|string|true|none|none|
|taker|string|true|none|none|
|makerRelayerFee|number|true|none|none|
|takerRelayerFee|number|true|none|none|
|takerCashbackFee|number|true|none|none|
|feeRecipient|string|true|none|none|
|side|number|true|none|none|
|saleKind|number|true|none|none|
|target|string|true|none|none|
|howToCall|number|true|none|none|
|data|string|true|none|none|
|replacementPattern|string|true|none|none|
|royaltyData|string|true|none|none|
|staticTarget|string|true|none|none|
|staticExtradata|string|true|none|none|
|paymentToken|string|true|none|none|
|basePrice|number|true|none|none|
|extra|number|true|none|none|
|listingTime|number|true|none|none|
|expirationTime|number|true|none|none|
|salt|number|true|none|none|
|nonce|number|true|none|none|

<h2 id="tocS_CreateOfferDto">CreateOfferDto</h2>
<!-- backwards compatibility -->
<a id="schemacreateofferdto"></a>
<a id="schema_CreateOfferDto"></a>
<a id="tocScreateofferdto"></a>
<a id="tocscreateofferdto"></a>

```json
{
  "price": 0,
  "paymentToken": "string",
  "quantity": 0,
  "item": "string",
  "Expires": 0,
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|price|number|true|none|none|
|paymentToken|string|true|none|none|
|quantity|number|true|none|none|
|item|string|true|none|none|
|Expires|number|true|none|Unix timestamp value for expiration window|
|auctionId|string|false|none|none|
|signatureObject|[Signature](#schemasignature)|true|none|none|
|signature|string|true|none|none|

<h2 id="tocS_UpdateOfferDto">UpdateOfferDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdateofferdto"></a>
<a id="schema_UpdateOfferDto"></a>
<a id="tocSupdateofferdto"></a>
<a id="tocsupdateofferdto"></a>

```json
{
  "price": 0,
  "paymentToken": "string",
  "Expires": 0,
  "quantity": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|price|number|false|none|none|
|paymentToken|string|false|none|none|
|Expires|number|false|none|none|
|quantity|number|false|none|none|

<h2 id="tocS_AcceptOfferDto">AcceptOfferDto</h2>
<!-- backwards compatibility -->
<a id="schemaacceptofferdto"></a>
<a id="schema_AcceptOfferDto"></a>
<a id="tocSacceptofferdto"></a>
<a id="tocsacceptofferdto"></a>

```json
{
  "offerID": "string",
  "transactionHash": "string",
  "url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|offerID|string|true|none|none|
|transactionHash|string|true|none|none|
|url|string|true|none|none|

<h2 id="tocS_CreateOfferSignatureDto">CreateOfferSignatureDto</h2>
<!-- backwards compatibility -->
<a id="schemacreateoffersignaturedto"></a>
<a id="schema_CreateOfferSignatureDto"></a>
<a id="tocScreateoffersignaturedto"></a>
<a id="tocscreateoffersignaturedto"></a>

```json
{
  "offerId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|offerId|string|true|none|none|
|signatureObject|[Signature](#schemasignature)|true|none|none|
|signature|string|true|none|none|

<h2 id="tocS_CollectionMinimumOfferPrice">CollectionMinimumOfferPrice</h2>
<!-- backwards compatibility -->
<a id="schemacollectionminimumofferprice"></a>
<a id="schema_CollectionMinimumOfferPrice"></a>
<a id="tocScollectionminimumofferprice"></a>
<a id="tocscollectionminimumofferprice"></a>

```json
{
  "collectionId": "string",
  "price": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionId|string|true|none|none|
|price|number|true|none|none|

<h2 id="tocS_UpdateCollectionOfferPriceDto">UpdateCollectionOfferPriceDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecollectionofferpricedto"></a>
<a id="schema_UpdateCollectionOfferPriceDto"></a>
<a id="tocSupdatecollectionofferpricedto"></a>
<a id="tocsupdatecollectionofferpricedto"></a>

```json
{
  "collectionsMinimumOfferPrice": [
    {
      "collectionId": "string",
      "price": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|collectionsMinimumOfferPrice|[[CollectionMinimumOfferPrice](#schemacollectionminimumofferprice)]|true|none|none|

<h2 id="tocS_UserFavouritesDto">UserFavouritesDto</h2>
<!-- backwards compatibility -->
<a id="schemauserfavouritesdto"></a>
<a id="schema_UserFavouritesDto"></a>
<a id="tocSuserfavouritesdto"></a>
<a id="tocsuserfavouritesdto"></a>

```json
{
  "isFavourite": true,
  "itemId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isFavourite|boolean|true|none|none|
|itemId|string|true|none|none|

<h2 id="tocS_HideItemDto">HideItemDto</h2>
<!-- backwards compatibility -->
<a id="schemahideitemdto"></a>
<a id="schema_HideItemDto"></a>
<a id="tocShideitemdto"></a>
<a id="tocshideitemdto"></a>

```json
{
  "itemId": "string",
  "isHidden": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|true|none|none|
|isHidden|boolean|true|none|none|

<h2 id="tocS_TransferItemDto">TransferItemDto</h2>
<!-- backwards compatibility -->
<a id="schematransferitemdto"></a>
<a id="schema_TransferItemDto"></a>
<a id="tocStransferitemdto"></a>
<a id="tocstransferitemdto"></a>

```json
{
  "userWalletAddress": "string",
  "supply": 0,
  "hash": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|userWalletAddress|string|true|none|none|
|supply|number|false|none|none|
|hash|string|true|none|none|

<h2 id="tocS_BuyItemDto">BuyItemDto</h2>
<!-- backwards compatibility -->
<a id="schemabuyitemdto"></a>
<a id="schema_BuyItemDto"></a>
<a id="tocSbuyitemdto"></a>
<a id="tocsbuyitemdto"></a>

```json
{
  "auctionId": "string",
  "soldPrice": 0,
  "itemId": "string",
  "transactionHash": "string",
  "transactionUrl": "string",
  "isDirectPurchase": false
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|auctionId|string|true|none|none|
|soldPrice|number|true|none|none|
|itemId|string|true|none|none|
|transactionHash|string|true|none|none|
|transactionUrl|string|true|none|none|
|isDirectPurchase|boolean|false|none|For direct purchase|

<h2 id="tocS_UpdateCashbackDto">UpdateCashbackDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatecashbackdto"></a>
<a id="schema_UpdateCashbackDto"></a>
<a id="tocSupdatecashbackdto"></a>
<a id="tocsupdatecashbackdto"></a>

```json
{
  "itemID": "string",
  "cashback": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemID|string|true|none|none|
|cashback|number|true|none|none|

<h2 id="tocS_BlockItemDto">BlockItemDto</h2>
<!-- backwards compatibility -->
<a id="schemablockitemdto"></a>
<a id="schema_BlockItemDto"></a>
<a id="tocSblockitemdto"></a>
<a id="tocsblockitemdto"></a>

```json
{
  "ItemId": "string",
  "isBlocked": true,
  "isblockedByAI": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ItemId|string|true|none|none|
|isBlocked|boolean|true|none|Boolean value for isBlocked|
|isblockedByAI|boolean|true|none|Boolean value for blockedByAI|

<h2 id="tocS_FreezeMetaDataDto">FreezeMetaDataDto</h2>
<!-- backwards compatibility -->
<a id="schemafreezemetadatadto"></a>
<a id="schema_FreezeMetaDataDto"></a>
<a id="tocSfreezemetadatadto"></a>
<a id="tocsfreezemetadatadto"></a>

```json
{
  "itemId": "string",
  "nftItemUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|true|none|none|
|nftItemUrl|string|true|none|none|

<h2 id="tocS_CreateBatchNftDto">CreateBatchNftDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatebatchnftdto"></a>
<a id="schema_CreateBatchNftDto"></a>
<a id="tocScreatebatchnftdto"></a>
<a id="tocscreatebatchnftdto"></a>

```json
{
  "fileUrl": [
    "string"
  ],
  "fileName": "string",
  "externalUrl": "string",
  "previewImage": "string",
  "description": "string",
  "collectionId": "string",
  "properties": [
    {
      "type": "string",
      "name": "string",
      "percentage": 0
    }
  ],
  "levels": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "stats": [
    {
      "name": "string",
      "value": 0,
      "maxValue": 0
    }
  ],
  "isLockable": true,
  "lockableContent": "string",
  "isExplicit": true,
  "supply": 0,
  "blockChainId": "string",
  "contractAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fileUrl|[string]|true|none|none|
|fileName|string|true|none|none|
|externalUrl|string|false|none|none|
|previewImage|string|false|none|none|
|description|string|false|none|none|
|collectionId|string|false|none|none|
|properties|[[Properties](#schemaproperties)]|false|none|properties|
|levels|[[Levels](#schemalevels)]|false|none|Levels|
|stats|[[ItemStats](#schemaitemstats)]|false|none|Stats|
|isLockable|boolean|false|none|none|
|lockableContent|string|false|none|none|
|isExplicit|boolean|false|none|none|
|supply|number|false|none|none|
|blockChainId|string|true|none|none|
|contractAddress|string|false|none|none|

<h2 id="tocS_PurchaseDropOff">PurchaseDropOff</h2>
<!-- backwards compatibility -->
<a id="schemapurchasedropoff"></a>
<a id="schema_PurchaseDropOff"></a>
<a id="tocSpurchasedropoff"></a>
<a id="tocspurchasedropoff"></a>

```json
{
  "nftId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|nftId|string|true|none|none|

<h2 id="tocS_FollowUnfollowDto">FollowUnfollowDto</h2>
<!-- backwards compatibility -->
<a id="schemafollowunfollowdto"></a>
<a id="schema_FollowUnfollowDto"></a>
<a id="tocSfollowunfollowdto"></a>
<a id="tocsfollowunfollowdto"></a>

```json
{
  "toFollow": true,
  "itemId": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|toFollow|boolean|true|none|none|
|itemId|string|true|none|none|

<h2 id="tocS_Bundle">Bundle</h2>
<!-- backwards compatibility -->
<a id="schemabundle"></a>
<a id="schema_Bundle"></a>
<a id="tocSbundle"></a>
<a id="tocsbundle"></a>

```json
{
  "isBundle": true,
  "name": "string",
  "description": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isBundle|boolean|true|none|none|
|name|string|true|none|none|
|description|string|true|none|none|

<h2 id="tocS_ReservedAuction">ReservedAuction</h2>
<!-- backwards compatibility -->
<a id="schemareservedauction"></a>
<a id="schema_ReservedAuction"></a>
<a id="tocSreservedauction"></a>
<a id="tocsreservedauction"></a>

```json
{
  "isReservedAuction": true,
  "walletAddress": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|isReservedAuction|boolean|true|none|none|
|walletAddress|string|true|none|none|

<h2 id="tocS_SignatureObject">SignatureObject</h2>
<!-- backwards compatibility -->
<a id="schemasignatureobject"></a>
<a id="schema_SignatureObject"></a>
<a id="tocSsignatureobject"></a>
<a id="tocssignatureobject"></a>

```json
{
  "exchange": "string",
  "maker": "string",
  "taker": "string",
  "makerRelayerFee": 0,
  "takerRelayerFee": 0,
  "takerCashbackFee": 0,
  "feeRecipient": "string",
  "side": 0,
  "saleKind": 0,
  "target": "string",
  "howToCall": 0,
  "data": "string",
  "replacementPattern": "string",
  "royaltyData": "string",
  "staticTarget": "string",
  "staticExtradata": "string",
  "paymentToken": "string",
  "basePrice": 0,
  "extra": 0,
  "listingTime": 0,
  "expirationTime": 0,
  "salt": 0,
  "nonce": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|exchange|string|true|none|none|
|maker|string|true|none|none|
|taker|string|true|none|none|
|makerRelayerFee|number|true|none|none|
|takerRelayerFee|number|true|none|none|
|takerCashbackFee|number|true|none|none|
|feeRecipient|string|true|none|none|
|side|number|true|none|none|
|saleKind|number|true|none|none|
|target|string|true|none|none|
|howToCall|number|true|none|none|
|data|string|true|none|none|
|replacementPattern|string|true|none|none|
|royaltyData|string|true|none|none|
|staticTarget|string|true|none|none|
|staticExtradata|string|true|none|none|
|paymentToken|string|true|none|none|
|basePrice|number|true|none|none|
|extra|number|true|none|none|
|listingTime|number|true|none|none|
|expirationTime|number|true|none|none|
|salt|number|true|none|none|
|nonce|number|true|none|none|

<h2 id="tocS_CreateAuctionDto">CreateAuctionDto</h2>
<!-- backwards compatibility -->
<a id="schemacreateauctiondto"></a>
<a id="schema_CreateAuctionDto"></a>
<a id="tocScreateauctiondto"></a>
<a id="tocscreateauctiondto"></a>

```json
{
  "auction_item": "string",
  "bundle_items": [
    "string"
  ],
  "auction_collection": "string",
  "startDate": 0,
  "endDate": 0,
  "tokens": "string",
  "auctionType": "string",
  "bundle": {
    "isBundle": true,
    "name": "string",
    "description": "string"
  },
  "reservedAuction": {
    "isReservedAuction": true,
    "walletAddress": "string"
  },
  "quantity": 0,
  "startingPrice": 0,
  "endingPrice": 0,
  "reservedPrice": 0,
  "timedAuctionMethod": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|auction_item|string|true|none|none|
|bundle_items|[string]|true|none|none|
|auction_collection|string|true|none|none|
|startDate|number|true|none|none|
|endDate|number|true|none|none|
|tokens|string|true|none|none|
|auctionType|string|true|none|none|
|bundle|[Bundle](#schemabundle)|false|none|none|
|reservedAuction|[ReservedAuction](#schemareservedauction)|false|none|none|
|quantity|number|false|none|none|
|startingPrice|number|false|none|none|
|endingPrice|number|false|none|none|
|reservedPrice|number|false|none|none|
|timedAuctionMethod|string|false|none|none|
|signatureObject|[SignatureObject](#schemasignatureobject)|true|none|none|
|signature|string|true|none|none|

<h2 id="tocS_CancelAuctionDto">CancelAuctionDto</h2>
<!-- backwards compatibility -->
<a id="schemacancelauctiondto"></a>
<a id="schema_CancelAuctionDto"></a>
<a id="tocScancelauctiondto"></a>
<a id="tocscancelauctiondto"></a>

```json
{
  "auctionId": "string",
  "transactionHash": "string",
  "transactionUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|auctionId|string|true|none|none|
|transactionHash|string|true|none|none|
|transactionUrl|string|true|none|none|

<h2 id="tocS_UpdateAuctionDto">UpdateAuctionDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdateauctiondto"></a>
<a id="schema_UpdateAuctionDto"></a>
<a id="tocSupdateauctiondto"></a>
<a id="tocsupdateauctiondto"></a>

```json
{
  "auctionId": "string",
  "endDate": 0,
  "price": 0,
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|auctionId|string|true|none|none|
|endDate|number|false|none|none|
|price|number|false|none|none|
|signatureObject|[SignatureObject](#schemasignatureobject)|true|none|none|
|signature|string|true|none|none|

<h2 id="tocS_CreateSignatureDto">CreateSignatureDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatesignaturedto"></a>
<a id="schema_CreateSignatureDto"></a>
<a id="tocScreatesignaturedto"></a>
<a id="tocscreatesignaturedto"></a>

```json
{
  "auctionId": "string",
  "signatureObject": {
    "exchange": "string",
    "maker": "string",
    "taker": "string",
    "makerRelayerFee": 0,
    "takerRelayerFee": 0,
    "takerCashbackFee": 0,
    "feeRecipient": "string",
    "side": 0,
    "saleKind": 0,
    "target": "string",
    "howToCall": 0,
    "data": "string",
    "replacementPattern": "string",
    "royaltyData": "string",
    "staticTarget": "string",
    "staticExtradata": "string",
    "paymentToken": "string",
    "basePrice": 0,
    "extra": 0,
    "listingTime": 0,
    "expirationTime": 0,
    "salt": 0,
    "nonce": 0
  },
  "signature": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|auctionId|string|true|none|none|
|signatureObject|[SignatureObject](#schemasignatureobject)|true|none|none|
|signature|string|true|none|none|

<h2 id="tocS_UpdateHighestBidDto">UpdateHighestBidDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatehighestbiddto"></a>
<a id="schema_UpdateHighestBidDto"></a>
<a id="tocSupdatehighestbiddto"></a>
<a id="tocsupdatehighestbiddto"></a>

```json
{
  "id": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|[string]|true|none|none|

<h2 id="tocS_ReportDto">ReportDto</h2>
<!-- backwards compatibility -->
<a id="schemareportdto"></a>
<a id="schema_ReportDto"></a>
<a id="tocSreportdto"></a>
<a id="tocsreportdto"></a>

```json
{
  "id": "string",
  "message": "string",
  "originalCreatorUrl": "string",
  "reason": "string",
  "reportType": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|id of item or collection or user|
|message|string|false|none|to add comment or message while reporting|
|originalCreatorUrl|string|false|none|url of collection|
|reason|string|true|none|which type of report is it eg. Spam|
|reportType|number|true|none|to report a item = 0 for collection = 1 & for user = 2|

<h2 id="tocS_AboutUsDto">AboutUsDto</h2>
<!-- backwards compatibility -->
<a id="schemaaboutusdto"></a>
<a id="schema_AboutUsDto"></a>
<a id="tocSaboutusdto"></a>
<a id="tocsaboutusdto"></a>

```json
{
  "description": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|description|string|true|none|none|

<h2 id="tocS_TermConditionDto">TermConditionDto</h2>
<!-- backwards compatibility -->
<a id="schematermconditiondto"></a>
<a id="schema_TermConditionDto"></a>
<a id="tocStermconditiondto"></a>
<a id="tocstermconditiondto"></a>

```json
{
  "termCondition": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|termCondition|string|true|none|none|

<h2 id="tocS_FandQDto">FandQDto</h2>
<!-- backwards compatibility -->
<a id="schemafandqdto"></a>
<a id="schema_FandQDto"></a>
<a id="tocSfandqdto"></a>
<a id="tocsfandqdto"></a>

```json
{
  "question": "string",
  "answer": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|question|string|true|none|none|
|answer|string|true|none|none|

<h2 id="tocS_UpdateFandQDto">UpdateFandQDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatefandqdto"></a>
<a id="schema_UpdateFandQDto"></a>
<a id="tocSupdatefandqdto"></a>
<a id="tocsupdatefandqdto"></a>

```json
{
  "id": "string",
  "question": "string",
  "answer": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|none|
|question|string|true|none|none|
|answer|string|true|none|none|

<h2 id="tocS_PrivacyDto">PrivacyDto</h2>
<!-- backwards compatibility -->
<a id="schemaprivacydto"></a>
<a id="schema_PrivacyDto"></a>
<a id="tocSprivacydto"></a>
<a id="tocsprivacydto"></a>

```json
{
  "privacyPolicy": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|privacyPolicy|string|true|none|none|

<h2 id="tocS_KycSessionDto">KycSessionDto</h2>
<!-- backwards compatibility -->
<a id="schemakycsessiondto"></a>
<a id="schema_KycSessionDto"></a>
<a id="tocSkycsessiondto"></a>
<a id="tocskycsessiondto"></a>

```json
{
  "request_data": "string",
  "user_data": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|request_data|string|true|none|Request data for kyc submition|
|user_data|string|true|none|User entered data|

<h2 id="tocS_CreateStatusDto">CreateStatusDto</h2>
<!-- backwards compatibility -->
<a id="schemacreatestatusdto"></a>
<a id="schema_CreateStatusDto"></a>
<a id="tocScreatestatusdto"></a>
<a id="tocscreatestatusdto"></a>

```json
{
  "content": "string",
  "version": 0,
  "isActive": true,
  "status": "general",
  "imageUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|content|string|true|none|content|
|version|number|true|none|version in number|
|isActive|boolean|true|none|isActive boolean|
|status|string|true|none|status (general/homepage)|
|imageUrl|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|general|
|status|homepage|

<h2 id="tocS_UpdateStatusDto">UpdateStatusDto</h2>
<!-- backwards compatibility -->
<a id="schemaupdatestatusdto"></a>
<a id="schema_UpdateStatusDto"></a>
<a id="tocSupdatestatusdto"></a>
<a id="tocsupdatestatusdto"></a>

```json
{
  "content": "string",
  "version": 0,
  "isActive": true,
  "imageUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|content|string|true|none|content|
|version|number|true|none|version in number|
|isActive|boolean|true|none|isActive boolean|
|imageUrl|string|true|none|none|

