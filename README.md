Poole Client
==========

Poole App Client, a promise-based wrapper for PooleApp.com

Installation
----
`npm install poole-client --save`


Usage
----

Require client from node:

```javascript
var poole = require('poole');
```

Get data via get() function, then access success and error handlers using the async callbacks:

```javascript
poole.get()
  .then(function(data) {

    console.log('got some data from poole', data);

  }, function(err) {
    console.log('error', err);
  });
```

Save data by sending form key-value pairs to add() function:

```javascript
poole.add(formData)
  .then(function() {
      
    // data saved, return a 201 response or something

  }, function(err) {
    console.log('error saving data', err);

  });
```

