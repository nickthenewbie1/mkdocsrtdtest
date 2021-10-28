---
id: jsdocs-rest-server
title: Rest Server
---
## Classes

<dl>
<dt><a href="#OAuthToken">OAuthToken</a></dt>
<dd><p>class that manages an OAuthToken</p>
</dd>
<dt><a href="#OutboundProcessor">OutboundProcessor</a></dt>
<dd><p>create a processor to recieve outbound messages, and send http queries from those outbound messages</p>
</dd>
</dl>

## Members

<dl>
<dt><a href="#post/rcv">post/rcv</a></dt>
<dd><p>route to create an inboundDataEventMsg</p>
</dd>
<dt><a href="#post/ack">post/ack</a></dt>
<dd><p>route to acknowledge a message</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#fetch">fetch(url, opts)</a></dt>
<dd><p>make an http request and returns the json</p>
</dd>
<dt><a href="#ApiError">ApiError(json, response)</a></dt>
<dd><p>combines the json with a function that will return the response</p>
</dd>
<dt><a href="#checkStatus">checkStatus(response)</a></dt>
<dd><p>checks the response status, and then performs error handling</p>
</dd>
<dt><a href="#parseJSON">parseJSON(response)</a></dt>
<dd><p>returns the json from a response</p>
</dd>
<dt><a href="#getTimestamp">getTimestamp()</a></dt>
<dd><p>get seconds timestamp</p>
</dd>
<dt><a href="#encodeData">encodeData(toEncode)</a></dt>
<dd><p>encodes data to URI</p>
</dd>
<dt><a href="#normalizeUrl">normalizeUrl(url)</a></dt>
<dd><p>parses an url and adds a port and path to it</p>
</dd>
<dt><a href="#isOAuthParam">isOAuthParam(parameter)</a></dt>
<dd><p>Is the parameter considered an OAuth parameter</p>
</dd>
<dt><a href="#buildAuthorizationHeaders">buildAuthorizationHeaders(orderedParameters)</a></dt>
<dd><p>build the OAuth request authorization header</p>
</dd>
<dt><a href="#makeArrayOfArgumentsHash">makeArrayOfArgumentsHash(argumentsHash)</a></dt>
<dd><p>Takes an object literal that represents the arguments, and returns an array of argument/value pairs.</p>
</dd>
<dt><a href="#sortRequestParams">sortRequestParams(argumentPairs)</a></dt>
<dd><p>Sorts the encoded key value pairs by encoded name, then encoded value</p>
</dd>
<dt><a href="#normalizeRequestParams">normalizeRequestParams(args)</a></dt>
<dd><p>encodes request parameters and then formats them into a http query string</p>
</dd>
<dt><a href="#getNonce">getNonce(nonceSize)</a></dt>
<dd><p>creates and returns the nonce</p>
</dd>
<dt><a href="#start">start(options)</a></dt>
<dd><p>creates a rest Api to recieve inbound data, events and acknowledgements</p>
</dd>
</dl>

<a name="OAuthToken"></a>

## OAuthToken
class that manages an OAuthToken

**Kind**: global class  

