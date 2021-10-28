---
id: jsdocs-value-cache
title: Value Cache
---
## Classes

<dl>
<dt><a href="#ValueCache">ValueCache</a></dt>
<dd><p>The ValueCache holds one value and the variables
used to calculate the value. To get the value,
call valueCache.value after checking that isSame()
returns true.</p>
</dd>
<dt><a href="#ValuesCache">ValuesCache</a></dt>
<dd><p>ValuesCache manages many ValueCache objects with names
for convenience.</p>
</dd>
</dl>

<a name="ValueCache"></a>

## ValueCache
The ValueCache holds one value and the variables
used to calculate the value. To get the value,
call valueCache.value after checking that isSame()
returns true.

**Kind**: global class  

* [ValueCache](#ValueCache)
    * [.isSame(...conditions)](#ValueCache+isSame) ⇒ <code>boolean</code>
    * [.set(value, ...the)](#ValueCache+set) ⇒ <code>any</code>
    * [.clear()](#ValueCache+clear)
    * [.calc(compute, ...conditions)](#ValueCache+calc) ⇒ <code>any</code>

<a name="ValueCache+isSame"></a>

### valueCache.isSame(...conditions) ⇒ <code>boolean</code>
Returns true if the supplied conditions
are the same as the ones given last time

**Kind**: instance method of [<code>ValueCache</code>](#ValueCache)  
**Returns**: <code>boolean</code> - true if the cached value can be used  

| Param | Type | Description |
| --- | --- | --- |
| ...conditions | <code>any</code> | the variables used to decide whether or not the cached value can be reused |

<a name="ValueCache+set"></a>

### valueCache.set(value, ...the) ⇒ <code>any</code>
Sets the cached values and the variable used
to compute it. The value is returned

**Kind**: instance method of [<code>ValueCache</code>](#ValueCache)  
**Returns**: <code>any</code> - the value  

| Param | Type | Description |
| --- | --- | --- |
| value | <code>any</code> | the value to cache |
| ...the | <code>any</code> | variables used to compute the value |

<a name="ValueCache+clear"></a>

### valueCache.clear()
Clears the cached value and the conditions

**Kind**: instance method of [<code>ValueCache</code>](#ValueCache)  
<a name="ValueCache+calc"></a>

### valueCache.calc(compute, ...conditions) ⇒ <code>any</code>
Optional way of using ValueCache to check and compute in one step

**Kind**: instance method of [<code>ValueCache</code>](#ValueCache)  
**Returns**: <code>any</code> - either the cached value or the newly computed one  

| Param | Type | Description |
| --- | --- | --- |
| compute | <code>function</code> | a function of form function( ...conditions ) that computes and returns the value |
| ...conditions | <code>any</code> | the set of conditions that define the value |

<a name="ValuesCache"></a>

## ValuesCache
ValuesCache manages many ValueCache objects with names
for convenience.

**Kind**: global class  

* [ValuesCache](#ValuesCache)
    * [.cache(key)](#ValuesCache+cache) ⇒ [<code>ValueCache</code>](#ValueCache)
    * [.isSame(key, ...conditions)](#ValuesCache+isSame) ⇒ <code>boolean</code>
    * [.value(key)](#ValuesCache+value) ⇒ <code>any</code>
    * [.set(key, value, ...the)](#ValuesCache+set) ⇒ <code>any</code>
    * [.clear(key)](#ValuesCache+clear)
    * [.clearAll()](#ValuesCache+clearAll)
    * [.calc(the, compute, ...conditions)](#ValuesCache+calc) ⇒ <code>any</code>

<a name="ValuesCache+cache"></a>

### valuesCache.cache(key) ⇒ [<code>ValueCache</code>](#ValueCache)
Returns, creating if necessary the ValueCache for
the given key

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
**Returns**: [<code>ValueCache</code>](#ValueCache) - the ValueCache with the name  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the ValueCache to get/create |

<a name="ValuesCache+isSame"></a>

### valuesCache.isSame(key, ...conditions) ⇒ <code>boolean</code>
Returns true if the supplied conditions are the same as the 
ones given last time

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
**Returns**: <code>boolean</code> - true if the cached value can be used  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the ValueCache to check |
| ...conditions | <code>any</code> | the variables used to decide whether or not the cached value can be reused |

<a name="ValuesCache+value"></a>

### valuesCache.value(key) ⇒ <code>any</code>
Returns the last cachec value for the given key

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
**Returns**: <code>any</code> - the value  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the ValueCache whose value should be returned |

<a name="ValuesCache+set"></a>

### valuesCache.set(key, value, ...the) ⇒ <code>any</code>
Sets the named cached values and the variable used
to compute it. The value is returned

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
**Returns**: <code>any</code> - the value  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the ValueCache to set |
| value | <code>any</code> | the value to cache |
| ...the | <code>any</code> | variables used to compute the value |

<a name="ValuesCache+clear"></a>

### valuesCache.clear(key)
Clears the cached value and the conditions stored
at the given key

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the ValueCache to clear |

<a name="ValuesCache+clearAll"></a>

### valuesCache.clearAll()
Clears all of the cached values and their conditions

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
<a name="ValuesCache+calc"></a>

### valuesCache.calc(the, compute, ...conditions) ⇒ <code>any</code>
Optional way of using ValuesCache to check and compute in one step

**Kind**: instance method of [<code>ValuesCache</code>](#ValuesCache)  
**Returns**: <code>any</code> - either the cached value or the newly computed one  

| Param | Type | Description |
| --- | --- | --- |
| the | <code>string</code> | name of the value to cache |
| compute | <code>function</code> | a function of form function( ...conditions ) that computes and returns the value |
| ...conditions | <code>any</code> | the set of conditions that define the value |

