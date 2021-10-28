---
id: jsdocs-limit
title: Limit
---
## Classes

<dl>
<dt><a href="#InMemoryLimitHandle">InMemoryLimitHandle</a></dt>
<dd><p>The InMemoryLimitHandle is returned from the InMemoryLimit and acts an as interface
to the actual limit object.</p>
</dd>
<dt><a href="#InMemoryLimit">InMemoryLimit</a></dt>
<dd><p>An InMemoryLimit represents a per process limit implemented by using
local storage to track the limiting activities. An InMemoryLimit will
not be shareable between processes.</p>
</dd>
<dt><a href="#Limit">Limit</a></dt>
<dd></dd>
<dt><a href="#RedisLimitHandle">RedisLimitHandle</a></dt>
<dd><p>The LimitHandle is returned from the RedisLimit and acts an as interface
to the actual limit.</p>
</dd>
<dt><a href="#RedisLimit">RedisLimit</a></dt>
<dd><p>The RedisLimit represent a Limit object &quot;stored&quot; in redis. Actually, the
Limit&#39;s key and its limiting timeout key are stored in redis, which
means these Limit types may be shared amongst processes.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#create">create(options)</a></dt>
<dd><p>Creates a limit of a specifed type</p>
</dd>
<dt><a href="#expand">expand()</a></dt>
<dd><p>If config exists, attempt to extract it via json or file read, then
adjust the option to look like that plus the rest.</p>
</dd>
</dl>

<a name="InMemoryLimitHandle"></a>

## InMemoryLimitHandle
The InMemoryLimitHandle is returned from the InMemoryLimit and acts an as interface
to the actual limit object.

**Kind**: global class  

