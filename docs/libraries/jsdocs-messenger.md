---
id: jsdocs-messenger
title: Messenger
---
## Classes

<dl>
<dt><a href="#SmsProcessor">SmsProcessor</a></dt>
<dd><p>creates a Processor that will process messages on a topic, and will format and send a message to Twilio or other comparable service</p>
</dd>
<dt><a href="#Twilio">Twilio</a></dt>
<dd><p>a class to make api requests to twilio</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#checkRecipient">checkRecipient(r, templateId, limiter, onFirst)</a> ⇒</dt>
<dd><p>The checkRecipient function is exposed here to facilitate testing with
the new Limit logic.</p>
</dd>
</dl>

<a name="SmsProcessor"></a>

## SmsProcessor
creates a Processor that will process messages on a topic, and will format and send a message to Twilio or other comparable service

**Kind**: global class  
<a name="new_SmsProcessor_new"></a>

### new SmsProcessor()

| Param | Type | Description |
| --- | --- | --- |
| options.sender | [<code>Twilio</code>](#Twilio) | responsible for taking the message and sending it to twilio |
| options.templatizer | <code>Templatizer</code> | instance of the @leverege/templatizer library |

<a name="Twilio"></a>

## Twilio
a class to make api requests to twilio

**Kind**: global class  

* [Twilio](#Twilio)
    * [new Twilio(options)](#new_Twilio_new)
    * [.sms(limitOptions)](#Twilio+sms)

<a name="new_Twilio_new"></a>

### new Twilio(options)

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | configuration for the twilio api |
| options.twilio.sid | <code>string</code> | twilio id |
| options.twilio.token | <code>string</code> | twilio token |
| options.limiter | <code>string</code> | limit config |

<a name="Twilio+sms"></a>

### twilio.sms(limitOptions)
method that will send a message to twilio that will then send a text message

**Kind**: instance method of [<code>Twilio</code>](#Twilio)  

| Param | Type | Description |
| --- | --- | --- |
| msg.recipients | <code>array</code> \| <code>string</code> | phone number/s that the message will be sent to |
| msg.message | <code>string</code> | the text of the message that will be sent |
| limitOptions | <code>object</code> | options to limit the |

<a name="checkRecipient"></a>

## checkRecipient(r, templateId, limiter, onFirst) ⇒
The checkRecipient function is exposed here to facilitate testing with
the new Limit logic.

**Kind**: global function  
**Returns**: an array of email targets  

| Param | Type | Description |
| --- | --- | --- |
| r |  | recipients in the form of a string or an array |
| templateId | <code>string</code> | the id of the template or null if one doesnt exist |
| limiter |  | the actual Limit instance to use |
| onFirst |  | a callback on the first time the limit occurs for a target |

<a name="checkRecipient..filterLimited"></a>

### checkRecipient~filterLimited()
Iterates over the array, checking each target to see if it has been
limited from email.

**Kind**: inner method of [<code>checkRecipient</code>](#checkRecipient)  
