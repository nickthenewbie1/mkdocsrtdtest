---
id: jsdocs-api-server
title: API Server
---
## Classes

<dl>
<dt><a href="#EventController">EventController</a></dt>
<dd><p>This class acts a controller for all things related to events</p>
</dd>
<dt><a href="#HistoryController">HistoryController</a></dt>
<dd><p>This class acts a controller for all things related to history</p>
</dd>
<dt><a href="#PendingUserController">PendingUserController</a></dt>
<dd><p>Table
projectId | Issuer | emailOrName | PermissionId | Context</p>
</dd>
<dt><a href="#BigQueryQueryer">BigQueryQueryer</a></dt>
<dd><p>This is the connection/query engine owner for a big query json layout</p>
</dd>
<dt><a href="#JsonQueryer">JsonQueryer</a></dt>
<dd><p>This is the connection/query engine owner for a big query json layout</p>
</dd>
<dt><a href="#Models">Models</a></dt>
<dd><p>This is a subtle wrapper around sequelize to create and sync the database.</p>
</dd>
</dl>

## Members

<dl>
<dt><a href="#systemId">systemId</a></dt>
<dd><p>Returns the project id if the data is loaded</p>
</dd>
<dt><a href="#projectId">projectId</a></dt>
<dd><p>Returns the project id if the data is loaded</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#columnTest">columnTest</a></dt>
<dd><p>This is a regex test that detects if the input
string matches the format to reference a column
in an aggregate function</p>
</dd>
<dt><a href="#DEFAULT_RAW_OPERATORS">DEFAULT_RAW_OPERATORS</a> : <code>Object</code></dt>
<dd><p>the default allowed raw operators and how to translate them in sequelize</p>
</dd>
<dt><a href="#DEFAULT_DEFAULT_TYPE">DEFAULT_DEFAULT_TYPE</a> : <code>String</code></dt>
<dd><p>the default type to cast to when all else fails</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#create">create(options)</a></dt>
<dd><p>Returns an object containing named controllers. This controllers
will be installed into the context and will be available for use
to access/change data. To use these, there are two steps. The first
it to invoke this method. The results should be merged into the context
object. The second step it to call init() with the result and the context
to &#39;start&#39; the controllers.</p>
</dd>
<dt><a href="#init">init(cxt, controllers)</a></dt>
<dd><p>This will call init(cxt) on all the controllers in the controllers object</p>
</dd>
<dt><a href="#resolveTemplate">resolveTemplate()</a></dt>
<dd><p>Returns a Template object. idOrTemp can be either an
id, a Template object, or a { id }</p>
</dd>
<dt><a href="#buildStruct">buildStruct(attrTree)</a> ⇒</dt>
<dd><p>This function builds a tree out of a list of requested attributes</p>
</dd>
<dt><a href="#buildStruct">buildStruct(attrTree)</a> ⇒</dt>
<dd><p>This function builds a tree out of a list of requested attributes</p>
</dd>
<dt><a href="#getServiceConfig">getServiceConfig()</a></dt>
<dd><p>returns the firebase definition to be sent to a service</p>
</dd>
<dt><a href="#simpleLiteralFunctionBuilder">simpleLiteralFunctionBuilder(literal)</a> ⇒</dt>
<dd><p>This function is a builder for an arithmetic
operation handler designed to be plugged back through
the json query util</p>
</dd>
<dt><a href="#bucketTimeArgs">bucketTimeArgs(args)</a> ⇒</dt>
<dd></dd>
<dt><a href="#BUCKET_TIME">BUCKET_TIME(args)</a> ⇒</dt>
<dd><p>This is an alias that will look like a single sql function, but that actually
consists of a set of operations that transform time fields into discrete buckets
that can then be grouped/aggregated by bucket/window</p>
</dd>
<dt><a href="#getSqlFromFindAll">getSqlFromFindAll(the, the)</a> ⇒ <code>Promise.&lt;string&gt;</code></dt>
<dd><p>a function to get a find all query from a model and some options
<a href="https://github.com/sequelize/sequelize/issues/2325">https://github.com/sequelize/sequelize/issues/2325</a> &lt;- screw this guy</p>
</dd>
<dt><a href="#prepareOptions">prepareOptions()</a></dt>
<dd><p>taken from sequelize</p>
</dd>
<dt><a href="#buildStruct">buildStruct(attrTree)</a> ⇒</dt>
<dd><p>This function builds a tree out of a list of requested attributes</p>
</dd>
<dt><a href="#getChildrenData">getChildrenData()</a></dt>
<dd><p>Returns the child objects in the table. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ obj1...objN ] }</p>
</dd>
<dt><a href="#removeAll">removeAll()</a></dt>
<dd><p>This will call delete on all children in the
table. If the accumBuffer is not null, the
update to the db is not performed here, but
from the invoker.</p>
</dd>
<dt><a href="#getData">getData()</a></dt>
<dd><p>Retrieves the data object form this DataItem, sets it as
the current data, and returns it as the result in the callback</p>
</dd>
<dt><a href="#delete">delete()</a></dt>
<dd><p>Deletes the data item and all its children. If the accumBuffer is not defined,
than this is the root of the delete. All children should be removed, as well as
all references. If accumBuffer is present, it&#39;s keys should be updated with the
new firebase value (normally null). All changes will be pushed at once.</p>
<p>If this class implements a deleteResources( accumBuffer, cb ) method, it will be
invoked to allow for the cleanup of any external resources.</p>
</dd>
<dt><a href="#changeNetwork">changeNetwork()</a></dt>
<dd><p>Changes the networkId of the device. This will remove aliases from the current
network and call join/leaveNetwork as needed</p>
</dd>
<dt><a href="#changeSimNetwork">changeSimNetwork()</a></dt>
<dd><p>Changes the simNetworkId of the device. This will remove aliases from the current
network and call join/leaveNetwork as needed</p>
</dd>
<dt><a href="#getMessageRouteForDevice">getMessageRouteForDevice()</a></dt>
<dd><p>This will return a Promise with the &#39;routes&#39; part of a MessageRoute.</p>
</dd>
<dt><a href="#getId">getId()</a></dt>
<dd><p>Returns the id of device with the given network, aliasKey and alias</p>
</dd>
<dt><a href="#getNetworkAliases">getNetworkAliases()</a></dt>
<dd><p>Looks up the networkAliases on the object with the given id</p>
</dd>
<dt><a href="#getAlias">getAlias()</a></dt>
<dd><p>Looks up the specific networkAlias on the object with the given id</p>
</dd>
<dt><a href="#addAccount">addAccount()</a></dt>
<dd><p>Accounts are Users that were made by the project. They are deleted when the project is deleted,
and the user&#39;s username is unique in the project.</p>
</dd>
<dt><a href="#acquireProjectAlias">acquireProjectAlias()</a></dt>
<dd><p>Attempts to acquire the aliasName for the project. The aliasType determines
the kind of alias (like a &#39;blueprint&#39; alias), the aliasName is the desired
human readable name, and the id is the actual if of the referenced object.</p>
<p>The lock will be saved like this:
   -projectAlias
     -projectId
       -aliasType
         -aliasName : id</p>
</dd>
<dt><a href="#removeRef">removeRef()</a></dt>
<dd><p>Removes the ref between the owner and the reference object.</p>
</dd>
<dt><a href="#getRef">getRef()</a></dt>
<dd><p>Returns the value stored at the ownerId&#39;s refId. This is the last
value pasted into addRef for the given ownerId/refId</p>
</dd>
<dt><a href="#getRefSubValue">getRefSubValue()</a></dt>
<dd><p>Returns the value stored at the ownerId&#39;s refId[subpath]. This is the last
value passed into addRef for the given ownerId/refId</p>
</dd>
<dt><a href="#getRefsData">getRefsData()</a></dt>
<dd><p>Returns the ref objects in the table. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ obj1...objN ] }. Each
objN will contain: { id : <id>, type : <type>, value : <value> }</p>
</dd>
<dt><a href="#getOwnerIds">getOwnerIds()</a></dt>
<dd><p>Returns the owner ids of the owners that include the ref. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ ownerId1...ownerIdN ] }.</p>
</dd>
<dt><a href="#saveWithManualId">saveWithManualId(rootRef, idFunc(, data, cb)</a></dt>
<dd><p>This will attempt to create a rootRef/<id> entry where the
id is created by idFunc. This allows human friendly ideas to
be created.</p>
</dd>
<dt><a href="#deleteResources">deleteResources()</a></dt>
<dd><p>Remove the project alias if it exists. Note, the check of the validity of
the alias is performed in the controller</p>
</dd>
<dt><a href="#delete">delete()</a></dt>
<dd><p>This assumes the user has been deleted</p>
</dd>
<dt><a href="#encodeOpenIdUser">encodeOpenIdUser()</a></dt>
<dd><p>Encodes the iss and sub into a string useable as a firebase key</p>
</dd>
<dt><a href="#keyForOpenIdUser">keyForOpenIdUser(iss, sub)</a></dt>
<dd><p>Returns the firebase key for the openid</p>
</dd>
<dt><a href="#openIdUserExists">openIdUserExists(iss, sub)</a> ⇒ <code>boolean</code> | <code>string</code></dt>
<dd><p>Returns the user if for the iss/sub combination, or false if it doesn&#39;t exist</p>
</dd>
<dt><a href="#getOpenIdUserForJwt">getOpenIdUserForJwt(jwt)</a></dt>
<dd><p>returns the User data or null if they don&#39;t exist</p>
</dd>
<dt><a href="#createOpenIdUser">createOpenIdUser(iss, sub, userInfo, returnExistingUser)</a></dt>
<dd><p>This will create and return the user for the</p>
</dd>
<dt><a href="#deleteOpenIdUser">deleteOpenIdUser()</a></dt>
<dd><p>This assumes the user has been deleted</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>This will create a Models object and starts it. If options.createModels
is null, this will use the Definitions.createModels by default.</p>
</dd>
<dt><a href="#convertToData">convertToData()</a></dt>
<dd><p>Converts the object into the form:
[ { path : <path>, value : <value> }, ...]
The value forms of obj are:
1) { values : [ { path : <path>, value : <value> }, ...] }
2) [ { path : <path>, value : <value> }, ...]
3) { path : <path>, value: <value> }
4) { keyValue : { <path1> : <value>, <path2> : <value> }}</p>
</dd>
<dt><a href="#setDeviceData">setDeviceData()</a></dt>
<dd><p>Sets the realtime data for the device. The data should be one of these formats:
1) { values : [ { path : <path>, value : <value> }, ...] }
2) [ { path : <path>, value : <value> }, ...]
3) { path : <path>, value: <value> }
4) { keyValue : { <path1> : <value>, <path2> : <value> }}</p>
</dd>
<dt><a href="#addDeviceUser">addDeviceUser(device, userData)</a></dt>
<dd><p>Addes a user to the system.</p>
</dd>
<dt><a href="#createCheckNearestPermission">createCheckNearestPermission(deviceSource, check)</a></dt>
<dd><p>This will return a function(req, res, next) that will check for read permissions on the 
devicec and walk the device.parentDeviceId field to check to see if the
user has permission to read the device from any of those devices</p>
</dd>
<dt><a href="#sendMessage">sendMessage(sendMessage, device, message)</a></dt>
<dd><p>This function will send an outbound message to a device on its network</p>
</dd>
<dt><a href="#flatten">flatten()</a></dt>
<dd><p>This will flatten either an patch ops array or an object
into { &#39;a/b/c&#39; : 1 }</p>
</dd>
<dt><a href="#projectTransfer">projectTransfer()</a></dt>
<dd><p>Determines if a project transfer is occuring anf performs it.
the next function will be invoked with next( err, [ ..ops..] ),
where the &#39;projectId&#39; element in the ops array will be removed.</p>
</dd>
<dt><a href="#appendLookupToResultList">appendLookupToResultList(options)</a></dt>
<dd><p>Will look for items to expand and include in the result list. The result object
should look like { startIndex, count, total, items, search }. This will append
to result, a refs : { XXX : { id : {...} } } object, where XXX is blueprint, network, 
etc</p>
</dd>
<dt><a href="#createGetAccessToken">createGetAccessToken()</a></dt>
<dd><p>Returns a function that will request an access token from the database in
dbInfo. dbInfo should contain { db : the database, service: the service, key : the 
location to place the accessToken in applyTo  }</p>
</dd>
<dt><a href="#allowUpdate">allowUpdate()</a></dt>
<dd><p>Returns false if the patch ops array contains a path that is not
in the given valid array</p>
</dd>
<dt><a href="#createResult">createResult(user, options, authJwt)</a> ⇒ <code>Promise.&lt;Object&gt;</code></dt>
<dd><p>Creates response object for a verification of the previous jwt token</p>
</dd>
<dt><a href="#sendDeviceMessage">sendDeviceMessage()</a></dt>
<dd><p>Sends the message using the device&#39;s routes model or the defaultTopic</p>
</dd>
<dt><a href="#joinNetwork">joinNetwork(cb)</a></dt>
<dd></dd>
<dt><a href="#leaveNetwork">leaveNetwork(cb)</a></dt>
<dd></dd>
<dt><a href="#aliasSet">aliasSet(cb)</a></dt>
<dd></dd>
<dt><a href="#sendMessage">sendMessage(network, device, msg, cb)</a></dt>
<dd><p>Attempts to send a message to the given device on the given
network.</p>
</dd>
<dt><a href="#cleanse">cleanse()</a> ⇒</dt>
<dd><p>Removes any project sensitive data from the network.</p>
</dd>
<dt><a href="#send">send()</a></dt>
<dd><p>Uses Request to send a message. Unlike request, this
will convert any statusCode &lt; 200 or &gt;= 300 to an error</p>
</dd>
<dt><a href="#getTemplateContext">getTemplateContext()</a></dt>
<dd><p>Used to constuct a template context for use in building the db root. The extra
should contain at least systemId and deviceId.</p>
</dd>
<dt><a href="#v4">v4()</a></dt>
<dd><p>v4</p>
</dd>
<dt><a href="#v1">v1()</a></dt>
<dd><p>v1</p>
</dd>
<dt><a href="#encode">encode()</a></dt>
<dd><p>encode</p>
</dd>
<dt><a href="#decode">decode()</a></dt>
<dd><p>decode</p>
</dd>
<dt><a href="#ensureLength">ensureLength()</a></dt>
<dd><p>ensureLength</p>
</dd>
<dt><a href="#padLeft">padLeft()</a></dt>
<dd><p>padLeft</p>
</dd>
<dt><a href="#trimLeft">trimLeft()</a></dt>
<dd><p>trimLeft</p>
</dd>
</dl>

<a name="EventController"></a>

## EventController
This class acts a controller for all things related to events

**Kind**: global class  

* [EventController](#EventController)
    * _instance_
        * [.ackEvent(projectId, ack, device)](#EventController+ackEvent) ⇒ <code>Promise</code>
        * [.initProject(projectId)](#EventController+initProject) ⇒ <code>Promise.&lt;array&gt;</code>
        * [.query(q, context)](#EventController+query) ⇒ <code>Promise.&lt;object&gt;</code>
        * [.initQueryUtil(util, models)](#EventController+initQueryUtil)
    * _static_
        * [.queryTransform(model, obj, q)](#EventController.queryTransform) ⇒ <code>string</code>

<a name="EventController+ackEvent"></a>

### eventController.ackEvent(projectId, ack, device) ⇒ <code>Promise</code>
This functions attempts to ack an event

**Kind**: instance method of [<code>EventController</code>](#EventController)  
**Returns**: <code>Promise</code> - resolves after sending the event on the device route  

| Param | Type | Description |
| --- | --- | --- |
| projectId | <code>string</code> | the project we are acking an event in |
| ack | <code>object</code> | the ack object to send back to the writer |
| device | <code>Device</code> | the device object needed to send back to writer |

<a name="EventController+initProject"></a>

### eventController.initProject(projectId) ⇒ <code>Promise.&lt;array&gt;</code>
this attempts to create the pea table in all of the dbs (sql and bigquery)

**Kind**: instance method of [<code>EventController</code>](#EventController)  
**Returns**: <code>Promise.&lt;array&gt;</code> - resolves once all of the tables exists or fails if creation fails  

| Param | Type | Description |
| --- | --- | --- |
| projectId | <code>string</code> | the id of the project we need to make tables for |

<a name="EventController+query"></a>

### eventController.query(q, context) ⇒ <code>Promise.&lt;object&gt;</code>
**Kind**: instance method of [<code>EventController</code>](#EventController)  
**Returns**: <code>Promise.&lt;object&gt;</code> - the results of the query  

| Param | Type | Description |
| --- | --- | --- |
| q | <code>object</code> | the query object |
| context | <code>object</code> | the context of the query process |
| context.deviceId | <code>object</code> | the (potential) device to query |
| context.systemId | <code>object</code> | the (potential) system to query |
| context.projectId | <code>object</code> | the project to query |
| context.mode | <code>object</code> | device|system|project dictates the table to hit |

<a name="EventController+initQueryUtil"></a>

### eventController.initQueryUtil(util, models)
This function inits a query util for either bigquery or cloudsql

**Kind**: instance method of [<code>EventController</code>](#EventController)  

| Param | Type | Description |
| --- | --- | --- |
| util | <code>object</code> | the query util we need to define the models in |
| models | <code>object</code> | the models object to add the resulting models to |

<a name="EventController.queryTransform"></a>

### EventController.queryTransform(model, obj, q) ⇒ <code>string</code>
**Kind**: static method of [<code>EventController</code>](#EventController)  
**Returns**: <code>string</code> - the edited query string  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>Sequelize.Model</code> | A sequelize model that we are querying (some kind of event always) |
| model.imaginePrefix | <code>Sequelize.Model</code> | the table prefix |
| obj | <code>object</code> | a context object containing the table name |
| obj.table | <code>string</code> | the table that we are replacing in |
| obj.database | <code>string</code> | the database that we are replacing in |
| q | <code>string</code> | the query string that we are transforming |

<a name="HistoryController"></a>

## HistoryController
This class acts a controller for all things related to history

**Kind**: global class  

* [HistoryController](#HistoryController)
    * _instance_
        * [.query(q, context)](#HistoryController+query) ⇒ <code>Promise.&lt;object&gt;</code>
        * [.initQueryUtil(util, models)](#HistoryController+initQueryUtil)
    * _static_
        * [.queryTransform(model, obj, q)](#HistoryController.queryTransform) ⇒ <code>string</code>

<a name="HistoryController+query"></a>

### historyController.query(q, context) ⇒ <code>Promise.&lt;object&gt;</code>
**Kind**: instance method of [<code>HistoryController</code>](#HistoryController)  
**Returns**: <code>Promise.&lt;object&gt;</code> - the results of the query  

| Param | Type | Description |
| --- | --- | --- |
| q | <code>object</code> | the query object |
| context | <code>object</code> | the context of the query process |
| context.deviceId | <code>object</code> | the (potential) device to query |
| context.systemId | <code>object</code> | the (potential) system to query |
| context.projectId | <code>object</code> | the project to query |
| context.mode | <code>object</code> | device|system|project dictates the table to hit |

<a name="HistoryController+initQueryUtil"></a>

### historyController.initQueryUtil(util, models)
This function inits a query util for either bigquery or cloudsql

**Kind**: instance method of [<code>HistoryController</code>](#HistoryController)  

| Param | Type | Description |
| --- | --- | --- |
| util | <code>object</code> | the query util we need to define the models in |
| models | <code>object</code> | the models object to add the resulting models to |

<a name="HistoryController.queryTransform"></a>

### HistoryController.queryTransform(model, obj, q) ⇒ <code>string</code>
**Kind**: static method of [<code>HistoryController</code>](#HistoryController)  
**Returns**: <code>string</code> - the edited query string  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>Sequelize.Model</code> | A sequelize model that we are querying (some kind of event always) |
| model.imaginePrefix | <code>Sequelize.Model</code> | the table prefix |
| obj | <code>object</code> | a context object containing the table name |
| obj.table | <code>string</code> | the table that we are replacing in |
| obj.database | <code>string</code> | the database that we are replacing in |
| q | <code>string</code> | the query string that we are transforming |

<a name="PendingUserController"></a>

## PendingUserController
Table
projectId | Issuer | emailOrName | PermissionId | Context

**Kind**: global class  

* [PendingUserController](#PendingUserController)
    * [.add()](#PendingUserController+add)
    * [.delete()](#PendingUserController+delete)
    * [.list()](#PendingUserController+list)

<a name="PendingUserController+add"></a>

### pendingUserController.add()
Adds an issuer/emailOrName permission for project and a context

**Kind**: instance method of [<code>PendingUserController</code>](#PendingUserController)  
<a name="PendingUserController+delete"></a>

### pendingUserController.delete()
Removes an issuer/emailOrName permission for project and a context

**Kind**: instance method of [<code>PendingUserController</code>](#PendingUserController)  
<a name="PendingUserController+list"></a>

### pendingUserController.list()
Gets the issuer, emailOrName, permission and context objects for the projectId

**Kind**: instance method of [<code>PendingUserController</code>](#PendingUserController)  
<a name="BigQueryQueryer"></a>

## BigQueryQueryer
This is the connection/query engine owner for a big query json layout

**Kind**: global class  
<a name="BigQueryQueryer+initProject"></a>

### bigQueryQueryer.initProject(projectId) ⇒ <code>Promise</code>
inits a database for a given project

**Kind**: instance method of [<code>BigQueryQueryer</code>](#BigQueryQueryer)  
**Returns**: <code>Promise</code> - resolves when the project has been initialized  

| Param | Type | Description |
| --- | --- | --- |
| projectId | <code>string</code> | the id of the project |

<a name="JsonQueryer"></a>

## JsonQueryer
This is the connection/query engine owner for a big query json layout

**Kind**: global class  

* [JsonQueryer](#JsonQueryer)
    * [.initProject(projectId)](#JsonQueryer+initProject) ⇒ <code>Promise</code>
    * [.query(model, include, q, opts)](#JsonQueryer+query) ⇒ <code>promise.&lt;array&gt;</code>

<a name="JsonQueryer+initProject"></a>

### jsonQueryer.initProject(projectId) ⇒ <code>Promise</code>
inits a database for a given project

**Kind**: instance method of [<code>JsonQueryer</code>](#JsonQueryer)  
**Returns**: <code>Promise</code> - resolves when the project has been initialized  

| Param | Type | Description |
| --- | --- | --- |
| projectId | <code>string</code> | the id of the project |

<a name="JsonQueryer+query"></a>

### jsonQueryer.query(model, include, q, opts) ⇒ <code>promise.&lt;array&gt;</code>
queries bigquery with the query built by the query utility

**Kind**: instance method of [<code>JsonQueryer</code>](#JsonQueryer)  
**Returns**: <code>promise.&lt;array&gt;</code> - resolves a promise with the results of the query  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>Sequelize.Model</code> | the model to query against |
| include | <code>array</code> | an optional set of models to join in the query |
| q | <code>object</code> | the query object |
| opts | <code>object</code> | a configuration manager for querying |

<a name="Models"></a>

## Models
This is a subtle wrapper around sequelize to create and sync the database.

**Kind**: global class  

* [Models](#Models)
    * [new Models(options)](#new_Models_new)
    * [.checkDatabase()](#Models+checkDatabase)
    * [.start()](#Models+start)
    * [.stop()](#Models+stop)
    * [.destroy()](#Models+destroy)

<a name="new_Models_new"></a>

### new Models(options)
Create Models object


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.sequelize | <code>object</code> | the sequelize options |
| options.createModels | <code>function</code> | a function( sequelize ) that defines the models. This function should NOT call sync() on sequelize |

<a name="Models+checkDatabase"></a>

### models.checkDatabase()
Creates the database if it does not exist

**Kind**: instance method of [<code>Models</code>](#Models)  
<a name="Models+start"></a>

### models.start()
Starts sequelize

**Kind**: instance method of [<code>Models</code>](#Models)  
<a name="Models+stop"></a>

### models.stop()
Stops sequelize

**Kind**: instance method of [<code>Models</code>](#Models)  
<a name="Models+destroy"></a>

### models.destroy()
This only works in test mode. It will drop the database

**Kind**: instance method of [<code>Models</code>](#Models)  
<a name="systemId"></a>

## systemId
Returns the project id if the data is loaded

**Kind**: global variable  
<a name="projectId"></a>

## projectId
Returns the project id if the data is loaded

**Kind**: global variable  
<a name="columnTest"></a>

## columnTest
This is a regex test that detects if the input
string matches the format to reference a column
in an aggregate function

**Kind**: global constant  
<a name="DEFAULT_RAW_OPERATORS"></a>

## DEFAULT\_RAW\_OPERATORS : <code>Object</code>
the default allowed raw operators and how to translate them in sequelize

**Kind**: global constant  
<a name="DEFAULT_DEFAULT_TYPE"></a>

## DEFAULT\_DEFAULT\_TYPE : <code>String</code>
the default type to cast to when all else fails

**Kind**: global constant  
<a name="create"></a>

## create(options)
Returns an object containing named controllers. This controllers
will be installed into the context and will be available for use
to access/change data. To use these, there are two steps. The first
it to invoke this method. The results should be merged into the context
object. The second step it to call init() with the result and the context
to 'start' the controllers.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | The system configuration |

<a name="init"></a>

## init(cxt, controllers)
This will call init(cxt) on all the controllers in the controllers object

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| cxt | <code>object</code> | the context |
| controllers | <code>object</code> | the result returned from create() |

<a name="resolveTemplate"></a>

## resolveTemplate()
Returns a Template object. idOrTemp can be either an
id, a Template object, or a { id }

**Kind**: global function  
<a name="buildStruct"></a>

## buildStruct(attrTree) ⇒
This function builds a tree out of a list of requested attributes

**Kind**: global function  
**Returns**: a list of arguments for a JSON_OBJECT sql function call  

| Param | Type | Description |
| --- | --- | --- |
| attrTree | <code>Object</code> | a deep object of attributes to turn into a query |

<a name="buildStruct"></a>

## buildStruct(attrTree) ⇒
This function builds a tree out of a list of requested attributes

**Kind**: global function  
**Returns**: a list of arguments for a JSON_OBJECT sql function call  

| Param | Type | Description |
| --- | --- | --- |
| attrTree | <code>Object</code> | a deep object of attributes to turn into a query |

<a name="getServiceConfig"></a>

## getServiceConfig()
returns the firebase definition to be sent to a service

**Kind**: global function  
<a name="simpleLiteralFunctionBuilder"></a>

## simpleLiteralFunctionBuilder(literal) ⇒
This function is a builder for an arithmetic
operation handler designed to be plugged back through
the json query util

**Kind**: global function  
**Returns**: a builder function for the arithmetic operator  

| Param | Type | Description |
| --- | --- | --- |
| literal | <code>string</code> | the arithmetic operator |

<a name="bucketTimeArgs"></a>

## bucketTimeArgs(args) ⇒
**Kind**: global function  
**Returns**: an object with the resolved bucketSize and column  

| Param | Type | Description |
| --- | --- | --- |
| args | <code>Array</code> | an arrray of arguments for a bucket time function |

<a name="BUCKET_TIME"></a>

## BUCKET\_TIME(args) ⇒
This is an alias that will look like a single sql function, but that actually
consists of a set of operations that transform time fields into discrete buckets
that can then be grouped/aggregated by bucket/window

**Kind**: global function  
**Returns**: the resulting function operators to be passed back to the json query util  

| Param | Type | Description |
| --- | --- | --- |
| args | <code>array</code> | the arguments for the BUCKET_TIME sql alias |

<a name="getSqlFromFindAll"></a>

## getSqlFromFindAll(the, the) ⇒ <code>Promise.&lt;string&gt;</code>
a function to get a find all query from a model and some options
https://github.com/sequelize/sequelize/issues/2325 <- screw this guy

**Kind**: global function  
**Returns**: <code>Promise.&lt;string&gt;</code> - resolves with the query  

| Param | Type | Description |
| --- | --- | --- |
| the | <code>Sequelize.Model</code> | model to build the query with |
| the | <code>object</code> | sequelize query options |

<a name="prepareOptions"></a>

## prepareOptions()
taken from sequelize

**Kind**: global function  
<a name="buildStruct"></a>

## buildStruct(attrTree) ⇒
This function builds a tree out of a list of requested attributes

**Kind**: global function  
**Returns**: a list of arguments for a JSON_OBJECT sql function call  

| Param | Type | Description |
| --- | --- | --- |
| attrTree | <code>Object</code> | a deep object of attributes to turn into a query |

<a name="getChildrenData"></a>

## getChildrenData()
Returns the child objects in the table. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ obj1...objN ] }

**Kind**: global function  
<a name="removeAll"></a>

## removeAll()
This will call delete on all children in the
table. If the accumBuffer is not null, the
update to the db is not performed here, but
from the invoker.

**Kind**: global function  
<a name="getData"></a>

## getData()
Retrieves the data object form this DataItem, sets it as
the current data, and returns it as the result in the callback

**Kind**: global function  
<a name="delete"></a>

## delete()
Deletes the data item and all its children. If the accumBuffer is not defined,
than this is the root of the delete. All children should be removed, as well as
all references. If accumBuffer is present, it's keys should be updated with the
new firebase value (normally null). All changes will be pushed at once.

If this class implements a deleteResources( accumBuffer, cb ) method, it will be
invoked to allow for the cleanup of any external resources.

**Kind**: global function  
<a name="changeNetwork"></a>

## changeNetwork()
Changes the networkId of the device. This will remove aliases from the current
network and call join/leaveNetwork as needed

**Kind**: global function  
<a name="changeSimNetwork"></a>

## changeSimNetwork()
Changes the simNetworkId of the device. This will remove aliases from the current
network and call join/leaveNetwork as needed

**Kind**: global function  
<a name="getMessageRouteForDevice"></a>

## getMessageRouteForDevice()
This will return a Promise with the 'routes' part of a MessageRoute.

**Kind**: global function  
<a name="getId"></a>

## getId()
Returns the id of device with the given network, aliasKey and alias

**Kind**: global function  
<a name="getNetworkAliases"></a>

## getNetworkAliases()
Looks up the networkAliases on the object with the given id

**Kind**: global function  
<a name="getAlias"></a>

## getAlias()
Looks up the specific networkAlias on the object with the given id

**Kind**: global function  
<a name="addAccount"></a>

## addAccount()
Accounts are Users that were made by the project. They are deleted when the project is deleted,
and the user's username is unique in the project.

**Kind**: global function  
<a name="acquireProjectAlias"></a>

## acquireProjectAlias()
Attempts to acquire the aliasName for the project. The aliasType determines
the kind of alias (like a 'blueprint' alias), the aliasName is the desired
human readable name, and the id is the actual if of the referenced object.

The lock will be saved like this:
   -projectAlias
     -projectId
       -aliasType
         -aliasName : id

**Kind**: global function  
<a name="removeRef"></a>

## removeRef()
Removes the ref between the owner and the reference object.

**Kind**: global function  
<a name="getRef"></a>

## getRef()
Returns the value stored at the ownerId's refId. This is the last
value pasted into addRef for the given ownerId/refId

**Kind**: global function  
<a name="getRefSubValue"></a>

## getRefSubValue()
Returns the value stored at the ownerId's refId[subpath]. This is the last
value passed into addRef for the given ownerId/refId

**Kind**: global function  
<a name="getRefsData"></a>

## getRefsData()
Returns the ref objects in the table. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ obj1...objN ] }. Each
objN will contain: { id : <id>, type : <type>, value : <value> }

**Kind**: global function  
<a name="getOwnerIds"></a>

## getOwnerIds()
Returns the owner ids of the owners that include the ref. Currently, this will
return all the objects in the list in a object that looks like:
{ startIndex : 0, count : <N>, items : [ ownerId1...ownerIdN ] }.

**Kind**: global function  
<a name="saveWithManualId"></a>

## saveWithManualId(rootRef, idFunc(, data, cb)
This will attempt to create a rootRef/<id> entry where the
id is created by idFunc. This allows human friendly ideas to
be created.

**Kind**: global function  

| Param | Description |
| --- | --- |
| rootRef | the ref to the containing list |
| idFunc( | count, dat ) returns the next id to try |
| data | the data to data. data.id will be set to the final id |
| cb | the file callback that is invoked. |

<a name="deleteResources"></a>

## deleteResources()
Remove the project alias if it exists. Note, the check of the validity of
the alias is performed in the controller

**Kind**: global function  
<a name="delete"></a>

## delete()
This assumes the user has been deleted

**Kind**: global function  
<a name="encodeOpenIdUser"></a>

## encodeOpenIdUser()
Encodes the iss and sub into a string useable as a firebase key

**Kind**: global function  
<a name="keyForOpenIdUser"></a>

## keyForOpenIdUser(iss, sub)
Returns the firebase key for the openid

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| iss | <code>string</code> | the issuer |
| sub | <code>string</code> | the subject |

<a name="openIdUserExists"></a>

## openIdUserExists(iss, sub) ⇒ <code>boolean</code> \| <code>string</code>
Returns the user if for the iss/sub combination, or false if it doesn't exist

**Kind**: global function  
**Returns**: <code>boolean</code> \| <code>string</code> - if found, the user id is returned. Otherwise, false is returned  

| Param | Type |
| --- | --- |
| iss | <code>string</code> | 
| sub | <code>string</code> | 

<a name="getOpenIdUserForJwt"></a>

## getOpenIdUserForJwt(jwt)
returns the User data or null if they don't exist

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| jwt | <code>object</code> | The jwt token containing the user's iss and sub |

<a name="createOpenIdUser"></a>

## createOpenIdUser(iss, sub, userInfo, returnExistingUser)
This will create and return the user for the

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| iss | <code>string</code> |  |  |
| sub | <code>string</code> |  |  |
| userInfo | <code>object</code> |  | the openid connect userInfo object |
| returnExistingUser | <code>boolean</code> | <code>true</code> | if false, this will throw an exception if the user already exists. Otherwise, the existing user will be returned [true] |

<a name="deleteOpenIdUser"></a>

## deleteOpenIdUser()
This assumes the user has been deleted

**Kind**: global function  
<a name="create"></a>

## create()
This will create a Models object and starts it. If options.createModels
is null, this will use the Definitions.createModels by default.

**Kind**: global function  
<a name="convertToData"></a>

## convertToData()
Converts the object into the form:
[ { path : <path>, value : <value> }, ...]
The value forms of obj are:
1) { values : [ { path : <path>, value : <value> }, ...] }
2) [ { path : <path>, value : <value> }, ...]
3) { path : <path>, value: <value> }
4) { keyValue : { <path1> : <value>, <path2> : <value> }}

**Kind**: global function  
<a name="setDeviceData"></a>

## setDeviceData()
Sets the realtime data for the device. The data should be one of these formats:
1) { values : [ { path : <path>, value : <value> }, ...] }
2) [ { path : <path>, value : <value> }, ...]
3) { path : <path>, value: <value> }
4) { keyValue : { <path1> : <value>, <path2> : <value> }}

**Kind**: global function  
<a name="addDeviceUser"></a>

## addDeviceUser(device, userData)
Addes a user to the system.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| device | <code>Object</code> | the Device object to add the user to |
| userData | <code>Object</code> | The  body should have the following values: |
| userData.id | <code>string</code> | The User id to add (note, not the username) |
| userData.permissions | <code>Object</code> | An object with at least { role : admin' | 'user' } |
| userData.metadata | <code>Object</code> | optional user specific data in regards to the system |

<a name="createCheckNearestPermission"></a>

## createCheckNearestPermission(deviceSource, check)
This will return a function(req, res, next) that will check for read permissions on the 
devicec and walk the device.parentDeviceId field to check to see if the
user has permission to read the device from any of those devices

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| deviceSource | <code>Object</code> \| <code>string</code> | .              a Device instance or                a string used to access the name of the device object off of req or                a function(req) to return the device |
| check | <code>function</code> | a function( permissionObject, { device, req } ) |

<a name="sendMessage"></a>

## sendMessage(sendMessage, device, message)
This function will send an outbound message to a device on its network

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| sendMessage | <code>\*</code> | the function to use to send the message |
| device | <code>\*</code> | the device object |
| message | <code>\*</code> | the message to send to the device |

<a name="flatten"></a>

## flatten()
This will flatten either an patch ops array or an object
into { 'a/b/c' : 1 }

**Kind**: global function  
<a name="projectTransfer"></a>

## projectTransfer()
Determines if a project transfer is occuring anf performs it.
the next function will be invoked with next( err, [ ..ops..] ),
where the 'projectId' element in the ops array will be removed.

**Kind**: global function  
<a name="appendLookupToResultList"></a>

## appendLookupToResultList(options)
Will look for items to expand and include in the result list. The result object
should look like { startIndex, count, total, items, search }. This will append
to result, a refs : { XXX : { id : {...} } } object, where XXX is blueprint, network, 
etc

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>Object</code> | flatten : [true|false]       if true, refs will contain { <id> : <obj> }.      if true, refs will contain { <name like user|blueprint> : { <id> : <obj> } } |

<a name="createGetAccessToken"></a>

## createGetAccessToken()
Returns a function that will request an access token from the database in
dbInfo. dbInfo should contain { db : the database, service: the service, key : the 
location to place the accessToken in applyTo  }

**Kind**: global function  
<a name="allowUpdate"></a>

## allowUpdate()
Returns false if the patch ops array contains a path that is not
in the given valid array

**Kind**: global function  
<a name="createResult"></a>

## createResult(user, options, authJwt) ⇒ <code>Promise.&lt;Object&gt;</code>
Creates response object for a verification of the previous jwt token

**Kind**: global function  
**Returns**: <code>Promise.&lt;Object&gt;</code> - if the user is a User, the resolved object will
contain { profile, idToken, ..other }. If its an ApiAccess object, it will be 
the ApiAccess's data  

| Param | Type | Description |
| --- | --- | --- |
| user | <code>User</code> \| <code>ApiAccess</code> | the User or ApiAccess object |
| options | <code>Object</code> | the current permissions, used to sanitize the user data |
| authJwt | <code>Object</code> | an object containing the secret, issuer, audience, expiresIn. If the Project exists and has a jwtTokenExpiration the expiresIn will be replaced with that value |

<a name="sendDeviceMessage"></a>

## sendDeviceMessage()
Sends the message using the device's routes model or the defaultTopic

**Kind**: global function  
<a name="joinNetwork"></a>

## joinNetwork(cb)
**Kind**: global function  

| Param | Description |
| --- | --- |
| cb | function( err, deviceData ) |

<a name="leaveNetwork"></a>

## leaveNetwork(cb)
**Kind**: global function  

| Param | Description |
| --- | --- |
| cb | function( err, deviceData ) |

<a name="aliasSet"></a>

## aliasSet(cb)
**Kind**: global function  

| Param | Description |
| --- | --- |
| cb | function( err, deviceData ) |

<a name="sendMessage"></a>

## sendMessage(network, device, msg, cb)
Attempts to send a message to the given device on the given
network.

**Kind**: global function  

| Param | Description |
| --- | --- |
| network | the data representing the network |
| device | the data representing the device |
| msg | the message to send |
| cb | the callback |

<a name="cleanse"></a>

## cleanse() ⇒
Removes any project sensitive data from the network.

**Kind**: global function  
**Returns**: the network data object to use  
<a name="send"></a>

## send()
Uses Request to send a message. Unlike request, this
will convert any statusCode < 200 or >= 300 to an error

**Kind**: global function  
<a name="getTemplateContext"></a>

## getTemplateContext()
Used to constuct a template context for use in building the db root. The extra
should contain at least systemId and deviceId.

**Kind**: global function  
<a name="v4"></a>

## v4()
v4

**Kind**: global function  
<a name="v1"></a>

## v1()
v1

**Kind**: global function  
<a name="encode"></a>

## encode()
encode

**Kind**: global function  
<a name="decode"></a>

## decode()
decode

**Kind**: global function  
<a name="ensureLength"></a>

## ensureLength()
ensureLength

**Kind**: global function  
**Api**: private  
<a name="padLeft"></a>

## padLeft()
padLeft

**Kind**: global function  
**Api**: private  
<a name="trimLeft"></a>

## trimLeft()
trimLeft

**Kind**: global function  
**Api**: private  
