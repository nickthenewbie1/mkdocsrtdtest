---
id: jsdocs-message-processor
title: Message Processor
---
## Classes

<dl>
<dt><a href="#AckProcessor">AckProcessor</a></dt>
<dd><p>class that recieves inboundAckMsgs and then turns them into deviceAckMsgs for ingestion into the leverege system
Expects input of messages as follows:</p>
<p>{
   aliasKey : the alias id of the external to internal device mapping
   deviceId : the external device id
   message : 
}</p>
</dd>
<dt><a href="#DefaultProcessor">DefaultProcessor</a></dt>
<dd><p>receives inboundDataEventMsgs and transforms them into deviceDataEventMsg for ingestion into the leverege system
Expects input of messages as follows:</p>
<p>{
   aliasKey : the alias id of the external to internal device mapping
   deviceId : the external device id
   message : 
}</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#parse">parse(time, dTime)</a></dt>
<dd><p>Attempts to turn time into a milliseconds time. If it cannot, it will
return dTime, which defaults to Date.now()</p>
</dd>
</dl>

<a name="AckProcessor"></a>

## AckProcessor
class that recieves inboundAckMsgs and then turns them into deviceAckMsgs for ingestion into the leverege system
Expects input of messages as follows:

{
   aliasKey : the alias id of the external to internal device mapping
   deviceId : the external device id
   message : 
}

**Kind**: global class  
<a name="DefaultProcessor"></a>

## DefaultProcessor
receives inboundDataEventMsgs and transforms them into deviceDataEventMsg for ingestion into the leverege system
Expects input of messages as follows:

{
   aliasKey : the alias id of the external to internal device mapping
   deviceId : the external device id
   message : 
}

**Kind**: global class  
<a name="parse"></a>

## parse(time, dTime)
Attempts to turn time into a milliseconds time. If it cannot, it will
return dTime, which defaults to Date.now()

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| time | <code>any</code> | if a valid time can be returned from this, it will be |
| dTime | <code>number</code> | default returned if time is not valid |