* [InMemoryLimitHandle](#InMemoryLimitHandle)
    * [new InMemoryLimitHandle(limit, key, options)](#new_InMemoryLimitHandle_new)
    * [.reset()](#InMemoryLimitHandle+reset)
    * [.isLimited()](#InMemoryLimitHandle+isLimited) ⇒ <code>boolean</code>
    * [.unlimit()](#InMemoryLimitHandle+unlimit) ⇒ <code>Promise</code>

<a name="new_InMemoryLimitHandle_new"></a>

### new InMemoryLimitHandle(limit, key, options)
Creates a handle for the specified InMemory based Limit.


| Param | Type | Description |
| --- | --- | --- |
| limit | [<code>InMemoryLimit</code>](#InMemoryLimit) | the Limit wrapped by this interface |
| key | <code>string</code> | the key to limit |
| options | <code>object</code> | the options for the limit |
| options.count | <code>int</code> | the maximum number of times that an   activity may occur over a given period of time |
| options.period | <code>int</code> | the amount of time that the activity may   occur before being marked as limited (milliseconds) |
| options.duration | <code>int</code> | the amount of time to keep the activity   marked as limited (milliseconds) |

<a name="InMemoryLimitHandle+reset"></a>

### inMemoryLimitHandle.reset()
A method for reseting the limit back to its initial state.

**Kind**: instance method of [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle)  
<a name="InMemoryLimitHandle+isLimited"></a>

### inMemoryLimitHandle.isLimited() ⇒ <code>boolean</code>
**Kind**: instance method of [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle)  
**Returns**: <code>boolean</code> - true if limiting is active, else false  
<a name="InMemoryLimitHandle+unlimit"></a>

### inMemoryLimitHandle.unlimit() ⇒ <code>Promise</code>
Release the limit.

**Kind**: instance method of [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle)  
**Returns**: <code>Promise</code> - a Promise to release the limit  
<a name="InMemoryLimit"></a>

## InMemoryLimit
An InMemoryLimit represents a per process limit implemented by using
local storage to track the limiting activities. An InMemoryLimit will
not be shareable between processes.

**Kind**: global class  

* [InMemoryLimit](#InMemoryLimit)
    * [new InMemoryLimit(options)](#new_InMemoryLimit_new)
    * [.limit(key, options)](#InMemoryLimit+limit) ⇒ [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle)

<a name="new_InMemoryLimit_new"></a>

### new InMemoryLimit(options)
Creates a memory based limit object.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the parameters for the limiter |
| options.namespace | <code>string</code> | the namespace used in limitNs |
| options.limitConfig | <code>object</code> | the Limit connection parameters |
| options.limitConfig.type | <code>string</code> | the type of Limit to create   ('inMemory') |
| options.limitConfig.limitOptions.count | <code>int</code> | the number   of times the isLimited method may be checked within the period |
| options.limitConfig.limitOptions.period | <code>int</code> | the length of   time which the isLimited method may be checked before being limited (mS) |
| options.limitConfig.limitOptions.duration | <code>int</code> | the amount of   time the limit will be in effect (mS) |

**Example**  
```js
const Limit = require( '@leverege/limit' )
 const limiter = Limit.create( {
   namespace : 'example',
   limitConfig : {
     type : 'inMemory',
     limitOptions : { // default limit options
       count : 10,
       period : 30*1000,
       duration : 60*60*1000,
     },
   },
 })

 // Create a limit that will allow 25 occurances over a 5 second
 // period before imposing a 60 minute limit.
 //
 const memlim = limiter.limit( 'testKey', { count : 25,
                                           period : 5000,
                                         duration : 60*60 })
```
<a name="InMemoryLimit+limit"></a>

### inMemoryLimit.limit(key, options) ⇒ [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle)
Limits on the key. This will not auto-prefix the key with the namespace.
To auto prefix the key, use limitNs( key ).

**Kind**: instance method of [<code>InMemoryLimit</code>](#InMemoryLimit)  
**Returns**: [<code>InMemoryLimitHandle</code>](#InMemoryLimitHandle) - a Promise that will resolve to an InMemoryLimitHandle.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> | the options for the limit |
| options.count | <code>int</code> | the maximum number of times that an   activity may occur over a given period of time |
| options.period | <code>int</code> | the amount of time that the activity may   occur before being marked as limited (milliseconds) |
| options.duration | <code>int</code> | the amount of time to keep the activity   marked as limited (milliseconds) |

<a name="Limit"></a>

## Limit
**Kind**: global class  

* [Limit](#Limit)
    * [new Limit(options)](#new_Limit_new)
    * _instance_
        * [.getKey(key, namespace)](#Limit+getKey) ⇒ <code>string</code>
        * [.limit(key, options)](#Limit+limit) ⇒ <code>Promise</code>
        * [.limitNs(key, options)](#Limit+limitNs)
        * *[.isLimited()](#Limit+isLimited)*
        * *[.end()](#Limit+end)*
    * _static_
        * [.SecondsPerDay](#Limit.SecondsPerDay) ⇒
        * [.mergeDefaults()](#Limit.mergeDefaults)

<a name="new_Limit_new"></a>

### new Limit(options)
This class provides the frame work for building rate limiting into an
application. A Limit controls the number of times an operation may be
performed (count) within a certain time frame (period), and once 
exceeded, will stay limited (squelched) for some period of time. The
count, period and duration are configurable options specified when
a Limit is created.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | specific settings for the derived Limit class |
| options.namespace | <code>string</code> | the namespace string to use (default='app:') |

<a name="Limit+getKey"></a>

### limit.getKey(key, namespace) ⇒ <code>string</code>
Returns the actual key to use. This will combine the namespace + ':' +
key if a namespace is available.

**Kind**: instance method of [<code>Limit</code>](#Limit)  
**Returns**: <code>string</code> - the namespaced key value  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| key | <code>string</code> |  | a key to prefix with the namespace |
| namespace | <code>string</code> | <code>null</code> | if supplied, this will be used as the namespace,   otherwise, the namespace provided at construction will be used |

<a name="Limit+limit"></a>

### limit.limit(key, options) ⇒ <code>Promise</code>
Limits on the key. This will not auto-prefix the key with the namespace.
To auto prefix the key, use limitNs( key ).

**Kind**: instance method of [<code>Limit</code>](#Limit)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> | specific settings for the Limit class |

<a name="Limit+limitNs"></a>

### limit.limitNs(key, options)
Limits on the namespace:key

**Kind**: instance method of [<code>Limit</code>](#Limit)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> | specific settings for the Limit class |

<a name="Limit+isLimited"></a>

### *limit.isLimited()*
This method must be overridden by the child class that extends from Limit.

**Kind**: instance abstract method of [<code>Limit</code>](#Limit)  
<a name="Limit+end"></a>

### *limit.end()*
This method may be overridden by the child class that extends from Limit.
It should be used to clean up any system resources, especially those
that can cause unit tests to hang until everything shuts down cleanly.

**Kind**: instance abstract method of [<code>Limit</code>](#Limit)  
<a name="Limit.SecondsPerDay"></a>

### Limit.SecondsPerDay ⇒
Returns the number of seconds in one 24 hour period (60*60*24)

**Kind**: static property of [<code>Limit</code>](#Limit)  
**Returns**: [int] a description of the return  
<a name="Limit.mergeDefaults"></a>

### Limit.mergeDefaults()
Returns a record containing a merging of the specified options and the
default limitOptions that may be loaded from a config entry. The
defaults are values of 10 hits in 30 seconds results in a 60
minute limit.

**Kind**: static method of [<code>Limit</code>](#Limit)  
<a name="RedisLimitHandle"></a>

## RedisLimitHandle
The LimitHandle is returned from the RedisLimit and acts an as interface
to the actual limit.

**Kind**: global class  

* [RedisLimitHandle](#RedisLimitHandle)
    * [new RedisLimitHandle(limit, key, options)](#new_RedisLimitHandle_new)
    * [.isLimited()](#RedisLimitHandle+isLimited) ⇒ <code>boolean</code>
    * [.unlimit()](#RedisLimitHandle+unlimit) ⇒ <code>Promise</code>

<a name="new_RedisLimitHandle_new"></a>

### new RedisLimitHandle(limit, key, options)
Creates a handle for the specified Redis based Limit.


| Param | Type | Description |
| --- | --- | --- |
| limit | [<code>RedisLimit</code>](#RedisLimit) | the Limit wrapped by this interface |
| key | <code>string</code> | the key to limit |
| options | <code>object</code> | the options for the limit |
| options.count | <code>int</code> | the maximum number of times that an   activity may occur over a given period of time |
| options.period | <code>int</code> | the amount of time that the activity may   occur before being marked as limited (milliseconds) |
| options.duration | <code>int</code> | the amount of time to keep the activity   marked as limited (milliseconds) |

<a name="RedisLimitHandle+isLimited"></a>

### redisLimitHandle.isLimited() ⇒ <code>boolean</code>
**Kind**: instance method of [<code>RedisLimitHandle</code>](#RedisLimitHandle)  
**Returns**: <code>boolean</code> - true if limiting is active, else false  
<a name="RedisLimitHandle+unlimit"></a>

### redisLimitHandle.unlimit() ⇒ <code>Promise</code>
Release the limits.

**Kind**: instance method of [<code>RedisLimitHandle</code>](#RedisLimitHandle)  
**Returns**: <code>Promise</code> - a Promise to release the limit  
<a name="RedisLimit"></a>

## RedisLimit
The RedisLimit represent a Limit object "stored" in redis. Actually, the
Limit's key and its limiting timeout key are stored in redis, which
means these Limit types may be shared amongst processes.

**Kind**: global class  

* [RedisLimit](#RedisLimit)
    * [new RedisLimit(options)](#new_RedisLimit_new)
    * [.limit(key, options)](#RedisLimit+limit) ⇒ [<code>RedisLimitHandle</code>](#RedisLimitHandle)

<a name="new_RedisLimit_new"></a>

### new RedisLimit(options)
Creates a redis based limit object.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the parameters for the limiter |
| options.namespace | <code>string</code> | the namespace used in limitNs |
| options.limitConfig | <code>object</code> | the Limit connection parameters |
| options.limitConfig.type | <code>string</code> | the type of Limit to create   ('redis') |
| options.limitConfig.connection | <code>object</code> | the redis client   connection settings |
| options.limitConfig.connection.host | <code>string</code> | the hostname or   IP address where the redis server is running |
| options.limitConfig.connection.port | <code>int</code> | the port number   that the redis server is listening on |
| options.limitConfig.limitOptions.count | <code>int</code> | the number   of times the isLimited method may be checked within the period |
| options.limitConfig.limitOptions.period | <code>int</code> | the length of   time which the isLimited method may be checked before being limited (mS) |
| options.limitConfig.limitOptions.duration | <code>int</code> | the amount of   time the limit will be in effect (mS) |

**Example**  
```js
const Limit = require( '@leverege/limit' )
 const limiter = Limit.create( {
   namespace : 'example',
   limitConfig : {
     type : 'redis',
     connection : {
       host : '127.0.0.1',
       port : 6379,
     },
     limitOptions : { // default limit options
       count : 10,
       period : 30*1000,
       duration : 60*60*1000,
     },
   },
 } )

 // Create a limit that will allow 25 occurances over a 5 second
 // period before imposing a 60 minute limit.
 //
 const redlim = limiter.limit( 'testKey', { count : 25,
                                               period : 5000,
                                             duration : 60*60*1000 })
```
<a name="RedisLimit+limit"></a>

### redisLimit.limit(key, options) ⇒ [<code>RedisLimitHandle</code>](#RedisLimitHandle)
Limits on the key. This will not auto-prefix the key with the namespace.
To auto prefix the key, use limitNs( key ).

**Kind**: instance method of [<code>RedisLimit</code>](#RedisLimit)  
**Returns**: [<code>RedisLimitHandle</code>](#RedisLimitHandle) - a Promise that will resolve to an RedisLimitHandle.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> | the options for the limit |
| options.count | <code>int</code> | the maximum number of times that an   activity may occur over a given period of time |
| options.period | <code>int</code> | the amount of time that the activity may   occur before being marked as limited (milliseconds) |
| options.duration | <code>int</code> | the amount of time to keep the activity   marked as limited (milliseconds) |

<a name="create"></a>

## create(options)
Creates a limit of a specifed type

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the lock options |
| options.type | <code>string</code> | the type of lock to make. If unrecognized, this will throw an  exception. Possible values: 'redis', 'inMemory' |
| options.namespace | <code>string</code> | a string that will prepended (with a ':') to all lock keys  when accessing the lock using lockNS. The resulting key will be namespace:key |
| options.limitConfig | <code>object</code> | This can be an object, JSON or reference to a json/js file.  If defined, it will be expanded and merged with the other options like prefix. This allows the lock type to be controlled by an environment variable or file. |

<a name="expand"></a>

## expand()
If config exists, attempt to extract it via json or file read, then
adjust the option to look like that plus the rest.

**Kind**: global function  
