---
id: jsdocs-lock
title: Lock
---
## Classes

<dl>
<dt><a href="#LockHandle">LockHandle</a></dt>
<dd><p>The LockHandle is returned from the InMemoryLock and acts
as interface to the actual lock</p>
</dd>
<dt><a href="#InMemoryLock">InMemoryLock</a></dt>
<dd><p>The InMemoryLock is represents a per process lock</p>
</dd>
<dt><a href="#Lock">Lock</a></dt>
<dd></dd>
<dt><a href="#LockHandle">LockHandle</a></dt>
<dd><p>The LockHandle is returned from the RedisLock and acts
as interface to the actual lock.</p>
</dd>
<dt><a href="#RedisLock">RedisLock</a></dt>
<dd><p>The RedisLock is represents lock shareable between processes.</p>
</dd>
<dt><a href="#LockHandle">LockHandle</a></dt>
<dd><p>The LockHandle is returned from the InMemoryLock and acts
as interface to the actual lock</p>
</dd>
<dt><a href="#InMemoryLock">InMemoryLock</a></dt>
<dd><p>The InMemoryLock is represents a per process lock</p>
</dd>
<dt><a href="#Lock">Lock</a></dt>
<dd></dd>
<dt><a href="#LockHandle">LockHandle</a></dt>
<dd><p>The LockHandle is returned from the RedisLock and acts
as interface to the actual lock.</p>
</dd>
<dt><a href="#RedisLock">RedisLock</a></dt>
<dd><p>The RedisLock is represents lock shareable between processes.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#create">create(options)</a></dt>
<dd><p>Creates a lock of a specifed type</p>
</dd>
<dt><a href="#wait">wait()</a></dt>
<dd><p>A promise version of setTimeout</p>
</dd>
<dt><a href="#create">create(options)</a></dt>
<dd><p>Creates a lock of a specifed type</p>
</dd>
<dt><a href="#wait">wait()</a></dt>
<dd><p>A promise version of setTimeout</p>
</dd>
</dl>

<a name="LockHandle"></a>

## LockHandle
The LockHandle is returned from the InMemoryLock and acts
as interface to the actual lock

**Kind**: global class  

