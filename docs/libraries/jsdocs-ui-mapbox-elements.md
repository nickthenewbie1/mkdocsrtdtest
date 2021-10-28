---
id: jsdocs-ui-mapbox-elements
title: UI Mapbox Elements
---
## Classes

<dl>
<dt><a href="#GeoshapeAdapter">GeoshapeAdapter</a></dt>
<dd><p>This should be derived from and supplied to the GeoshapeController
to perform actions related to creating, updating, and display
geoshapes on the map</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#SATELLITE">SATELLITE</a></dt>
<dd><p>This file is used to control the types and url of the mapboxs imagery.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#url">url(style)</a> ⇒</dt>
<dd><p>Returns the mapbox url for the given style</p>
</dd>
<dt><a href="#next">next(style)</a> ⇒</dt>
<dd><p>Returns the next style, assuming the types exist in a list</p>
</dd>
<dt><a href="#init">init(options)</a></dt>
<dd><p>Sets the options for the style.</p>
</dd>
<dt><a href="#create">create()</a></dt>
<dd><p>Returns a Symbolizer that will return { symbol, layer } where
symbol is the name or <name>-<targeted | selected | rollover>
if the data item is targeted, selected or rolled over</p>
</dd>
<dt><a href="#addImage">addImage(name, imageOptions)</a></dt>
<dd><p>Adds an image to the Symbols</p>
</dd>
<dt><a href="#addAlias">addAlias()</a></dt>
<dd><p>Adds an alias. Any references to name will be redirected
to the param mapsTo</p>
</dd>
<dt><a href="#getImagesArray">getImagesArray()</a></dt>
<dd><p>Reorganizes this.images into [ [name0, image0], ..., [nameN, imageN]]
for mapbox</p>
</dd>
<dt><a href="#getLayers">getLayers()</a></dt>
<dd><p>Returns a array of layers to render. Because Mapbox cannot control the line properties
of a filled shape very well, this will create two separate layers per geoshape, one for
the fill and selection, on for the outline.</p>
</dd>
<dt><a href="#getLayers">getLayers(sourceMap)</a></dt>
<dd><p>Returns an object { normal : [ <Layers> ], rollover : [ <Layers> ] }</p>
</dd>
<dt><a href="#getPosition">getPosition(data)</a></dt>
<dd><p>Returns the position array [longitude, latitude] for the given data. By default
this will use the Path access objects to get the position</p>
</dd>
<dt><a href="#getLayerNames">getLayerNames()</a></dt>
<dd><p>Returns the layer names that will be generated. Useful for supplying to 
selectableLayerIds or rolloverableLayersIds to set what types can be clicked
or rolled over.</p>
</dd>
<dt><a href="#getLayers">getLayers(dataList, options)</a> ⇒</dt>
<dd><p>This will return a set of layers used to represent the dataList</p>
</dd>
</dl>

<a name="GeoshapeAdapter"></a>

## GeoshapeAdapter
This should be derived from and supplied to the GeoshapeController
to perform actions related to creating, updating, and display
geoshapes on the map

**Kind**: global class  

