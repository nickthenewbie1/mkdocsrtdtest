---
id: jsdocs-reason
title: Reason
---
## Classes

<dl>
<dt><a href="#InboundProcessor">InboundProcessor</a></dt>
<dd><p>This will process the messages from the system</p>
</dd>
<dt><a href="#ResultProcessor">ResultProcessor</a></dt>
<dd><p>This will process the messages from the system</p>
</dd>
</dl>

<a name="InboundProcessor"></a>

## InboundProcessor
This will process the messages from the system

**Kind**: global class  

* [InboundProcessor](#InboundProcessor)
    * [new InboundProcessor(options)](#new_InboundProcessor_new)
    * [.process(message, options)](#InboundProcessor+process) ⇒ <code>Promise</code>

<a name="new_InboundProcessor_new"></a>

### new InboundProcessor(options)
Constructs an in bound processor


| Param | Type | Description |
| --- | --- | --- |
| options | <code>Object</code> | should include a processors object that defines type to processor binding. |

<a name="InboundProcessor+process"></a>

### inboundProcessor.process(message, options) ⇒ <code>Promise</code>
Processes the message by looking up its type
in the processors map givin in the constructor

**Kind**: instance method of [<code>InboundProcessor</code>](#InboundProcessor)  
**Returns**: <code>Promise</code> - A promise that will define how to route 
the message  

| Param | Type | Description |
| --- | --- | --- |
| message | <code>Message</code> | the message to process |
| options | <code>Object</code> | the options for the message |

<a name="ResultProcessor"></a>

## ResultProcessor
This will process the messages from the system

**Kind**: global class  
<a name="ResultProcessor+process"></a>

### resultProcessor.process(message, options) ⇒ <code>Promise</code>
Processes the message by looking up its type
in the processors map givin in the constructor

**Kind**: instance method of [<code>ResultProcessor</code>](#ResultProcessor)  
**Returns**: <code>Promise</code> - A promise that will define how to route 
the message  

| Param | Type | Description |
| --- | --- | --- |
| message | <code>Message</code> | the message to process |
| options | <code>Object</code> | the options for the message |