* [OAuthToken](#OAuthToken)
    * [new OAuthToken(opts)](#new_OAuthToken_new)
    * [.getToken(method, url, extraParams)](#OAuthToken+getToken)
    * [._prepareParameters(method, url, extraParams)](#OAuthToken+_prepareParameters)
    * [._getSignature(method, url, parameters, tokenSecret)](#OAuthToken+_getSignature)
    * [._createSignatureBase(method, url, parameters)](#OAuthToken+_createSignatureBase)
    * [._createSignature(signatureBase, tokenSecret)](#OAuthToken+_createSignature)

<a name="new_OAuthToken_new"></a>

### new OAuthToken(opts)

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 
| opts.apiKey | <code>string</code> | 
| opts.secret | <code>string</code> | 
| opts.signatureMethod | <code>string</code> | 
| opts.nouncSize | <code>number</code> | 

<a name="OAuthToken+getToken"></a>

### oAuthToken.getToken(method, url, extraParams)
calculates the OAuth token and returns it

**Kind**: instance method of [<code>OAuthToken</code>](#OAuthToken)  

| Param | Type | Description |
| --- | --- | --- |
| method | <code>string</code> | http method |
| url | <code>string</code> | http url |
| extraParams | <code>object</code> |  |

<a name="OAuthToken+_prepareParameters"></a>

### oAuthToken.\_prepareParameters(method, url, extraParams)
prepares the parameters for the OAuth Token

**Kind**: instance method of [<code>OAuthToken</code>](#OAuthToken)  

| Param | Type |
| --- | --- |
| method | <code>string</code> | 
| url | <code>string</code> | 
| extraParams | <code>object</code> | 

<a name="OAuthToken+_getSignature"></a>

### oAuthToken.\_getSignature(method, url, parameters, tokenSecret)
creates the signature

**Kind**: instance method of [<code>OAuthToken</code>](#OAuthToken)  

| Param | Type |
| --- | --- |
| method | <code>string</code> | 
| url | <code>string</code> | 
| parameters | <code>object</code> | 
| tokenSecret | <code>string</code> | 

<a name="OAuthToken+_createSignatureBase"></a>

### oAuthToken.\_createSignatureBase(method, url, parameters)
creates the base signature

**Kind**: instance method of [<code>OAuthToken</code>](#OAuthToken)  

| Param | Type |
| --- | --- |
| method | <code>string</code> | 
| url | <code>string</code> | 
| parameters | <code>object</code> | 

<a name="OAuthToken+_createSignature"></a>

### oAuthToken.\_createSignature(signatureBase, tokenSecret)
creates the signature

**Kind**: instance method of [<code>OAuthToken</code>](#OAuthToken)  

| Param | Type |
| --- | --- |
| signatureBase | <code>string</code> | 
| tokenSecret | <code>string</code> | 

<a name="OutboundProcessor"></a>

## OutboundProcessor
create a processor to recieve outbound messages, and send http queries from those outbound messages

**Kind**: global class  
<a name="new_OutboundProcessor_new"></a>

### new OutboundProcessor(options)

| Param | Type |
| --- | --- |
| options | <code>object</code> | 
| options.sentTopic | <code>string</code> | 
| options.writer | <code>Writer</code> | 

<a name="post/rcv"></a>

## post/rcv
route to create an inboundDataEventMsg

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| network | <code>string</code> | imagine network that the device belongs to |
| body | <code>object</code> | needs a deviceId and data or an event |

<a name="post/ack"></a>

## post/ack
route to acknowledge a message

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| body | <code>object</code> | needs a msgId, status, deviceId, response |

<a name="fetch"></a>

## fetch(url, opts)
make an http request and returns the json

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| url | <code>string</code> | the url to make an http request to |
| opts | <code>object</code> |  |

<a name="ApiError"></a>

## ApiError(json, response)
combines the json with a function that will return the response

**Kind**: global function  

| Param | Type |
| --- | --- |
| json | <code>object</code> | 
| response | <code>object</code> | 

<a name="checkStatus"></a>

## checkStatus(response)
checks the response status, and then performs error handling

**Kind**: global function  

| Param | Type |
| --- | --- |
| response | <code>object</code> | 

<a name="parseJSON"></a>

## parseJSON(response)
returns the json from a response

**Kind**: global function  

| Param | Type |
| --- | --- |
| response | <code>object</code> | 

<a name="getTimestamp"></a>

## getTimestamp()
get seconds timestamp

**Kind**: global function  
<a name="encodeData"></a>

## encodeData(toEncode)
encodes data to URI

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| toEncode | <code>string</code> | string to encode |

<a name="normalizeUrl"></a>

## normalizeUrl(url)
parses an url and adds a port and path to it

**Kind**: global function  

| Param | Type |
| --- | --- |
| url | <code>string</code> | 

<a name="isOAuthParam"></a>

## isOAuthParam(parameter)
Is the parameter considered an OAuth parameter

**Kind**: global function  

| Param | Type |
| --- | --- |
| parameter | <code>string</code> | 

<a name="buildAuthorizationHeaders"></a>

## buildAuthorizationHeaders(orderedParameters)
build the OAuth request authorization header

**Kind**: global function  

| Param | Type |
| --- | --- |
| orderedParameters | <code>array</code> | 

<a name="makeArrayOfArgumentsHash"></a>

## makeArrayOfArgumentsHash(argumentsHash)
Takes an object literal that represents the arguments, and returns an array of argument/value pairs.

**Kind**: global function  

| Param | Type |
| --- | --- |
| argumentsHash | <code>object</code> | 

<a name="sortRequestParams"></a>

## sortRequestParams(argumentPairs)
Sorts the encoded key value pairs by encoded name, then encoded value

**Kind**: global function  

| Param | Type |
| --- | --- |
| argumentPairs | <code>array</code> | 

<a name="normalizeRequestParams"></a>

## normalizeRequestParams(args)
encodes request parameters and then formats them into a http query string

**Kind**: global function  

| Param | Type |
| --- | --- |
| args | <code>object</code> | 

<a name="getNonce"></a>

## getNonce(nonceSize)
creates and returns the nonce

**Kind**: global function  

| Param | Type |
| --- | --- |
| nonceSize | <code>number</code> | 

<a name="start"></a>

## start(options)
creates a rest Api to recieve inbound data, events and acknowledgements

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.inboundWriter | <code>Writer</code> | writer for inbound messages |
| options.inboundTopic | <code>string</code> | topic inbound messages will be sent on |
| options.ackWriter | <code>Writer</code> | writer for inbound acks |
| options.ackTopic | <code>string</code> | topic for inbound ack messages |

