This API consists of two keys.

* `KEY-token`, which is given on page user

Each of these two has different accesses.

## Cache

It is where all directions with their respective pages are stored. Only be stored the `html`

### Put page

Make the call to a page, Response, will be the `html` after being executed.

```console
{ANY} /put?acces_token={KEY-TOKEN} HTTP/1.1
 Accept: */* 
Connection: close
 Host: service.cache.watch
```

En el query o body

| Requerido | Name         |
|-----------| ------------ |
| [x]       | host         |
|           | protocol     |
|           | path         |
|           | query        |
|           | Hash         |

### One page

Response

```JSON
{
	"error" : [
		"Error : Example Error"
	],
	"totalPages" : {NUMBER_PAGES},
	"cache" : {
		"url" : "{URL}",
		"numb" : {NUMBER_REQUESTS},
		"date" : "{TIME_CREATE}",
		"_id" : "{ID_CACHE}",
	}
}
```
Get the information of a page
```console
GET /url/{ID_CACHE} HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

#### Update

Updating the `html`

```console
POST /url/{ID_CACHE} HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

#### Delete

Remove the record

```console
DELETE /url/{ID_CACHE} HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

### List

Response

```JSON
{
	"error" : [
		"Error : Example Error"
	],
	"totalPages" : {NUMBER_PAGES},
	"list" : [ {
		"url" : "{URL}",
		"numb" : {NUMBER_REQUESTS},
		"date" : "{TIME_CREATE}",
		"_id" : "{ID_CACHE}",
	}]
}
```
Returns a list of pages that exist on the server.

```console
GET /url HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```


#### Delete

Clean list.

```console
Delete /url HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

## User

Response

```JSON
{
	"error" : [
		"Error : Example Error"
	],
	"user" : {
		"bit" : "{BITCOIN}",
		"data" : {
			"updated_at" : "{TIME_UPDATE_GITHUB}",
			"created_at" : "{TIME_CREATE_GITHUB}",
			"name" : "{USER_GITHUB}",
			"company" : "",
			"type" : "User",
			"organizations_url": "https://api.github.com/users/{USER_GITHUB}/orgs",
			"html_url" : "https://github.com/{USER_GITHUB}",
			"avatar_url" : "https://avatars.githubusercontent.com/u/{ID_GITHUB}?v=3",
			"login" : "{USER_GITHUB}"
		},
		"__v":0,
		"time": {NUMBER_DAYS},
		"date" : "{TIME_CREATE}",
		"web" : "{KEY-WEB}",
		"token" : "{KEY-TOKEN}",
		"id" : "{ID_USER}"
	}
}
```
Gets the user

```console
GET /profile/me HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

### Update user

Updated user information.

```console
POST /profile/me HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

Send 

```JSON
{
	"time" : {NUMBER_DAYS}
}
```
### Token

It generates a new `KEY-TOKEN`

```console
POST /profile/token HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

## Baucher

Returns all purchases have been made.

```console
GET /profile/baucher HTTP/1.1
 Accept: */* 
 X-AUTH-WEB: {KEY-WEB}
Connection: close
 Host: service.cache.watch
```

Response

```JSON
{
	"error" : [
		"Error : Example Error"
	],
	"plans" : [{
		"hash": "{HASH-BITCOIN}",
		"num" : {NUMBER-MAX-PER-PAGE},
		"total" : {PRICE},
		"date" : "{DATE-END}",
		"start" : "{DATE-PAROCHE}",
	}]
}
```

Booty Swing by Parov Stelar