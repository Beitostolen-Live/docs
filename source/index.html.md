---
title: API Reference

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
  - php
  - csharp
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - festival
  - volunteers
  - customer
  - schema
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Beitostølen Live API's
---

# Introduction

Welcome to Beitostølen Live API documentation. The collection of API's is most for internal use in our applications.

# Authentication

> To authorize, use this code:

```php
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

```csharp
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

## Login

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "token": "<YOUR TOKEN>",
    "token_type": "bearer",
    "expires_in": 3600
}
```

This endpoint retrieves all events.

### HTTP Request

`POST https://auth.beitostolenlive.no/api/v1/login`

### Form Data Parameters

Parameter | Default | Description
--------- | ------- | -----------
email | false | Your username.
password | false | Your password.

<aside class="success">
You will then use your token on all other requests!
</aside>

## Register

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "token": "<YOUR TOKEN>",
    "token_type": "bearer",
    "expires_in": 3600
}
```

This endpoint retrieves all events.

### HTTP Request

`POST https://auth.beitostolenlive.no/api/v1/register`

### Form Data Parameters

Parameter | Default | Description
--------- | ------- | -----------
email | false | Your username.
password | false | Your password.
name | false | Your name.