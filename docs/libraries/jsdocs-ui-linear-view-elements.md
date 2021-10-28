---
id: jsdocs-ui-linear-view-elements
title: UI Linear View Elements
---
## Classes

<dl>
<dt><a href="#Projection">Projection</a></dt>
<dd><p>class that calculates a pixel width based off of elapsed time</p>
</dd>
<dt><a href="#Block">Block</a></dt>
<dd><p>React class that renders a block with a set position and width, one of the main visual elements of the ghant chart</p>
</dd>
<dt><a href="#LinearView">LinearView</a></dt>
<dd><p>React class that renders the main veiw of the ghant chart
Props:</p>
</dd>
<dt><a href="#MomentBackground">MomentBackground</a></dt>
<dd><p>react class that renders header cells</p>
</dd>
<dt><a href="#MomentHeader">MomentHeader</a></dt>
<dd><p>Params</p>
</dd>
<dt><a href="#Row">Row</a></dt>
<dd><p>react class to render a ghant chart row</p>
</dd>
</dl>

<a name="Projection"></a>

## Projection
class that calculates a pixel width based off of elapsed time

**Kind**: global class  
<a name="new_Projection_new"></a>

### new Projection(pixelValue, startValue, stopValue)

| Param | Type | Description |
| --- | --- | --- |
| pixelValue | <code>number</code> | the base unit of time for one pixel |
| startValue | <code>number</code> | start of the block |
| stopValue | <code>number</code> | end of the block |

<a name="Block"></a>

## Block
React class that renders a block with a set position and width, one of the main visual elements of the ghant chart

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| x1 | <code>number</code> | starting x value of the element |
| x2 | <code>number</code> | ending x value of the element |
| onRollover | <code>function</code> | rollover functionality |
| onClick | <code>function</code> | onClick functionality |
| data | <code>any</code> | added to the rollover and click function callbacks |
| className | <code>string</code> | class to be applied to the element |
| style | <code>object</code> | css properties to be applied to the element |
| children | <code>node</code> | children to be rendered in the element |

<a name="LinearView"></a>

## LinearView
React class that renders the main veiw of the ghant chart
Props:

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| rowClass | <code>function</code> \| <code>string</code> | return className for rowData |
| blockClass | <code>function</code> \| <code>string</code> | return className for block |
| rowAccess | <code>function</code> | return array of rows from data |
| onClick | <code>function</code> | callback when a block is clicked |
| onClick | <code>function</code> | callback when a block is clicked |
| startAccess | <code>function</code> | returns start value from a block |
| stopAccess | <code>function</code> | returns stop value from a block |
| hScroll | <code>component</code> | custom horizontal scrollbar component |
| vScroll | <code>component</code> | custom vertical scrollbar component |
| blockStylizer | <code>function</code> | function( item, project, startValue stopValue, x1, x2 ) and returns { className, style, children } options for the block. Good for dynamic styling |
| setScrollTop | <code>function</code> | function to be used to set the scrollTop value of the element |

<a name="MomentBackground"></a>

## MomentBackground
react class that renders header cells

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| projection | <code>projection</code> | the projection used to create the header |
| unit | <code>string</code> | the unit used to calculate the group. 'day', 'month', etc |
| format | <code>string</code> | if present, moment.format( format ) will be used to create the label |
| dynamicClass | <code>function</code> | if present, this function will be invoked with dynamicClass( moment, width, left, right ) and should return a className to add to the cell. |
| className | <code>string</code> | the className to apply to the background |
| cellClassName | <code>string</code> | the className to apply to each cell |

<a name="MomentHeader"></a>

## MomentHeader
Params

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| projection | <code>projection</code> | the projection used to create the header |
| unit | <code>string</code> | the unit used to calculate the group. 'day', 'month', etc |
| format | <code>string</code> | if present, moment.format( format ) will be used to create the label |
| value | <code>string</code> \| <code>function</code> | if this is a function, it will be invoked with value( moment, width, left, right ) and the function should return a string | component for the label. If value is a string, moment[value]() will be invoked (ie 'date' will return the day of the month) |
| className | <code>string</code> | the className for the label |
| clip | <code>boolean</code> | if true, the positions of the header cell will be clipped to the projection time. This is useful for left or right aligning labels like month |
| className | <code>string</code> | the className to apply to the header |
| cellClassName | <code>string</code> | the className to apply to each cell |

<a name="Row"></a>

## Row
react class to render a ghant chart row

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| onRollover | <code>function</code> | rollover functionality |
| onClick | <code>function</code> | onClick functionality |
| rowData | <code>any</code> | added to the rollover and click function callbacks |
| className | <code>string</code> | class to be applied to the element |
| style | <code>object</code> | css properties to be applied to the element |
| blockAccess | <code>function</code> | accessor to get block data from row data |
| startAccess | <code>function</code> | accessor to get the start time from the data |
| stopAccess | <code>function</code> | accessor to get the stop time from the data |
| blockStylizer | <code>function</code> | calculates the style for the block |
| blockClass | <code>string</code> | class to be applied to the blocks |
| projection | [<code>Projection</code>](#Projection) | instance of the projection class |