* [LockHandle](#LockHandle)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="InMemoryLock"></a>

## InMemoryLock
The InMemoryLock is represents a per process lock

**Kind**: global class  

* [InMemoryLock](#InMemoryLock)
    * [new InMemoryLock(options)](#new_InMemoryLock_new)
    * [new InMemoryLock(options)](#new_InMemoryLock_new)
    * [.lock(key, options)](#InMemoryLock+lock) ⇒ <code>Promise</code>
    * [.obtainLock(key, options, count)](#InMemoryLock+obtainLock)
    * [.lock(key, options)](#InMemoryLock+lock) ⇒ <code>Promise</code>
    * [.obtainLock(key, options, count)](#InMemoryLock+obtainLock)

<a name="new_InMemoryLock_new"></a>

### new InMemoryLock(options)
Creates an InMemoryLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.retry | <code>int</code> | the number of times to retry to claim the lock |
| options.delay | <code>int</code> | the delay in milliseconds between attempts to claim the lock |

<a name="new_InMemoryLock_new"></a>

### new InMemoryLock(options)
Creates an InMemoryLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.retry | <code>int</code> | the number of times to retry to claim the lock |
| options.delay | <code>int</code> | the delay in milliseconds between attempts to claim the lock |

<a name="InMemoryLock+lock"></a>

### inMemoryLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="InMemoryLock+obtainLock"></a>

### inMemoryLock.obtainLock(key, options, count)
This will attempt to obtain a lock until the count
exceeds the max retries.

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the lock |
| options | <code>object</code> | the options object |
| options.ttl | <code>int</code> | the time to keep the lock in milliseconds |
| count | <code>int</code> | the number of times the obtain lock has been attempted |

<a name="InMemoryLock+lock"></a>

### inMemoryLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="InMemoryLock+obtainLock"></a>

### inMemoryLock.obtainLock(key, options, count)
This will attempt to obtain a lock until the count
exceeds the max retries.

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the lock |
| options | <code>object</code> | the options object |
| options.ttl | <code>int</code> | the time to keep the lock in milliseconds |
| count | <code>int</code> | the number of times the obtain lock has been attempted |

<a name="Lock"></a>

## Lock
**Kind**: global class  

* [Lock](#Lock)
    * [new Lock()](#new_Lock_new)
    * [new Lock()](#new_Lock_new)
    * [.stop()](#Lock+stop) ⇒ <code>Promise</code>
    * [.getKey(namespace)](#Lock+getKey)
    * [.lock(key, options)](#Lock+lock) ⇒ <code>Promise</code>
    * [.lockNs(key, options)](#Lock+lockNs)
    * [.stop()](#Lock+stop) ⇒ <code>Promise</code>
    * [.getKey(namespace)](#Lock+getKey)
    * [.lock(key, options)](#Lock+lock) ⇒ <code>Promise</code>
    * [.lockNs(key, options)](#Lock+lockNs)

<a name="new_Lock_new"></a>

### new Lock()
Creates a Cache object


| Param | Type | Description |
| --- | --- | --- |
| options.namespace | <code>string</code> | the namespace string to use in the xxxNs methods. Defaults to  'app' |

<a name="new_Lock_new"></a>

### new Lock()
Creates a Cache object


| Param | Type | Description |
| --- | --- | --- |
| options.namespace | <code>string</code> | the namespace string to use in the xxxNs methods. Defaults to  'app' |

<a name="Lock+stop"></a>

### lock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>Lock</code>](#Lock)  
<a name="Lock+getKey"></a>

### lock.getKey(namespace)
Returns the actual key to use. This will combine
the namespace + ':' + key if a namespace is available.

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Oaram**: <code>string</code> key an key to prefix with namespace  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| namespace | <code>string</code> | <code>null</code> | if supplied, this will be used as the namespace. Otherwise, the namespace supplied in the options will be used. |

<a name="Lock+lock"></a>

### lock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="Lock+lockNs"></a>

### lock.lockNs(key, options)
Locks on the namespace:key

**Kind**: instance method of [<code>Lock</code>](#Lock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds   * @return {Promise} a Promise that will resolve with a Lock Handle. The LockHandle has two methods: unlock : Release the lock, returns a Promise extend( timeMilliseconds ) : extend the lock for a time from now. |

<a name="Lock+stop"></a>

### lock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>Lock</code>](#Lock)  
<a name="Lock+getKey"></a>

### lock.getKey(namespace)
Returns the actual key to use. This will combine
the namespace + ':' + key if a namespace is available.

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Oaram**: <code>string</code> key an key to prefix with namespace  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| namespace | <code>string</code> | <code>null</code> | if supplied, this will be used as the namespace. Otherwise, the namespace supplied in the options will be used. |

<a name="Lock+lock"></a>

### lock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="Lock+lockNs"></a>

### lock.lockNs(key, options)
Locks on the namespace:key

**Kind**: instance method of [<code>Lock</code>](#Lock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds   * @return {Promise} a Promise that will resolve with a Lock Handle. The LockHandle has two methods: unlock : Release the lock, returns a Promise extend( timeMilliseconds ) : extend the lock for a time from now. |

<a name="LockHandle"></a>

## LockHandle
The LockHandle is returned from the RedisLock and acts
as interface to the actual lock.

**Kind**: global class  

* [LockHandle](#LockHandle)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="RedisLock"></a>

## RedisLock
The RedisLock is represents lock shareable between processes.

**Kind**: global class  

* [RedisLock](#RedisLock)
    * [new RedisLock(options)](#new_RedisLock_new)
    * [new RedisLock(options)](#new_RedisLock_new)
    * [.stop()](#RedisLock+stop) ⇒ <code>Promise</code>
    * [.lock(key, options)](#RedisLock+lock) ⇒ <code>Promise</code>
    * [.stop()](#RedisLock+stop) ⇒ <code>Promise</code>
    * [.lock(key, options)](#RedisLock+lock) ⇒ <code>Promise</code>

<a name="new_RedisLock_new"></a>

### new RedisLock(options)
Creates an RedisLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.connection | <code>object</code> | the redis connection object |
| options.lockOptions | <code>object</code> | the options for the lock |
| options.lockOptions.retryCount | <code>int</code> | the number of times to try to claim  the lock. If negative one, this will try forever. |
| options.lockOptions.retryDelay | <code>int</code> | the time in ms between attempts |
| options.lockOptions.retryJitter | <code>int</code> | the max time in ms randomly added to retries |
| options.lockOptions.driftFactor | <code>number</code> | the expected clock drift in ms |

<a name="new_RedisLock_new"></a>

### new RedisLock(options)
Creates an RedisLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.connection | <code>object</code> | the redis connection object |
| options.lockOptions | <code>object</code> | the options for the lock |
| options.lockOptions.retryCount | <code>int</code> | the number of times to try to claim  the lock. If negative one, this will try forever. |
| options.lockOptions.retryDelay | <code>int</code> | the time in ms between attempts |
| options.lockOptions.retryJitter | <code>int</code> | the max time in ms randomly added to retries |
| options.lockOptions.driftFactor | <code>number</code> | the expected clock drift in ms |

<a name="RedisLock+stop"></a>

### redisLock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
<a name="RedisLock+lock"></a>

### redisLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="RedisLock+stop"></a>

### redisLock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
<a name="RedisLock+lock"></a>

### redisLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="LockHandle"></a>

## LockHandle
The LockHandle is returned from the InMemoryLock and acts
as interface to the actual lock

**Kind**: global class  

* [LockHandle](#LockHandle)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="InMemoryLock"></a>

## InMemoryLock
The InMemoryLock is represents a per process lock

**Kind**: global class  

* [InMemoryLock](#InMemoryLock)
    * [new InMemoryLock(options)](#new_InMemoryLock_new)
    * [new InMemoryLock(options)](#new_InMemoryLock_new)
    * [.lock(key, options)](#InMemoryLock+lock) ⇒ <code>Promise</code>
    * [.obtainLock(key, options, count)](#InMemoryLock+obtainLock)
    * [.lock(key, options)](#InMemoryLock+lock) ⇒ <code>Promise</code>
    * [.obtainLock(key, options, count)](#InMemoryLock+obtainLock)

<a name="new_InMemoryLock_new"></a>

### new InMemoryLock(options)
Creates an InMemoryLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.retry | <code>int</code> | the number of times to retry to claim the lock |
| options.delay | <code>int</code> | the delay in milliseconds between attempts to claim the lock |

<a name="new_InMemoryLock_new"></a>

### new InMemoryLock(options)
Creates an InMemoryLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.retry | <code>int</code> | the number of times to retry to claim the lock |
| options.delay | <code>int</code> | the delay in milliseconds between attempts to claim the lock |

<a name="InMemoryLock+lock"></a>

### inMemoryLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="InMemoryLock+obtainLock"></a>

### inMemoryLock.obtainLock(key, options, count)
This will attempt to obtain a lock until the count
exceeds the max retries.

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the lock |
| options | <code>object</code> | the options object |
| options.ttl | <code>int</code> | the time to keep the lock in milliseconds |
| count | <code>int</code> | the number of times the obtain lock has been attempted |

<a name="InMemoryLock+lock"></a>

### inMemoryLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="InMemoryLock+obtainLock"></a>

### inMemoryLock.obtainLock(key, options, count)
This will attempt to obtain a lock until the count
exceeds the max retries.

**Kind**: instance method of [<code>InMemoryLock</code>](#InMemoryLock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the lock |
| options | <code>object</code> | the options object |
| options.ttl | <code>int</code> | the time to keep the lock in milliseconds |
| count | <code>int</code> | the number of times the obtain lock has been attempted |

<a name="Lock"></a>

## Lock
**Kind**: global class  

* [Lock](#Lock)
    * [new Lock()](#new_Lock_new)
    * [new Lock()](#new_Lock_new)
    * [.stop()](#Lock+stop) ⇒ <code>Promise</code>
    * [.getKey(namespace)](#Lock+getKey)
    * [.lock(key, options)](#Lock+lock) ⇒ <code>Promise</code>
    * [.lockNs(key, options)](#Lock+lockNs)
    * [.stop()](#Lock+stop) ⇒ <code>Promise</code>
    * [.getKey(namespace)](#Lock+getKey)
    * [.lock(key, options)](#Lock+lock) ⇒ <code>Promise</code>
    * [.lockNs(key, options)](#Lock+lockNs)

<a name="new_Lock_new"></a>

### new Lock()
Creates a Cache object


| Param | Type | Description |
| --- | --- | --- |
| options.namespace | <code>string</code> | the namespace string to use in the xxxNs methods. Defaults to  'app' |

<a name="new_Lock_new"></a>

### new Lock()
Creates a Cache object


| Param | Type | Description |
| --- | --- | --- |
| options.namespace | <code>string</code> | the namespace string to use in the xxxNs methods. Defaults to  'app' |

<a name="Lock+stop"></a>

### lock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>Lock</code>](#Lock)  
<a name="Lock+getKey"></a>

### lock.getKey(namespace)
Returns the actual key to use. This will combine
the namespace + ':' + key if a namespace is available.

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Oaram**: <code>string</code> key an key to prefix with namespace  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| namespace | <code>string</code> | <code>null</code> | if supplied, this will be used as the namespace. Otherwise, the namespace supplied in the options will be used. |

<a name="Lock+lock"></a>

### lock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="Lock+lockNs"></a>

### lock.lockNs(key, options)
Locks on the namespace:key

**Kind**: instance method of [<code>Lock</code>](#Lock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds   * @return {Promise} a Promise that will resolve with a Lock Handle. The LockHandle has two methods: unlock : Release the lock, returns a Promise extend( timeMilliseconds ) : extend the lock for a time from now. |

<a name="Lock+stop"></a>

### lock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>Lock</code>](#Lock)  
<a name="Lock+getKey"></a>

### lock.getKey(namespace)
Returns the actual key to use. This will combine
the namespace + ':' + key if a namespace is available.

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Oaram**: <code>string</code> key an key to prefix with namespace  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| namespace | <code>string</code> | <code>null</code> | if supplied, this will be used as the namespace. Otherwise, the namespace supplied in the options will be used. |

<a name="Lock+lock"></a>

### lock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>Lock</code>](#Lock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="Lock+lockNs"></a>

### lock.lockNs(key, options)
Locks on the namespace:key

**Kind**: instance method of [<code>Lock</code>](#Lock)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds   * @return {Promise} a Promise that will resolve with a Lock Handle. The LockHandle has two methods: unlock : Release the lock, returns a Promise extend( timeMilliseconds ) : extend the lock for a time from now. |

<a name="LockHandle"></a>

## LockHandle
The LockHandle is returned from the RedisLock and acts
as interface to the actual lock.

**Kind**: global class  

* [LockHandle](#LockHandle)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [new LockHandle(memLock, key, ttl)](#new_LockHandle_new)
    * [new LockHandle(lock)](#new_LockHandle_new)
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>
    * [.unlock()](#LockHandle+unlock) ⇒ <code>Promise</code>
    * [.extend(time)](#LockHandle+extend) ⇒ <code>Promise</code>

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="new_LockHandle_new"></a>

### new LockHandle(memLock, key, ttl)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| memLock | [<code>InMemoryLock</code>](#InMemoryLock) | the memory lock |
| key | <code>string</code> | the key to lock |
| ttl | <code>int</code> | the time to keep the lock |

<a name="new_LockHandle_new"></a>

### new LockHandle(lock)
Creates the lock handle


| Param | Type | Description |
| --- | --- | --- |
| lock | <code>lock</code> | the RedLock lock object |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="LockHandle+unlock"></a>

### lockHandle.unlock() ⇒ <code>Promise</code>
Release the lock.

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise to release the lock  
<a name="LockHandle+extend"></a>

### lockHandle.extend(time) ⇒ <code>Promise</code>
Extend the lock's time

**Kind**: instance method of [<code>LockHandle</code>](#LockHandle)  
**Returns**: <code>Promise</code> - a Promise that returns this Lock object  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>int</code> | the time in milliseconds to set the lock. This will set the lock's expiration to be Date.now() + time |

<a name="RedisLock"></a>

## RedisLock
The RedisLock is represents lock shareable between processes.

**Kind**: global class  

* [RedisLock](#RedisLock)
    * [new RedisLock(options)](#new_RedisLock_new)
    * [new RedisLock(options)](#new_RedisLock_new)
    * [.stop()](#RedisLock+stop) ⇒ <code>Promise</code>
    * [.lock(key, options)](#RedisLock+lock) ⇒ <code>Promise</code>
    * [.stop()](#RedisLock+stop) ⇒ <code>Promise</code>
    * [.lock(key, options)](#RedisLock+lock) ⇒ <code>Promise</code>

<a name="new_RedisLock_new"></a>

### new RedisLock(options)
Creates an RedisLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.connection | <code>object</code> | the redis connection object |
| options.lockOptions | <code>object</code> | the options for the lock |
| options.lockOptions.retryCount | <code>int</code> | the number of times to try to claim  the lock. If negative one, this will try forever. |
| options.lockOptions.retryDelay | <code>int</code> | the time in ms between attempts |
| options.lockOptions.retryJitter | <code>int</code> | the max time in ms randomly added to retries |
| options.lockOptions.driftFactor | <code>number</code> | the expected clock drift in ms |

<a name="new_RedisLock_new"></a>

### new RedisLock(options)
Creates an RedisLock.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options for the lock |
| options.namespace | <code>string</code> | the namespace used in lockNS. |
| options.connection | <code>object</code> | the redis connection object |
| options.lockOptions | <code>object</code> | the options for the lock |
| options.lockOptions.retryCount | <code>int</code> | the number of times to try to claim  the lock. If negative one, this will try forever. |
| options.lockOptions.retryDelay | <code>int</code> | the time in ms between attempts |
| options.lockOptions.retryJitter | <code>int</code> | the max time in ms randomly added to retries |
| options.lockOptions.driftFactor | <code>number</code> | the expected clock drift in ms |

<a name="RedisLock+stop"></a>

### redisLock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
<a name="RedisLock+lock"></a>

### redisLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="RedisLock+stop"></a>

### redisLock.stop() ⇒ <code>Promise</code>
Destroys all resources

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
<a name="RedisLock+lock"></a>

### redisLock.lock(key, options) ⇒ <code>Promise</code>
Locks on the key. This will not auto-prefix the key
with the namespace. To auto prefix the key, use lockNs( key )

**Kind**: instance method of [<code>RedisLock</code>](#RedisLock)  
**Returns**: <code>Promise</code> - a Promise that will resolve with a Lock Handle.
The LockHandle has two methods:
unlock : Release the lock, returns a Promise
extend( timeMilliseconds ) : extend the lock for a time from now.  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the key to lookup |
| options | <code>object</code> \| <code>int</code> | either a time in milliseconds to keep the lock or and object containing the options for the lock |
| options.ttl | <code>int</code> | time to keep lock in milliseconds |

<a name="create"></a>

## create(options)
Creates a lock of a specifed type

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the lock options |
| options.type | <code>string</code> | the type of lock to make. If unrecognized,  this will throw an exception. Possible values: 'redis', 'inMemory' |
| options.namespace | <code>string</code> | a string that will prepended (with a ':') to all lock keys  when accessing the lock using lockNS. The resulting key will be namespace:key |
| options.lockConfig | <code>object</code> | This can be an object, JSON or reference to a json/js file. If defined, it will be expanded and merged with the other options like prefix. This allows the lock type to be controlled by an environment variable or file. |

<a name="wait"></a>

## wait()
A promise version of setTimeout

**Kind**: global function  
<a name="create"></a>

## create(options)
Creates a lock of a specifed type

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the lock options |
| options.type | <code>string</code> | the type of lock to make. If unrecognized,  this will throw an exception. Possible values: 'redis', 'inMemory' |
| options.namespace | <code>string</code> | a string that will prepended (with a ':') to all lock keys  when accessing the lock using lockNS. The resulting key will be namespace:key |
| options.lockConfig | <code>object</code> | This can be an object, JSON or reference to a json/js file. If defined, it will be expanded and merged with the other options like prefix. This allows the lock type to be controlled by an environment variable or file. |

<a name="wait"></a>

## wait()
A promise version of setTimeout

**Kind**: global function  
