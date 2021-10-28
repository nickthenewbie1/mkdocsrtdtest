---
id: jsdocs-exit
title: Exit
---
## Functions

<dl>
<dt><a href="#init">init(opts)</a></dt>
<dd><p>Initializes the Exit parameters</p>
</dd>
<dt><a href="#add">add(callback, [eventType])</a></dt>
<dd><p>Adds a callback to the exit hooks. These will be called to allow graceful clean up
of resources in an asynchronous way.</p>
</dd>
<dt><a href="#remove">remove(callback)</a></dt>
<dd><p>Removes a callback from the hooks</p>
</dd>
<dt><a href="#callbacks">callbacks([eventType], all)</a></dt>
<dd><p>Returns a new array containing the callbacks</p>
</dd>
<dt><a href="#onUnhandledRejection">onUnhandledRejection()</a></dt>
<dd><p>A shortcut for add( callback, &#39;unhandledRejection&#39; )</p>
</dd>
<dt><a href="#onUncaughtException">onUncaughtException()</a></dt>
<dd><p>A shortcut for add( callback, &#39;uncaughtException&#39; )</p>
</dd>
<dt><a href="#setExitTimeout">setExitTimeout()</a></dt>
<dd><p>Sets the max time in milliseconds to wait before an exit is forced</p>
</dd>
<dt><a href="#getExitTimeout">getExitTimeout()</a></dt>
<dd><p>Returns the max time in milliseconds to wait before an exit is forced</p>
</dd>
<dt><a href="#setExitDelay">setExitDelay()</a></dt>
<dd><p>Sets the time in milliseconds to delay after hooks have finsihed before calling exit</p>
</dd>
<dt><a href="#getExitDelay">getExitDelay()</a></dt>
<dd><p>Gets the time in milliseconds to delay after hooks have finsihed before calling exit</p>
</dd>
<dt><a href="#setExit">setExit()</a></dt>
<dd><p>Sets the exit function. For testing purposes.</p>
</dd>
<dt><a href="#getExit">getExit()</a></dt>
<dd><p>Gets the exit function</p>
</dd>
<dt><a href="#setExitCancelled">setExitCancelled()</a></dt>
<dd><p>Sets the exit cancelled function. For testing purposes. Invoked when
an event has been filtered</p>
</dd>
<dt><a href="#getExitCancelled">getExitCancelled()</a></dt>
<dd><p>Gets the exit cancelled function</p>
</dd>
<dt><a href="#unhandle">unhandle(eventType)</a></dt>
<dd><p>Removes listeners from handling the event of the given type</p>
</dd>
<dt><a href="#handle">handle(eventType, exitCode, opts)</a></dt>
<dd><p>Causes Exit to exit when the event type is received.</p>
</dd>
<dt><a href="#handleErr">handleErr(eventType, exitCode, opts)</a></dt>
<dd><p>Causes Exit to exit when the event type is received. It is treated as an error.</p>
</dd>
<dt><a href="#handlers">handlers()</a> ⇒ <code>object</code></dt>
<dd><p>Returns the installed handlers</p>
</dd>
<dt><a href="#addFilter">addFilter(eventType, filter)</a></dt>
<dd><p>Add a filter for the given event type. A filter can be installed to
stop an exit from occuring. Filters are run before and shutdown hooks.</p>
</dd>
<dt><a href="#removeFilter">removeFilter(eventType, exitCode)</a> ⇒ <code>boolean</code></dt>
<dd><p>Causes Exit to exit when the event type is received.</p>
</dd>
<dt><a href="#filters">filters(eventType)</a> ⇒ <code>object</code> | <code>array</code></dt>
<dd><p>Returns the current filters</p>
</dd>
<dt><a href="#exit">exit(code)</a></dt>
<dd><p>Request a graceful exit</p>
</dd>
<dt><a href="#installDefaultHandlers">installDefaultHandlers()</a></dt>
<dd><p>Installs default signal handlers for SIGINT, SIGHUP, SIGTERM and SIGBREAK.
This will also install uncaughtException and unhandledRejection exceptions</p>
</dd>
</dl>

<a name="init"></a>

## init(opts)
Initializes the Exit parameters

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> | options to set |
| opts.timeout | <code>int</code> | (20000) sets the time in ms to exit event if callbacks havent completed |
| opts.exitDelay | <code>int</code> | (100) sets the time in ms to delay after callbacks have completed before calling exit |
| opts.exit | <code>function</code> | if set, this will be called instead of process.exit(). For testing |
| opts.exitCancelled | <code>function</code> | if set, this will be called when a filter cancels an exit. For testing |

<a name="add"></a>

## add(callback, [eventType])
Adds a callback to the exit hooks. These will be called to allow graceful clean up
of resources in an asynchronous way.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | this function( err, { eventType, code } ) should return a Promise. |
| [eventType] | <code>string</code> | the type to trigger. if this undefined/null, the callback will be triggered for all types. This is mainly used to register callbacks against 'uncaughtException' or 'unhandledRejection' |

<a name="remove"></a>

## remove(callback)
Removes a callback from the hooks

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| callback | <code>function</code> | the function to remove |

<a name="callbacks"></a>

## callbacks([eventType], all)
Returns a new array containing the callbacks

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| [eventType] | <code>string</code> | if supplied, this will return only the callbacks specifically registered for the eventType. |
| all | <code>boolean</code> | if true, then both the specific and general call backs are returned |

<a name="onUnhandledRejection"></a>

## onUnhandledRejection()
A shortcut for add( callback, 'unhandledRejection' )

**Kind**: global function  
<a name="onUncaughtException"></a>

## onUncaughtException()
A shortcut for add( callback, 'uncaughtException' )

**Kind**: global function  
<a name="setExitTimeout"></a>

## setExitTimeout()
Sets the max time in milliseconds to wait before an exit is forced

**Kind**: global function  
<a name="getExitTimeout"></a>

## getExitTimeout()
Returns the max time in milliseconds to wait before an exit is forced

**Kind**: global function  
<a name="setExitDelay"></a>

## setExitDelay()
Sets the time in milliseconds to delay after hooks have finsihed before calling exit

**Kind**: global function  
<a name="getExitDelay"></a>

## getExitDelay()
Gets the time in milliseconds to delay after hooks have finsihed before calling exit

**Kind**: global function  
<a name="setExit"></a>

## setExit()
Sets the exit function. For testing purposes.

**Kind**: global function  
<a name="getExit"></a>

## getExit()
Gets the exit function

**Kind**: global function  
<a name="setExitCancelled"></a>

## setExitCancelled()
Sets the exit cancelled function. For testing purposes. Invoked when
an event has been filtered

**Kind**: global function  
<a name="getExitCancelled"></a>

## getExitCancelled()
Gets the exit cancelled function

**Kind**: global function  
<a name="unhandle"></a>

## unhandle(eventType)
Removes listeners from handling the event of the given type

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the event type to stop listening to. |

<a name="handle"></a>

## handle(eventType, exitCode, opts)
Causes Exit to exit when the event type is received.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the type of event to listen for |
| exitCode | <code>int</code> | the exit code |
| opts | <code>object</code> |  |

<a name="handleErr"></a>

## handleErr(eventType, exitCode, opts)
Causes Exit to exit when the event type is received. It is treated as an error.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the type of event to listen for |
| exitCode | <code>int</code> | the exit code |
| opts | <code>object</code> |  |

<a name="handlers"></a>

## handlers() ⇒ <code>object</code>
Returns the installed handlers

**Kind**: global function  
**Returns**: <code>object</code> - the installed handlers  
<a name="addFilter"></a>

## addFilter(eventType, filter)
Add a filter for the given event type. A filter can be installed to
stop an exit from occuring. Filters are run before and shutdown hooks.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the type to filter |
| filter | <code>function</code> | this function will be given the arguments of the event. If it returns true, the exit will not occur |

<a name="removeFilter"></a>

## removeFilter(eventType, exitCode) ⇒ <code>boolean</code>
Causes Exit to exit when the event type is received.

**Kind**: global function  
**Returns**: <code>boolean</code> - true if the filter was removed  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the type of event to listen for |
| exitCode | <code>int</code> | the exit code |

<a name="filters"></a>

## filters(eventType) ⇒ <code>object</code> \| <code>array</code>
Returns the current filters

**Kind**: global function  
**Returns**: <code>object</code> \| <code>array</code> - if eventType is null, an object of eventType : Array<Filters>
will be returned. Otherwise, an array (possibly empty) will be returned.  

| Param | Type | Description |
| --- | --- | --- |
| eventType | <code>string</code> | the type of filters. If null, all will be returned |

<a name="exit"></a>

## exit(code)
Request a graceful exit

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| code | <code>int</code> | the exit code to use, defaults to zero. |

<a name="installDefaultHandlers"></a>

## installDefaultHandlers()
Installs default signal handlers for SIGINT, SIGHUP, SIGTERM and SIGBREAK.
This will also install uncaughtException and unhandledRejection exceptions

**Kind**: global function  
