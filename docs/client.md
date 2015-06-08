# On Client
Customers are built directly into the `JavaScript` and `html` have been designed to operate in multiple frameworks. You can use the service without having to make use of these `JavaScript`, however can not guarantee proper functioning.

## AngularJs

### Install

```
$ [npm|bower] install cachewatch-angular
```

### Use

In `HTML`

```html
<script type="text/javascript" src="angular.js" ></script>
<script type="text/javascript" src="cachewatch-angular.js" ></script>
<script type="text/javascript" src="app.js" ></script>
<body ng-app="app" >
	<input ng-model="myModel" />
	<p>{{myModel}}</p>
</body>
```
In your App

```JavaScript
angular
	.module('app', ['cachewatch'])
	.controller('MyController', [ '$scope', 'cachewatch',
		function($scope, cache){
		cache.ready();
	}]);
```

## jQuery

### Install

```
$ [npm|bower] install cachewatch-jquery
```

### Use

In `HTML`

```html
<script type="text/javascript" src="jquery.js" ></script>
<script type="text/javascript" src="cachewatch-jquery.js" ></script>
<script type="text/javascript" src="app.js" ></script>
```
In your app

```JavaScript
$.cachewatch.ready();
```
