---
id: jsdocs-db-curator
title: DB Curator
---
## Constants

<dl>
<dt><a href="#the">the</a></dt>
<dd></dd>
</dl>

## Functions

<dl>
<dt><a href="#timeout">timeout(ms)</a></dt>
<dd></dd>
<dt><a href="#promisifyQuery">promisifyQuery(Object)</a></dt>
<dd><p>Takes a queryable object, and promisifies its query function</p>
</dd>
<dt><a href="#getCleanupTime">getCleanupTime()</a> ⇒</dt>
<dd></dd>
<dt><a href="#cleanTable">cleanTable(query, db, table, stopTime, startTime)</a></dt>
<dd></dd>
<dt><a href="#cleanDb">cleanDb(query, db, tables, stopTime, startTime)</a></dt>
<dd></dd>
</dl>

<a name="the"></a>

## the
**Kind**: global constant  
<a name="timeout"></a>

## timeout(ms)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| ms | <code>integer</code> | the time to wait |

<a name="promisifyQuery"></a>

## promisifyQuery(Object)
Takes a queryable object, and promisifies its query function

**Kind**: global function  

| Param | Description |
| --- | --- |
| Object | queryable an object with a query function (like a mysql connection or pool) |

<a name="getCleanupTime"></a>

## getCleanupTime() ⇒
**Kind**: global function  
**Returns**: the time to run the next loop ( 3 A.M. UTC in theory )  
<a name="cleanTable"></a>

## cleanTable(query, db, table, stopTime, startTime)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>function</code> | passthrough function to sql query |
| db | <code>string</code> | the database to clean |
| table | <code>string</code> | the table to clean |
| stopTime | <code>Date</code> | the time to stop deleting data |
| startTime | <code>Date</code> | the time to start deleting data |

<a name="cleanDb"></a>

## cleanDb(query, db, tables, stopTime, startTime)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>function</code> | passthrough to sql query |
| db | <code>string</code> | the db to clean |
| tables | <code>Array</code> | all of the tables in the db to clean |
| stopTime | <code>Date</code> | the time to stop deleting data |
| startTime | <code>Date</code> | the time to start deleting data |

