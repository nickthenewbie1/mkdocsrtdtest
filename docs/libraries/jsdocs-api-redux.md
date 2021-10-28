---
id: jsdocs-api-redux
title: API Redux
---
## Classes

<dl>
<dt><a href="#Grp - Class representing a group of items">Grp - Class representing a group of items</a></dt>
<dd></dd>
<dt><a href="#Grp">Grp</a></dt>
<dd></dd>
<dt><a href="#Interface">Interface</a></dt>
<dd><p>Class representing the interface route of the api</p>
</dd>
<dt><a href="#Messages">Messages</a></dt>
<dd></dd>
<dt><a href="#Obj - class representing a Single device">Obj - class representing a Single device</a></dt>
<dd></dd>
<dt><a href="#Obj">Obj</a></dt>
<dd></dd>
<dt><a href="#User">User</a></dt>
<dd><p>User - class representing a user</p>
</dd>
<dt><a href="#Users">Users</a></dt>
<dd><p>Users - class representing a group of users</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#verify">verify(targetLocation)</a> ⇒ <code>function</code></dt>
<dd><p>gets and verifies the Bearer token</p>
</dd>
<dt><a href="#login">login(username, password, projectId)</a> ⇒ <code>function</code></dt>
<dd><p>will log in the user</p>
</dd>
<dt><a href="#logout">logout()</a> ⇒ <code>function</code></dt>
<dd><p>will log the user out</p>
</dd>
<dt><a href="#forgotPassword">forgotPassword(username, projectId)</a> ⇒ <code>function</code></dt>
<dd><p>sends an email to reset the password</p>
</dd>
<dt><a href="#changePassword">changePassword(oldPassword, newPassword)</a> ⇒ <code>function</code></dt>
<dd><p>change the currently logged in user&#39;s password</p>
</dd>
<dt><a href="#resetPassword">resetPassword(username, password, confirm, token, projectId)</a> ⇒ <code>function</code></dt>
<dd><p>changes the user&#39;s password</p>
</dd>
<dt><a href="#renew">renew(auto)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#isLoggedIn">isLoggedIn(state)</a> ⇒ <code>boolean</code></dt>
<dd><p>checks if there is a user logged in</p>
</dd>
<dt><a href="#isLoading">isLoading(state)</a> ⇒ <code>boolean</code></dt>
<dd><p>checks if the ui is attempting to log in or verify a user</p>
</dd>
<dt><a href="#isVerifying">isVerifying(state)</a> ⇒ <code>boolean</code></dt>
<dd><p>checks if the ui is attempting to verify a user</p>
</dd>
<dt><a href="#isError">isError(state)</a> ⇒ <code>boolean</code></dt>
<dd><p>checks if there was an error on the most recent action taken</p>
</dd>
<dt><a href="#getErrorMessage">getErrorMessage(state)</a> ⇒ <code>string</code></dt>
<dd></dd>
<dt><a href="#getUsername">getUsername(state)</a> ⇒ <code>string</code></dt>
<dd></dd>
<dt><a href="#getUserId">getUserId(state)</a> ⇒ <code>string</code></dt>
<dd></dd>
<dt><a href="#getProfile">getProfile(state)</a> ⇒ <code>object</code></dt>
<dd></dd>
<dt><a href="#isLoading">isLoading(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>checks if a query is loading</p>
</dd>
<dt><a href="#isError">isError(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>check if a query is in error</p>
</dd>
<dt><a href="#isDone">isDone(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>check if a query has completed</p>
</dd>
<dt><a href="#isList">isList(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>check if a query result is a list</p>
</dd>
<dt><a href="#isTable">isTable(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>check if a query result is a table</p>
</dd>
<dt><a href="#isObject">isObject(state, path)</a> ⇒ <code>boolean</code></dt>
<dd><p>check if a query result is an object</p>
</dd>
<dt><a href="#getObject">getObject(state, path)</a> ⇒ <code>object</code></dt>
<dd><p>gets the result of a query if it is an object</p>
</dd>
<dt><a href="#getHistory">getHistory(state, path, queryName)</a> ⇒ <code>object</code></dt>
<dd><p>gets the result of a history query</p>
</dd>
<dt><a href="#getList">getList(state, path, opts)</a> ⇒ <code>array</code></dt>
<dd><p>get the list result of a query</p>
</dd>
<dt><a href="#getTable">getTable(state, path, opts)</a> ⇒ <code>array</code></dt>
<dd><p>get the table result of a query</p>
</dd>
<dt><a href="#setFilter">setFilter(name, filter)</a></dt>
<dd><p>Registers a filter function against the filter type.</p>
</dd>
<dt><a href="#getFilter">getFilter()</a></dt>
<dd><p>Returns the filter function registerd at the name</p>
</dd>
<dt><a href="#getTextFilter">getTextFilter()</a></dt>
<dd><p>Returns the default text filter</p>
</dd>
<dt><a href="#createPromise">createPromise(method, path, body, options, type, extra)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#list">list(path, parentId, type, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#create">create(path, obj, parentId, type, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#get">get(path, parentPath, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#getHistory">getHistory(path, parentPath, options, queryName)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#remove">remove(path, id, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#update">update(path, data, parentPath, parentId, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#createDeviceUser">createDeviceUser(path, obj, parentPath, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#addDeviceUser">addDeviceUser(path, obj, parentId, options)</a> ⇒ <code>function</code></dt>
<dd><p>creates a user, and then addes them to the device</p>
</dd>
<dt><a href="#sendOutboundDeviceMessage">sendOutboundDeviceMessage(path, obj, parentId, options)</a> ⇒ <code>function</code></dt>
<dd><p>sends an outbound message to a device</p>
</dd>
<dt><a href="#updateDeviceUser">updateDeviceUser(path, obj, parentId, options)</a> ⇒ <code>promise</code></dt>
<dd></dd>
<dt><a href="#removeDeviceUser">removeDeviceUser(path, obj, parentId, options)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#copy">copy()</a></dt>
<dd><p>Shallow copies the state, as well as the lookup and data if needed</p>
</dd>
<dt><a href="#getApiQueryable">getApiQueryable(query)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#getApiQueryable">getApiQueryable(query)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#defaultGetApiQueryable">defaultGetApiQueryable(query)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#create">create(query)</a> ⇒ <code>function</code></dt>
<dd></dd>
<dt><a href="#getActionConstant">getActionConstant(action, mode)</a> ⇒ <code>string</code></dt>
<dd></dd>
<dt><a href="#isSimpleTimeQuery">isSimpleTimeQuery(q)</a> ⇒ <code>boolean</code></dt>
<dd></dd>
<dt><a href="#isReversed">isReversed(opts)</a> ⇒ <code>boolean</code></dt>
<dd></dd>
<dt><a href="#mergeItems">mergeItems(items, newItems, range)</a> ⇒ <code>array</code></dt>
<dd></dd>
<dt><a href="#getQueryChunks">getQueryChunks(opts, chunkSize)</a> ⇒ <code>object</code></dt>
<dd></dd>
<dt><a href="#getQueryOptions">getQueryOptions(opts)</a> ⇒ <code>object</code></dt>
<dd></dd>
<dt><a href="#receive">receive(state, action)</a></dt>
<dd><p>behavior for the GET action</p>
</dd>
<dt><a href="#update">update(state, action)</a></dt>
<dd><p>behavior for the UPDATE action</p>
</dd>
<dt><a href="#add">add(state, action)</a></dt>
<dd><p>behavior for the ADD action</p>
</dd>
<dt><a href="#remove">remove(state, action)</a></dt>
<dd><p>behavior for the REMOVE action</p>
</dd>
<dt><a href="#reducer">reducer(initialState, actionTypeBase, additionalReducers)</a></dt>
<dd><p>creates and returns a generic reducer</p>
</dd>
<dt><a href="#list">list(opts)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call to get the list of current users for the project</p>
</dd>
<dt><a href="#create">create(item)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call to create a new user</p>
</dd>
<dt><a href="#get">get(item, opts)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call to get a user</p>
</dd>
<dt><a href="#remove">remove(item)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call to remove a user</p>
</dd>
<dt><a href="#update">update(item, patchOps, opts)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call to update a user</p>
</dd>
<dt><a href="#forcePWReset">forcePWReset(item, projectId)</a> ⇒ <code>function</code></dt>
<dd><p>makes an api call sending an email to the provided user making them reset their password</p>
</dd>
<dt><a href="#encodeQ">encodeQ(options)</a></dt>
<dd><p>turns a query object to a string to be appended to an http request url</p>
</dd>
<dt><a href="#objectToQueryString">objectToQueryString(a)</a></dt>
<dd><p>turns an object into a string that can be used in a http request url</p>
</dd>
<dt><a href="#buildParams">buildParams(prefix, obj, add)</a></dt>
<dd><p>manipulates obj according to the add function provided to it</p>
</dd>
<dt><a href="#getPatchOpsArray">getPatchOpsArray(patchOps)</a></dt>
<dd><p>transforms an object into an array of {path, value, op} objects</p>
</dd>
<dt><a href="#combinePath">combinePath(path, subpath)</a></dt>
<dd><p>checks for &#39;/&#39; and appends the subpath onto the path</p>
</dd>
<dt><a href="#getId">getId(id, throwIfNull)</a></dt>
<dd><p>returns id if id is string or id.id if id is an object</p>
</dd>
<dt><a href="#getLastInPath">getLastInPath(path)</a></dt>
<dd><p>returns the substring after the last &#39;/&#39;</p>
</dd>
</dl>

<a name="Grp - Class representing a group of items"></a>

## Grp - Class representing a group of items
**Kind**: global class  
<a name="Grp"></a>

## Grp
**Kind**: global class  

* [Grp](#Grp)
    * [new Grp(parentPath, id, attribute)](#new_Grp_new)
    * [.list(options)](#Grp+list) ⇒ <code>function</code>
    * [.create(obj, options)](#Grp+create) ⇒ <code>function</code>
    * [.get(id, options)](#Grp+get) ⇒ <code>function</code>
    * [.update(id, data, options)](#Grp+update) ⇒ <code>function</code>
    * [.delete(id, options)](#Grp+delete) ⇒ <code>function</code>
    * [.model(options)](#Grp+model) ⇒ <code>function</code>
    * [.filter(filter)](#Grp+filter)
    * [.obj(id)](#Grp+obj) ⇒ [<code>Obj</code>](#Obj)
    * [.getList(state, opts)](#Grp+getList) ⇒ <code>object</code>
    * [.isTable(state, opts)](#Grp+isTable) ⇒ <code>boolean</code>
    * [.getObject(state, id, opts)](#Grp+getObject) ⇒ <code>object</code>
    * [.getModel(state)](#Grp+getModel) ⇒ <code>object</code>
    * [.isLoading(state)](#Grp+isLoading) ⇒ <code>boolean</code>
    * [.isError(state)](#Grp+isError) ⇒ <code>boolean</code>
    * [.isDone(state)](#Grp+isDone) ⇒ <code>boolean</code>

<a name="new_Grp_new"></a>

### new Grp(parentPath, id, attribute)
creates a group


| Param | Type | Description |
| --- | --- | --- |
| parentPath | <code>string</code> | the path of the api call for the immediate parent |
| id | <code>string</code> | identifier for the group to be queried for |
| attribute | <code>string</code> | additional information to be added to the path |

<a name="Grp+list"></a>

### grp.list(options) ⇒ <code>function</code>
makes an api call for the list of objects

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Grp+create"></a>

### grp.create(obj, options) ⇒ <code>function</code>
api call to create an item as a child of the current path

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | item to be created |
| options | <code>object</code> | api options |

<a name="Grp+get"></a>

### grp.get(id, options) ⇒ <code>function</code>
api call to get a child of the current path

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the item to be returned |
| options | <code>object</code> | api options |

<a name="Grp+update"></a>

### grp.update(id, data, options) ⇒ <code>function</code>
api call to update a child of the current path

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the item to be updated |
| data | <code>object</code> | values of the item to be changed |
| options | <code>object</code> | api options |

<a name="Grp+delete"></a>

### grp.delete(id, options) ⇒ <code>function</code>
api call to delete a child of the current path

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the item to be deleted |
| options | <code>object</code> | api options |

<a name="Grp+model"></a>

### grp.model(options) ⇒ <code>function</code>
api call to get the model for the path

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Grp+filter"></a>

### grp.filter(filter)
locally filters the results

**Kind**: instance method of [<code>Grp</code>](#Grp)  

| Param | Type | Description |
| --- | --- | --- |
| filter | <code>object</code> | the filter object for the path |

<a name="Grp+obj"></a>

### grp.obj(id) ⇒ [<code>Obj</code>](#Obj)
returns an instance of the obj class with the current path prepended

**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: [<code>Obj</code>](#Obj) - has the current path with the id  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 

<a name="Grp+getList"></a>

### grp.getList(state, opts) ⇒ <code>object</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>object</code> - results, in the form of a list  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| opts | <code>object</code> |  |

<a name="Grp+isTable"></a>

### grp.isTable(state, opts) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>boolean</code> - whether or not the results can be returned as a table  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| opts | <code>object</code> |  |

<a name="Grp+getObject"></a>

### grp.getObject(state, id, opts) ⇒ <code>object</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>object</code> - returns the resulting object from the query  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| id | <code>string</code> | id of the object |
| opts | <code>object</code> |  |

<a name="Grp+getModel"></a>

### grp.getModel(state) ⇒ <code>object</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>object</code> - returns a model for the query  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Grp+isLoading"></a>

### grp.isLoading(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>boolean</code> - whether the query is loading  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Grp+isError"></a>

### grp.isError(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>boolean</code> - whether the query had an error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Grp+isDone"></a>

### grp.isDone(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Grp</code>](#Grp)  
**Returns**: <code>boolean</code> - whether the query is finished  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Interface"></a>

## Interface
Class representing the interface route of the api

**Kind**: global class  

* [Interface](#Interface)
    * [new Interface(system, type)](#new_Interface_new)
    * [.list(options)](#Interface+list) ⇒ <code>function</code>
    * [.filter(filter)](#Interface+filter)
    * [.create(obj, options)](#Interface+create) ⇒ <code>function</code>
    * [.delete(id, options)](#Interface+delete) ⇒ <code>function</code>
    * [.model(options)](#Interface+model) ⇒ <code>function</code>
    * [.obj(id)](#Interface+obj) ⇒ [<code>Obj</code>](#Obj)
    * [.getList(state, opts)](#Interface+getList) ⇒ <code>object</code>
    * [.getModel(state)](#Interface+getModel) ⇒ <code>object</code>
    * [.isLoading(state)](#Interface+isLoading) ⇒ <code>boolean</code>
    * [.isError(state)](#Interface+isError) ⇒ <code>boolean</code>
    * [.isDone(state)](#Interface+isDone) ⇒ <code>boolean</code>

<a name="new_Interface_new"></a>

### new Interface(system, type)
create the Interface


| Param | Type | Description |
| --- | --- | --- |
| system | <code>string</code> | id or alias of the system to connect to |
| type | <code>string</code> | the alias of the type of blueprint/devices |

<a name="Interface+list"></a>

### interface.list(options) ⇒ <code>function</code>
api call to get the list of devices of the provided type

**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | to be included in the api call |

<a name="Interface+filter"></a>

### interface.filter(filter)
locally filters the results

**Kind**: instance method of [<code>Interface</code>](#Interface)  

| Param | Type | Description |
| --- | --- | --- |
| filter | <code>object</code> | the filter object for the path |

<a name="Interface+create"></a>

### interface.create(obj, options) ⇒ <code>function</code>
api call to create a device of the provided type

**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | device to be created |
| options | <code>object</code> | to be included in the api call |

<a name="Interface+delete"></a>

### interface.delete(id, options) ⇒ <code>function</code>
api call to delete a device of the provided type

**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the device to be deleted |
| options | <code>object</code> | to be included in the api call |

<a name="Interface+model"></a>

### interface.model(options) ⇒ <code>function</code>
api call to get the model of a device of the provided type

**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | to be included in the api call |

<a name="Interface+obj"></a>

### interface.obj(id) ⇒ [<code>Obj</code>](#Obj)
returns an instance of the obj class with the current path prepended

**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: [<code>Obj</code>](#Obj) - has the current path with the id  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 

<a name="Interface+getList"></a>

### interface.getList(state, opts) ⇒ <code>object</code>
**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>object</code> - results, in the form of a list  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| opts | <code>object</code> |  |

<a name="Interface+getModel"></a>

### interface.getModel(state) ⇒ <code>object</code>
**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>object</code> - returns a model for the query  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Interface+isLoading"></a>

### interface.isLoading(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>boolean</code> - whether the query is loading  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Interface+isError"></a>

### interface.isError(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>boolean</code> - whether the query had an error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Interface+isDone"></a>

### interface.isDone(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Interface</code>](#Interface)  
**Returns**: <code>boolean</code> - whether the query is finished  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Messages"></a>

## Messages
**Kind**: global class  

* [Messages](#Messages)
    * [new Messages(parentPath)](#new_Messages_new)
    * [.getMessages(state, queryName)](#Messages+getMessages) ⇒ <code>object</code>

<a name="new_Messages_new"></a>

### new Messages(parentPath)
creates Messages


| Param | Type | Description |
| --- | --- | --- |
| parentPath | <code>string</code> | the path of the api call for the immediate parent |

<a name="Messages+getMessages"></a>

### messages.getMessages(state, queryName) ⇒ <code>object</code>
gets the sent outbound messages

**Kind**: instance method of [<code>Messages</code>](#Messages)  
**Returns**: <code>object</code> - the sent outbound messages  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| queryName | <code>string</code> | identifier of the query |

<a name="Obj - class representing a Single device"></a>

## Obj - class representing a Single device
**Kind**: global class  
<a name="Obj"></a>

## Obj
**Kind**: global class  

* [Obj](#Obj)
    * [new Obj(parentPath, id, isInGroup)](#new_Obj_new)
    * [.get(options)](#Obj+get) ⇒ <code>function</code>
    * [.history(options)](#Obj+history) ⇒ <code>function</code>
    * [.create(obj, options)](#Obj+create) ⇒ <code>function</code>
    * [.update(obj, options)](#Obj+update) ⇒ <code>function</code>
    * [.delete(options)](#Obj+delete) ⇒ <code>function</code>
    * [.model(options)](#Obj+model) ⇒ <code>function</code>
    * [.obj(id)](#Obj+obj) ⇒ [<code>Obj</code>](#Obj)
    * [.grp(attribute)](#Obj+grp) ⇒ [<code>Grp</code>](#Grp)
    * [.users()](#Obj+users) ⇒ <code>object</code>
    * [.messages()](#Obj+messages) ⇒ <code>object</code>
    * [.getObject(state)](#Obj+getObject) ⇒ <code>object</code>
    * [.getTable(state, opts)](#Obj+getTable) ⇒ <code>object</code>
    * [.getModel(state)](#Obj+getModel) ⇒ <code>object</code>
    * [.getHistory(state, queryName)](#Obj+getHistory) ⇒ <code>object</code>
    * [.isTable(state)](#Obj+isTable) ⇒ <code>boolean</code>
    * [.isLoading(state)](#Obj+isLoading) ⇒ <code>boolean</code>
    * [.isError(state)](#Obj+isError) ⇒ <code>boolean</code>
    * [.isDone(state)](#Obj+isDone) ⇒ <code>boolean</code>

<a name="new_Obj_new"></a>

### new Obj(parentPath, id, isInGroup)
creates an Object


| Param | Type | Description |
| --- | --- | --- |
| parentPath | <code>string</code> | the path of the api call for the immediate parent |
| id | <code>string</code> | identifier for the group to be queried for |
| isInGroup | <code>boolean</code> | represents if the object is in a group |

<a name="Obj+get"></a>

### obj.get(options) ⇒ <code>function</code>
makes an api call for the for the Object at the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Obj+history"></a>

### obj.history(options) ⇒ <code>function</code>
makes an api call to get the history of an object at the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| query.query | <code>object</code> | query params that the server will use |
| query.queryName | <code>string</code> | query identifier |
| options | <code>object</code> | api options |

<a name="Obj+create"></a>

### obj.create(obj, options) ⇒ <code>function</code>
makes an api call to create an object at the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | the object to be created |
| options | <code>object</code> | api options |

<a name="Obj+update"></a>

### obj.update(obj, options) ⇒ <code>function</code>
makes an api call to update the object at the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | the object values to be updated |
| options | <code>object</code> | api options |

<a name="Obj+delete"></a>

### obj.delete(options) ⇒ <code>function</code>
makes an api call to delete the object at the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Obj+model"></a>

### obj.model(options) ⇒ <code>function</code>
api call to get the model for the path

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Obj+obj"></a>

### obj.obj(id) ⇒ [<code>Obj</code>](#Obj)
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: [<code>Obj</code>](#Obj) - object with the current path and the id provided  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of an obj |

<a name="Obj+grp"></a>

### obj.grp(attribute) ⇒ [<code>Grp</code>](#Grp)
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: [<code>Grp</code>](#Grp) - group class with the current path and attribute  

| Param | Type | Description |
| --- | --- | --- |
| attribute | <code>string</code> | the attribute representing a group on the current object |

<a name="Obj+users"></a>

### obj.users() ⇒ <code>object</code>
makes an api call to get the users on the device

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - represents the users permissioned on the device  
<a name="Obj+messages"></a>

### obj.messages() ⇒ <code>object</code>
makes an api access object for managing a device's outbound messages

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - the api access object  
<a name="Obj+getObject"></a>

### obj.getObject(state) ⇒ <code>object</code>
get the current object from the state

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - the object  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Obj+getTable"></a>

### obj.getTable(state, opts) ⇒ <code>object</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - table of the results  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux state |
| opts | <code>object</code> |  |

<a name="Obj+getModel"></a>

### obj.getModel(state) ⇒ <code>object</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - the model for the object  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Obj+getHistory"></a>

### obj.getHistory(state, queryName) ⇒ <code>object</code>
gets the results of a specific query

**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>object</code> - the results of the query  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |
| queryName | <code>string</code> | identifier of the query |

<a name="Obj+isTable"></a>

### obj.isTable(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>boolean</code> - whether or not the results can be returned as a table  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Obj+isLoading"></a>

### obj.isLoading(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>boolean</code> - whether the query is loading  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Obj+isError"></a>

### obj.isError(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>boolean</code> - whether the query had an error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Obj+isDone"></a>

### obj.isDone(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Obj</code>](#Obj)  
**Returns**: <code>boolean</code> - whether the query is finished  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="User"></a>

## User
User - class representing a user

**Kind**: global class  

* [User](#User)
    * [new User(parentPath, parentId, id)](#new_User_new)
    * [.get(options)](#User+get) ⇒ <code>function</code>
    * [.update()](#User+update) ⇒ <code>function</code>
    * [.delete(options)](#User+delete) ⇒ <code>function</code>
    * [.remove(options)](#User+remove) ⇒ <code>function</code>
    * [.getObject(state)](#User+getObject) ⇒ <code>object</code>
    * [.isLoading(state)](#User+isLoading) ⇒ <code>boolean</code>
    * [.isError(state)](#User+isError) ⇒ <code>boolean</code>
    * [.isDone(state)](#User+isDone) ⇒ <code>boolean</code>

<a name="new_User_new"></a>

### new User(parentPath, parentId, id)
creates a User


| Param | Type | Description |
| --- | --- | --- |
| parentPath | <code>string</code> | the path of the api call for the immediate parent |
| parentId | <code>string</code> | the id for the immediate parent |
| id | <code>string</code> | identifier for the user |

<a name="User+get"></a>

### user.get(options) ⇒ <code>function</code>
Requests the object at this path

**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="User+update"></a>

### user.update() ⇒ <code>function</code>
Updates the object at this path

**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
|  | <code>object</code> |  |
| object.permissions | <code>object</code> | permissions of the user being updated |
| object.metadata | <code>object</code> | metadata of the user being created |

<a name="User+delete"></a>

### user.delete(options) ⇒ <code>function</code>
Deletes the object at the path

**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="User+remove"></a>

### user.remove(options) ⇒ <code>function</code>
Deletes the object at the path

**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="User+getObject"></a>

### user.getObject(state) ⇒ <code>object</code>
gets the user of the current path

**Kind**: instance method of [<code>User</code>](#User)  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="User+isLoading"></a>

### user.isLoading(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>boolean</code> - whether the query is loading  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="User+isError"></a>

### user.isError(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>boolean</code> - whether the query had an error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="User+isDone"></a>

### user.isDone(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>User</code>](#User)  
**Returns**: <code>boolean</code> - whether the query is finished  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Users"></a>

## Users
Users - class representing a group of users

**Kind**: global class  

* [Users](#Users)
    * [new Users(parentPath, id)](#new_Users_new)
    * [.list(options)](#Users+list) ⇒ <code>function</code>
    * [.create(object, options)](#Users+create) ⇒ <code>function</code>
    * [.add(user)](#Users+add) ⇒ <code>function</code>
    * [.update(id, data)](#Users+update) ⇒ <code>function</code>
    * [.delete(id, options)](#Users+delete) ⇒ <code>function</code>
    * [.remove(id, options)](#Users+remove) ⇒ <code>function</code>
    * [.user(id)](#Users+user) ⇒ [<code>User</code>](#User)
    * [.getList(state, opts)](#Users+getList) ⇒ <code>object</code>
    * [.isLoading(state)](#Users+isLoading) ⇒ <code>boolean</code>
    * [.isError(state)](#Users+isError) ⇒ <code>boolean</code>
    * [.isDone(state)](#Users+isDone) ⇒ <code>boolean</code>

<a name="new_Users_new"></a>

### new Users(parentPath, id)
creates Users


| Param | Type | Description |
| --- | --- | --- |
| parentPath | <code>string</code> | the path of the api call for the immediate parent |
| id | <code>string</code> | identifier for the user |

<a name="Users+list"></a>

### users.list(options) ⇒ <code>function</code>
make an api call for the list of users

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | api options |

<a name="Users+create"></a>

### users.create(object, options) ⇒ <code>function</code>
makes an api call to create a user and permission them on the current path

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| object | <code>object</code> |  |
| object.user | <code>object</code> | represents the user to be created |
| object.permissions | <code>object</code> | represents the permissions of the user |
| object.metadata | <code>object</code> | metadata of the user to be created |
| options | <code>object</code> | api options |

<a name="Users+add"></a>

### users.add(user) ⇒ <code>function</code>
Adds a user with permission to the device. One of id, username, or user (object with id) is required.

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type |
| --- | --- |
| user | <code>object</code> | 
| user.id | <code>string</code> | 
| user.username | <code>string</code> | 
| user.user | <code>object</code> | 
| user.permissions | <code>object</code> | 
| user.metadata | <code>object</code> | 

<a name="Users+update"></a>

### users.update(id, data) ⇒ <code>function</code>
If permission is an array, it is sent as a patchOps. Otherwise, a
a patch ops will be build to replace permissions and metdata.

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | id of the user |
| data | <code>object</code> |  |
| data.permissions | <code>object</code> |  |
| data.metadata | <code>object</code> |  |

<a name="Users+delete"></a>

### users.delete(id, options) ⇒ <code>function</code>
Deletes the user at the path

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | user id |
| options | <code>object</code> | api options |

<a name="Users+remove"></a>

### users.remove(id, options) ⇒ <code>function</code>
Deletes the object at the path

**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | user id |
| options | <code>object</code> | api options |

<a name="Users+user"></a>

### users.user(id) ⇒ [<code>User</code>](#User)
**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: [<code>User</code>](#User) - a user object for the given Id  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>string</code> | user id |

<a name="Users+getList"></a>

### users.getList(state, opts) ⇒ <code>object</code>
**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>object</code> - list from the current state  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux state |
| opts | <code>object</code> |  |

<a name="Users+isLoading"></a>

### users.isLoading(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>boolean</code> - whether the query is loading  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Users+isError"></a>

### users.isError(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>boolean</code> - whether the query had an error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="Users+isDone"></a>

### users.isDone(state) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>Users</code>](#Users)  
**Returns**: <code>boolean</code> - whether the query is finished  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current redux state |

<a name="verify"></a>

## verify(targetLocation) ⇒ <code>function</code>
gets and verifies the Bearer token

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type |
| --- | --- |
| targetLocation | <code>string</code> | 

<a name="login"></a>

## login(username, password, projectId) ⇒ <code>function</code>
will log in the user

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| username | <code>string</code> |  |
| password | <code>string</code> |  |
| projectId | <code>string</code> | imagine projectId, will use the project id from the api object passed to redux thunk if none provided |

<a name="logout"></a>

## logout() ⇒ <code>function</code>
will log the user out

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  
<a name="forgotPassword"></a>

## forgotPassword(username, projectId) ⇒ <code>function</code>
sends an email to reset the password

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| username | <code>string</code> | the user that the email will be sent to |
| projectId | <code>string</code> | imagine projectId, will use the project id from the api object passed to redux thunk if none provided |

<a name="changePassword"></a>

## changePassword(oldPassword, newPassword) ⇒ <code>function</code>
change the currently logged in user's password

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type |
| --- | --- |
| oldPassword | <code>string</code> | 
| newPassword | <code>string</code> | 

<a name="resetPassword"></a>

## resetPassword(username, password, confirm, token, projectId) ⇒ <code>function</code>
changes the user's password

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| username | <code>string</code> |  |
| password | <code>string</code> |  |
| confirm | <code>string</code> | 2nd password entry to confirm first is correct |
| token | <code>string</code> | api generated token |
| projectId | <code>string</code> |  |

<a name="renew"></a>

## renew(auto) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Default |
| --- | --- | --- |
| auto | <code>number</code> | <code>0</code> | 

<a name="isLoggedIn"></a>

## isLoggedIn(state) ⇒ <code>boolean</code>
checks if there is a user logged in

**Kind**: global function  
**Returns**: <code>boolean</code> - if there is a user logged in or not  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="isLoading"></a>

## isLoading(state) ⇒ <code>boolean</code>
checks if the ui is attempting to log in or verify a user

**Kind**: global function  
**Returns**: <code>boolean</code> - true if loading property is verifying or logging in  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="isVerifying"></a>

## isVerifying(state) ⇒ <code>boolean</code>
checks if the ui is attempting to verify a user

**Kind**: global function  
**Returns**: <code>boolean</code> - if loading property is verifying  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="isError"></a>

## isError(state) ⇒ <code>boolean</code>
checks if there was an error on the most recent action taken

**Kind**: global function  
**Returns**: <code>boolean</code> - true if error occured  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="getErrorMessage"></a>

## getErrorMessage(state) ⇒ <code>string</code>
**Kind**: global function  
**Returns**: <code>string</code> - the message/reason for error  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="getUsername"></a>

## getUsername(state) ⇒ <code>string</code>
**Kind**: global function  
**Returns**: <code>string</code> - username of currently logged in user  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="getUserId"></a>

## getUserId(state) ⇒ <code>string</code>
**Kind**: global function  
**Returns**: <code>string</code> - id of currently logged in user  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="getProfile"></a>

## getProfile(state) ⇒ <code>object</code>
**Kind**: global function  
**Returns**: <code>object</code> - profile of the currently logged in user  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current Auth redux state |

<a name="isLoading"></a>

## isLoading(state, path) ⇒ <code>boolean</code>
checks if a query is loading

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="isError"></a>

## isError(state, path) ⇒ <code>boolean</code>
check if a query is in error

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="isDone"></a>

## isDone(state, path) ⇒ <code>boolean</code>
check if a query has completed

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="isList"></a>

## isList(state, path) ⇒ <code>boolean</code>
check if a query result is a list

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="isTable"></a>

## isTable(state, path) ⇒ <code>boolean</code>
check if a query result is a table

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="isObject"></a>

## isObject(state, path) ⇒ <code>boolean</code>
check if a query result is an object

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="getObject"></a>

## getObject(state, path) ⇒ <code>object</code>
gets the result of a query if it is an object

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |

<a name="getHistory"></a>

## getHistory(state, path, queryName) ⇒ <code>object</code>
gets the result of a history query

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |
| queryName | <code>string</code> | name of the query |

<a name="getList"></a>

## getList(state, path, opts) ⇒ <code>array</code>
get the list result of a query

**Kind**: global function  
**Returns**: <code>array</code> - array of items  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |
| opts | <code>object</code> |  |

<a name="getTable"></a>

## getTable(state, path, opts) ⇒ <code>array</code>
get the table result of a query

**Kind**: global function  
**Returns**: <code>array</code> - array of items  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | the current interface redux object |
| path | <code>string</code> | string representing the query path sent to the api |
| opts | <code>object</code> |  |

<a name="setFilter"></a>

## setFilter(name, filter)
Registers a filter function against the filter type.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | the type name of the filter |
| filter | <code>function</code> | the function is given ( filter, items ) and should return a new list, filterer as needed. The supplied filter and list should NOT be modified. |

<a name="getFilter"></a>

## getFilter()
Returns the filter function registerd at the name

**Kind**: global function  
<a name="getTextFilter"></a>

## getTextFilter()
Returns the default text filter

**Kind**: global function  
<a name="createPromise"></a>

## createPromise(method, path, body, options, type, extra) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| method | <code>string</code> | http method |
| path | <code>string</code> | api route to be queried |
| body | <code>object</code> | data to be sent in the api call |
| options | <code>object</code> | options to be sent in the api call |
| type | <code>string</code> | action type to be used to maintain the api-redux status |
| extra | <code>object</code> | additional information to be incuded in redux dispatches |

<a name="list"></a>

## list(path, parentId, type, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| parentId | <code>string</code> | id of the parent device |
| type | <code>string</code> | action type to maintain the redux state |
| options | <code>object</code> | to be included in the api call |

<a name="create"></a>

## create(path, obj, parentId, type, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | the item to be created |
| parentId | <code>string</code> | id of the parent device |
| type | <code>string</code> | action type to maintain the redux state |
| options | <code>object</code> | to be included in the api call |

<a name="get"></a>

## get(path, parentPath, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| parentPath | <code>string</code> | path to the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="getHistory"></a>

## getHistory(path, parentPath, options, queryName) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| parentPath | <code>string</code> | path to the parent device |
| options | <code>object</code> | to be included in the api call |
| queryName | <code>string</code> | identifier to maintian different query statuses |

<a name="remove"></a>

## remove(path, id, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| id | <code>string</code> | device to be removed |
| options | <code>object</code> | to be included in the api call |

<a name="update"></a>

## update(path, data, parentPath, parentId, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| data | <code>object</code> | data to update the device with |
| parentPath | <code>string</code> | path to the parent device |
| parentId | <code>string</code> | id of the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="createDeviceUser"></a>

## createDeviceUser(path, obj, parentPath, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | user to be created and added to the device |
| parentPath | <code>string</code> | path to the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="addDeviceUser"></a>

## addDeviceUser(path, obj, parentId, options) ⇒ <code>function</code>
creates a user, and then addes them to the device

**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | user to be added to the device |
| parentId | <code>string</code> | id of the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="sendOutboundDeviceMessage"></a>

## sendOutboundDeviceMessage(path, obj, parentId, options) ⇒ <code>function</code>
sends an outbound message to a device

**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | message to be sent to the device |
| parentId | <code>string</code> | id of the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="updateDeviceUser"></a>

## updateDeviceUser(path, obj, parentId, options) ⇒ <code>promise</code>
**Kind**: global function  
**Returns**: <code>promise</code> - represents the result of the api call  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | user of the device and their values to be updated |
| parentId | <code>string</code> | id of the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="removeDeviceUser"></a>

## removeDeviceUser(path, obj, parentId, options) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - call to createPromise  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | route to be queried from the api |
| obj | <code>object</code> | user to be removed from the device |
| parentId | <code>string</code> | id of the parent device |
| options | <code>object</code> | to be included in the api call |

<a name="copy"></a>

## copy()
Shallow copies the state, as well as the lookup and data if needed

**Kind**: global function  
<a name="getApiQueryable"></a>

## getApiQueryable(query) ⇒ <code>function</code>
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>object</code> |  |
| query.api | <code>object</code> | an api object |
| query.type | <code>string</code> |  |
| query.mode | <code>string</code> |  |
| query.queryable | <code>string</code> |  |

<a name="getApiQueryable"></a>

## getApiQueryable(query) ⇒ <code>function</code>
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>object</code> |  |
| query.api | <code>object</code> | an api object |
| query.type | <code>string</code> |  |
| query.mode | <code>string</code> |  |
| query.queryable | <code>string</code> |  |

<a name="defaultGetApiQueryable"></a>

## defaultGetApiQueryable(query) ⇒ <code>function</code>
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>object</code> |  |
| query.api | <code>object</code> | an api object |
| query.type | <code>string</code> |  |
| query.mode | <code>string</code> |  |
| query.obj | <code>string</code> |  |

<a name="create"></a>

## create(query) ⇒ <code>function</code>
**Kind**: global function  
**Returns**: <code>function</code> - install function  

| Param | Type |
| --- | --- |
| query | <code>object</code> | 
| query.mode | <code>string</code> | 
| query.getApiQueryable | <code>object</code> | 
| query.chunkTime | <code>string</code> | 

<a name="getActionConstant"></a>

## getActionConstant(action, mode) ⇒ <code>string</code>
**Kind**: global function  
**Returns**: <code>string</code> - string representing the constant for the provided action  

| Param | Type | Description |
| --- | --- | --- |
| action | <code>string</code> | action being taken |
| mode | <code>string</code> |  |

<a name="isSimpleTimeQuery"></a>

## isSimpleTimeQuery(q) ⇒ <code>boolean</code>
**Kind**: global function  
**Returns**: <code>boolean</code> - represents whether the provided query is just time based or not  

| Param | Type | Description |
| --- | --- | --- |
| q | <code>object</code> | the query object |

<a name="isReversed"></a>

## isReversed(opts) ⇒ <code>boolean</code>
**Kind**: global function  
**Returns**: <code>boolean</code> - represents whether the provided query is in descending order or not  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> | the query object |

<a name="mergeItems"></a>

## mergeItems(items, newItems, range) ⇒ <code>array</code>
**Kind**: global function  
**Returns**: <code>array</code> - array of items with newItems inserted in for the given range  

| Param | Type | Description |
| --- | --- | --- |
| items | <code>array</code> | current items |
| newItems | <code>array</code> | items to be merged in |
| range | <code>array</code> | tuple of start and end |

<a name="getQueryChunks"></a>

## getQueryChunks(opts, chunkSize) ⇒ <code>object</code>
**Kind**: global function  
**Returns**: <code>object</code> - options for an api call for a chunk of data  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> |  |
| chunkSize | <code>number</code> | size of the api result queries |

<a name="getQueryOptions"></a>

## getQueryOptions(opts) ⇒ <code>object</code>
**Kind**: global function  
**Returns**: <code>object</code> - returns the opts object with correct start and end  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> | query options |

<a name="receive"></a>

## receive(state, action)
behavior for the GET action

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux state |
| action | <code>object</code> | redux action |

<a name="update"></a>

## update(state, action)
behavior for the UPDATE action

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux state |
| action | <code>object</code> | redux action |

<a name="add"></a>

## add(state, action)
behavior for the ADD action

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux state |
| action | <code>object</code> | redux action |

<a name="remove"></a>

## remove(state, action)
behavior for the REMOVE action

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| state | <code>object</code> | current redux stae |
| action | <code>object</code> | redux action |

<a name="reducer"></a>

## reducer(initialState, actionTypeBase, additionalReducers)
creates and returns a generic reducer

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| initialState | <code>object</code> |  |
| actionTypeBase | <code>string</code> | determines what constants will be used for the action types |
| additionalReducers | <code>\*</code> | function that will be called with state and action in the default case |

<a name="list"></a>

## list(opts) ⇒ <code>function</code>
makes an api call to get the list of current users for the project

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| opts | <code>object</code> | options to be provided to the api call |

<a name="create"></a>

## create(item) ⇒ <code>function</code>
makes an api call to create a new user

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| item | <code>object</code> | the new user to be created |

<a name="get"></a>

## get(item, opts) ⇒ <code>function</code>
makes an api call to get a user

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| item | <code>string</code> | id of the user |
| opts | <code>object</code> | options to be inculded in the api call |

<a name="remove"></a>

## remove(item) ⇒ <code>function</code>
makes an api call to remove a user

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| item | <code>string</code> | id of the user |

<a name="update"></a>

## update(item, patchOps, opts) ⇒ <code>function</code>
makes an api call to update a user

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type | Description |
| --- | --- | --- |
| item | <code>string</code> | id of the user to be updated |
| patchOps | <code>object</code> | object with the values to be updated |
| opts | <code>object</code> | any additional options to be sent to the api |

<a name="forcePWReset"></a>

## forcePWReset(item, projectId) ⇒ <code>function</code>
makes an api call sending an email to the provided user making them reset their password

**Kind**: global function  
**Returns**: <code>function</code> - redux thunk function  

| Param | Type |
| --- | --- |
| item | <code>string</code> | 
| projectId | <code>string</code> | 

<a name="encodeQ"></a>

## encodeQ(options)
turns a query object to a string to be appended to an http request url

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the parameters to be sent with a http request url |

<a name="objectToQueryString"></a>

## objectToQueryString(a)
turns an object into a string that can be used in a http request url

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| a | <code>object</code> | the object to be turned into a query string |

<a name="buildParams"></a>

## buildParams(prefix, obj, add)
manipulates obj according to the add function provided to it

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| prefix | <code>string</code> |  |
| obj | <code>object</code> \| <code>array</code> | the object to be manipulated |
| add | <code>function</code> | function used to do the manipulation |

<a name="getPatchOpsArray"></a>

## getPatchOpsArray(patchOps)
transforms an object into an array of {path, value, op} objects

**Kind**: global function  

| Param | Type |
| --- | --- |
| patchOps | <code>object</code> | 

<a name="combinePath"></a>

## combinePath(path, subpath)
checks for '/' and appends the subpath onto the path

**Kind**: global function  

| Param | Type |
| --- | --- |
| path | <code>string</code> | 
| subpath | <code>string</code> | 

<a name="getId"></a>

## getId(id, throwIfNull)
returns id if id is string or id.id if id is an object

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| id | <code>string</code> \| <code>object</code> |  |  |
| throwIfNull | <code>boolean</code> | <code>true</code> | if true will throw an error if there is no id |

<a name="getLastInPath"></a>

## getLastInPath(path)
returns the substring after the last '/'

**Kind**: global function  

| Param | Type |
| --- | --- |
| path | <code>string</code> | 

