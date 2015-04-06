## loopback-connector-sqlite
`loopback-connector-sqlite` is the SQLite3 connector module for [loopback-datasource-juggler](https://github.com/strongloop/loopback-datasource-juggler).

## Basic usage
You will require [loopback-datasource-juggler](https://github.com/strongloop/loopback-datasource-juggler) and [node-sqlite3](https://github.com/mapbox/node-sqlite3) modules for using this connector.

A DataSource with basic settings can be defined as shown below:
```javascript
var DataSource = require('loopback-datasource-juggler').DataSource;
var dataSource = new DataSource(require('../index'), {
  file_name: 'dev.sqlite3',
  debug: false
});
```

Checkout `examples\example.js` to get the idea of basic usage.
Run the example from the root directory as follows:
```sh
node examples/example.js
```

Further usage documentation: TBD

## SQLite3 configuration for tests
The .loopbackrc file holds the settings for the tests. It's in JSON format and has following content:
```JSON
{
  "sqlite": {
    "test": {
      "file_name": "test.sqlite3",
      "debug": false
    }
  }
}
```
The `file_name` is the name of the sqlite3 DB file, which will be created, or, used if already present.
The `debug` value is to set debugging mode.

## Running the tests
* execute `npm install` for installing all the dependencies.
* execute `npm test` to run all the tests.