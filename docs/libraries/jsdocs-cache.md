---
id: jsdocs-cache
title: Cache
---
## Classes

<dl>
<dt><a href="#Cache">Cache</a></dt>
<dd></dd>
<dt><a href="#InMemoryCache">InMemoryCache</a></dt>
<dd><p>creates an in memory cache and an interface to interact with it</p>
</dd>
<dt><a href="#RedisCache">RedisCache</a></dt>
<dd><p>maintains a connection with redis and communicates with redis</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#NO_VALUE Returns a string that is usable as an indication that a value was stored into the cache that represents a null value">NO_VALUE Returns a string that is usable as an indication that a value was stored into the cache that represents a null value()</a></dt>
<dd></dd>
<dt><a href="#get Returns the cache value for key. This will not auto-prefix the key with the namespace. To auto prefix the key, use getNs( key )"> use getNs(key)</a> ⇒ <code>Promise</code></dt>
<dd></dd>
<dt><a href="#multiGet Returns an array of the cached values for key arr. This will not auto-prefix the key with the namespace. To auto prefix the key, use multiGetNs( key )"> use multiGetNs(keys)</a> ⇒ <code>Promise</code></dt>
<dd></dd>
<dt><a href="#end This method may be overridden by the child class that extends from Cache. It should be used to clean up any system resources, especially those that can cause unit tests to hang until everything shuts down cleanly."> especially those that can cause unit tests to hang until everything shuts down cleanly.()</a></dt>
<dd></dd>
<dt><a href="#create Creates a cache of a specifed type">create Creates a cache of a specifed type(options)</a></dt>
<dd></dd>
<dt><a href="#get gets the value at the key">get gets the value at the key(key)</a></dt>
<dd></dd>
<dt><a href="#multiGet gets and returns that values from multiple keys">multiGet gets and returns that values from multiple keys(keys)</a></dt>
<dd></dd>
<dt><a href="#set sets a value into the cache">set sets a value into the cache(key, value, opts)</a></dt>
<dd></dd>
<dt><a href="#remove removes a value from the cache">remove removes a value from the cache(key)</a></dt>
<dd></dd>
<dt><a href="#clear clears the inmemory cache">clear clears the inmemory cache()</a></dt>
<dd></dd>
<dt><a href="#get gets and returns a value from the cache">get gets and returns a value from the cache(key)</a></dt>
<dd></dd>
<dt><a href="#multiGet gets and returns that values from multiple keys">multiGet gets and returns that values from multiple keys(keys)</a></dt>
<dd></dd>
<dt><a href="#set sets a value into the redis cache">set sets a value into the redis cache(key, value, opts)</a></dt>
<dd></dd>
<dt><a href="#remove removes a value from the redis cache">remove removes a value from the redis cache(key, opts)</a></dt>
<dd></dd>
<dt><a href="#end ends the connection to the redis database">end ends the connection to the redis database()</a></dt>
<dd></dd>
</dl>

<a name="Cache"></a>

## Cache
**Kind**: global class  
<a name="new_Cache_new"></a>

### new Cache()
Creates a Cache object


| Param | Type | Description |
| --- | --- | --- |
| options.namespace | <code>string</code> | the namespace string to use in the xxxNs methods. Defaults to  'app' |

<a name="InMemoryCache"></a>

## InMemoryCache
creates an in memory cache and an interface to interact with it

**Kind**: global class  
<a name="new_InMemoryCache_new"></a>

### new InMemoryCache(options)

| Param | Type |
| --- | --- |
| options | <code>object</code> | 

<a name="RedisCache"></a>

## RedisCache
maintains a connection with redis and communicates with redis

**Kind**: global class  
<a name="new_RedisCache_new"></a>

### new RedisCache(options)

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.connection | <code>object</code> | config for the redis connection |

<a name="NO_VALUE Returns a string that is usable as an indication that a value was stored into the cache that represents a null value"></a>

## NO\_VALUE Returns a string that is usable as an indication that a value was stored into the cache that represents a null value()
**Kind**: global function  
<a name="create Creates a cache of a specifed type"></a>

## create Creates a cache of a specifed type(options)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the cache options |
| options.type | <code>string</code> | the type of cache to make. If unrecognized, this will return a no-op cache. Possible values: 'redis', 'inMemory', none' |
| options.prefix | <code>string</code> | a string that will prepended (with a ':') to all keys when accessing the cache. The resulting key will be prefix:key |
| options.cacheConfig | <code>object</code> | This can be an object, JSON or reference to a json/js file. If defined, it will be expanded and merged with the other options like prefix. This allows the cache type to be controlled by an environment variable or file. |

<a name="get gets the value at the key"></a>

## get gets the value at the key(key)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the value to get |

<a name="multiGet gets and returns that values from multiple keys"></a>

## multiGet gets and returns that values from multiple keys(keys)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| keys | <code>array</code> | the keys to get the values for |

<a name="set sets a value into the cache"></a>

## set sets a value into the cache(key, value, opts)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to set the value at |
| value | <code>any</code> | the value to be set |
| opts | <code>objct</code> |  |

<a name="remove removes a value from the cache"></a>

## remove removes a value from the cache(key)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to remove the value at |

<a name="clear clears the inmemory cache"></a>

## clear clears the inmemory cache()
**Kind**: global function  
<a name="get gets and returns a value from the cache"></a>

## get gets and returns a value from the cache(key)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | value to get from the cache |

<a name="multiGet gets and returns that values from multiple keys"></a>

## multiGet gets and returns that values from multiple keys(keys)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| keys | <code>array</code> | the keys to get the values for |

<a name="set sets a value into the redis cache"></a>

## set sets a value into the redis cache(key, value, opts)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to set the value at |
| value | <code>any</code> | the value to be set |
| opts | <code>objct</code> |  |

<a name="remove removes a value from the redis cache"></a>

## remove removes a value from the redis cache(key, opts)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to remove the value at |
| opts | <code>\*</code> |  |

<a name="end ends the connection to the redis database"></a>

## end ends the connection to the redis database()
**Kind**: global function  
