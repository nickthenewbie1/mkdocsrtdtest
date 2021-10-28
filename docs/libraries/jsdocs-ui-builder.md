---
id: jsdocs-ui-builder
title: Ui Builder
---
## Constants

<dl>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#TYPE">TYPE</a></dt>
<dd><p>This is the model type of the element. It is embedded into the Model&#39;s type
field and is used to find Jss generators, editors, etc.</p>
</dd>
<dt><a href="#JssSpec">JssSpec</a></dt>
<dd><p>Defines how to map the model into jss/css via selectors</p>
</dd>
<dt><a href="#initialState">initialState</a></dt>
<dd><p>Format is: {
  <componentType> : {
    style : {
    }
    classes : { 
      <variant name 0> : <auto generated classname 0>
      <variant name N> : <auto generated classname N>
    },
    undo : [ ],
    redo : [ ]
  }
}</p>
</dd>
<dt><a href="#initialState">initialState</a></dt>
<dd><p>Format is {
  <componentType> : {
    variant : <the name of the selected variant to edit>
    group : <the sub group (hover, normal, disabled, etc) that is being edited>
  }
}</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#save">save()</a></dt>
<dd><p>Saves the current Appearance into a new AppearanceProject</p>
</dd>
<dt><a href="#create">create()</a> ⇒ <code>Promise</code></dt>
<dd><p>Creates a new Project with the given name and description. If the activeAppearanceId is
supplied, it is assumed that an already existing Appearance object is the projects main
appearance. Otherwise, a new appearance will be created from theme, component or their
default versions.</p>
</dd>
<dt><a href="#addVersion">addVersion()</a> ⇒ <code>Promise</code></dt>
<dd><p>Creates a new Version for the Project with the given name and description. If the activeAppearanceId is
supplied, it is assumed that an already existing Appearance object is to be added to version list. NOTE,
an appearance can be in only on AppearanceProjects version list.
Otherwise, a new appearance will be created from theme and component</p>
</dd>
<dt><a href="#addColorsToProjects">addColorsToProjects(fbContext, vals)</a></dt>
<dd></dd>
<dt><a href="#update">update()</a></dt>
<dd><p>Updates the style for a component</p>
</dd>
<dt><a href="#undo">undo()</a></dt>
<dd><p>Undo the style for a component</p>
</dd>
<dt><a href="#redo">redo()</a></dt>
<dd><p>Redo the style for a component</p>
</dd>
<dt><a href="#updateStyleState">updateStyleState()</a></dt>
<dd><p>Updates the style state for a component</p>
</dd>
<dt><a href="#isStyle">isStyle(currState, isState, [defaults])</a></dt>
<dd><p>Returns true if all the keys value pairs in isState
are contained in currState</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#createTab">createTab(create)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#toJss">toJss()</a></dt>
<dd><p>Converts the model into a jss object</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#create">create(createSubModels)</a></dt>
<dd><p>Create the model that represents the element</p>
</dd>
<dt><a href="#needsUpdate">needsUpdate(model, version)</a></dt>
<dd><p>Return true if the old model needs to be updated</p>
</dd>
<dt><a href="#update">update(model, version)</a></dt>
<dd><p>Updates the model if needed and returns the new
model to use. This should NOT mutate the model</p>
</dd>
<dt><a href="#id">id()</a></dt>
<dd><p>Status Accessors</p>
</dd>
<dt><a href="#name">name()</a></dt>
<dd><p>Header Accessors</p>
</dd>
<dt><a href="#getTheme">getTheme()</a></dt>
<dd><p>Theme Accessors</p>
</dd>
<dt><a href="#getComponents">getComponents()</a></dt>
<dd><p>Component Accessors</p>
</dd>
<dt><a href="#getComponentModels">getComponentModels()</a></dt>
<dd><p>Extracts just the component models from the redux state
and return a map of ComponentType : Model</p>
</dd>
<dt><a href="#resolve">resolve()</a></dt>
<dd><p>Given a value, it will be analyzed for expansion into
a CSS string.</p>
</dd>
<dt><a href="#resolveStyle">resolveStyle()</a></dt>
<dd><p>Given a style object, this will</p>
</dd>
<dt><a href="#update">update()</a> ⇒ <code>object</code></dt>
<dd><p>Updates the current components if needed</p>
</dd>
<dt><a href="#isUpdateNeeded">isUpdateNeeded(components, [full])</a> ⇒ <code>boolean</code> | <code>object</code></dt>
<dd><p>Compute which components needs updated</p>
</dd>
<dt><a href="#appearanceData">appearanceData()</a> ⇒ <code>DataItem</code></dt>
<dd></dd>
<dt><a href="#appearanceCss">appearanceCss()</a> ⇒ <code>DataItem</code></dt>
<dd></dd>
<dt><a href="#getColors">getColors()</a></dt>
<dd><p>Loads some colors for the appearance.</p>
</dd>
<dt><a href="#deletePaths">deletePaths()</a></dt>
<dd><p>Returns the delete paths</p>
</dd>
<dt><a href="#getChildIds">getChildIds()</a></dt>
<dd><p>Note : no pagination</p>
</dd>
<dt><a href="#getAll">getAll(options)</a></dt>
<dd><p>Returns an array of child objects in the table.</p>
</dd>
<dt><a href="#deletePaths">deletePaths()</a></dt>
<dd><p>This will return all the delete paths. This is an object
containing { [path1] : null, [path2] : null }</p>
</dd>
<dt><a href="#removeAll">removeAll()</a></dt>
<dd><p>This will remove all the children</p>
</dd>
<dt><a href="#path">path()</a></dt>
<dd><p>Returns the path relative to the rootRef in context</p>
</dd>
<dt><a href="#listPath">listPath()</a></dt>
<dd><p>Returns the path that holds the objects. Normally just type</p>
</dd>
<dt><a href="#validateData">validateData()</a></dt>
<dd><p>Called during create/set to check the data. This should throw an exception 
if it is invalid</p>
</dd>
<dt><a href="#validateUpdate">validateUpdate()</a></dt>
<dd><p>Called during update to check the data. This should throw an exception 
if it is invalid</p>
</dd>
<dt><a href="#create">create([data], [read])</a></dt>
<dd><p>Creates a new id if needed for the object and calls set</p>
</dd>
<dt><a href="#set">set([read])</a> ⇒ <code>Promise</code></dt>
<dd><p>Sets the data on the item</p>
</dd>
<dt><a href="#update">update(updates, [read])</a></dt>
<dd></dd>
<dt><a href="#updatePath">updatePath(updates, [read])</a></dt>
<dd></dd>
<dt><a href="#read">read()</a></dt>
<dd><p>Reads the data for the item</p>
</dd>
<dt><a href="#deletePaths">deletePaths()</a></dt>
<dd><p>This will return all the delete paths. This is an object
containing { [path1] : null, [path2] : null }</p>
</dd>
<dt><a href="#getValue">getValue()</a></dt>
<dd><p>This will read the data at the given path and return it.</p>
</dd>
<dt><a href="#getKeys">getKeys()</a></dt>
<dd><p>This will read the data at the given path and return it.</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>Returns an object of the specified type to be used to
handle manipulation of the data</p>
</dd>
<dt><a href="#getAll">getAll()</a></dt>
<dd><p>This will read all the data for a type and return it as an array.</p>
</dd>
<dt><a href="#onAppearanceLoaded">onAppearanceLoaded()</a></dt>
<dd><p>Invoked on the initial download of the firebase appearance</p>
</dd>
<dt><a href="#stylesheetToFlat">stylesheetToFlat()</a></dt>
<dd><p>Turn a (jss) stylesheet into a flatted path/value
hierarchical map. Conditional rules (media queries)
will be placed in the hierarchy and will have type
set to &#39;conditional&#39;. To avoid reordering in firebase,
this will put the selector rules into arrays.</p>
</dd>
<dt><a href="#props">props(component, variant)</a> ⇒ <code>object</code></dt>
<dd><p>Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component&#39;s default props and the component&#39;s variant props.</p>
<p>If the second argument is an object, it is considered to be the
React component&#39;s actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( &#39;Checkbox&#39;, this.props )</p>
</dd>
<dt><a href="#variantClassNames">variantClassNames(component, classes, type, variant)</a></dt>
<dd><p>Turns the variant&#39;s hierarchy into a hashified set of classnames.</p>
</dd>
<dt><a href="#props">props(component, variant)</a> ⇒ <code>object</code></dt>
<dd><p>Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component&#39;s default props and the component&#39;s variant props.</p>
<p>If the second argument is an object, it is considered to be the
React component&#39;s actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( &#39;Checkbox&#39;, this.props )</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>Call this to create a Factory. Options include
  name : <string> the name of the factory for debug
  allowsCreate : <bool> includes a create method. Default is true
  react : <bool> If true, React.createElement will be used. Default is false</p>
