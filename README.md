# Turph Database

> Simple Database using MongoDB

## Documentation

### new Database()

```js
new database(mongo url, options)
```

Parameter | Type | Optional | Description
--- | --- | --- | ---
Mongo URL | [URL](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL) | ✖ | The URL given to you by the MongoDB Atlas Connection
Options | [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | null | null
Options.name | [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | ✖ | The name of the collection you want to create

#### Example

```js
  const turphDatabase = require('./database.js'); // Note: since this is not a NPM Package you need to make a new file for this called "database.js" if you wish to use this line of code
  
  const database = new turphDatabase('{ INSERT MONGO URL HERE }', { name: 'database' });
  db
  .on('error', err => console.log(err))
  .on('connected', info => console.log(info));
```

### database.set()


```js
database.set(key, value)
```

Parameter | Type | Optional | Description
--- | --- | --- | ---
Key | [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | ✖ | The key of the value
Value | [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) / [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | ✖ | The value of the key you wish to set

#### Example

```js
await database.set('foo', 'fee');
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)>

### database.get()


```js
await database.get(key)
```
 
__Example__

```js
await database.get('foo'); // fee
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)>

### database.search()


```js
database.search(query)
```

__Example__

```js
await database.search('foo');
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)>

### database.find()


```js
database.find(query)
```

__Example__

```js
await database.find('foo');
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)>

### database.all()


```js
database.all()
```

__Example__

```js
await database.all()
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)>

### database.delete()


```js
database.delete(key)
```

__Example__

```js
await database.delete('foo');
```

Returns [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)<[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)>
