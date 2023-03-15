# Schema

## Get Codeset without codes

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "id": 3000,
    "typeCodeSetId": null,
    "typeCodeId": null,
    "name": "Skjemakodeverk",
    "description": "Kodeverk brukt i skjemaer",
    "deleted_at": null,
    "created_at": "2021-04-10T22:10:18.000000Z",
    "updated_at": "2021-04-10T22:10:18.000000Z"
}
```

This endpoint retrieves codeset without codes.

### HTTP Request

`GET https://schema.beitostolenlive.no/api/v1/codeset/<ID>`

### Route Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID | false | Codeset id

## Get Codeset with codes

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "id": 2001,
    "typeCodeSetId": 2000,
    "typeCodeId": "KOMMUNER",
    "name": "Norske kommuner",
    "description": "Kodeverk over norske kommuner",
    "deleted_at": null,
    "created_at": "2021-04-10T17:56:54.000000Z",
    "updated_at": "2021-04-10T17:56:54.000000Z",
    "codes": [
        {
            "codesetid": 2001,
            "codeid": "1101",
            "description": "Eigersund",
            "valid_from": "2001-01-01 00:00:00",
            "valid_to": null,
            "created_at": "2021-04-10T21:28:09.000000Z",
            "updated_at": "2021-04-10T21:28:09.000000Z",
            "deleted_at": null
        },
        {
            "codesetid": 2001,
            "codeid": "1103",
            "description": "Stavanger",
            "valid_from": "2001-01-01 00:00:00",
            "valid_to": null,
            "created_at": "2021-04-10T21:28:38.000000Z",
            "updated_at": "2021-04-10T21:28:38.000000Z",
            "deleted_at": null
        }
    ]
}
```

This endpoint retrieves codeset without codes.

### HTTP Request

`GET https://schema.beitostolenlive.no/api/v1/codeset/<ID>/codes`

### Route Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID | false | Codeset id

## Get Code

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "codesetid": 1001,
    "codeid": "BAR",
    "description": "Barutstyr",
    "valid_from": "2019-01-01 00:00:00",
    "valid_to": null,
    "created_at": "2021-04-10T21:52:00.000000Z",
    "updated_at": "2021-04-10T21:52:00.000000Z",
    "deleted_at": null
}
```

This endpoint retrieves codeset without codes.

### HTTP Request

`GET https://schema.beitostolenlive.no/api/v1/codeset/<ID>/code/<CODE>`

### Route Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID | false | Codeset id
CODE | false | Code id that is in the codeset

## Create Codeset

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "codesetid": 1001,
    "codeid": "BAR",
    "description": "Barutstyr",
    "valid_from": "2019-01-01 00:00:00",
    "valid_to": null,
    "created_at": "2021-04-10T21:52:00.000000Z",
    "updated_at": "2021-04-10T21:52:00.000000Z",
    "deleted_at": null
}
```

This endpoint retrieves codeset without codes.

### HTTP Request

`POST https://schema.beitostolenlive.no/api/v1/codeset/<ID>`

### Route Parameter

Parameter | Default | Description
--------- | ------- | -----------#
ID | false | Id for the new codeset

### Form Data Parameters

Parameter | Default | Description
--------- | ------- | -----------#
name | false | Name of codeset
description | false | Description of codeset
typeCodeSetId | true | Parent codeset id. Default is null.
typeCodeId | true | Parent codeset code id. Default is null.

## Create Code in Codeset

```php
```

```csharp
```

```javascript
```

> The above command returns JSON structured like this:

```json
{
    "codesetid": 1001,
    "codeid": "BAR",
    "description": "Barutstyr",
    "valid_from": "2019-01-01 00:00:00",
    "valid_to": null,
    "created_at": "2021-04-10T21:52:00.000000Z",
    "updated_at": "2021-04-10T21:52:00.000000Z",
    "deleted_at": null
}
```

This endpoint retrieves codeset without codes.

### HTTP Request

`POST https://schema.beitostolenlive.no/api/v1/codeset/<ID>/code/<CODE>`

### Route Parameter

Parameter | Default | Description
--------- | ------- | -----------#
ID | false | Id for the codeset
CODE | false | Code for the new code

### Form Data Parameters

Parameter | Default | Description
--------- | ------- | -----------#
description | false | Description of code
valid_from | false | Code valid from datetime.
valid_to | true | Parent codeset id. Default is null.