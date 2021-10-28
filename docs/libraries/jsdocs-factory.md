---
id: jsdocs-factory
title: Factory
---
## Classes

<dl>
<dt><a href="#Factory">Factory</a></dt>
<dd><p>The Factory allows the lookup and construction of objects/results based on
a type. A sample usage is:</p>
<p>const f = new Factory( )
f.add( &#39;myType&#39;, MyTypeMsg )
f.add( &#39;myOtherType&#39;, MyOtherTypeMsg )
const msg = f.create( { type : &#39;myOtherType&#39;, value : 5 } )
// msg is equivalent to new MyOtherMsg( { type : &#39;myOtherType&#39;, value : 5 } )</p>
<p>Strategies when create( obj, arg1, argN ) is called. Below, clzz equals get( obj )
  ALL (default): 
    new clzz( obj, arg1, argN ) // clzz is a class
    clzz( obj, arg1, argN )     // clzz is a function
  NONE: 
    new clzz( )
    clzz( )
  ARGS: 
    new clzz( arg1, argN )
    clzz( arg1, argN )
  MERGE: 
    const alt1 = { model : obj, ...arg1 }
    new clzz( alt1, argN )
    clzz( alt1, argN )
  LOOKUP: 
    clzz
  <function>:
    return strategy( this, clzz, obj, arg1, argN )</p>
<p>ALL is equivalent to ARGS is create( model, model, arg1, argN ) is called</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#allStrategy">allStrategy(factory, clzz, typeOrObject)</a> ⇒</dt>
<dd><p>A strategy where the args passed into the constructor/function
are ( typeOrObject, arg1, arg2, ...etc... )</p>
</dd>
<dt><a href="#noneStrategy">noneStrategy(factory, clzz, typeOrObject)</a> ⇒</dt>
<dd><p>A strategy where no args passed into the constructor/function</p>
</dd>
<dt><a href="#argsStrategy">argsStrategy(factory, clzz, typeOrObject)</a> ⇒</dt>
<dd><p>A strategy where the args passed into the constructor/function
are ( arg1, arg2, ...etc... )</p>
</dd>
<dt><a href="#lookupStrategy">lookupStrategy(factory, clzz, typeOrObject)</a> ⇒</dt>
<dd><p>A strategy where clzz is returned</p>
</dd>
<dt><a href="#mergeStrategy">mergeStrategy(key)</a> ⇒</dt>
<dd><p>Creates a strategy where the args passed into the constructor/function
are ( MOD, arg2, ...etc... ), where MOD is { [key] : typeOrObject, ...args[0] }</p>
</dd>
<dt><a href="#reactStrategy">reactStrategy(React, propKey)</a> ⇒</dt>
<dd><p>Creates a strategy for createing react elements. The clzz object given to the
strategy is assumed to be a React.Component or React pure component/function.
the typeOrObejct will be merge into the props at the specified propKey.</p>
</dd>
</dl>

<a name="Factory"></a>

## Factory
The Factory allows the lookup and construction of objects/results based on
a type. A sample usage is:

const f = new Factory( )
f.add( 'myType', MyTypeMsg )
f.add( 'myOtherType', MyOtherTypeMsg )
const msg = f.create( { type : 'myOtherType', value : 5 } )
// msg is equivalent to new MyOtherMsg( { type : 'myOtherType', value : 5 } )



Strategies when create( obj, arg1, argN ) is called. Below, clzz equals get( obj )
  ALL (default): 
    new clzz( obj, arg1, argN ) // clzz is a class
    clzz( obj, arg1, argN )     // clzz is a function
  NONE: 
    new clzz( )
    clzz( )
  ARGS: 
    new clzz( arg1, argN )
    clzz( arg1, argN )
  MERGE: 
    const alt1 = { model : obj, ...arg1 }
    new clzz( alt1, argN )
    clzz( alt1, argN )
  LOOKUP: 
    clzz
  <function>:
    return strategy( this, clzz, obj, arg1, argN )

ALL is equivalent to ARGS is create( model, model, arg1, argN ) is called

**Kind**: global class  

* [Factory](#Factory)
    * [new Factory(options, name, typeKey, [registry], defaultObject, strategy)](#new_Factory_new)
    * [.add(type, obj)](#Factory+add)
    * [.remove(type)](#Factory+remove)
    * [.getType(typeOrObj)](#Factory+getType) ⇒
    * [.has()](#Factory+has) ⇒ <code>boolean</code>
    * [.get(type)](#Factory+get) ⇒ <code>any</code>
    * [.getAll()](#Factory+getAll) ⇒ <code>object</code>
    * [.create(...args)](#Factory+create) ⇒ <code>any</code>

<a name="new_Factory_new"></a>

### new Factory(options, name, typeKey, [registry], defaultObject, strategy)
Create a factory object.


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> \| <code>function</code> | the options for the factory. If this is a function, it is the strategy. |
| name | <code>string</code> | the name of the factory |
| typeKey | <code>string</code> | the property to look at when determining the type of an object. Defaults to 'type' |
| [registry] | <code>object</code> | a type to obj map. Using this is the same as calling add for each key/value pair |
| defaultObject | <code>any</code> | If a lookup results in null/undefined, this object will be used |
| strategy | <code>function</code> | a function( factory, clzz, typeOrClass, ...args ) invoked to  create the returned object. (Defaults to Factory.ALL) |

<a name="Factory+add"></a>

### factory.add(type, obj)
Registers an object to support the type. If there
is already an object registered for the type, this
will throw an exception unless overwrite is set to true

**Kind**: instance method of [<code>Factory</code>](#Factory)  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | the type to register |
| obj | <code>any</code> | the thing to register for the type |

<a name="Factory+remove"></a>

### factory.remove(type)
Removes a registered type.

**Kind**: instance method of [<code>Factory</code>](#Factory)  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | the type to remove |

<a name="Factory+getType"></a>

### factory.getType(typeOrObj) ⇒
If typeOrObj is an object, this will extract the type from 
the object usin the typeKey field. Otherwise, typeOrObject
will be returned

**Kind**: instance method of [<code>Factory</code>](#Factory)  
**Returns**: the type  

| Param | Type | Description |
| --- | --- | --- |
| typeOrObj | <code>any</code> | the type or an object containing the type |

<a name="Factory+has"></a>

### factory.has() ⇒ <code>boolean</code>
Return true if an object is registered to suppor the type.

**Kind**: instance method of [<code>Factory</code>](#Factory)  
**Returns**: <code>boolean</code> - true if there is a registered object  
<a name="Factory+get"></a>

### factory.get(type) ⇒ <code>any</code>
Returns the function/class registered to manager
the object of the specified type.

**Kind**: instance method of [<code>Factory</code>](#Factory)  
**Returns**: <code>any</code> - the thing registered at that that location  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>object</code> \| <code>string</code> | If this is a string, it is used as the type to lookup. If it is an object, the typeKey field of the object is used to do the lookup. |

<a name="Factory+getAll"></a>

### factory.getAll() ⇒ <code>object</code>
Returns an object containing the mapping between
the types and the things registered to suppor that
type.

**Kind**: instance method of [<code>Factory</code>](#Factory)  
**Returns**: <code>object</code> - the mapping  
<a name="Factory+create"></a>

### factory.create(...args) ⇒ <code>any</code>
Creates the thing used to support the typeOfObj.

**Kind**: instance method of [<code>Factory</code>](#Factory)  
**Returns**: <code>any</code> - the constructed item  
**Oaram**: <code>object\|string</code> typeOrObj usually the object we're creating
a handler for, but in some strategies, this might just be the type  

| Param | Type | Description |
| --- | --- | --- |
| ...args | <code>array</code> | the rest of the params |

<a name="allStrategy"></a>

## allStrategy(factory, clzz, typeOrObject) ⇒
A strategy where the args passed into the constructor/function
are ( typeOrObject, arg1, arg2, ...etc... )

**Kind**: global function  
**Returns**: the new class, the result of the function, or clzz if
clzz is not a class or function.  

| Param | Type | Description |
| --- | --- | --- |
| factory | [<code>Factory</code>](#Factory) | the invoking factory |
| clzz | <code>Class</code> \| <code>function</code> | the registered |
| typeOrObject | <code>object</code> \| <code>string</code> | the object used to lookup the clzz |
| ...args | <code>array</code> | the rest of the args |

<a name="noneStrategy"></a>

## noneStrategy(factory, clzz, typeOrObject) ⇒
A strategy where no args passed into the constructor/function

**Kind**: global function  
**Returns**: the new class, the result of the function, or clzz if
clzz is not a class or function.  

| Param | Type | Description |
| --- | --- | --- |
| factory | [<code>Factory</code>](#Factory) | the invoking factory |
| clzz | <code>Class</code> \| <code>function</code> | the registered |
| typeOrObject | <code>object</code> \| <code>string</code> | the object used to lookup the clzz |
| ...args | <code>array</code> | the rest of the args |

<a name="argsStrategy"></a>

## argsStrategy(factory, clzz, typeOrObject) ⇒
A strategy where the args passed into the constructor/function
are ( arg1, arg2, ...etc... )

**Kind**: global function  
**Returns**: the new class, the result of the function, or clzz if
clzz is not a class or function.  

| Param | Type | Description |
| --- | --- | --- |
| factory | [<code>Factory</code>](#Factory) | the invoking factory |
| clzz | <code>Class</code> \| <code>function</code> | the registered |
| typeOrObject | <code>object</code> \| <code>string</code> | the object used to lookup the clzz |
| ...args | <code>array</code> | the rest of the args |

<a name="lookupStrategy"></a>

## lookupStrategy(factory, clzz, typeOrObject) ⇒
A strategy where clzz is returned

**Kind**: global function  
**Returns**: the new class, the result of the function, or clzz if
clzz is not a class or function.  

| Param | Type | Description |
| --- | --- | --- |
| factory | [<code>Factory</code>](#Factory) | the invoking factory |
| clzz | <code>Class</code> \| <code>function</code> | the registered |
| typeOrObject | <code>object</code> \| <code>string</code> | the object used to lookup the clzz |
| ...args | <code>array</code> | the rest of the args |

<a name="mergeStrategy"></a>

## mergeStrategy(key) ⇒
Creates a strategy where the args passed into the constructor/function
are ( MOD, arg2, ...etc... ), where MOD is { [key] : typeOrObject, ...args[0] }

**Kind**: global function  
**Returns**: the new merge strategy  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| key | <code>string</code> | <code>&quot;model&quot;</code> | the the merge key |

<a name="reactStrategy"></a>

## reactStrategy(React, propKey) ⇒
Creates a strategy for createing react elements. The clzz object given to the
strategy is assumed to be a React.Component or React pure component/function.
the typeOrObejct will be merge into the props at the specified propKey.

**Kind**: global function  
**Returns**: the react element  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| React | <code>React</code> |  | the React library |
| propKey | <code>string</code> \| <code>false</code> | <code>&quot;model&quot;</code> | if this is a string, the typeOrObject will be merged into the props at that key. Otherwise, it will not be supplied |

