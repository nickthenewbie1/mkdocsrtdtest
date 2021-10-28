---
id: jsdocs-ui-theme
title: Ui Theme
---
## Modules

<dl>
<dt><a href="#module_CssGenerators">CssGenerators</a></dt>
<dd></dd>
<dt><a href="#module_GroupSelectorModel">GroupSelectorModel</a></dt>
<dd></dd>
<dt><a href="#module_HierarchyGenerators">HierarchyGenerators</a></dt>
<dd></dd>
<dt><a href="#module_MediaSelectorModel">MediaSelectorModel</a></dt>
<dd></dd>
<dt><a href="#module_PropertiesModel">PropertiesModel</a></dt>
<dd></dd>
<dt><a href="#module_PropGenerators">PropGenerators</a></dt>
<dd></dd>
<dt><a href="#module_VariantStyleModel">VariantStyleModel</a></dt>
<dd><p>The VariantStyleModel is normally the root model of a style tree.
It supports variants and subvariants, each with their own model. The
VariantStyleModel also support per variant props that inherit from
the parent and default variants. Often, the style model for each
variant will be a MediaSelectorModel</p>
</dd>
</dl>

## Classes

<dl>
<dt><a href="#JssCreator">JssCreator</a></dt>
<dd><p>A helper class to create a Jss map for</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#varTypes">varTypes</a></dt>
<dd><p>Used to decide whether or a value can be referenced
as a less/css variable</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#setColor">setColor()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its color,
and returns the copy</p>
</dd>
<dt><a href="#setClearLayers">setClearLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its clearLayers,
and returns the copy</p>
</dd>
<dt><a href="#setLayer">setLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown</p>
</dd>
<dt><a href="#addLayer">addLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and adds the layer</p>
</dd>
<dt><a href="#swapLayers">swapLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#removeLayer">removeLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#setClearLayers">setClearLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its clearLayers,
and returns the copy</p>
</dd>
<dt><a href="#setLayer">setLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown</p>
</dd>
<dt><a href="#addLayer">addLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and adds the layer</p>
</dd>
<dt><a href="#swapLayers">swapLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#removeLayer">removeLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#setClearLayers">setClearLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its clearLayers,
and returns the copy</p>
</dd>
<dt><a href="#setLayer">setLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown</p>
</dd>
<dt><a href="#addLayer">addLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and adds the layer</p>
</dd>
<dt><a href="#swapLayers">swapLayers()</a></dt>
<dd><p>Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#removeLayer">removeLayer()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>{ type : &#39;transform&#39;,
    clear : true | false,
    fucntions : [
    ]
  }</p>
</dd>
<dt><a href="#setClear">setClear()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its clearLayers,
and returns the copy</p>
</dd>
<dt><a href="#setFunction">setFunction()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the function at the
specified index. If index is out of bouds, an error is thrown</p>
</dd>
<dt><a href="#addFunction">addFunction()</a></dt>
<dd><p>Creates a shallow copy of the model, and adds the layer</p>
</dd>
<dt><a href="#swapFunctions">swapFunctions()</a></dt>
<dd><p>Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#removeFunction">removeFunction()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>{ type : &#39;transition&#39;,
    clear : true | false,
    properties : {
      name : { duration, timingFunction, delay }
    }}</p>
