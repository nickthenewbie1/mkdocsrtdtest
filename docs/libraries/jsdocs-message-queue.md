---
id: jsdocs-message-queue
title: Message Queue
---
## Classes

<dl>
<dt><a href="#AWSReader">AWSReader</a></dt>
<dd><p>Options :
{
   type : &#39;aws&#39;,
   topic : <string>,
   queue : <string>,
   region : <string>,
   credentials : <aws credentials file>
}</p>
</dd>
<dt><a href="#Message">Message</a></dt>
<dd><p>The message abstracts away the transport&#39;s acknowledge and no-acknowledge, as
well as handling routing unpacking</p>
</dd>
<dt><a href="#MessageProcessor">MessageProcessor</a></dt>
<dd><p>Creates a Message processor. Thes will supply some auto acknowledge logic
and default routing to other queues.<br>options:
   autoAck: [&#39;onReceipt&#39;|&#39;afterProcess&#39;|&#39;none&#39;] 
     If &#39;onReceipt&#39;, Message.ack() will be called immediately on receipt of the message
     If &#39;afterProcess&#39;, Message.ack() will be called immediately after processing of the message
     If &#39;none&#39;, Message.ack() will not be called, and the processor must handle it.
   ackOnError: [true|false] 
     Only used if autoAck === &#39;afterProcess&#39;
     If true, Message.ack() will be called on process error
     else, Message.noAck() will be called on process error</p>
</dd>
<dt><a href="#NsqReader">NsqReader</a></dt>
<dd><p>Options :
{
   type : &#39;nsq&#39;,
   nsqd : [ ..nsqOptions... ]
   topic : <string>
   channel : <string>
   maxInFlight : <number default=5>
   processor : &lt;function( msg, reader )&gt; | <object with onMessage( msg, reader )>
   closeCountKey
   errorCountKey
   errorResponseCountKey
}</p>
</dd>
<dt><a href="#PubSubReader">PubSubReader</a></dt>
<dd><p>Options :
{
   type : &#39;pubsub&#39;,
   topic : <string>
   channel : <string>
   projectId : <The pubsub project>,
   keyFilename : <The location of the service account file>,
   subscriptionOptions : { } // see <a href="https://cloud.google.com/nodejs/docs/reference/pubsub/0.16.x/global#CreateSubscriptionRequest">https://cloud.google.com/nodejs/docs/reference/pubsub/0.16.x/global#CreateSubscriptionRequest</a>
}</p>
</dd>
<dt><a href="#Reader">Reader</a></dt>
<dd><p>The base class for a Reader. This will manage processing a message via
the processor function or object. Normally options.processor will be an
object that extends MessageProcessor. Subclasses should override onStart()
to connect to their transport and onStop() to disconnect</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#routeFor">routeFor(conditionRouteModel, type, object)</a></dt>
<dd><p>Given a condition route model and a type, the model&#39;s rules will
be evaluated to find a particular route for that type.</p>
</dd>
<dt><a href="#createWriter">createWriter()</a></dt>
<dd><p>Options
 nsqd : [ ...nsqd.... ]</p>
</dd>
<dt><a href="#routeTargets">routeTargets()</a></dt>
<dd><p>A Route has the form:
route := &lt;topic_name&gt; | &lt;route_array&gt; | <topic> | <concurrent>
route_array := [ <route>, <route>, ...]
topic_name := <string>
topic = { topic : &lt;topic_name&gt;, options : <object> optional, route : &lt;route_array&gt; optional, terminate : true | false optional }
concurrent := { &lt;topic_name_0&gt; : true | &lt;route_array&gt; | <topic>, ... &lt;topic_name_n&gt; : true | &lt;route_array&gt; | <topic> } |
              { type : &#39;concurrent&#39;, routes : [ &lt;topic_name&gt; | <topic> ] }</p>
<p>routeTargets() will return an array containing topic objects or null, if there are no routes.</p>
</dd>
<dt><a href="#createRouteMsg">createRouteMsg()</a></dt>
<dd><p>Creates a RouteMsg if either the options or the route is not null. Otherwise
the message will be returned</p>
</dd>
</dl>

<a name="AWSReader"></a>

## AWSReader
Options :
{
   type : 'aws',
   topic : <string>,
   queue : <string>,
   region : <string>,
   credentials : <aws credentials file>
}

**Kind**: global class  
<a name="Message"></a>

## Message
The message abstracts away the transport's acknowledge and no-acknowledge, as
well as handling routing unpacking

**Kind**: global class  

* [Message](#Message)
    * [.rawMsg()](#Message+rawMsg)
    * [.json()](#Message+json)
    * [.raw()](#Message+raw)
    * [.getType()](#Message+getType)
    * [.getMessage()](#Message+getMessage)
    * [.isRouteMessage()](#Message+isRouteMessage)
    * [.getRouteOptions()](#Message+getRouteOptions)
    * [.getNextRoutes()](#Message+getNextRoutes)
    * [.getReceived()](#Message+getReceived)
    * [.getTimestamp()](#Message+getTimestamp)

<a name="Message+rawMsg"></a>

### message.rawMsg()
Returns the raw native message that that transport delivered

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+json"></a>

### message.json()
Returns a json representation of the data

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+raw"></a>

### message.raw()
Returns the raw message data, often the same as json()

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getType"></a>

### message.getType()
Returns the type or Message being routed or json().type if
this is not a route message

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getMessage"></a>

### message.getMessage()
Returns the Message being routed or json() if
this is not a route message

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+isRouteMessage"></a>

### message.isRouteMessage()
Returns true if the message type is ROUTE_MSG_TYPE

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getRouteOptions"></a>

### message.getRouteOptions()
If this is a Route Message, this will return any optional
options associated with the message

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getNextRoutes"></a>

### message.getNextRoutes()
Returns an array of the next routes to deliver the data on or null if
none exist or this is not a route message

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getReceived"></a>

### message.getReceived()
The time the message was created.

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="Message+getTimestamp"></a>

### message.getTimestamp()
If possible, subclasses should overload this.

**Kind**: instance method of [<code>Message</code>](#Message)  
<a name="MessageProcessor"></a>

## MessageProcessor
Creates a Message processor. Thes will supply some auto acknowledge logic
and default routing to other queues.  
options:
   autoAck: ['onReceipt'|'afterProcess'|'none'] 
     If 'onReceipt', Message.ack() will be called immediately on receipt of the message
     If 'afterProcess', Message.ack() will be called immediately after processing of the message
     If 'none', Message.ack() will not be called, and the processor must handle it.
   ackOnError: [true|false] 
     Only used if autoAck === 'afterProcess'
     If true, Message.ack() will be called on process error
     else, Message.noAck() will be called on process error

**Kind**: global class  

* [MessageProcessor](#MessageProcessor)
    * [.onMessage(msg)](#MessageProcessor+onMessage) ⇒ <code>Promise</code>
    * [.route()](#MessageProcessor+route)
    * [.process(message, options)](#MessageProcessor+process) ⇒

<a name="MessageProcessor+onMessage"></a>

### messageProcessor.onMessage(msg) ⇒ <code>Promise</code>
Invoked when the reader has a new message to process.

**Kind**: instance method of [<code>MessageProcessor</code>](#MessageProcessor)  
**Returns**: <code>Promise</code> - a Promise that will resolve with an object
        { processed : msg, result : <message forwarded> }  

| Param | Type | Description |
| --- | --- | --- |
| msg | [<code>Message</code>](#Message) | a Message object |

<a name="MessageProcessor+route"></a>

### messageProcessor.route()
This will route the message to the writers as specified by
the Message object and forward. Currently, this is fire and forget.
If forward is false, no routing occurs. If forward is null, message.getMessage()
is routed to the route specifed in the message. If forward is an object, 
it is routed as specified in message (in lieu of message.getMessage() )

**Kind**: instance method of [<code>MessageProcessor</code>](#MessageProcessor)  
<a name="MessageProcessor+process"></a>

### messageProcessor.process(message, options) ⇒
This method should operate on the message and return a promise. This is invoked 
from onMessage(), which will route based on the return. 
The message is an a protocol specific Message object. Use Message.getMessage() to get 
the actual data to process.

**Kind**: instance method of [<code>MessageProcessor</code>](#MessageProcessor)  
**Returns**: a Promise that completes with either null, false, or a replacement message to
forward. If false is returned in the promise, all forward routing is stopped. If null
is returned, the current message will be forwarded. If an object is returned, that
object will be forwarded inplace of the current message. To send messages to other routes,
call this.writer.route() or this.writer.publish()  

| Param | Type | Description |
| --- | --- | --- |
| message | [<code>Message</code>](#Message) | the Message object. |
| options | <code>object</code> | the route options if any were present. This is message.getRoutingOptions() |

<a name="NsqReader"></a>

## NsqReader
Options :
{
   type : 'nsq',
   nsqd : [ ..nsqOptions... ]
   topic : <string>
   channel : <string>
   maxInFlight : <number default=5>
   processor : <function( msg, reader )> | <object with onMessage( msg, reader )>
   closeCountKey
   errorCountKey
   errorResponseCountKey
}

**Kind**: global class  
<a name="PubSubReader"></a>

## PubSubReader
Options :
{
   type : 'pubsub',
   topic : <string>
   channel : <string>
   projectId : <The pubsub project>,
   keyFilename : <The location of the service account file>,
   subscriptionOptions : { } // see https://cloud.google.com/nodejs/docs/reference/pubsub/0.16.x/global#CreateSubscriptionRequest
}

**Kind**: global class  
<a name="Reader"></a>

## Reader
The base class for a Reader. This will manage processing a message via
the processor function or object. Normally options.processor will be an
object that extends MessageProcessor. Subclasses should override onStart()
to connect to their transport and onStop() to disconnect

**Kind**: global class  

* [Reader](#Reader)
    * [.onMessage](#Reader+onMessage)
    * [.onExit](#Reader+onExit)
    * [.start()](#Reader+start)
    * [.onStart()](#Reader+onStart) ⇒ <code>Promise.&lt;this&gt;</code>
    * [.stop()](#Reader+stop)
    * [.onStop()](#Reader+onStop)
    * [.onProcessStarted()](#Reader+onProcessStarted)
    * [.onProcessComplete()](#Reader+onProcessComplete)

<a name="Reader+onMessage"></a>

### reader.onMessage
Routes the message to the processor

**Kind**: instance property of [<code>Reader</code>](#Reader)  
<a name="Reader+onExit"></a>

### reader.onExit
This is used to manage a graceful exit. Do not invoke.

**Kind**: instance property of [<code>Reader</code>](#Reader)  
<a name="Reader+start"></a>

### reader.start()
This should be called to start the reader. 
Returns a Promise indicating when the reader has been initialized

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="Reader+onStart"></a>

### reader.onStart() ⇒ <code>Promise.&lt;this&gt;</code>
Returns a Promise indicating when the reader has been initialized.
Subclasses should override this method. This should not be called
directly. Use start()

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="Reader+stop"></a>

### reader.stop()
Stops the reader from receiving and processing messages
from its connection

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="Reader+onStop"></a>

### reader.onStop()
Called to let subclasses shutdown their connections. This should not be called
directly. Use stop()

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="Reader+onProcessStarted"></a>

### reader.onProcessStarted()
Called at the beginning of onMessage() to increment
the number of active processing threads.

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="Reader+onProcessComplete"></a>

### reader.onProcessComplete()
Called at the end of onMessage() to decrement
the number of active processing threads. If this
reaches zero and the system is exiting, the exit
promise resolved

**Kind**: instance method of [<code>Reader</code>](#Reader)  
<a name="routeFor"></a>

## routeFor(conditionRouteModel, type, object)
Given a condition route model and a type, the model's rules will
be evaluated to find a particular route for that type.

**Kind**: global function  

| Param | Description |
| --- | --- |
| conditionRouteModel | the model to inspect |
| type | <string> the string type to follow, normally a message type |
| object | <map> the objects that are given to the rules for evaluation.   Normally this will have device and msg |

<a name="createWriter"></a>

## createWriter()
Options
 nsqd : [ ...nsqd.... ]

**Kind**: global function  
<a name="routeTargets"></a>

## routeTargets()
A Route has the form:
route := <topic_name> | <route_array> | <topic> | <concurrent>
route_array := [ <route>, <route>, ...]
topic_name := <string>
topic = { topic : <topic_name>, options : <object> optional, route : <route_array> optional, terminate : true | false optional }
concurrent := { <topic_name_0> : true | <route_array> | <topic>, ... <topic_name_n> : true | <route_array> | <topic> } |
              { type : 'concurrent', routes : [ <topic_name> | <topic> ] }

routeTargets() will return an array containing topic objects or null, if there are no routes.

**Kind**: global function  
<a name="createRouteMsg"></a>

## createRouteMsg()
Creates a RouteMsg if either the options or the route is not null. Otherwise
the message will be returned

**Kind**: global function  
