---
id: permissions
title: Permissions
---
# Usage 
## Standalone
Permissions can be used to check an object for a value

```

let {has} = require( 'permissions' )
let perms = ...

if ( has( perms, 'users', 'r' ) {
  // allow 'r' access - like read
}

perms = { scopes : [ ... ] }
if ( has( perms, 'scopes', 'create_user' )) {
  // do stuff for create user
}

```

There are several methods:

* has
* hasAny
* hasAll
* hasNone
* equals
* equalsAny
* doesNotEqual
* doesNotEqualAny
* exists
* doesNotExist

## Express

To use this in express, you can install it as middleware by using the `guard` function:

```

let {guard} = require( 'permissions' )

app.get( 'users', guard.has( 'users', 'r' ), function( req, res, next ) {
  ...
})

```

Guard has all the methods defined above as well as three more:

* init( opts ) : create a new guard object that takes an options object
    * pkey : where to get the permissions object from the request. (default 'permission')
    * statusCode : the status code to send in the error message { status : 403, message : 'forbidden' }
* and
* or

The method and() and or() take an arbitrary number of other guard condition methods and performs
either an And or an Or function on the results. In an And, all conditions must be met. In an an
Or, only one must be met


```

let {guard} = require( 'permissions' )

app.get( 'users', guard.or( guard.equals( 'role', 'a' ), guard.has( 'user', 'w' ) ),  function( req, res, next ) {
  ...
})

```

When the guard functions are used, a function can be sent in place of the key and values. The function will
be given the request object to extract its data from. A convience function called reqValueAt( stringPath ) 
is supplied to extract values at paths