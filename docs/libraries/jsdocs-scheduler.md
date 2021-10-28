---
id: jsdocs-scheduler
title: Scheduler
---
## Members

<dl>
<dt><a href="#get/">get/</a></dt>
<dd><p>route to check the status of the server</p>
</dd>
<dt><a href="#post/timer">post/timer</a></dt>
<dd><p>route to create a timer</p>
</dd>
<dt><a href="#get/timer">get/timer</a></dt>
<dd><p>gets all timer/s associated with a system, project or device</p>
</dd>
<dt><a href="#get/timer/_id">get/timer/:id</a></dt>
<dd><p>gets a specific timer associated with an id</p>
</dd>
<dt><a href="#put/timer">put/timer</a></dt>
<dd><p>updates a timer</p>
</dd>
<dt><a href="#delete/timer">delete/timer</a></dt>
<dd><p>deletes a timer</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#validateURL">validateURL(urlString)</a></dt>
<dd><p>validates a URL</p>
</dd>
<dt><a href="#ApiAction">ApiAction(action)</a></dt>
<dd><p>Validates that an action has a valid url associated with it</p>
</dd>
<dt><a href="#create">create(options)</a></dt>
<dd><p>creates an Express app with routes</p>
</dd>
<dt><a href="#addErrorHandler">addErrorHandler(app)</a></dt>
<dd><p>middleware error handler</p>
</dd>
<dt><a href="#responseTime">responseTime()</a></dt>
<dd><p>logs how long the server it taking to respond</p>
</dd>
<dt><a href="#makeApiTimer">makeApiTimer(rawTimer)</a></dt>
<dd><p>deletes processed fields and parse action and timer fields</p>
</dd>
<dt><a href="#install">install(app, options)</a></dt>
<dd><p>adds routes onto an express app</p>
</dd>
<dt><a href="#init">init(builderOptions)</a></dt>
<dd><p>returns an object with several methods for interacting with the database</p>
</dd>
</dl>

<a name="get/"></a>

## get/
route to check the status of the server

**Kind**: global variable  
<a name="post/timer"></a>

## post/timer
route to create a timer

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the timer to be created |
| timer | <code>Timer</code> | timer that will be created |

<a name="get/timer"></a>

## get/timer
gets all timer/s associated with a system, project or device

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | system, device or project id |

<a name="get/timer/_id"></a>

## get/timer/:id
gets a specific timer associated with an id

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | timer id |

<a name="put/timer"></a>

## put/timer
updates a timer

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the timer to be updated |
| timer | <code>Timer</code> | updated timer to replace the current timer |

<a name="delete/timer"></a>

## delete/timer
deletes a timer

**Kind**: global variable  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the timer to be deleted |

<a name="validateURL"></a>

## validateURL(urlString)
validates a URL

**Kind**: global function  

| Param | Type |
| --- | --- |
| urlString | <code>string</code> | 

<a name="ApiAction"></a>

## ApiAction(action)
Validates that an action has a valid url associated with it

**Kind**: global function  

| Param | Type |
| --- | --- |
| action | <code>object</code> | 

<a name="create"></a>

## create(options)
creates an Express app with routes

**Kind**: global function  

| Param | Type |
| --- | --- |
| options | <code>object</code> | 

<a name="addErrorHandler"></a>

## addErrorHandler(app)
middleware error handler

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| app | <code>Express</code> | express app |

<a name="responseTime"></a>

## responseTime()
logs how long the server it taking to respond

**Kind**: global function  
<a name="makeApiTimer"></a>

## makeApiTimer(rawTimer)
deletes processed fields and parse action and timer fields

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| rawTimer | <code>Timer</code> | timer that will be processed into an ApiTimer |

<a name="install"></a>

## install(app, options)
adds routes onto an express app

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| app | <code>Express</code> | express app |
| options | <code>object</code> |  |

<a name="init"></a>

## init(builderOptions)
returns an object with several methods for interacting with the database

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| builderOptions | <code>object</code> | database options |