</dd>
<dt><a href="#setClear">setClear()</a></dt>
<dd><p>Creates a shallow copy of the model, sets its clearLayers,
and returns the copy</p>
</dd>
<dt><a href="#setTransition">setTransition()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the property.</p>
</dd>
<dt><a href="#removeTransition">removeTransition()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the property.</p>
</dd>
<dt><a href="#update">update()</a></dt>
<dd><p>Creates a shallow copy of the model, and removes the property.</p>
</dd>
<dt><a href="#updateDuration">updateDuration()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the duration for the name.</p>
</dd>
<dt><a href="#updateDelay">updateDelay()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the delay for the name.</p>
</dd>
<dt><a href="#updateTiming">updateTiming()</a></dt>
<dd><p>Creates a shallow copy of the model, and sets the duration for the name.</p>
</dd>
<dt><a href="#addModel">addModel(type, modelFunctions)</a></dt>
<dd><p>This will register the modelFunctions as a CssGenerator and
a VersionUpdater</p>
</dd>
<dt><a href="#isOldVersion">isOldVersion(model, currentVersion, dVersion)</a></dt>
<dd><p>Returns true if the model&#39;s version is not equal to the model&#39;s version.</p>
</dd>
<dt><a href="#isThemeVar">isThemeVar()</a></dt>
<dd><p>Returns true if v matches the theme var format</p>
</dd>
<dt><a href="#isThemeVarType">isThemeVarType()</a></dt>
<dd><p>Returns true if v matches the theme var format and is of the type</p>
</dd>
<dt><a href="#filterThemeVars">filterThemeVars()</a></dt>
<dd><p>Removes vars that are not of the specified type</p>
</dd>
<dt><a href="#resolve">resolve()</a></dt>
<dd><p>Looks at model.extend to find an immediate parent
and merges the model and extended model. It then 
proceeds to resolve all the keys in the merged object.
This is shallow and only works at the model&#39;s key level</p>
</dd>
<dt><a href="#createSetValue">createSetValue(key, [create])</a></dt>
<dd><p>This will return a function (model, value) that makes a shallow copy of 
of the model and sets the value on model[key]. If model is null and create
is supplied, this will call create to make a model</p>
</dd>
<dt><a href="#mergeJss">mergeJss()</a></dt>
<dd><p>This will take the css/jss properties and merge them into
the baseJss with the given selector and variant</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#Spec">Spec</a></dt>
<dd></dd>
</dl>

<a name="module_CssGenerators"></a>

## CssGenerators
<a name="module_GroupSelectorModel"></a>

## GroupSelectorModel

