# On Server

If the implementation you need is not in this list, remember that you can own with the [API](../api/#put-page).

## NodeJs

This plugin was designed to [express](http://expressjs.com/). However it can be used in cualquer farmework.

### Install

```
$ npm install cachewatch
```

### Use

```javascript
var app = express();
var Cache = require('cachewatch');
app.use(Cache('-- KEY-TOKEN --').watch);
```