* [init(builderOptions)](#init)
    * [~getDatabase(escape)](#init..getDatabase)
    * [~getTable(escape)](#init..getTable)
    * [~createDatabase()](#init..createDatabase)
    * [~createTable()](#init..createTable)
    * [~scheduleTimer(timer)](#init..scheduleTimer)
    * [~scheduleOrReplaceTimer(timer)](#init..scheduleOrReplaceTimer)
    * [~queryFromArray(query)](#init..queryFromArray)
    * [~orderFromOpts(opts)](#init..orderFromOpts)
    * [~limitFromOpts(opts)](#init..limitFromOpts)
    * [~getTimers(opts)](#init..getTimers)
    * [~deleteTimersByHints(opts)](#init..deleteTimersByHints)
    * [~getTimersToProcess(opts)](#init..getTimersToProcess)
    * [~markNextTimers(opts)](#init..markNextTimers)
    * [~rescheduleTimer(timer, now)](#init..rescheduleTimer)
    * [~bulkRescheduleTimers(timers, now)](#init..bulkRescheduleTimers)
    * [~deleteTimers(opts)](#init..deleteTimers)

<a name="init..getDatabase"></a>

### init~getDatabase(escape)
gets the database

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| escape | <code>boolean</code> | if true will use the escaped db |

<a name="init..getTable"></a>

### init~getTable(escape)
gets the table

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| escape | <code>boolean</code> | if true will use the escaped table |

<a name="init..createDatabase"></a>

### init~createDatabase()
returns a sql statement to create a database if it doesn't exist

**Kind**: inner method of [<code>init</code>](#init)  
<a name="init..createTable"></a>

### init~createTable()
returns a sql statement to create a table if it doesn't exist

**Kind**: inner method of [<code>init</code>](#init)  
<a name="init..scheduleTimer"></a>

### init~scheduleTimer(timer)
returns a sql statement that will insert into a timer

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| timer | <code>Timer</code> | timer that will be added to the database |

<a name="init..scheduleOrReplaceTimer"></a>

### init~scheduleOrReplaceTimer(timer)
returns a replace sql statement

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| timer | <code>Timer</code> | timer that will be replaced |

<a name="init..queryFromArray"></a>

### init~queryFromArray(query)
creates a query that performs several operations

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>object</code> |  |
| query.token | <code>array</code> | objects that have an operation, column and value |

<a name="init..orderFromOpts"></a>

### init~orderFromOpts(opts)
creates an order by clause

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> |  |
| opts.order | <code>string</code> | value to order by |

<a name="init..limitFromOpts"></a>

### init~limitFromOpts(opts)
creates a limit clause

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 
| opts.limit | <code>string</code> \| <code>numbder</code> | 

<a name="init..getTimers"></a>

### init~getTimers(opts)
creates a select query for timers

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 

<a name="init..deleteTimersByHints"></a>

### init~deleteTimersByHints(opts)
creates a delete query for timers

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 
| opts.query | <code>object</code> | 

<a name="init..getTimersToProcess"></a>

### init~getTimersToProcess(opts)
creates a select query to get unprocessed timers

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 

<a name="init..markNextTimers"></a>

### init~markNextTimers(opts)
creates a query to update processed and processedBy

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 

<a name="init..rescheduleTimer"></a>

### init~rescheduleTimer(timer, now)
creates a query to update when for and unprocessed timer

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| timer | <code>Timer</code> | 
| now | <code>Date</code> | 

<a name="init..bulkRescheduleTimers"></a>

### init~bulkRescheduleTimers(timers, now)
creates a query to update when for many unprocessed timers

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type | Description |
| --- | --- | --- |
| timers | <code>array</code> | array of Timers |
| now | <code>Date</code> |  |

<a name="init..deleteTimers"></a>

### init~deleteTimers(opts)
creates a query to delete timer/s

**Kind**: inner method of [<code>init</code>](#init)  

| Param | Type |
| --- | --- |
| opts | <code>object</code> | 