* [GroupSelectorModel](#module_GroupSelectorModel)
    * [~create()](#module_GroupSelectorModel..create) ⇒ <code>GroupSelectorModel</code>
    * [~Group](#module_GroupSelectorModel..Group) : <code>Object</code>
    * [~GroupSelectorModel](#module_GroupSelectorModel..GroupSelectorModel) : <code>Object</code>

<a name="module_GroupSelectorModel..create"></a>

### GroupSelectorModel~create() ⇒ <code>GroupSelectorModel</code>
Creates a GroupSelectorModel.

**Kind**: inner method of [<code>GroupSelectorModel</code>](#module_GroupSelectorModel)  
**Returns**: <code>GroupSelectorModel</code> - The group model  
<a name="module_GroupSelectorModel..Group"></a>

### GroupSelectorModel~Group : <code>Object</code>
**Kind**: inner typedef of [<code>GroupSelectorModel</code>](#module_GroupSelectorModel)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| group | <code>string</code> | the name of the group |
| name | <code>string</code> | the name for the part of this group |
| model | <code>object</code> | the model for the group part |

<a name="module_GroupSelectorModel..GroupSelectorModel"></a>

### GroupSelectorModel~GroupSelectorModel : <code>Object</code>
**Kind**: inner typedef of [<code>GroupSelectorModel</code>](#module_GroupSelectorModel)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | 'groupSelector' |
| groups | <code>Array.&lt;Group&gt;</code> | the groups in the model |

<a name="module_HierarchyGenerators"></a>

## HierarchyGenerators
<a name="module_MediaSelectorModel"></a>

## MediaSelectorModel

* [MediaSelectorModel](#module_MediaSelectorModel)
    * [~getMediaModels()](#module_MediaSelectorModel..getMediaModels)
    * [~add()](#module_MediaSelectorModel..add)
    * [~remove()](#module_MediaSelectorModel..remove)
    * [~update()](#module_MediaSelectorModel..update)

<a name="module_MediaSelectorModel..getMediaModels"></a>

### MediaSelectorModel~getMediaModels()
Returns an array of MediaModels whose query is equal to the 
given mediaQuery. Each Media Model will contain { query, model }

**Kind**: inner method of [<code>MediaSelectorModel</code>](#module_MediaSelectorModel)  
<a name="module_MediaSelectorModel..add"></a>

### MediaSelectorModel~add()
This will make a shallow copy of the current MediaSelector
and add the media query and model to the copy.

**Kind**: inner method of [<code>MediaSelectorModel</code>](#module_MediaSelectorModel)  
<a name="module_MediaSelectorModel..remove"></a>

### MediaSelectorModel~remove()
This will make a shallow copy of the current MediaSelector
and remove all the media queries / models from the copy
that have the appropriate mediaQuery

**Kind**: inner method of [<code>MediaSelectorModel</code>](#module_MediaSelectorModel)  
<a name="module_MediaSelectorModel..update"></a>

### MediaSelectorModel~update()
Updates the model to the current version, including all submodels

**Kind**: inner method of [<code>MediaSelectorModel</code>](#module_MediaSelectorModel)  
<a name="module_PropertiesModel"></a>

## PropertiesModel
<a name="module_PropGenerators"></a>

## PropGenerators
<a name="module_VariantStyleModel"></a>

## VariantStyleModel
The VariantStyleModel is normally the root model of a style tree.
It supports variants and subvariants, each with their own model. The
VariantStyleModel also support per variant props that inherit from
the parent and default variants. Often, the style model for each
variant will be a MediaSelectorModel


* [VariantStyleModel](#module_VariantStyleModel)
    * [~getVariants()](#module_VariantStyleModel..getVariants)
    * [~setVariant(model, variant, variantStyle, props, replace)](#module_VariantStyleModel..setVariant) ⇒ <code>VariantStyleModel</code>
    * [~removeVariant()](#module_VariantStyleModel..removeVariant)
    * [~renameVariant()](#module_VariantStyleModel..renameVariant)
    * [~setVariantParent()](#module_VariantStyleModel..setVariantParent)
    * [~setVariantProps(model, variant, props)](#module_VariantStyleModel..setVariantProps)
    * [~toProps()](#module_VariantStyleModel..toProps)
    * [~toHierarchy()](#module_VariantStyleModel..toHierarchy)
    * [~getVariantProps()](#module_VariantStyleModel..getVariantProps)
    * [~getParentVariant()](#module_VariantStyleModel..getParentVariant)
    * [~toJs()](#module_VariantStyleModel..toJs)
    * [~update()](#module_VariantStyleModel..update)
    * [~Variant](#module_VariantStyleModel..Variant) : <code>Object</code>
    * [~VariantStyleModel](#module_VariantStyleModel..VariantStyleModel) : <code>Object</code>

<a name="module_VariantStyleModel..getVariants"></a>

### VariantStyleModel~getVariants()
Returns all the variants in the model

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..setVariant"></a>

### VariantStyleModel~setVariant(model, variant, variantStyle, props, replace) ⇒ <code>VariantStyleModel</code>
This will make a shallow copy of the model and create
a new VariantModel with the given variant name and style.
If the variant name is not a string of the correct format,
an Error will be thrown. If a VariantModel of specified name
already exists, it will be replaced by the new model if the
replace argument is equal to true. Otherwise an error will be
thrown.

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>VariantStyleModel</code> | the model to copy |
| variant | <code>string</code> | the name of the variant |
| variantStyle | <code>variantStyle</code> | the style model to use for the variant |
| props | <code>object</code> \| <code>boolean</code> | the non css props for the variant. If this is a a boolean, it is treated as the replace option |
| replace | <code>boolean</code> | if true, this will overwrite a variant with the same name |

<a name="module_VariantStyleModel..removeVariant"></a>

### VariantStyleModel~removeVariant()
This will make a shallow copy of the model with the
specified variant removed. If the variant doesnt exist,
model will be returned

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..renameVariant"></a>

### VariantStyleModel~renameVariant()
This will make a shallow copy of the model with the
specified variant renamed. If the variant doesnt exist,
model will be returned

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..setVariantParent"></a>

### VariantStyleModel~setVariantParent()
This will make a shallow copy of the model with the
specified variant's parent set to the new value. If the 
variant doesnt exist, model will be returned. To clear
the parent, pass null. If a cycle is create by the addition of
parent, and error will be thrown

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..setVariantProps"></a>

### VariantStyleModel~setVariantProps(model, variant, props)
Sets the props of model's variant to props. If the variant
doesnt exist, this will throw an exception. This will create
shallow copy of the model with the change applied and return it

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>VariantStyleModel</code> | the model to apply the change |
| variant | <code>string</code> | the name of the variant |
| props | <code>object</code> | the new props |

<a name="module_VariantStyleModel..toProps"></a>

### VariantStyleModel~toProps()
Returns an object<variantName,object<string,any>> that has all the
variant props

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..toHierarchy"></a>

### VariantStyleModel~toHierarchy()
Returns an object<variantName,Array<String>> that has all the
variant's ancestors. The Array will contained variant class
names <baseName>-<variant>, as well as the <baseName>

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..getVariantProps"></a>

### VariantStyleModel~getVariantProps()
Returns the merged props for the variant

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..getParentVariant"></a>

### VariantStyleModel~getParentVariant()
Gets the parent variant of the given variant model. If variantModel
is the default variant, null is returned. If the specified parent
does not exist, the default variant is returned.

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..toJs"></a>

### VariantStyleModel~toJs()
Returns a string that is suitable for writing to a .js file

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..update"></a>

### VariantStyleModel~update()
Updates the model to the current version, including all submodels

**Kind**: inner method of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
<a name="module_VariantStyleModel..Variant"></a>

### VariantStyleModel~Variant : <code>Object</code>
**Kind**: inner typedef of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| variant | <code>string</code> | the name of the component |
| parent | <code>string</code> | the name of the parent variant or null. |
| style | <code>object</code> | the style model for the variant |
| props | <code>object</code> | the props for the variant |

<a name="module_VariantStyleModel..VariantStyleModel"></a>

### VariantStyleModel~VariantStyleModel : <code>Object</code>
**Kind**: inner typedef of [<code>VariantStyleModel</code>](#module_VariantStyleModel)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| baseName | <code>string</code> | the name of the component |
| variants | <code>array.&lt;Variant&gt;</code> | the variants of the style |

<a name="JssCreator"></a>

## JssCreator
A helper class to create a Jss map for

**Kind**: global class  

* [JssCreator](#JssCreator)
    * [.add(cssProperties, selector)](#JssCreator+add)
    * [.addFromModel(model, spec, opts)](#JssCreator+addFromModel)
    * [.addClasses()](#JssCreator+addClasses)
    * [.getLocalClasses()](#JssCreator+getLocalClasses)

<a name="JssCreator+add"></a>

### jssCreator.add(cssProperties, selector)
This will merge the properties into the Jss object for the given selector

**Kind**: instance method of [<code>JssCreator</code>](#JssCreator)  

| Param | Type | Description |
| --- | --- | --- |
| cssProperties | <code>object</code> | the jss attributes |
| selector | <code>string</code> | the selector, relative to the baseClass variant, that indicates where to put the attributes. |

<a name="JssCreator+addFromModel"></a>

### jssCreator.addFromModel(model, spec, opts)
This will generate jss properties from the model
using the given spec.

**Kind**: instance method of [<code>JssCreator</code>](#JssCreator)  

| Param | Type | Description |
| --- | --- | --- |
| model | <code>object</code> | the data model holding css property models |
| spec | [<code>Array.&lt;Spec&gt;</code>](#Spec) | the spec of how to extract fields from the model and apply them to the jss object. This will use PropertyGenerator to generate the jss attributes |
| opts | <code>object</code> | the options passed to PropertyGenerator along with the attribute model |

<a name="JssCreator+addClasses"></a>

### jssCreator.addClasses()
Makes sure that the classes exist in the jss

**Kind**: instance method of [<code>JssCreator</code>](#JssCreator)  
<a name="JssCreator+getLocalClasses"></a>

### jssCreator.getLocalClasses()
Parses the selector, and returns the local class references

**Kind**: instance method of [<code>JssCreator</code>](#JssCreator)  
<a name="varTypes"></a>

## varTypes
Used to decide whether or a value can be referenced
as a less/css variable

**Kind**: global constant  
<a name="setColor"></a>

## setColor()
Creates a shallow copy of the model, sets its color,
and returns the copy

**Kind**: global function  
<a name="setClearLayers"></a>

## setClearLayers()
Creates a shallow copy of the model, sets its clearLayers,
and returns the copy

**Kind**: global function  
<a name="setLayer"></a>

## setLayer()
Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown

**Kind**: global function  
<a name="addLayer"></a>

## addLayer()
Creates a shallow copy of the model, and adds the layer

**Kind**: global function  
<a name="swapLayers"></a>

## swapLayers()
Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="removeLayer"></a>

## removeLayer()
Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="setClearLayers"></a>

## setClearLayers()
Creates a shallow copy of the model, sets its clearLayers,
and returns the copy

**Kind**: global function  
<a name="setLayer"></a>

## setLayer()
Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown

**Kind**: global function  
<a name="addLayer"></a>

## addLayer()
Creates a shallow copy of the model, and adds the layer

**Kind**: global function  
<a name="swapLayers"></a>

## swapLayers()
Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="removeLayer"></a>

## removeLayer()
Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="setClearLayers"></a>

## setClearLayers()
Creates a shallow copy of the model, sets its clearLayers,
and returns the copy

**Kind**: global function  
<a name="setLayer"></a>

## setLayer()
Creates a shallow copy of the model, and sets the layer at the
specified index. If index is out of bouds, an error is thrown

**Kind**: global function  
<a name="addLayer"></a>

## addLayer()
Creates a shallow copy of the model, and adds the layer

**Kind**: global function  
<a name="swapLayers"></a>

## swapLayers()
Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="removeLayer"></a>

## removeLayer()
Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="create"></a>

## create()
{ type : 'transform',
    clear : true | false,
    fucntions : [
    ]
  }

**Kind**: global function  
<a name="setClear"></a>

## setClear()
Creates a shallow copy of the model, sets its clearLayers,
and returns the copy

**Kind**: global function  
<a name="setFunction"></a>

## setFunction()
Creates a shallow copy of the model, and sets the function at the
specified index. If index is out of bouds, an error is thrown

**Kind**: global function  
<a name="addFunction"></a>

## addFunction()
Creates a shallow copy of the model, and adds the layer

**Kind**: global function  
<a name="swapFunctions"></a>

## swapFunctions()
Creates a shallow copy of the model, and swaps the layers.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="removeFunction"></a>

## removeFunction()
Creates a shallow copy of the model, and removes the layer.
An error is thrown if the indices are out of bounds

**Kind**: global function  
<a name="create"></a>

## create()
{ type : 'transition',
    clear : true | false,
    properties : {
      name : { duration, timingFunction, delay }
    }}

**Kind**: global function  
<a name="setClear"></a>

## setClear()
Creates a shallow copy of the model, sets its clearLayers,
and returns the copy

**Kind**: global function  
<a name="setTransition"></a>

## setTransition()
Creates a shallow copy of the model, and sets the property.

**Kind**: global function  
<a name="removeTransition"></a>

## removeTransition()
Creates a shallow copy of the model, and removes the property.

**Kind**: global function  
<a name="update"></a>

## update()
Creates a shallow copy of the model, and removes the property.

**Kind**: global function  
<a name="updateDuration"></a>

## updateDuration()
Creates a shallow copy of the model, and sets the duration for the name.

**Kind**: global function  
<a name="updateDelay"></a>

## updateDelay()
Creates a shallow copy of the model, and sets the delay for the name.

**Kind**: global function  
<a name="updateTiming"></a>

## updateTiming()
Creates a shallow copy of the model, and sets the duration for the name.

**Kind**: global function  
<a name="addModel"></a>

## addModel(type, modelFunctions)
This will register the modelFunctions as a CssGenerator and
a VersionUpdater

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | the type of the model |
| modelFunctions | <code>object</code> | the object that contains toJss(), needsUpdate(), update(), and create() functions |

<a name="isOldVersion"></a>

## isOldVersion(model, currentVersion, dVersion)
Returns true if the model's version is not equal to the model's version.

**Kind**: global function  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| model | <code>object</code> |  | the model to examine |
| currentVersion | <code>number</code> |  | the current expected version |
| dVersion | <code>number</code> | <code>1</code> | the version to use if model.version is undefined (default is 1) |

<a name="isThemeVar"></a>

## isThemeVar()
Returns true if v matches the theme var format

**Kind**: global function  
<a name="isThemeVarType"></a>

## isThemeVarType()
Returns true if v matches the theme var format and is of the type

**Kind**: global function  
<a name="filterThemeVars"></a>

## filterThemeVars()
Removes vars that are not of the specified type

**Kind**: global function  
<a name="resolve"></a>

## resolve()
Looks at model.extend to find an immediate parent
and merges the model and extended model. It then 
proceeds to resolve all the keys in the merged object.
This is shallow and only works at the model's key level

**Kind**: global function  
<a name="createSetValue"></a>

## createSetValue(key, [create])
This will return a function (model, value) that makes a shallow copy of 
of the model and sets the value on model[key]. If model is null and create
is supplied, this will call create to make a model

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | the name of the attribute that we are making a copy of |
| [create] | <code>function</code> | a model creator method |

<a name="mergeJss"></a>

## mergeJss()
This will take the css/jss properties and merge them into
the baseJss with the given selector and variant

**Kind**: global function  
<a name="Spec"></a>

## Spec
**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| selectors | <code>string</code> \| <code>Array.&lt;string&gt;</code> | defines where the attributes will  be applied in the jss object |
| paths | <code>string</code> \| <code>Array.&lt;string&gt;</code> | the locations of the attribute models in the main model that will be applied to the selectors |
| static | <code>object</code> | an object that defines static rules to apply to the selector |
| [property] | <code>string</code> \| <code>function</code> | if present and a string, this will apply the value at the path to property named by the string. If this is a function, it will be invoked with ( mdl, { selector, path, options, model } ). If an object is returned, it will be applied to the selector |

