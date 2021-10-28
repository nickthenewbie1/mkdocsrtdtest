---
id: jsdocs-data-store
title: Data Store
---
## Classes

<dl>
<dt><a href="#Access">Access</a></dt>
<dd><p>Access contains a set of standard methods for getting and setting data for any database</p>
</dd>
<dt><a href="#AppState">AppState</a></dt>
<dd><p>The AppState allows the using application to store its current
state in a common way, as well as any app specific data needed.</p>
<p>This is expecting a Database Adapter as its argument. It is assumed
that the AppState owns the root of the database, as destroy() will
remove it.</p>
<p>Structure :
{
   status : {
     state : &#39;initializing&#39; | &#39;started&#39; | ...
     info : &#39;sub state&#39;
     detail : { } 
     updated : timestamp
   }
   app : { }
}</p>
</dd>
<dt><a href="#DeviceStore">DeviceStore</a></dt>
<dd><p>Returns a new DeviceStore class that is used to access the various bins of a Device&#39;s information</p>
</dd>
<dt><a href="#Access">Access</a></dt>
<dd><p>Returns a new FirebaseStore class that will use the firebase library passed in. This should be either &#39;firebase&#39; (on browser) or &#39;firebase-admin&#39; on server.</p>
</dd>
<dt><a href="#FirebaseStore">FirebaseStore</a></dt>
<dd><p>contains many methods for interacting with the firebase database</p>
</dd>
<dt><a href="#RootStore">RootStore</a></dt>
<dd><p>Returns a new SystemStore class that is used to access the various bins of a Device&#39;s information</p>
</dd>
<dt><a href="#SystemStore">SystemStore</a></dt>
<dd><p>Returns a new SystemStore class that is used to access the various bins of a Device&#39;s information</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#_refFor returns the ref for a child or the current ref">_refFor returns the ref for a child or the current ref(path)</a></dt>
<dd></dd>
<dt><a href="#child returns an access object for the child">child returns an access object for the child(path)</a></dt>
<dd></dd>
<dt><a href="#on starts an on listener">on starts an on listener(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#off starts an off listener">off starts an off listener(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#onAdd starts a listener for when a child is added">onAdd starts a listener for when a child is added(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#offAdd starts a listener for when a child is added">offAdd starts a listener for when a child is added(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#onRemove start a listener for when a child is removed">onRemove start a listener for when a child is removed(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#offRemove start a listener for when a child is removed">offRemove start a listener for when a child is removed(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#once make a one time query to the database for information">once make a one time query to the database for information(path, onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#set sets the value at the given path">set sets the value at the given path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#push pushes the value at the given path">push pushes the value at the given path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#update updates the value at the given path">update updates the value at the given path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#remove the data at the given path">remove the data at the given path(path, onComplete)</a></dt>
<dd></dd>
<dt><a href="#timestampValue returns the timestamp of the server">timestampValue returns the timestamp of the server()</a></dt>
<dd></dd>
<dt><a href="#destroy Complete removes the state for this app">destroy Complete removes the state for this app(onComplete)</a></dt>
<dd></dd>
<dt><a href="#signIn sign in to the database">signIn sign in to the database()</a></dt>
<dd></dd>
<dt><a href="#setState sets the status state">setState sets the status state(value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#setInfo Sets an optional sub-state value into the status block">setInfo Sets an optional sub-state value into the status block(value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#getInfo gets info from the database">getInfo gets info from the database(onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#setDetailData sets the value at the path">setDetailData sets the value at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#removeDetailData removes the data at the path">removeDetailData removes the data at the path(path, onComplete)</a></dt>
<dd></dd>
<dt><a href="#getDetailData gets the data on the path">getDetailData gets the data on the path(path, onComplete, onError, cxt)</a></dt>
<dd></dd>
<dt><a href="#getStatus Returns a Promise that is querying the app for its full status.">getStatus Returns a Promise that is querying the app for its full status.(onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#onStatus Listens for changes to the status object">onStatus Listens for changes to the status object(onComplete, onCancel)</a></dt>
<dd></dd>
<dt><a href="#offStatus Listens for changes to the status object">offStatus Listens for changes to the status object(callback)</a></dt>
<dd></dd>
<dt><a href="#setAppData sets app data at the path">setAppData sets app data at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#getAppData gets the app data at the path">getAppData gets the app data at the path(path, onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#onAppData listen for changes to the app data">onAppData listen for changes to the app data(path, onComplete, onCancel)</a></dt>
<dd></dd>
<dt><a href="#offAppData listen for changes to the app data">offAppData listen for changes to the app data(path, callback)</a></dt>
<dd></dd>
<dt><a href="#updateAppData updates the app data">updateAppData updates the app data(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#removeAppData removes the app data at the path">removeAppData removes the app data at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#signIn If on the client side, sign in with a custom jwt token"> sign in with a custom jwt token(jwt)</a></dt>
<dd></dd>
<dt><a href="#child Create a child at the specified relative path, using the specified class"> using the specified class(path, ClassType)</a></dt>
<dd></dd>
<dt><a href="#access Creates an Access object referencing the location retrive to the current root">access Creates an Access object referencing the location retrive to the current root(path)</a></dt>
<dd></dd>
<dt><a href="#service If invoked with no arguments, this will return a Access object pointing at root/srv (which is not normal except for perhaps monitoring). Otherwise, an Access object pointing to <root>/srv/<name> is created"> an Access object pointing to <root>/srv/<name> is created(name)</a></dt>
<dd></dd>
<dt><a href="#timestampValue returns the timestamp of the server">timestampValue returns the timestamp of the server()</a></dt>
<dd></dd>
<dt><a href="#appByName searchs firebase instance for an app with the name">appByName searchs firebase instance for an app with the name(firebase, name)</a></dt>
<dd></dd>
<dt><a href="#registerDatabase adds a database class to the databases object">registerDatabase adds a database class to the databases object(type, clzz)</a></dt>
<dd></dd>
<dt><a href="#registerLib adds a library to the lib object">registerLib adds a library to the lib object(type, lib)</a></dt>
<dd></dd>
<dt><a href="#createRootStore creates a store with the root store class">createRootStore creates a store with the root store class(options)</a></dt>
<dd></dd>
<dt><a href="#createSystemStore creates a store with the system store class">createSystemStore creates a store with the system store class(options)</a></dt>
<dd></dd>
<dt><a href="#createDeviceStore creates a store with the device store class">createDeviceStore creates a store with the device store class(options)</a></dt>
<dd></dd>
<dt><a href="#createAppState Creates an AppState object from the given arguments_">createAppState Creates an AppState object from the given arguments:(options, name)</a></dt>
<dd></dd>
<dt><a href="#data returns an instance of access for getting data">data returns an instance of access for getting data()</a></dt>
<dd></dd>
<dt><a href="#meta returns an instance of access for getting the meta">meta returns an instance of access for getting the meta()</a></dt>
<dd></dd>
<dt><a href="#events returns an instance of access for getting events">events returns an instance of access for getting events()</a></dt>
<dd></dd>
<dt><a href="#outbound returns an instance of access for outbound data">outbound returns an instance of access for outbound data()</a></dt>
<dd></dd>
<dt><a href="#device returns an instance of access for devices">device returns an instance of access for devices()</a></dt>
<dd></dd>
<dt><a href="#cache returns an instance of access for the cache">cache returns an instance of access for the cache()</a></dt>
<dd></dd>
<dt><a href="#init creates and returns an instance of a class for interacting with the database">init creates and returns an instance of a class for interacting with the database(firebase)</a></dt>
<dd></dd>
<dt><a href="#_refFor returns the reference for the given path">_refFor returns the reference for the given path(path)</a></dt>
<dd></dd>
<dt><a href="#child returns an access object for the provided path">child returns an access object for the provided path(path)</a></dt>
<dd></dd>
<dt><a href="#on starts a listener on the provided path">on starts a listener on the provided path(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#off starts a listener on the provided path">off starts a listener on the provided path(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#onAdd starts a listener on the provided path for children being added">onAdd starts a listener on the provided path for children being added(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#offAdd starts a listener on the path for children being added">offAdd starts a listener on the path for children being added(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#onRemove starts a listener for children being removed">onRemove starts a listener for children being removed(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#offRemove starts a listener for children being removed">offRemove starts a listener for children being removed(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#once makes a one time call to the database for information">once makes a one time call to the database for information(path, onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#set sets the value at the path">set sets the value at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#update updates the value at the path">update updates the value at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#remove removes the value at the path">remove removes the value at the path(path, onComplete)</a></dt>
<dd></dd>
<dt><a href="#timestampValue returns the timestamp of the firebase server">timestampValue returns the timestamp of the firebase server()</a></dt>
<dd></dd>
<dt><a href="#_refFor gets a database reference for the path">_refFor gets a database reference for the path(path)</a></dt>
<dd></dd>
<dt><a href="#_metaRefFor gets a database reference for the meta data of the path">_metaRefFor gets a database reference for the meta data of the path(path)</a></dt>
<dd></dd>
<dt><a href="#_serviceRefFor gets a database reference for the service data of the path">_serviceRefFor gets a database reference for the service data of the path(path)</a></dt>
<dd></dd>
<dt><a href="#signIn If on the client side, sign in with a custom jwt token"> sign in with a custom jwt token(jwt)</a></dt>
<dd></dd>
<dt><a href="#child returns a new FirebaseStore with the a new root">child returns a new FirebaseStore with the a new root(path)</a></dt>
<dd></dd>
<dt><a href="#data returns a new Access object to the data root">data returns a new Access object to the data root()</a></dt>
<dd></dd>
<dt><a href="#meta returns a new Access object to the meta root">meta returns a new Access object to the meta root()</a></dt>
<dd></dd>
<dt><a href="#device returns a new Accees object to the device root">device returns a new Accees object to the device root()</a></dt>
<dd></dd>
<dt><a href="#access Creates an Access object referencing the location reative to the current root">access Creates an Access object referencing the location reative to the current root(path)</a></dt>
<dd></dd>
<dt><a href="#on creates a listener for when the data at the path is changed">on creates a listener for when the data at the path is changed(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#off create a listener for when the data at the path is changed">off create a listener for when the data at the path is changed(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#once get the data one time">once get the data one time(path, onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#set sets the data at the path">set sets the data at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#update updates the data at the path">update updates the data at the path(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#remove removes the data at the path">remove removes the data at the path(path, onComplete)</a></dt>
<dd></dd>
<dt><a href="#metaOn adds a listener to the meta data at the path">metaOn adds a listener to the meta data at the path(path, onComplete, onCancelled, cxt)</a></dt>
<dd></dd>
<dt><a href="#metaOff adds a listener to the meta data at the path">metaOff adds a listener to the meta data at the path(path, callback, cxt)</a></dt>
<dd></dd>
<dt><a href="#metaOnce gets the meta data once">metaOnce gets the meta data once(path, onComplete, onError)</a></dt>
<dd></dd>
<dt><a href="#metaSet sets the meta data">metaSet sets the meta data(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#metaUpdate updates the meta data">metaUpdate updates the meta data(path, value, onComplete)</a></dt>
<dd></dd>
<dt><a href="#metaRemove removes the meta at the path">metaRemove removes the meta at the path(path, onComplete)</a></dt>
<dd></dd>
<dt><a href="#timestampValue gets the timestamp of the database">timestampValue gets the timestamp of the database()</a></dt>
<dd></dd>
<dt><a href="#appByName gets a firebase app based off its name">appByName gets a firebase app based off its name(name)</a></dt>
<dd></dd>
<dt><a href="#Creates a DeviceStore for the systems device">Creates a DeviceStore for the systems device(dev)</a></dt>
<dd></dd>
<dt><a href="#deviceStore Creates a DeviceStore for the systems device">deviceStore Creates a DeviceStore for the systems device(dev)</a></dt>
<dd></dd>
</dl>

<a name="Access"></a>

## Access
Access contains a set of standard methods for getting and setting data for any database

**Kind**: global class  

* [Access](#Access)
    * [new Access(ref, firebase)](#new_Access_new)
    * [new Access(ref)](#new_Access_new)

<a name="new_Access_new"></a>

### new Access(ref, firebase)

| Param | Type | Description |
| --- | --- | --- |
| ref | <code>object</code> | contains all the methods for interacting with the database |
| firebase | <code>object</code> | firebase database object |

<a name="new_Access_new"></a>

### new Access(ref)

| Param | Type | Description |
| --- | --- | --- |
| ref | <code>object</code> | object with methods to interact with the database |

<a name="AppState"></a>

## AppState
The AppState allows the using application to store its current
state in a common way, as well as any app specific data needed.

This is expecting a Database Adapter as its argument. It is assumed
that the AppState owns the root of the database, as destroy() will
remove it.

Structure :
{
   status : {
     state : 'initializing' | 'started' | ...
     info : 'sub state'
     detail : { } 
     updated : timestamp
   }
   app : { }
}

**Kind**: global class  
<a name="DeviceStore"></a>

## DeviceStore
Returns a new DeviceStore class that is used to access the various bins of a Device's information

**Kind**: global class  
<a name="Access"></a>

## Access
Returns a new FirebaseStore class that will use the firebase library passed in. This should be either 'firebase' (on browser) or 'firebase-admin' on server.

**Kind**: global class  

* [Access](#Access)
    * [new Access(ref, firebase)](#new_Access_new)
    * [new Access(ref)](#new_Access_new)

<a name="new_Access_new"></a>

### new Access(ref, firebase)

| Param | Type | Description |
| --- | --- | --- |
| ref | <code>object</code> | contains all the methods for interacting with the database |
| firebase | <code>object</code> | firebase database object |

<a name="new_Access_new"></a>

### new Access(ref)

| Param | Type | Description |
| --- | --- | --- |
| ref | <code>object</code> | object with methods to interact with the database |

<a name="FirebaseStore"></a>

## FirebaseStore
contains many methods for interacting with the firebase database

**Kind**: global class  
<a name="new_FirebaseStore_new"></a>

### new FirebaseStore(options)

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | firebase config |

<a name="RootStore"></a>

## RootStore
Returns a new SystemStore class that is used to access the various bins of a Device's information

**Kind**: global class  
<a name="SystemStore"></a>

## SystemStore
Returns a new SystemStore class that is used to access the various bins of a Device's information

**Kind**: global class  
<a name="_refFor returns the ref for a child or the current ref"></a>

## \_refFor returns the ref for a child or the current ref(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | null for current ref or child string for a child |

<a name="child returns an access object for the child"></a>

## child returns an access object for the child(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path for the child |

<a name="on starts an on listener"></a>

## on starts an on listener(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="off starts an off listener"></a>

## off starts an off listener(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="onAdd starts a listener for when a child is added"></a>

## onAdd starts a listener for when a child is added(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="offAdd starts a listener for when a child is added"></a>

## offAdd starts a listener for when a child is added(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="onRemove start a listener for when a child is removed"></a>

## onRemove start a listener for when a child is removed(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="offRemove start a listener for when a child is removed"></a>

## offRemove start a listener for when a child is removed(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="once make a one time query to the database for information"></a>

## once make a one time query to the database for information(path, onComplete, onError)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |

<a name="set sets the value at the given path"></a>

## set sets the value at the given path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to set the value on |
| value | <code>any</code> | the value to set |
| onComplete | <code>function</code> |  |

<a name="push pushes the value at the given path"></a>

## push pushes the value at the given path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to push the value to |
| value | <code>any</code> | the value to be pushed |
| onComplete | <code>function</code> |  |

<a name="update updates the value at the given path"></a>

## update updates the value at the given path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to update the data at |
| value | <code>any</code> | the value to be updated |
| onComplete | <code>function</code> |  |

<a name="remove the data at the given path"></a>

## remove the data at the given path(path, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to remove the data at |
| onComplete | <code>function</code> |  |

<a name="timestampValue returns the timestamp of the server"></a>

## timestampValue returns the timestamp of the server()
**Kind**: global function  
<a name="destroy Complete removes the state for this app"></a>

## destroy Complete removes the state for this app(onComplete)
**Kind**: global function  

| Param | Type |
| --- | --- |
| onComplete | <code>function</code> | 

<a name="signIn sign in to the database"></a>

## signIn sign in to the database()
**Kind**: global function  
<a name="setState sets the status state"></a>

## setState sets the status state(value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| value | <code>any</code> | value to set the state to |
| onComplete | <code>function</code> |  |

<a name="setInfo Sets an optional sub-state value into the status block"></a>

## setInfo Sets an optional sub-state value into the status block(value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| value | <code>any</code> | value to set the info to |
| onComplete | <code>function</code> |  |

<a name="getInfo gets info from the database"></a>

## getInfo gets info from the database(onComplete, onError)
**Kind**: global function  

| Param | Type |
| --- | --- |
| onComplete | <code>function</code> | 
| onError | <code>function</code> | 

<a name="setDetailData sets the value at the path"></a>

## setDetailData sets the value at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to set the value at |
| value | <code>any</code> | data to set at the path |
| onComplete | <code>function</code> |  |

<a name="removeDetailData removes the data at the path"></a>

## removeDetailData removes the data at the path(path, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to remove the data at |
| onComplete | <code>function</code> |  |

<a name="getDetailData gets the data on the path"></a>

## getDetailData gets the data on the path(path, onComplete, onError, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to get the data from |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |
| cxt | <code>any</code> |  |

<a name="getStatus Returns a Promise that is querying the app for its full status."></a>

## getStatus Returns a Promise that is querying the app for its full status.(onComplete, onError)
**Kind**: global function  

| Param | Type |
| --- | --- |
| onComplete | <code>function</code> | 
| onError | <code>function</code> | 

<a name="onStatus Listens for changes to the status object"></a>

## onStatus Listens for changes to the status object(onComplete, onCancel)
**Kind**: global function  

| Param | Type |
| --- | --- |
| onComplete | <code>function</code> | 
| onCancel | <code>function</code> | 

<a name="offStatus Listens for changes to the status object"></a>

## offStatus Listens for changes to the status object(callback)
**Kind**: global function  

| Param | Type |
| --- | --- |
| callback | <code>function</code> | 

<a name="setAppData sets app data at the path"></a>

## setAppData sets app data at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to set the data at |
| value | <code>any</code> | data to be set |
| onComplete | <code>function</code> |  |

<a name="getAppData gets the app data at the path"></a>

## getAppData gets the app data at the path(path, onComplete, onError)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to get the data at |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |

<a name="onAppData listen for changes to the app data"></a>

## onAppData listen for changes to the app data(path, onComplete, onCancel)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to listen to app data at |
| onComplete | <code>function</code> |  |
| onCancel | <code>function</code> |  |

<a name="offAppData listen for changes to the app data"></a>

## offAppData listen for changes to the app data(path, callback)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to listen to app data at |
| callback | <code>function</code> |  |

<a name="updateAppData updates the app data"></a>

## updateAppData updates the app data(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to update the data at |
| value | <code>any</code> | value to update the app data to |
| onComplete | <code>function</code> |  |

<a name="removeAppData removes the app data at the path"></a>

## removeAppData removes the app data at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to remove the data at |
| value | <code>any</code> | not used? |
| onComplete | <code>function</code> |  |

<a name="access Creates an Access object referencing the location retrive to the current root"></a>

## access Creates an Access object referencing the location retrive to the current root(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | data path |

<a name="timestampValue returns the timestamp of the server"></a>

## timestampValue returns the timestamp of the server()
**Kind**: global function  
<a name="appByName searchs firebase instance for an app with the name"></a>

## appByName searchs firebase instance for an app with the name(firebase, name)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| firebase | <code>object</code> |  |
| name | <code>string</code> | name of firebase app to search for |

<a name="registerDatabase adds a database class to the databases object"></a>

## registerDatabase adds a database class to the databases object(type, clzz)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | the look up string for the database |
| clzz | <code>class</code> | the class for creating databases |

<a name="registerLib adds a library to the lib object"></a>

## registerLib adds a library to the lib object(type, lib)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | the string that lib gets registered under |
| lib | <code>any</code> | the library to be registered |

<a name="createRootStore creates a store with the root store class"></a>

## createRootStore creates a store with the root store class(options)
**Kind**: global function  

| Param | Type |
| --- | --- |
| options | <code>object</code> | 

<a name="createSystemStore creates a store with the system store class"></a>

## createSystemStore creates a store with the system store class(options)
**Kind**: global function  

| Param | Type |
| --- | --- |
| options | <code>object</code> | 

<a name="createDeviceStore creates a store with the device store class"></a>

## createDeviceStore creates a store with the device store class(options)
**Kind**: global function  

| Param | Type |
| --- | --- |
| options | <code>object</code> | 

<a name="createAppState Creates an AppState object from the given arguments_"></a>

## createAppState Creates an AppState object from the given arguments:(options, name)
**Kind**: global function  

| Param | Description |
| --- | --- |
| options | either a config object, or a database |
| name | the name of AppState to attach too. If null/undefined the options.appName or  db.options.appName will be used. |

<a name="data returns an instance of access for getting data"></a>

## data returns an instance of access for getting data()
**Kind**: global function  
<a name="meta returns an instance of access for getting the meta"></a>

## meta returns an instance of access for getting the meta()
**Kind**: global function  
<a name="events returns an instance of access for getting events"></a>

## events returns an instance of access for getting events()
**Kind**: global function  
<a name="outbound returns an instance of access for outbound data"></a>

## outbound returns an instance of access for outbound data()
**Kind**: global function  
<a name="device returns an instance of access for devices"></a>

## device returns an instance of access for devices()
**Kind**: global function  
<a name="cache returns an instance of access for the cache"></a>

## cache returns an instance of access for the cache()
**Kind**: global function  
<a name="init creates and returns an instance of a class for interacting with the database"></a>

## init creates and returns an instance of a class for interacting with the database(firebase)
**Kind**: global function  

| Param | Type |
| --- | --- |
| firebase | <code>object</code> | 

<a name="_refFor returns the reference for the given path"></a>

## \_refFor returns the reference for the given path(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to return the ref of |

<a name="child returns an access object for the provided path"></a>

## child returns an access object for the provided path(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to return the new access object for |

<a name="on starts a listener on the provided path"></a>

## on starts a listener on the provided path(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to start the listener on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="off starts a listener on the provided path"></a>

## off starts a listener on the provided path(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to start the listener |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="onAdd starts a listener on the provided path for children being added"></a>

## onAdd starts a listener on the provided path for children being added(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="offAdd starts a listener on the path for children being added"></a>

## offAdd starts a listener on the path for children being added(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path for the listener |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="onRemove starts a listener for children being removed"></a>

## onRemove starts a listener for children being removed(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path for the listener |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="offRemove starts a listener for children being removed"></a>

## offRemove starts a listener for children being removed(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path for the listener |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="once makes a one time call to the database for information"></a>

## once makes a one time call to the database for information(path, onComplete, onError)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to get |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |

<a name="set sets the value at the path"></a>

## set sets the value at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to set |
| value | <code>any</code> | value that will be set |
| onComplete | <code>function</code> |  |

<a name="update updates the value at the path"></a>

## update updates the value at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to update |
| value | <code>any</code> | value that will be updated |
| onComplete | <code>function</code> |  |

<a name="remove removes the value at the path"></a>

## remove removes the value at the path(path, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path of the data to be removed |
| onComplete | <code>function</code> |  |

<a name="timestampValue returns the timestamp of the firebase server"></a>

## timestampValue returns the timestamp of the firebase server()
**Kind**: global function  
<a name="_refFor gets a database reference for the path"></a>

## \_refFor gets a database reference for the path(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to get a database reference for |

<a name="_metaRefFor gets a database reference for the meta data of the path"></a>

## \_metaRefFor gets a database reference for the meta data of the path(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to get the meta for |

<a name="_serviceRefFor gets a database reference for the service data of the path"></a>

## \_serviceRefFor gets a database reference for the service data of the path(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to get the service for |

<a name="child returns a new FirebaseStore with the a new root"></a>

## child returns a new FirebaseStore with the a new root(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | appended to the current root to make the root of the new FirebaseStore |

<a name="data returns a new Access object to the data root"></a>

## data returns a new Access object to the data root()
**Kind**: global function  
<a name="meta returns a new Access object to the meta root"></a>

## meta returns a new Access object to the meta root()
**Kind**: global function  
<a name="device returns a new Accees object to the device root"></a>

## device returns a new Accees object to the device root()
**Kind**: global function  
<a name="access Creates an Access object referencing the location reative to the current root"></a>

## access Creates an Access object referencing the location reative to the current root(path)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path for a new access object |

<a name="on creates a listener for when the data at the path is changed"></a>

## on creates a listener for when the data at the path is changed(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to the desired data to be listened to |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="off create a listener for when the data at the path is changed"></a>

## off create a listener for when the data at the path is changed(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to the desired data to be listened to |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="once get the data one time"></a>

## once get the data one time(path, onComplete, onError)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to get the data from |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |

<a name="set sets the data at the path"></a>

## set sets the data at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to set the value at |
| value | <code>any</code> | value to set |
| onComplete | <code>function</code> |  |

<a name="update updates the data at the path"></a>

## update updates the data at the path(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to update the value of |
| value | <code>any</code> | value to update |
| onComplete | <code>function</code> |  |

<a name="remove removes the data at the path"></a>

## remove removes the data at the path(path, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to remove |
| onComplete | <code>function</code> |  |

<a name="metaOn adds a listener to the meta data at the path"></a>

## metaOn adds a listener to the meta data at the path(path, onComplete, onCancelled, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen to the meta on |
| onComplete | <code>function</code> |  |
| onCancelled | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="metaOff adds a listener to the meta data at the path"></a>

## metaOff adds a listener to the meta data at the path(path, callback, cxt)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to listen to the meta |
| callback | <code>function</code> |  |
| cxt | <code>object</code> |  |

<a name="metaOnce gets the meta data once"></a>

## metaOnce gets the meta data once(path, onComplete, onError)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to get the meta from |
| onComplete | <code>function</code> |  |
| onError | <code>function</code> |  |

<a name="metaSet sets the meta data"></a>

## metaSet sets the meta data(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to set the meta on |
| value | <code>any</code> | the data to set at the path |
| onComplete | <code>function</code> |  |

<a name="metaUpdate updates the meta data"></a>

## metaUpdate updates the meta data(path, value, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | the path to update the meta on |
| value | <code>any</code> | the data to update the meta with |
| onComplete | <code>function</code> |  |

<a name="metaRemove removes the meta at the path"></a>

## metaRemove removes the meta at the path(path, onComplete)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | path to remove the meta on |
| onComplete | <code>function</code> |  |

<a name="timestampValue gets the timestamp of the database"></a>

## timestampValue gets the timestamp of the database()
**Kind**: global function  
<a name="appByName gets a firebase app based off its name"></a>

## appByName gets a firebase app based off its name(name)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | firebase app to use |

<a name="Creates a DeviceStore for the systems device"></a>

## Creates a DeviceStore for the systems device(dev)
**Kind**: global function  

| Param | Description |
| --- | --- |
| dev | either th id of the device, or a device object that contains an id field |

<a name="deviceStore Creates a DeviceStore for the systems device"></a>

## deviceStore Creates a DeviceStore for the systems device(dev)
**Kind**: global function  

| Param | Description |
| --- | --- |
| dev | either th id of the device, or a device object that contains an id field |

