---
id: jsdocs-messages
title: Messages
---
## Classes

<dl>
<dt><a href="#AbstractValidator">AbstractValidator</a></dt>
<dd><p>Class to preform the action of checking data in the form of an object against a struct</p>
</dd>
<dt><a href="#ApiEventMsg">ApiEventMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates the apiEventMsg</p>
</dd>
<dt><a href="#DeviceAckMsg">DeviceAckMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates the deviceAckMsg</p>
</dd>
<dt><a href="#DeviceDataEventMsg">DeviceDataEventMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates a DeviceDataEventMsg</p>
</dd>
<dt><a href="#DeviceEventAckMsg">DeviceEventAckMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates a DeviceEventAckMsg</p>
</dd>
<dt><a href="#InboundAckMsg">InboundAckMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates an InboundAckMsg</p>
</dd>
<dt><a href="#InboundDataEventMsg">InboundDataEventMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates an inboundDataEventMsg</p>
</dd>
<dt><a href="#IotHubEventMsg">IotHubEventMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates an iothubEventMsg</p>
</dd>
<dt><a href="#OutboundInitMsg">OutboundInitMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates the outboundInitMsg</p>
</dd>
<dt><a href="#OutboundSentMsg">OutboundSentMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates the outboundSentMsg</p>
</dd>
<dt><a href="#EmailMsg">EmailMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates an EmailMsg</p>
</dd>
<dt><a href="#SmsMsg">SmsMsg</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Validates a SmsMsg</p>
</dd>
<dt><a href="#SolarTimer">SolarTimer</a></dt>
<dd><p>Defines a Solar Timer. A solar timer will fire based off of an offset from
either sunrise or sunset.</p>
</dd>
<dt><a href="#AttributeCondition">AttributeCondition</a> ⇐ <code><a href="#Condition">Condition</a></code></dt>
<dd></dd>
<dt><a href="#Condition">Condition</a> ⇐ <code><a href="#AbstractValidator">AbstractValidator</a></code></dt>
<dd><p>Defines a condition that can be tested for, yielding either true or false</p>
</dd>
<dt><a href="#DeltaCondition">DeltaCondition</a> ⇐ <code><a href="#Condition">Condition</a></code></dt>
<dd></dd>
<dt><a href="#NotCondition">NotCondition</a> ⇐ <code><a href="#Condition">Condition</a></code></dt>
<dd></dd>
<dt><a href="#NotCondition">NotCondition</a> ⇐ <code><a href="#Condition">Condition</a></code></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#parse">parse()</a></dt>
<dd><p>Attempts to turn time into a milliseconds time. If it cannot, it will
return dTime, which defaults to Date.now()</p>
</dd>
</dl>

<a name="AbstractValidator"></a>

## AbstractValidator
Class to preform the action of checking data in the form of an object against a struct

**Kind**: global class  

