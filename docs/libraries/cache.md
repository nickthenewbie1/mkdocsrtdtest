---
id: cache
title: Cache
---

The Cache library creates an cache to quickly set are retrieve values and speed up the operation of services,

## Install
```
npm install --save @leverege/cache

const Cache = require( '@leverege/cache' );

```

## Usage

In general, use the cacheConfig to drive the type of cache.

```
const cacheConfig = process.env.CACHE_CONFIG || 
  { type : 'redis', 
    connection : {
      host : '127.0.0.1',
      port : 6379
    }
  };

const cache = Cache.create( { cacheConfig, namespace : 'myApp'} )
...
await cache.set( 'myKey', myValue )  // This will set a value to a global myKey
const v = await cache.get( 'myKey' ) // This will access a global myKey
await cache.setNs( 'myKey', myValue )  // This will set a value to a namespaced myKey (myApp:myKey)
const v = await cache.getNs( 'myKey' ) // This will access a namespaced myKey (myApp:myKey)

```


## Other usage
To make a redis cache:

```
const cache = Cache.create( { 
    type : 'redis',
    namespace : 'myApp', 
    connection : {
      host : '127.0.0.1',
      port : 6379
    }
  } )
```