</dd>
</dl>

<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="TYPE"></a>

## TYPE
This is the model type of the element. It is embedded into the Model's type
field and is used to find Jss generators, editors, etc.

**Kind**: global constant  
<a name="JssSpec"></a>

## JssSpec
Defines how to map the model into jss/css via selectors

**Kind**: global constant  
<a name="initialState"></a>

## initialState
Format is: {
  <componentType> : {
    style : {
    }
    classes : { 
      <variant name 0> : <auto generated classname 0>
      <variant name N> : <auto generated classname N>
    },
    undo : [ ],
    redo : [ ]
  }
}

**Kind**: global constant  
<a name="initialState"></a>

## initialState
Format is {
  <componentType> : {
    variant : <the name of the selected variant to edit>
    group : <the sub group (hover, normal, disabled, etc) that is being edited>
  }
}

**Kind**: global constant  
<a name="save"></a>

## save()
Saves the current Appearance into a new AppearanceProject

**Kind**: global function  
<a name="create"></a>

## create() ⇒ <code>Promise</code>
Creates a new Project with the given name and description. If the activeAppearanceId is
supplied, it is assumed that an already existing Appearance object is the projects main
appearance. Otherwise, a new appearance will be created from theme, component or their
default versions.

**Kind**: global function  
**Returns**: <code>Promise</code> - a promise containing the project  
<a name="addVersion"></a>

