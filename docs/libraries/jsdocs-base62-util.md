---
id: jsdocs-base62-util
title: Base62 Util
---
## Functions

<dl>
<dt><a href="#encode encodes a string">encode encodes a string(str, prefix)</a></dt>
<dd></dd>
<dt><a href="#decode decodes an encoded string">decode decodes an encoded string(str, prefix)</a></dt>
<dd></dd>
<dt><a href="#v4 creates a random UUID">v4 creates a random UUID()</a></dt>
<dd></dd>
<dt><a href="#v1 create a random UUID">v1 create a random UUID()</a></dt>
<dd></dd>
<dt><a href="#encode encodes the input with the provided encode method">encode encodes the input with the provided encode method(input, encoding)</a></dt>
<dd></dd>
<dt><a href="#decode decodes the encoded data with the encoding method">decode decodes the encoded data with the encoding method(b62Str, encoding)</a></dt>
<dd></dd>
<dt><a href="#ensureLength adds or removes 0s to the string to ensure the length">ensureLength adds or removes 0s to the string to ensure the length(str, maxLen)</a></dt>
<dd></dd>
<dt><a href="#padLeft adds 0s to the beginning of the string">padLeft adds 0s to the beginning of the string()</a></dt>
<dd></dd>
<dt><a href="#trimLeft removes 0s from the beginning of the string">trimLeft removes 0s from the beginning of the string()</a></dt>
<dd></dd>
</dl>

<a name="encode encodes a string"></a>

## encode encodes a string(str, prefix)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | the string to be encoded |
| prefix | <code>string</code> | a prefix to be added to the encoded string |

<a name="decode decodes an encoded string"></a>

## decode decodes an encoded string(str, prefix)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | the string to be decoded |
| prefix | <code>string</code> | prefix to be taken off the str before it is decoded |

<a name="v4 creates a random UUID"></a>

## v4 creates a random UUID()
**Kind**: global function  
<a name="v1 create a random UUID"></a>

## v1 create a random UUID()
**Kind**: global function  
<a name="encode encodes the input with the provided encode method"></a>

## encode encodes the input with the provided encode method(input, encoding)
**Kind**: global function  

| Param | Description |
| --- | --- |
| input | the input to be encoded |
| encoding | the method to encode the input with |

<a name="decode decodes the encoded data with the encoding method"></a>

## decode decodes the encoded data with the encoding method(b62Str, encoding)
**Kind**: global function  

| Param | Description |
| --- | --- |
| b62Str | encoded data to be decoded |
| encoding | the method to encode the input with |

<a name="ensureLength adds or removes 0s to the string to ensure the length"></a>

## ensureLength adds or removes 0s to the string to ensure the length(str, maxLen)
**Kind**: global function  
**Api**: private  

| Param | Type | Description |
| --- | --- | --- |
| str | <code>string</code> | the string to be manipulated |
| maxLen | <code>number</code> | the length to force the string to |

<a name="padLeft adds 0s to the beginning of the string"></a>

## padLeft adds 0s to the beginning of the string()
**Kind**: global function  
**Api**: private  
<a name="trimLeft removes 0s from the beginning of the string"></a>

## trimLeft removes 0s from the beginning of the string()
**Kind**: global function  
**Api**: private  
