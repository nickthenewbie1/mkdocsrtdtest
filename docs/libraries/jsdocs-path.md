---
id: jsdocs-path
title: Path
---
## Functions

<dl>
<dt><a href="#set">set()</a></dt>
<dd><p>Sets the value on the object at the path. This will
create intermediate objects as necessary.</p>
</dd>
<dt><a href="#delete">delete(obj)</a> ⇒ <code>boolean</code></dt>
<dd><p>Deletes the value on the object at the path. This will
not create intermediate.</p>
</dd>
<dt><a href="#copy">copy()</a></dt>
<dd><p>Creates a shallow copy of the object and all the paths
References to objects that are not in the path will reference
the same object. If the value is not undefined, it will be
set on the copied object.</p>
</dd>
</dl>

<a name="set"></a>

## set()
Sets the value on the object at the path. This will
create intermediate objects as necessary.

**Kind**: global function  
<a name="delete"></a>

## delete(obj) ⇒ <code>boolean</code>
Deletes the value on the object at the path. This will
not create intermediate.

**Kind**: global function  
**Returns**: <code>boolean</code> - true if a delete occurred  

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | the object to remove the path from |

<a name="copy"></a>

## copy()
Creates a shallow copy of the object and all the paths
References to objects that are not in the path will reference
the same object. If the value is not undefined, it will be
set on the copied object.

**Kind**: global function  