## addVersion() ⇒ <code>Promise</code>
Creates a new Version for the Project with the given name and description. If the activeAppearanceId is
supplied, it is assumed that an already existing Appearance object is to be added to version list. NOTE,
an appearance can be in only on AppearanceProjects version list.
Otherwise, a new appearance will be created from theme and component

**Kind**: global function  
**Returns**: <code>Promise</code> - a promise containing the project  
<a name="addColorsToProjects"></a>

## addColorsToProjects(fbContext, vals)
**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| fbContext | <code>Context</code> |  |
| vals | <code>Array</code> | array of data objects |

<a name="update"></a>

## update()
Updates the style for a component

**Kind**: global function  
<a name="undo"></a>

## undo()
Undo the style for a component

**Kind**: global function  
<a name="redo"></a>

## redo()
Redo the style for a component

**Kind**: global function  
<a name="updateStyleState"></a>

## updateStyleState()
Updates the style state for a component

**Kind**: global function  
<a name="isStyle"></a>

## isStyle(currState, isState, [defaults])
Returns true if all the keys value pairs in isState
are contained in currState

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| currState | <code>object</code> | the current state |
| isState | <code>object</code> | the state to compare |
| [defaults] | <code>object</code> | this is used to define default values for the currState (like group and variant ) |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="createTab"></a>

## createTab(create)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| create | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="toJss"></a>

## toJss()
Converts the model into a jss object

**Kind**: global function  
<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="create"></a>

## create(createSubModels)
Create the model that represents the element

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| createSubModels | <code>boolean</code> | <code>false</code> | if true, create a complete model, including all the submodels. The submodels should be in inactive states. (default is false) |

<a name="needsUpdate"></a>

## needsUpdate(model, version)
Return true if the old model needs to be updated

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive update checks |

<a name="update"></a>

## update(model, version)
Updates the model if needed and returns the new
model to use. This should NOT mutate the model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the to examine |
| version | <code>VersionUpdater</code> | the VersionUpdater object that can be used for recursive updates |

<a name="id"></a>

## id()
Status Accessors

**Kind**: global function  
<a name="name"></a>

## name()
Header Accessors

**Kind**: global function  
<a name="getTheme"></a>

## getTheme()
Theme Accessors

**Kind**: global function  
<a name="getComponents"></a>

## getComponents()
Component Accessors

**Kind**: global function  
<a name="getComponentModels"></a>

## getComponentModels()
Extracts just the component models from the redux state
and return a map of ComponentType : Model

**Kind**: global function  
<a name="resolve"></a>

## resolve()
Given a value, it will be analyzed for expansion into
a CSS string.

**Kind**: global function  
<a name="resolveStyle"></a>

## resolveStyle()
Given a style object, this will

**Kind**: global function  
<a name="update"></a>

## update() ⇒ <code>object</code>
Updates the current components if needed

**Kind**: global function  
**Returns**: <code>object</code> - a updated version of components  
<a name="isUpdateNeeded"></a>

## isUpdateNeeded(components, [full]) ⇒ <code>boolean</code> \| <code>object</code>
Compute which components needs updated

**Kind**: global function  
**Returns**: <code>boolean</code> \| <code>object</code> - If full is true, an object of the form
  { needsUpdate : true|false,
    which : {
      <ComponentType> : true | false | null ( if null, no plugin exists for component ) 
    }
  }
will be returned. Otherwise true or false will be returned  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| components | <code>object</code> |  | ComponentType to model map. |
| [full] | <code>boolean</code> | <code>false</code> | if false (default), this will return a simple true or false. If true, the detailed object will be returned |

<a name="appearanceData"></a>

## appearanceData() ⇒ <code>DataItem</code>
**Kind**: global function  
**Returns**: <code>DataItem</code> - the data item for the data.  
<a name="appearanceCss"></a>

## appearanceCss() ⇒ <code>DataItem</code>
**Kind**: global function  
**Returns**: <code>DataItem</code> - the data item for the data.  
<a name="getColors"></a>

## getColors()
Loads some colors for the appearance.

**Kind**: global function  
<a name="deletePaths"></a>

## deletePaths()
Returns the delete paths

