---
id: log
title: Log
---

The Log library abstracts away much of the logging functionality, making it so that with one call, log statements get logged in multiple places. 

## Usage
```
npm install @leverege/log --save
```

By default, the log defaults to the EmptyLog, which no-ops all logging methods.
To install a console logger, in the main class call:
```
const log = require( '@leverege/log' );
log.setAdapter( log.ConsoleLog() )
```

To install a bunyan logger, call:
```
const bunyanLog = bunyan.createLogger( { ... } );
log.setAdapter( log.BunyanLog( bunyanLog ) );
```

## Automated Log Creation and Installation

If you want to install a log entirely from a configuration variable (JSON, file, or plain object) call:
```
log.createAdapter(<config - object, JSON string, or file>, <params - object>, <install - boolean>)
```
This function will create an Adapter based on your configuration, can parameterize your configuration if you are using a string or file, and will automatically call setAdapter if install is not false.

a configuration may look like:
```
const logFile = '/var/config/transponder/logConfig.json'
```
or 
```
const logString = '{
	"type" : "bunyan",
	"name" : "${logName}",
	"streams" : [
		{ 
			"type" : "rotating-file",
			"period" : "1d",
			"count" : 3,
			"level" : "warn",
			"path" : "./logs3/${logName}"
		}, 
		{ 
			"type" : "stackdriver",
			"logName" : "${resource}",
			"keyFilename" : "${logServiceAccount}"
		}
	]
}'
```
or
```
const logObject = {
	type: 'console',
	mod: 'transponder'
}
```

In order to make the second JSON string configuration work, a parameters object would be supplied like so:
```
const logParams = {
	logName: ClusterManager.logName( 'transponder' ),
	resource: `transponder-${process.env.TRANSPONDER_RUN_MODE || 'all'}`,
    logServiceAccount: process.env.LOG_SERVICE_ACCOUNT
}
```

So the installation would look like the following:
```
log.createAdapter(logString, params, true)
```

### Sensitive Information
In order to not log sensitive information (e.g. auth token, password), pass in `"blacklist": true` as an option parameter. 

```
const logConfig = '{
	"type" : "bunyan",
	"name" : "${logName}",
	"blacklist" : true, 
	"streams" : [...]
}'
```

It will then omit those fields before outputing to log aggregater (e.g. Stackdriver). 

## Logging

To log, call:
```
const log = require( '@leverege/log' );
log.trace( 'trace log' );
log.debug( 'debug log' );
log.info( 'info log' );
log.warn( 'warn log' );
log.fatal( 'fatal log' );
```

The log methods can take an object as the first argument. See bunyans log for more information.

Other methods include:
```
child, setLevel, getLevel, isTrace, isDebug, isInfo, isWarn, isError, isError, isFatal
```

