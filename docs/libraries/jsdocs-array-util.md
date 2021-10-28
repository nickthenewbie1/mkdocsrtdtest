---
id: jsdocs-array-util
title: Array Util
---
## Functions

<dl>
<dt><a href="#index returns the first index of the array where the key of the element equals the value">index returns the first index of the array where the key of the element equals the value(arr, key, value, from)</a></dt>
<dd></dd>
<dt><a href="#find returns the first element of the array where the key of the element equals the value">find returns the first element of the array where the key of the element equals the value(arr, key, value, from)</a></dt>
<dd></dd>
<dt><a href="#replace returns the first index of the array where the key of the element equals the value after replacing it with elem">replace returns the first index of the array where the key of the element equals the value after replacing it with elem(arr, key, value, elem, from)</a></dt>
<dd></dd>
<dt><a href="#remove returns the first index of the array where the key of the element equals the value after removing it">remove returns the first index of the array where the key of the element equals the value after removing it(arr, key, value, from)</a></dt>
<dd></dd>
<dt><a href="#removeAll returns an array of all instances where the value was found after removing them from the original array">removeAll returns an array of all instances where the value was found after removing them from the original array(arr, key, value, from)</a></dt>
<dd></dd>
<dt><a href="#findRemove returns the first instance where the value was found after removing them from the original array">findRemove returns the first instance where the value was found after removing them from the original array(arr, key, value, from)</a></dt>
<dd></dd>
<dt><a href="#diff an object with added removed and same between the 2 arrays">diff an object with added removed and same between the 2 arrays(sArr, nArr)</a></dt>
<dd></dd>
</dl>

<a name="index returns the first index of the array where the key of the element equals the value"></a>

## index returns the first index of the array where the key of the element equals the value(arr, key, value, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for |
| from | <code>number</code> | the starting search index |

<a name="find returns the first element of the array where the key of the element equals the value"></a>

## find returns the first element of the array where the key of the element equals the value(arr, key, value, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for |
| from | <code>number</code> | the starting search index |

<a name="replace returns the first index of the array where the key of the element equals the value after replacing it with elem"></a>

## replace returns the first index of the array where the key of the element equals the value after replacing it with elem(arr, key, value, elem, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for and replaced |
| elem | <code>any</code> | the value that will replace the value |
| from | <code>number</code> | the starting search index |

<a name="remove returns the first index of the array where the key of the element equals the value after removing it"></a>

## remove returns the first index of the array where the key of the element equals the value after removing it(arr, key, value, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for and removed |
| from | <code>number</code> | the starting search index |

<a name="removeAll returns an array of all instances where the value was found after removing them from the original array"></a>

## removeAll returns an array of all instances where the value was found after removing them from the original array(arr, key, value, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for and removed |
| from | <code>number</code> | the starting search index |

<a name="findRemove returns the first instance where the value was found after removing them from the original array"></a>

## findRemove returns the first instance where the value was found after removing them from the original array(arr, key, value, from)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| arr | <code>array</code> | array of objects |
| key | <code>string</code> | the key of each object that will be compared |
| value | <code>any</code> | the value being looked for and removed |
| from | <code>number</code> | the starting search index |

<a name="diff an object with added removed and same between the 2 arrays"></a>

## diff an object with added removed and same between the 2 arrays(sArr, nArr)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| sArr | <code>array</code> | if in sArr, but not in nArr will be in removed |
| nArr | <code>array</code> | if in nArr, but not in sArr, will be in added |

