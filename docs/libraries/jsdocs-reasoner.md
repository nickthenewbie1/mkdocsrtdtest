---
id: jsdocs-reasoner
title: Reasoner
---
## Functions

<dl>
<dt><a href="#main">main(script, event, callback)</a></dt>
<dd></dd>
<dt><a href="#getJson">getJson()</a></dt>
<dd><p>Extracts the message from the pubsub event</p>
</dd>
<dt><a href="#publish">publish(topic, message)</a></dt>
<dd><p>publish a message into the leverege platform</p>
</dd>
<dt><a href="#filterBuildRecipients">filterBuildRecipients(users, defaultAccessor, filter, recipientKey)</a> ⇒ <code>Object</code></dt>
<dd><p>This method builds a list of contact information given a list of users, a method for
accessing and filtering users, and a key to put the user info on in a final object</p>
</dd>
<dt><a href="#sendToTargets">sendToTargets(msg, targets, targets[i, options, defaultUserAccessor, topic, allowedRecipientKeys, recipientOverride)</a> ⇒ <code>Promise</code></dt>
<dd></dd>
<dt><a href="#email">email(msg, targets, options)</a></dt>
<dd></dd>
<dt><a href="#sms">sms(msg, targets, options)</a></dt>
<dd></dd>
<dt><a href="#setDeviceData">setDeviceData(pathValueArray, oMsg, options)</a></dt>
<dd></dd>
<dt><a href="#message">message(msg, route, options)</a></dt>
<dd></dd>
<dt><a href="#send">send(topic, msg, route)</a></dt>
<dd><p>send a message into the leverege system</p>
</dd>
</dl>

<a name="main"></a>

## main(script, event, callback)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| script | <code>object</code> | the export of a script file |
| event | <code>object</code> | Pubsub message that triggered reasoner execution |
| callback | <code>function</code> | function to be run after the script has been executed |

<a name="getJson"></a>

## getJson()
Extracts the message from the pubsub event

**Kind**: global function  
<a name="publish"></a>

## publish(topic, message)
publish a message into the leverege platform

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| topic | <code>string</code> | the topic that the message will be published to |
| message | <code>Message</code> | acceptable messages can be found in the @leverege/messages library |

<a name="filterBuildRecipients"></a>

## filterBuildRecipients(users, defaultAccessor, filter, recipientKey) ⇒ <code>Object</code>
This method builds a list of contact information given a list of users, a method for
accessing and filtering users, and a key to put the user info on in a final object

**Kind**: global function  
**Returns**: <code>Object</code> - the recipients built from the user list  

| Param | Type | Description |
| --- | --- | --- |
| users | <code>\*</code> | a list of user objects, generally including metadata |
| defaultAccessor | <code>\*</code> | a default way to get relevant user contact info out |
| filter | <code>\*</code> | an accessor for how to filter users out of selection and get the relevant field |
| recipientKey | <code>\*</code> | the key to use in object creation |

<a name="sendToTargets"></a>

## sendToTargets(msg, targets, targets[i, options, defaultUserAccessor, topic, allowedRecipientKeys, recipientOverride) ⇒ <code>Promise</code>
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| msg | <code>Object</code> | the message to send to either emailer or messenger |
| targets | <code>Array</code> | the targets |
| targets[i | <code>Object</code> \| <code>string</code> | a target. if object see below, if string and string is 'device', use context                                   to get the device that came from the reason trigger and send to that, if string                                   and string is 'system', do the same but for the system |
| targets[i].type | <code>Object</code> | 'device'|'system' |
| targets[i].filter | <code>function</code> \| <code>string</code> | a way of telling whether a user should be messaged or not.                                            If a function, returning true will contact the user in a default manner,                                            returning a string or array will contact a user using the string                                            or list of strings returned, returning anything else will filter                                            the user. If a string, path is used to the same effect |
| targets[i].id | <code>string</code> | the id of the target to get |
| options | <code>\*</code> | an object passed in through closure by the reason script |
| defaultUserAccessor | <code>\*</code> | a default way to get the contact string for a user |
| topic | <code>\*</code> | the topic to ultimately send the message to |
| allowedRecipientKeys | <code>\*</code> | a set of keys we can modify along the way getting recipients |
| recipientOverride | <code>\*</code> | (optional) if specified, forces targeting to a specific key |

<a name="email"></a>

## email(msg, targets, options)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| msg | <code>object</code> | an email message as detailed in @leverege/messages |
| targets | <code>array</code> | recipients of the email |
| options | <code>object</code> |  |

<a name="sms"></a>

## sms(msg, targets, options)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| msg | <code>object</code> | a detailed description of supported messages can be found in @leverege/messages library |
| targets | <code>array</code> | recipients of the sms |
| options | <code>object</code> |  |

<a name="setDeviceData"></a>

## setDeviceData(pathValueArray, oMsg, options)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| pathValueArray | <code>array</code> | array of objects with a path key and a value key |
| oMsg | <code>object</code> | device, system, blueprint and project ids |
| options | <code>object</code> |  |

<a name="message"></a>

## message(msg, route, options)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| msg | <code>Message</code> | a detailed description of supported messages can be found in @leverege/messages library |
| route | <code>\*</code> | GCP route to send the message on |
| options | <code>object</code> |  |

<a name="send"></a>

## send(topic, msg, route)
send a message into the leverege system

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| topic | <code>string</code> | the topic that the message should be published to |
| msg | <code>Message</code> | a detailed description of supported messages can be found in @leverege/messages library |
| route | <code>\*</code> | GCP route to send the message on |