* [AbstractValidator](#AbstractValidator)
    * [new AbstractValidator(struct, data)](#new_AbstractValidator_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_AbstractValidator_new"></a>

### new AbstractValidator(struct, data)
class that will check an object against a struct and add all the keys to itself


| Param | Type | Description |
| --- | --- | --- |
| struct | <code>Struct</code> | a function returned by creating a struct with superstruct |
| data | <code>object</code> | an object that will be checked against the provided struct |

<a name="AbstractValidator+toObject"></a>

### abstractValidator.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>AbstractValidator</code>](#AbstractValidator)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="ApiEventMsg"></a>

## ApiEventMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates the apiEventMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [ApiEventMsg](#ApiEventMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new ApiEventMsg()](#new_ApiEventMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_ApiEventMsg_new"></a>

### new ApiEventMsg()
create a ApiEventMsg


| Param | Type | Description |
| --- | --- | --- |
| data.eventType | <code>string</code> | the number type of the event from the spec |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.blueprintId | <code>string</code> | the id of the blueprint that the device belongs to |
| data.projectId | <code>string</code> | the id of the project that the device belongs to |
| data.attributeId | <code>string</code> | the id of the attribute affected |
| data.networkId | <code>string</code> | The networkId of the source |
| data.userId | <code>string</code> | the string user id of the event source |
| data.route | <code>string</code> | the string route taken into the data to create the event |
| data.fromModelInterface | <code>string</code> | whether or not the event was generated by calls to the model interface |

<a name="AbstractValidator+toObject"></a>

### apiEventMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>ApiEventMsg</code>](#ApiEventMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="DeviceAckMsg"></a>

## DeviceAckMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates the deviceAckMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [DeviceAckMsg](#DeviceAckMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new DeviceAckMsg()](#new_DeviceAckMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_DeviceAckMsg_new"></a>

### new DeviceAckMsg()
create a DeviceAckMsg


| Param | Type | Description |
| --- | --- | --- |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.msgId | <code>string</code> | The message id, created at outbound initiated step |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.networkId | <code>string</code> | The networkId of the source |
| data.blueprintId | <code>string</code> | the id of the blueprint that the device belongs to |
| data.projectId | <code>string</code> | the id of the project that the device belongs to |
| data.status | <code>string</code> | final updated string status of the message |
| data.response | <code>object</code> | This contains the response data from the device |
| data.source | <code>object</code> | this contains the device, (or less likely) the user, or reason script source info of the inboundAckMsg this derived from |

<a name="AbstractValidator+toObject"></a>

### deviceAckMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>DeviceAckMsg</code>](#DeviceAckMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="DeviceDataEventMsg"></a>

## DeviceDataEventMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates a DeviceDataEventMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [DeviceDataEventMsg](#DeviceDataEventMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new DeviceDataEventMsg()](#new_DeviceDataEventMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_DeviceDataEventMsg_new"></a>

### new DeviceDataEventMsg()
create the DeviceDataEventMsg class


| Param | Type | Description |
| --- | --- | --- |
| data.id | <code>string</code> | A uuid generated for this message |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.storedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the writer |
| data.historical | <code>boolean</code> | whether or not the message is known to be historical only (don't write to rt dbs) |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.blueprintId | <code>string</code> | The id of the blueprint the device belongs to |
| data.projectId | <code>string</code> | The id of the project the device belongs to |
| data.networkId | <code>string</code> | The networkId of the source |
| data.data | <code>array</code> \| <code>object</code> | This contains a data report. The data report as a path, which is the name of the data field, and a value. The path should only contain a-z, A-Z, 0-9, _. Forward slashes (‘/’) are treated as directories |
| data.data.path | <code>string</code> | A string of keys, separated by a ‘/’. For examples, ‘speed’, or ‘battery/temperature1” |
| data.data.value | <code>number</code> | the value of the path |
| data.event | <code>array</code> \| <code>object</code> | This contains an event report. The event indicates that something significant has happened. |
| data.event.type | <code>string</code> | The list that the event should be inserted into. If not supplied, this will default to ‘default’ |
| data.event.time | <code>string</code> \| <code>number</code> | Optional. Server time will be used |
| device.event.id | <code>string</code> | reserved |
| data.source | <code>object</code> | this contains the device, user, or reason script source info of the object that created this msg |
| data.userId | <code>object</code> | the userId (if any) that initiated the writing of information |

<a name="AbstractValidator+toObject"></a>

### deviceDataEventMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>DeviceDataEventMsg</code>](#DeviceDataEventMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="DeviceEventAckMsg"></a>

## DeviceEventAckMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates a DeviceEventAckMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [DeviceEventAckMsg](#DeviceEventAckMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new DeviceEventAckMsg()](#new_DeviceEventAckMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_DeviceEventAckMsg_new"></a>

### new DeviceEventAckMsg()
create the DeviceEventAckMsg class


| Param | Type | Description |
| --- | --- | --- |
| data.id | <code>string</code> | the id of the event being acked |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.storedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the writer |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.blueprintId | <code>string</code> | The id of the blueprint the device belongs to |
| data.projectId | <code>string</code> | The id of the project the device belongs to |
| data.data | <code>array</code> \| <code>object</code> | This contains a data report. The data report as a path, which is the name of the data field, and a value. The path should only contain a-z, A-Z, 0-9, _. Forward slashes (‘/’) are treated as directories |
| data.data.path | <code>string</code> | A string of keys, separated by a ‘/’. For examples, ‘speed’, or ‘battery/temperature1” |
| data.data.value | <code>number</code> | the value of the path |
| data.eventType | <code>string</code> | the type of the event being acked by id |
| data.userId | <code>string</code> | the user (if any) that is acking the message |
| data.source | <code>string</code> | the source info of the device, user, or reason script (if any) that is acking the event |

<a name="AbstractValidator+toObject"></a>

### deviceEventAckMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>DeviceEventAckMsg</code>](#DeviceEventAckMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="InboundAckMsg"></a>

## InboundAckMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates an InboundAckMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [InboundAckMsg](#InboundAckMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new InboundAckMsg()](#new_InboundAckMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_InboundAckMsg_new"></a>

### new InboundAckMsg()
create a InboundAckMsg


| Param | Type | Description |
| --- | --- | --- |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.storedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the writer |
| data.msgId | <code>string</code> | The message id, created at outbound initiated step |
| data.networkId | <code>string</code> | The id of network contributing the acknowledgement |
| data.deviceId | <code>string</code> | A string representing the external name of the device. This could be an IotHub device id, a MAC address of a sensor, etc |
| data.systemId | <code>string</code> | the id of the system the device belongs to |
| data.aliasKey | <code>string</code> | The name of the key that forms the mapping between the external device’s id and the internal device. This is stored in the internal device’s aliases list, and tends to be unique per network. |
| data.status | <code>string</code> | an updated string status of the message |
| data.response | <code>object</code> | This contains the response data from the device |

<a name="AbstractValidator+toObject"></a>

### inboundAckMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>InboundAckMsg</code>](#InboundAckMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="InboundDataEventMsg"></a>

## InboundDataEventMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates an inboundDataEventMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [InboundDataEventMsg](#InboundDataEventMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new InboundDataEventMsg()](#new_InboundDataEventMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_InboundDataEventMsg_new"></a>

### new InboundDataEventMsg()
create an InboundDataEventMsg


| Param | Type | Description |
| --- | --- | --- |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.historical | <code>boolean</code> | whether or not the message is known to be historical only (don't write to rt dbs) |
| data.networkId | <code>string</code> | The networkId of the source |
| data.deviceId | <code>string</code> | A string representing the external name of the device. This could be an IotHub device id, a MAC address of a sensor, etc |
| data.aliasKey | <code>string</code> | The name of the key that forms the mapping between the external device’s id and the internal device. This is stored in the internal device’s aliases list, and tends to be unique per network. |
| data.data | <code>array</code> \| <code>object</code> | This contains a data report. The data report as a path, which is the name of the data field, and a value. The path should only contain a-z, A-Z, 0-9, _. Forward slashes (‘/’) are treated as directories |
| data.data.path | <code>string</code> | A string of keys, separated by a ‘/’. For examples, ‘speed’, or ‘battery/temperature1” |
| data.data.value | <code>number</code> | the value of the path |
| data.event | <code>array</code> \| <code>object</code> | This contains an event report. The event indicates that something significant has happened. |
| data.event.type | <code>string</code> | The list that the event should be inserted into. If not supplied, this will default to ‘default’ |
| data.event.time | <code>string</code> \| <code>number</code> | Optional. Server time will be used |
| data.event.id | <code>string</code> | reserved |
| data.source | <code>object</code> | additional info about the source of the message pertaining to a generating user or reason script |

<a name="AbstractValidator+toObject"></a>

### inboundDataEventMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>InboundDataEventMsg</code>](#InboundDataEventMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="IotHubEventMsg"></a>

## IotHubEventMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates an iothubEventMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [IotHubEventMsg](#IotHubEventMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new IotHubEventMsg()](#new_IotHubEventMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_IotHubEventMsg_new"></a>

### new IotHubEventMsg()

| Param | Type | Description |
| --- | --- | --- |
| data.data | <code>object</code> \| <code>array</code> | This contains a data report. The data report as a path, which is the name of the data field, and a value. Multiple reports can be sent at once by sending an array of the about objects. |
| data.data.path | <code>string</code> | A string of keys, separated by a ‘/’. For examples, ‘speed’, or ‘battery/temperature1” |
| data.data.value | <code>number</code> | the value of the path |
| data.event | <code>object</code> \| <code>array</code> | This contains an event report. The event indicates that something significant has happened |
| data.event.type | <code>string</code> | The list that the event should be inserted into. If not supplied, this will default to ‘default’ |
| data.event.time | <code>string</code> \| <code>number</code> | Optional. Server time will be used |
| device.event.id | <code>string</code> | reserved |

<a name="AbstractValidator+toObject"></a>

### iotHubEventMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>IotHubEventMsg</code>](#IotHubEventMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="OutboundInitMsg"></a>

## OutboundInitMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates the outboundInitMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [OutboundInitMsg](#OutboundInitMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new OutboundInitMsg()](#new_OutboundInitMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_OutboundInitMsg_new"></a>

### new OutboundInitMsg()
create a OutboundInitMsg


| Param | Type | Description |
| --- | --- | --- |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.msgId | <code>string</code> | The message id, created at outbound initiated step |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.blueprintId | <code>string</code> | the id of the blueprint that the device belongs to |
| data.projectId | <code>string</code> | the id of the project that the device belongs to |
| data.message | <code>object</code> | This contains the message to go out to the device |
| data.source | <code>object</code> | information about the device, (or less likely) the user, or reason script that generated this message |

<a name="AbstractValidator+toObject"></a>

### outboundInitMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>OutboundInitMsg</code>](#OutboundInitMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="OutboundSentMsg"></a>

## OutboundSentMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates the outboundSentMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [OutboundSentMsg](#OutboundSentMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new OutboundSentMsg()](#new_OutboundSentMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_OutboundSentMsg_new"></a>

### new OutboundSentMsg()
create a OutboundSentMsg


| Param | Type | Description |
| --- | --- | --- |
| data.time | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the device |
| data.receivedTime | <code>string</code> \| <code>integer</code> | the time of the message, as reported by the ingestion server |
| data.msgId | <code>string</code> | The message id, created at outbound initiated step |
| data.deviceId | <code>string</code> | A string representing the internal name of the device. |
| data.systemId | <code>string</code> | The name of the system the device belongs to |
| data.blueprintId | <code>string</code> | the id of the blueprint that the device belongs to |
| data.projectId | <code>string</code> | the id of the project that the device belongs to |
| data.status | <code>string</code> | an updated string status of the device |
| data.sendInfo | <code>object</code> | any information or notes about the data sent |
| data.source | <code>object</code> | information about the device, (or less likely) the user, or reason script that generated this message |

<a name="AbstractValidator+toObject"></a>

### outboundSentMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>OutboundSentMsg</code>](#OutboundSentMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="EmailMsg"></a>

## EmailMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates an EmailMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [EmailMsg](#EmailMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new EmailMsg()](#new_EmailMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_EmailMsg_new"></a>

### new EmailMsg()
create an EmailMsg


| Param | Type | Description |
| --- | --- | --- |
| data.subject | <code>string</code> | the subject line of the email to be sent |
| data.to | <code>string</code> \| <code>array</code> | the email address/es to send the email to |
| data.cc | <code>string</code> \| <code>array</code> | the email address/es to cc on the email |
| data.bcc | <code>string</code> \| <code>array</code> | the email address/es to bcc on the email |
| data.from | <code>string</code> | the email address the email is to be sent from |
| data.html | <code>string</code> | email content as html |
| data.text | <code>string</code> | email content as plain text |
| data.template | <code>string</code> |  |
| data.context | <code>string</code> |  |
| data.attachments | <code>array</code> | attachments to be included with the email |

<a name="AbstractValidator+toObject"></a>

### emailMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>EmailMsg</code>](#EmailMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="SmsMsg"></a>

## SmsMsg ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Validates a SmsMsg

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  

* [SmsMsg](#SmsMsg) ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
    * [new SmsMsg()](#new_SmsMsg_new)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>

<a name="new_SmsMsg_new"></a>

### new SmsMsg()
create a SmsProcessorMsg


| Param | Type | Description |
| --- | --- | --- |
| data.recipients | <code>array</code> \| <code>string</code> | the phone number/s to send the message to |
| data.message | <code>string</code> | the text of the message that will be sent |

<a name="AbstractValidator+toObject"></a>

### smsMsg.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>SmsMsg</code>](#SmsMsg)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="SolarTimer"></a>

## SolarTimer
Defines a Solar Timer. A solar timer will fire based off of an offset from
either sunrise or sunset.

**Kind**: global class  

* [SolarTimer](#SolarTimer)
    * [new SolarTimer(data)](#new_SolarTimer_new)
    * [.next()](#SolarTimer+next)

<a name="new_SolarTimer_new"></a>

### new SolarTimer(data)
Create a Solar Timer


| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> |  |
| data.latitude | <code>number</code> | the north/south position on the earth in degrees |
| data.longitude | <code>number</code> | the east/west position on the earth in degreews |
| data.fromSunrise | <code>boolean</code> | if true, the timer is based on sunrise. Otherwise, sunset is used |
| data.offset | <code>number</code> | the offset in milliseconds from sunrise or sunset |

<a name="SolarTimer+next"></a>

### solarTimer.next()
Returns the next time to fire from the current time.
If when is set and it is less than fromTime, -1 is returned.

**Kind**: instance method of [<code>SolarTimer</code>](#SolarTimer)  
<a name="AttributeCondition"></a>

## AttributeCondition ⇐ [<code>Condition</code>](#Condition)
**Kind**: global class  
**Extends**: [<code>Condition</code>](#Condition)  

* [AttributeCondition](#AttributeCondition) ⇐ [<code>Condition</code>](#Condition)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>
    * [.satisfies(context)](#AttributeCondition+satisfies)

<a name="AbstractValidator+toObject"></a>

### attributeCondition.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>AttributeCondition</code>](#AttributeCondition)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="AttributeCondition+satisfies"></a>

### attributeCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>AttributeCondition</code>](#AttributeCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="Condition"></a>

## Condition ⇐ [<code>AbstractValidator</code>](#AbstractValidator)
Defines a condition that can be tested for, yielding either true or false

**Kind**: global class  
**Extends**: [<code>AbstractValidator</code>](#AbstractValidator)  
<a name="AbstractValidator+toObject"></a>

### condition.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>Condition</code>](#Condition)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="DeltaCondition"></a>

## DeltaCondition ⇐ [<code>Condition</code>](#Condition)
**Kind**: global class  
**Extends**: [<code>Condition</code>](#Condition)  

* [DeltaCondition](#DeltaCondition) ⇐ [<code>Condition</code>](#Condition)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>
    * [.satisfies(context)](#DeltaCondition+satisfies)

<a name="AbstractValidator+toObject"></a>

### deltaCondition.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>DeltaCondition</code>](#DeltaCondition)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="DeltaCondition+satisfies"></a>

### deltaCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>DeltaCondition</code>](#DeltaCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="NotCondition"></a>

## NotCondition ⇐ [<code>Condition</code>](#Condition)
**Kind**: global class  
**Extends**: [<code>Condition</code>](#Condition)  

* [NotCondition](#NotCondition) ⇐ [<code>Condition</code>](#Condition)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>
    * [.satisfies(context)](#NotCondition+satisfies)
    * [.satisfies(context)](#NotCondition+satisfies)

<a name="AbstractValidator+toObject"></a>

### notCondition.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>NotCondition</code>](#NotCondition)  
**Overrides**: [<code>toObject</code>](#AbstractValidator+toObject)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="NotCondition+satisfies"></a>

### notCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>NotCondition</code>](#NotCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="NotCondition+satisfies"></a>

### notCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>NotCondition</code>](#NotCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="NotCondition"></a>

## NotCondition ⇐ [<code>Condition</code>](#Condition)
**Kind**: global class  
**Extends**: [<code>Condition</code>](#Condition)  

* [NotCondition](#NotCondition) ⇐ [<code>Condition</code>](#Condition)
    * [.toObject](#AbstractValidator+toObject) ⇒ <code>object</code>
    * [.satisfies(context)](#NotCondition+satisfies)
    * [.satisfies(context)](#NotCondition+satisfies)

<a name="AbstractValidator+toObject"></a>

### notCondition.toObject ⇒ <code>object</code>
**Kind**: instance property of [<code>NotCondition</code>](#NotCondition)  
**Overrides**: [<code>toObject</code>](#AbstractValidator+toObject)  
**Returns**: <code>object</code> - - the validated object of the data originally provided  
<a name="NotCondition+satisfies"></a>

### notCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>NotCondition</code>](#NotCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="NotCondition+satisfies"></a>

### notCondition.satisfies(context)
Determines whether the condition is met or not given the context

**Kind**: instance method of [<code>NotCondition</code>](#NotCondition)  

| Param | Type | Description |
| --- | --- | --- |
| context | <code>\*</code> | The context with which the satisfies method is to be executed |

<a name="parse"></a>

## parse()
Attempts to turn time into a milliseconds time. If it cannot, it will
return dTime, which defaults to Date.now()

**Kind**: global function  