**Kind**: global function  
<a name="getChildIds"></a>

## getChildIds()
Note : no pagination

**Kind**: global function  
<a name="getAll"></a>

## getAll(options)
Returns an array of child objects in the table.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.readData | <code>boolean</code> | if true, all the objects will have read() called on them |

<a name="deletePaths"></a>

## deletePaths()
This will return all the delete paths. This is an object
containing { [path1] : null, [path2] : null }

**Kind**: global function  
<a name="removeAll"></a>

## removeAll()
This will remove all the children

**Kind**: global function  
<a name="path"></a>

## path()
Returns the path relative to the rootRef in context

**Kind**: global function  
<a name="listPath"></a>

## listPath()
Returns the path that holds the objects. Normally just type

**Kind**: global function  
<a name="validateData"></a>

## validateData()
Called during create/set to check the data. This should throw an exception 
if it is invalid

**Kind**: global function  
<a name="validateUpdate"></a>

## validateUpdate()
Called during update to check the data. This should throw an exception 
if it is invalid

**Kind**: global function  
<a name="create"></a>

## create([data], [read])
Creates a new id if needed for the object and calls set

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [data] | <code>object</code> | <code></code> | the data representation. If null,  the current this.data is used |
| [read] | <code>boolean</code> | <code>true</code> | if true, the object will be read after writing so the data is up to date |

<a name="set"></a>

## set([read]) ⇒ <code>Promise</code>
Sets the data on the item

**Kind**: global function  
**Returns**: <code>Promise</code> - a promise that contains this DataItem  

| Param | Type | Description |
| --- | --- | --- |
| [read] | <code>boolean</code> | if true, the object will be read after writing so the data is up to date |

<a name="update"></a>

## update(updates, [read])
**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| updates | <code>object</code> |  | an path to value map |
| [read] | <code>boolean</code> | <code>false</code> | if true, the object will be read after writing so the data is up to date |

<a name="updatePath"></a>

## updatePath(updates, [read])
**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| updates | <code>object</code> |  | an path to value map |
| [read] | <code>boolean</code> | <code>false</code> | if true, the object will be read after writing so the data is up to date |

<a name="read"></a>

## read()
Reads the data for the item

**Kind**: global function  
<a name="deletePaths"></a>

## deletePaths()
This will return all the delete paths. This is an object
containing { [path1] : null, [path2] : null }

**Kind**: global function  
<a name="getValue"></a>

## getValue()
This will read the data at the given path and return it.

**Kind**: global function  
<a name="getKeys"></a>

## getKeys()
This will read the data at the given path and return it.

**Kind**: global function  
<a name="create"></a>

## create()
Returns an object of the specified type to be used to
handle manipulation of the data

**Kind**: global function  
<a name="getAll"></a>

## getAll()
This will read all the data for a type and return it as an array.

**Kind**: global function  
<a name="onAppearanceLoaded"></a>

## onAppearanceLoaded()
Invoked on the initial download of the firebase appearance

**Kind**: global function  
<a name="stylesheetToFlat"></a>

## stylesheetToFlat()
Turn a (jss) stylesheet into a flatted path/value
hierarchical map. Conditional rules (media queries)
will be placed in the hierarchy and will have type
set to 'conditional'. To avoid reordering in firebase,
this will put the selector rules into arrays.

**Kind**: global function  
<a name="props"></a>

## props(component, variant) ⇒ <code>object</code>
Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component's default props and the component's variant props.

If the second argument is an object, it is considered to be the
React component's actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( 'Checkbox', this.props )

**Kind**: global function  
**Returns**: <code>object</code> - an object containing the default props. This will be a 
merger of the default variant's props and the specified variants props. 
This will always return an object  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| variant | <code>string</code> \| <code>object</code> | the variant name to requsest. eg "small" |

<a name="variantClassNames"></a>

## variantClassNames(component, classes, type, variant)
Turns the variant's hierarchy into a hashified set of classnames.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>object</code> | the redux model for the component type |
| classes | <code>object</code> | the jss classname lookup |
| type | <code>string</code> | the component type |
| variant | <code>string</code> | the component variant |

<a name="props"></a>

## props(component, variant) ⇒ <code>object</code>
Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component's default props and the component's variant props.

If the second argument is an object, it is considered to be the
React component's actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( 'Checkbox', this.props )

**Kind**: global function  
**Returns**: <code>object</code> - an object containing the default props. This will be a 
merger of the default variant's props and the specified variants props. 
This will always return an object  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| variant | <code>string</code> \| <code>object</code> | the variant name to requsest. eg "small" |

<a name="create"></a>

## create()
Call this to create a Factory. Options include
  name : <string> the name of the factory for debug
  allowsCreate : <bool> includes a create method. Default is true
  react : <bool> If true, React.createElement will be used. Default is false

**Kind**: global function  