* [GeoshapeAdapter](#GeoshapeAdapter)
    * [.addShape(shape)](#GeoshapeAdapter+addShape) ⇒ <code>Promise(Shape)</code>
    * [.updateShape(shape)](#GeoshapeAdapter+updateShape) ⇒ <code>Promise</code>

<a name="GeoshapeAdapter+addShape"></a>

### geoshapeAdapter.addShape(shape) ⇒ <code>Promise(Shape)</code>
Called when a new shape should be added to the data source

**Kind**: instance method of [<code>GeoshapeAdapter</code>](#GeoshapeAdapter)  

| Param | Type | Description |
| --- | --- | --- |
| shape | <code>object</code> | the shape to add to the data source. Returned from createShape |

<a name="GeoshapeAdapter+updateShape"></a>

### geoshapeAdapter.updateShape(shape) ⇒ <code>Promise</code>
Update a shape should be added to the data source

**Kind**: instance method of [<code>GeoshapeAdapter</code>](#GeoshapeAdapter)  

| Param | Type | Description |
| --- | --- | --- |
| shape | <code>object</code> | the shape to add to the data source. Returned from createShape |

<a name="SATELLITE"></a>

## SATELLITE
This file is used to control the types and url of the mapboxs imagery.

**Kind**: global constant  
<a name="url"></a>

## url(style) ⇒
Returns the mapbox url for the given style

**Kind**: global function  
**Returns**: the mapbox url for the style, or for vector if 
the style is unknown  

| Param | Type | Description |
| --- | --- | --- |
| style | <code>string</code> | either SATELLITE or VECTOR |

<a name="next"></a>

## next(style) ⇒
Returns the next style, assuming the types exist in a list

**Kind**: global function  
**Returns**: the next style, or for VECTOR if the style is unknown  

| Param | Type | Description |
| --- | --- | --- |
| style | <code>string</code> | either SATELLITE or VECTOR |

<a name="init"></a>

## init(options)
Sets the options for the style.

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> |  |
| options.styles | <code>object</code> |  |
| options.styles.<STYLE | <code>string</code> | KEY> the mapbox url for the style |

<a name="create"></a>

## create()
Returns a Symbolizer that will return { symbol, layer } where
symbol is the name or <name>-<targeted | selected | rollover>
if the data item is targeted, selected or rolled over

**Kind**: global function  
<a name="addImage"></a>

## addImage(name, imageOptions)
Adds an image to the Symbols

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | the name of the symbol |
| imageOptions | <code>object</code> |  |
| imageOptions.src | <code>string</code> | the source of the image |
| imageOptions.width | <code>int</code> | the width to scale the image to |
| imageOptions.height | <code>int</code> | the height to scale the image to |

<a name="addAlias"></a>

## addAlias()
Adds an alias. Any references to name will be redirected
to the param mapsTo

**Kind**: global function  
<a name="getImagesArray"></a>

## getImagesArray()
Reorganizes this.images into [ [name0, image0], ..., [nameN, imageN]]
for mapbox

**Kind**: global function  
<a name="getLayers"></a>

## getLayers()
Returns a array of layers to render. Because Mapbox cannot control the line properties
of a filled shape very well, this will create two separate layers per geoshape, one for
the fill and selection, on for the outline.

**Kind**: global function  
<a name="getLayers"></a>

## getLayers(sourceMap)
Returns an object { normal : [ <Layers> ], rollover : [ <Layers> ] }

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| sourceMap | <code>object</code> | this supplies information that can be used to render the lines. The keys of this objects match the keys in the pointsMap. The default linePaint  will look for lineColor in the object at this key to determine the color of the lines specified by the objects in Array at pointsMap[key] |

<a name="getPosition"></a>

## getPosition(data)
Returns the position array [longitude, latitude] for the given data. By default
this will use the Path access objects to get the position

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>object</code> | the data object |

<a name="getLayerNames"></a>

## getLayerNames()
Returns the layer names that will be generated. Useful for supplying to 
selectableLayerIds or rolloverableLayersIds to set what types can be clicked
or rolled over.

**Kind**: global function  
<a name="getLayers"></a>

## getLayers(dataList, options) ⇒
This will return a set of layers used to represent the dataList

**Kind**: global function  
**Returns**: and object container normal, rollover, selected, targeted fields that
hold Layer objects  

| Param | Type | Description |
| --- | --- | --- |
| dataList | <code>array</code> | the objects to render |
| options | <code>object</code> |  |
| options.symbolizer | <code>object</code> | function( data, { selected, targeted, rollover } )) |
| options.selected | <code>object</code> | the selected data |
| options.targeted | <code>object</code> | the targeted data for the dataList |
| options.rollover | <code>object</code> | the rollover data for the dataList |
| options.isSelectable | <code>object</code> | true if the objects should be selectable |
| options.isRolloverable | <code>object</code> | true if the objects should be rolloverable |

