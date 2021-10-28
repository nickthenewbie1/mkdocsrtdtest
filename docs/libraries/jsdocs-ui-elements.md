---
id: jsdocs-ui-elements
title: UI Elements
---
## Classes

<dl>
<dt><a href="#ResourceTheme">ResourceTheme</a></dt>
<dd><p>the resource theme checks elements props and validates them against their theme, and will make some overrides based off props porvided from ui-builder</p>
</dd>
<dt><a href="#ScrollSync">ScrollSync</a></dt>
<dd><p>Sends events between multiple components to allow them to scroll in
unison.</p>
<ul>
<li>To use, create a ScrollSync in the constructor of your component.</li>
<li>In componentDidMount(), call this.scrollSync.start(), </li>
<li>In componentWillUnmount(), call this.scrollSync.stop()</li>
<li>Call this.scrollSync.onScroll( event ) when your local component scrolls.</li>
<li>The onRemoteScroll function given in the ScrollSync&#39;s constructor should 
immediately set the scroll position of your component as desired.</li>
</ul>
</dd>
<dt><a href="#AbstractFilterController">AbstractFilterController</a></dt>
<dd></dd>
<dt><a href="#FilterController">FilterController</a></dt>
<dd></dd>
<dt><a href="#AbstractSortController">AbstractSortController</a></dt>
<dd></dd>
<dt><a href="#SortController">SortController</a></dt>
<dd></dd>
<dt><a href="#Breadcrumbs">Breadcrumbs</a></dt>
<dd><p>React class that renders a button</p>
</dd>
<dt><a href="#Button">Button</a></dt>
<dd><p>React class that renders a button</p>
</dd>
<dt><a href="#Checkbox">Checkbox</a></dt>
<dd><p>Checkbox - React class that renders a checkbox</p>
</dd>
<dt><a href="#Combobox">Combobox</a></dt>
<dd><p>React class that renders a dropdown element and allows for the selection of one item</p>
</dd>
<dt><a href="#Content">Content</a></dt>
<dd><p>has a header, content and footer.</p>
</dd>
<dt><a href="#DataBlock">DataBlock</a></dt>
<dd><p>renders a column or row seperated title and data format</p>
</dd>
<dt><a href="#DateTimePicker">DateTimePicker</a></dt>
<dd><p>React class that renders a date time picker</p>
</dd>
<dt><a href="#DateTimeRangePicker">DateTimeRangePicker</a></dt>
<dd><p>React class that renders a date range picker</p>
</dd>
<dt><a href="#Dialog">Dialog</a></dt>
<dd><p>React class that renders a popup with a message or a question</p>
</dd>
<dt><a href="#Message">Message</a></dt>
<dd><p>React class to render a dialog message</p>
</dd>
<dt><a href="#Question">Question</a></dt>
<dd><p>React class to render a Dialog question</p>
</dd>
<dt><a href="#Dropdown">Dropdown</a></dt>
<dd><p>React class that renders a dropdown element and allows for the selection of one item</p>
</dd>
<dt><a href="#Flex">Flex</a></dt>
<dd><p>React class that renders a div with display flex</p>
</dd>
<dt><a href="#Header">Header</a></dt>
<dd><p>React class that renders a Hx html tag</p>
</dd>
<dt><a href="#Label">Label</a></dt>
<dd><p>React class that renders a label element</p>
</dd>
<dt><a href="#Item">Item</a></dt>
<dd><p>The Item represents a clickable and/or selectable element in the List. An
Item that supplies an item prop is selectable and clickable. An Item that 
supplies an eventData prop without an item prop will be clickable but not
selectable.</p>
</dd>
<dt><a href="#Dynamic">Dynamic</a></dt>
<dd><p>This takes an items array and a factory and produces item elements for the list.
The Factory.create() will be called with an item and props ( onClick, onEvent, selected )
and should return a List.Item (if the item should be selectable/clickable) or other
React component</p>
</dd>
<dt><a href="#List">List</a></dt>
<dd><p>React class that renders a List element</p>
</dd>
<dt><a href="#SingleSelector">SingleSelector</a></dt>
<dd><p>The SingleSelector will manage a state variable in you&#39;re controlling components
state. This will allow at most one item to be selected. Meta-click will unselect
a selected item.</p>
</dd>
<dt><a href="#MultiSelector">MultiSelector</a></dt>
<dd><p>The MultiSelector will manage a state variable in you&#39;re controlling components
state. This will allow multiple items to be selected. Meta-click will unselect
a selected item.</p>
</dd>
<dt><a href="#Login">Login</a></dt>
<dd><p>React login widget with several input and methods</p>
</dd>
<dt><a href="#MultiSelect">MultiSelect</a></dt>
<dd><p>React class that renders a multiselect widget</p>
</dd>
<dt><a href="#NumericInput">NumericInput</a></dt>
<dd><p>React class that renders an Input that only accepts numbers</p>
</dd>
<dt><a href="#Pane">Pane</a></dt>
<dd><p>React class that renders a pane</p>
</dd>
<dt><a href="#Item">Item</a></dt>
<dd><p>react class that renders an anchor tag with an onClick</p>
</dd>
<dt><a href="#Popup">Popup</a></dt>
<dd><p>React class to render a popup</p>
</dd>
<dt><a href="#RadioButton">RadioButton</a></dt>
<dd><p>Creates a Radio button element in react</p>
</dd>
<dt><a href="#ResetPassword">ResetPassword</a></dt>
<dd><p>React class that renders a widget to reset a user&#39;s password</p>
</dd>
<dt><a href="#Slider">Slider</a></dt>
<dd><p>React class that renders a Slider</p>
</dd>
<dt><a href="#SplitPane">SplitPane</a></dt>
<dd><p>React class that renders a SplitPane</p>
</dd>
<dt><a href="#Table">Table</a></dt>
<dd><p>React class that renders a table</p>
</dd>
<dt><a href="#Tab">Tab</a></dt>
<dd><p>react class to render a tab for the tab pane</p>
</dd>
<dt><a href="#TabPane">TabPane</a></dt>
<dd><p>React class for a component with as many tabs as desired. manages which tab is displayed</p>
</dd>
<dt><a href="#Text">Text</a></dt>
<dd><p>React class to render a block of text</p>
</dd>
<dt><a href="#TextArea">TextArea</a></dt>
<dd><p>React class to render a block of text</p>
</dd>
<dt><a href="#TextInput">TextInput</a></dt>
<dd><p>This TextInput field will allow you to install a function
to prohibit keys, validate the input, and to fire changes
only on a carriage return or blur.</p>
</dd>
<dt><a href="#ToggleButton">ToggleButton</a></dt>
<dd><p>React class that renders a button with an on and an off state</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#create">create()</a></dt>
<dd></dd>
<dt><a href="#classes">classes(component, type, variant, ...rest)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the classnames needed for the component&#39;s type and variant.</p>
</dd>
<dt><a href="#subclasses">subclasses(component, type, ...rest)</a> ⇒ <code>string</code></dt>
<dd><p>Returns the classnames needed for the component&#39;s sub element. The variant
is not needed here because it will be in the css rule as a parent.</p>
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
<dt><a href="#renderLayout">renderLayout(theme, layout, children)</a></dt>
<dd><p>Renders the layouts</p>
</dd>
<dt><a href="#ensureHierarchy">ensureHierarchy(theme, results, parents, options, name)</a></dt>
<dd><p>Makes sure that the parent layouts have been created and are in the
layout children arrays or the top level results array</p>
</dd>
<dt><a href="#createSublayouts">createSublayouts(elem)</a></dt>
<dd><p>Creates React elements from the sublayout object</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#FormData">FormData</a></dt>
<dd></dd>
</dl>

<a name="ResourceTheme"></a>

## ResourceTheme
the resource theme checks elements props and validates them against their theme, and will make some overrides based off props porvided from ui-builder

**Kind**: global class  

* [ResourceTheme](#ResourceTheme)
    * [.classes(componentType, type, variant, ...rest)](#ResourceTheme+classes) ⇒ <code>string</code>
    * [.subclasses(component, type, ...rest)](#ResourceTheme+subclasses) ⇒ <code>string</code>
    * [.props(component, variant)](#ResourceTheme+props) ⇒ <code>object</code>
    * [.variantClassNames(componentType, classes, variant)](#ResourceTheme+variantClassNames)

<a name="ResourceTheme+classes"></a>

### resourceTheme.classes(componentType, type, variant, ...rest) ⇒ <code>string</code>
Returns the classnames needed for the component's type and variant.

**Kind**: instance method of [<code>ResourceTheme</code>](#ResourceTheme)  
**Returns**: <code>string</code> - the classname  

| Param | Type | Description |
| --- | --- | --- |
| componentType | <code>string</code> | the name of the component type. eg "Button" |
| type | <code>string</code> | the part of the component to get. eg "button" |
| variant | <code>string</code> | the variant name to requsest. eg "small" |
| ...rest | <code>strings</code> | other strings to add to the classname |

<a name="ResourceTheme+subclasses"></a>

### resourceTheme.subclasses(component, type, ...rest) ⇒ <code>string</code>
Returns the classnames needed for the component's sub element. The variant
is not needed here because it will be in the css rule as a parent.

**Kind**: instance method of [<code>ResourceTheme</code>](#ResourceTheme)  
**Returns**: <code>string</code> - the classname  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| type | <code>string</code> | the sub-component of the component to get. eg "button" |
| ...rest | <code>strings</code> | other strings to add to the classname |

<a name="ResourceTheme+props"></a>

### resourceTheme.props(component, variant) ⇒ <code>object</code>
Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component's default props and the component's variant props.

If the second argument is an object, it is considered to be the
React component's actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( 'Checkbox', this.props )

**Kind**: instance method of [<code>ResourceTheme</code>](#ResourceTheme)  
**Returns**: <code>object</code> - an object containing the default props. This will be a 
merger of the default variant's props and the specified variants props. 
This will always return an object  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| variant | <code>string</code> \| <code>object</code> | the variant name to requsest. eg "small" |

<a name="ResourceTheme+variantClassNames"></a>

### resourceTheme.variantClassNames(componentType, classes, variant)
Turns the variant's hierarchy into a hashified set of classnames.

**Kind**: instance method of [<code>ResourceTheme</code>](#ResourceTheme)  

| Param | Type | Description |
| --- | --- | --- |
| componentType | <code>object</code> | the component type |
| classes | <code>object</code> | the jss classname lookup |
| variant | <code>string</code> | the component variant |

<a name="ScrollSync"></a>

## ScrollSync
Sends events between multiple components to allow them to scroll in
unison.
- To use, create a ScrollSync in the constructor of your component.
- In componentDidMount(), call this.scrollSync.start(), 
- In componentWillUnmount(), call this.scrollSync.stop()
- Call this.scrollSync.onScroll( event ) when your local component scrolls.
- The onRemoteScroll function given in the ScrollSync's constructor should 
immediately set the scroll position of your component as desired.

**Kind**: global class  

* [ScrollSync](#ScrollSync)
    * [new ScrollSync(options)](#new_ScrollSync_new)
    * [.onReceivedRemoteScroll](#ScrollSync+onReceivedRemoteScroll)
    * [.onScroll](#ScrollSync+onScroll)
    * [.start()](#ScrollSync+start)
    * [.stop()](#ScrollSync+stop)

<a name="new_ScrollSync_new"></a>

### new ScrollSync(options)
Create a ScrollSync


| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the options object |
| options.name | <code>string</code> | the name of the synchronization. Defaults to 'main' |
| options.onRemoteScroll | <code>function</code> | this function should set the scroll position of your component |

<a name="ScrollSync+onReceivedRemoteScroll"></a>

### scrollSync.onReceivedRemoteScroll
Private function that listens to events. This will call the onRemoteScroll
if the sync is not locked

**Kind**: instance property of [<code>ScrollSync</code>](#ScrollSync)  
<a name="ScrollSync+onScroll"></a>

### scrollSync.onScroll
Call this when your local scroll region updates

**Kind**: instance property of [<code>ScrollSync</code>](#ScrollSync)  
<a name="ScrollSync+start"></a>

### scrollSync.start()
Call this in componentDidMount()

**Kind**: instance method of [<code>ScrollSync</code>](#ScrollSync)  
<a name="ScrollSync+stop"></a>

### scrollSync.stop()
Call this in componentWillUnmount()

**Kind**: instance method of [<code>ScrollSync</code>](#ScrollSync)  
<a name="AbstractFilterController"></a>

## AbstractFilterController
**Kind**: global class  
<a name="new_AbstractFilterController_new"></a>

### new AbstractFilterController()
Generic filtering class

<a name="FilterController"></a>

## FilterController
**Kind**: global class  

* [FilterController](#FilterController)
    * [new FilterController(component, stateKey, options)](#new_FilterController_new)
    * [.key(column)](#FilterController+key) ⇒ <code>string</code>
    * [.isColumnFiltered(column)](#FilterController+isColumnFiltered) ⇒ <code>boolean</code>
    * [.filter(data, columns)](#FilterController+filter)
    * [.applyFilters(data, columns, filterModel)](#FilterController+applyFilters)
    * [.getFilterValue(column)](#FilterController+getFilterValue)
    * [.add(column, value)](#FilterController+add)

<a name="new_FilterController_new"></a>

### new FilterController(component, stateKey, options)
Filtering class which can filter multiple columns and stores its
filtering state on the state of a provided React component


| Param | Type | Description |
| --- | --- | --- |
| component | <code>React.Component</code> | Parent component where filtering state changes will be managed |
| stateKey | <code>string</code> | The key within the parent component's state where filtering state will be stored. |
| options | <code>Object</code> | idKey - The key within the column object to find the column's id                           idFunc - A function that returns a column's id |

<a name="FilterController+key"></a>

### filterController.key(column) ⇒ <code>string</code>
Returns a unique id key for the given column

**Kind**: instance method of [<code>FilterController</code>](#FilterController)  
**Returns**: <code>string</code> - - The id key for the column  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column object for which to return a key |

<a name="FilterController+isColumnFiltered"></a>

### filterController.isColumnFiltered(column) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>FilterController</code>](#FilterController)  
**Returns**: <code>boolean</code> - - Whether or not the column is filtered  

| Param | Type |
| --- | --- |
| column | <code>Object</code> | 

<a name="FilterController+filter"></a>

### filterController.filter(data, columns)
Filters the tabular data. By default uses String.includes

**Kind**: instance method of [<code>FilterController</code>](#FilterController)  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>Array</code> | The table data |
| columns | <code>Array</code> | The table columns |

<a name="FilterController+applyFilters"></a>

### filterController.applyFilters(data, columns, filterModel)
**Kind**: instance method of [<code>FilterController</code>](#FilterController)  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>Array</code> | The table data |
| columns | <code>Array</code> | The table columns |
| filterModel | <code>Object</code> | The stored filter model in the form of an object with column                          id keys and filter values |

<a name="FilterController+getFilterValue"></a>

### filterController.getFilterValue(column)
Returns the current filter value for the column

**Kind**: instance method of [<code>FilterController</code>](#FilterController)  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column for which to get the filter value. |

<a name="FilterController+add"></a>

### filterController.add(column, value)
Updates the filter model state

**Kind**: instance method of [<code>FilterController</code>](#FilterController)  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column to filter |
| value | <code>string</code> \| <code>number</code> | The value to filter on |

<a name="AbstractSortController"></a>

## AbstractSortController
**Kind**: global class  
<a name="new_AbstractSortController_new"></a>

### new AbstractSortController()
Generic sorting class

<a name="SortController"></a>

## SortController
**Kind**: global class  

* [SortController](#SortController)
    * [new SortController(component, stateKey, options)](#new_SortController_new)
    * [.key(column)](#SortController+key) ⇒ <code>string</code>
    * [.isColumnSorted(column)](#SortController+isColumnSorted) ⇒ <code>boolean</code>
    * [.sort(data, columns, [sortOverride])](#SortController+sort)
    * [.getSortDirection(column)](#SortController+getSortDirection) ⇒ <code>string</code>
    * [.set(column, [direciton])](#SortController+set)

<a name="new_SortController_new"></a>

### new SortController(component, stateKey, options)
Sorting class which sorts one column at a time and stores its sort state on the state
of a provided React component.


| Param | Type | Description |
| --- | --- | --- |
| component | <code>React.Component</code> | Parent component where sorting state changes will be managed |
| stateKey | <code>string</code> | The key within the parent component's state where sorting state will be stored. |
| options | <code>Object</code> | idKey - The key within the column object to find the column's id                           idFunc - A function that returns a column's id |

<a name="SortController+key"></a>

### sortController.key(column) ⇒ <code>string</code>
* Returns a unique id key for the given column

**Kind**: instance method of [<code>SortController</code>](#SortController)  
**Returns**: <code>string</code> - - The id key for the column  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column object for which to return a key |

<a name="SortController+isColumnSorted"></a>

### sortController.isColumnSorted(column) ⇒ <code>boolean</code>
**Kind**: instance method of [<code>SortController</code>](#SortController)  
**Returns**: <code>boolean</code> - - Whether or not the column is sorted  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column object |

<a name="SortController+sort"></a>

### sortController.sort(data, columns, [sortOverride])
Sorts the tabular data based on established sort model using

**Kind**: instance method of [<code>SortController</code>](#SortController)  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>Array</code> | The table data |
| columns | <code>Array</code> | The table columns |
| [sortOverride] | <code>function</code> | An override function to be used for sorting. Method signature is itemA, itemB, accessor |

<a name="SortController+getSortDirection"></a>

### sortController.getSortDirection(column) ⇒ <code>string</code>
Returns the direction that a given column is sorted based on sort state

**Kind**: instance method of [<code>SortController</code>](#SortController)  
**Returns**: <code>string</code> - - one of 'asc', 'desc' or null  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column for which to get sort direction |

<a name="SortController+set"></a>

### sortController.set(column, [direciton])
Sets a column's sort direction in state, starting with ascending.

**Kind**: instance method of [<code>SortController</code>](#SortController)  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>Object</code> | The column to sort by |
| [direciton] | <code>string</code> | asc or desc. Optional and the default is ascending OR the opposite of the current direction |

<a name="Breadcrumbs"></a>

## Breadcrumbs
React class that renders a button

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| onClick | <code>function</code> | function to be called when the button is clicked |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| internal | <code>node</code> | component children, will be handled by react |
| font | <code>string</code> | string corresponding to the icon to be rendered |

<a name="Breadcrumbs+onClick"></a>

### breadcrumbs.onClick
(Internal) onClick of the element just adds the eventData prop to the event, and then calls the onClick prop

**Kind**: instance property of [<code>Breadcrumbs</code>](#Breadcrumbs)  
<a name="Button"></a>

## Button
React class that renders a button

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| onClick | <code>function</code> | function to be called when the button is clicked |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| internal | <code>node</code> | component children, will be handled by react |
| font | <code>string</code> | string corresponding to the icon to be rendered |

<a name="Button+onClick"></a>

### button.onClick
(Internal) onClick of the element just adds the eventData prop to the event, and then calls the onClick prop

**Kind**: instance property of [<code>Button</code>](#Button)  
<a name="Checkbox"></a>

## Checkbox
Checkbox - React class that renders a checkbox

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| value | <code>boolean</code> | the value that the checkbox will display |
| disabled | <code>boolean</code> | whether the checkbox will be disabled |
| variant | <code>string</code> | Theme variant name to be added to the component |
| className | <code>string</code> | css class to be applied to this component |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| onChange | <code>function</code> | function to be called when the button is clicked |

<a name="Checkbox+onClick"></a>

### checkbox.onClick
(Internal) onClick of the element, adds the eventData prop to the event, adds a value to the event, and then calls the onChange prop

**Kind**: instance property of [<code>Checkbox</code>](#Checkbox)  
<a name="Combobox"></a>

## Combobox
React class that renders a dropdown element and allows for the selection of one item

**Kind**: global class  
**See**: [https://jquense.github.io/react-widgets/api/Combobox/](https://jquense.github.io/react-widgets/api/Combobox/)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| children | <code>node</code> | internal component children, will be handled by react |
| sendValueField | <code>boolean</code> |  |
| onChange | <code>function</code> | function to be called when the button is clicked |
| valueField | <code>string</code> | key corresponding to the value field in the data |
| textField | <code>string</code> | key corresponding to the text field in the data |
| value | <code>any</code> | value to be assigned to the input |
| data | <code>array</code> | array of objects with a value and a text, the keys of which should correspond to valueField and textField |
| selectIcon | <code>string</code> | string corresponding to a font class for the icon desired |

<a name="Combobox+onSelect"></a>

### combobox.onSelect
(Internal) calls the onChange prop with an object with value and data

**Kind**: instance property of [<code>Combobox</code>](#Combobox)  
<a name="Content"></a>

## Content
has a header, content and footer.

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| horizontal | <code>boolean</code> |  |
| inline | <code>boolean</code> |  |
| relative | <code>boolean</code> |  |
| vFill | <code>boolean</code> |  |

<a name="DataBlock"></a>

## DataBlock
renders a column or row seperated title and data format

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| vertical | <code>boolean</code> | determines if the block has a vertical layout or horizontal layout |
| fields | <code>array</code> | the fields to be rendered or read from the item and rendered each element is an object |
| item | <code>object</code> | the data item that is to be rendered by the data block |
| title | <code>string</code> \| <code>node</code> | text or element to be the block |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |

<a name="DateTimePicker"></a>

## DateTimePicker
React class that renders a date time picker

**Kind**: global class  
**See**: [https://jquense.github.io/react-widgets/api/DateTimePicker/](https://jquense.github.io/react-widgets/api/DateTimePicker/)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| timezone | <code>string</code> |  |
| variant | <code>string</code> | Theme variant name to be added to the component |
| className | <code>string</code> | css class to be applied to this component |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| onChange | <code>function</code> | function to be called when the button is clicked |
| sendValueField | <code>bool</code> | the field from the value object to be passed to the onChange field |

<a name="DateTimePicker+onSelect"></a>

### dateTimePicker.onSelect
(Internal) event that gets fired whenever the user makes a selection on the widget

**Kind**: instance property of [<code>DateTimePicker</code>](#DateTimePicker)  
<a name="DateTimeRangePicker"></a>

## DateTimeRangePicker
React class that renders a date range picker

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| onClick | <code>function</code> | function to be called when the button is clicked |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| internal | <code>node</code> | component children, will be handled by react |
| font | <code>string</code> | string corresponding to the icon to be rendered |

<a name="Dialog"></a>

## Dialog
React class that renders a popup with a message or a question

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| variant | <code>string</code> | Theme variant name to be added to the component |
| show | <code>boolean</code> | if true, the popup will be displayed on the page |
| title | <code>string</code> | the title of the popup |
| onClose | <code>function</code> | function to be executed when the popup gets closed |
| closeOnEscape | <code>boolean</code> | if true, popup will close when the esc key is hit |
| closeOnDocumentClick | <code>boolean</code> | if true popup will close when the document is clicked |
| onSubmit | <code>function</code> | function to be ran when the question answer is submitted |
| formProps | <code>object</code> | if there is an onSubmit function provided, a form will wrap the children, and this data will be passed into the form |
| children | <code>node</code> | React children of the element |

<a name="Message"></a>

## Message
React class to render a dialog message

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| variant | <code>string</code> | Theme variant name to be added to the component |
| okayVariant | <code>string</code> | Theme variant name to be applied to the dialog okay button |
| title | <code>string</code> | the title of the popup |
| okay | <code>string</code> | the text that will be on the okay button |
| show | <code>boolean</code> | if true, the popup will be displayed on the page |
| onClose | <code>function</code> | function to be executed when the popup gets closed |
| message | <code>string</code> | text or react element to be displayed to the user |
| children | <code>node</code> | React children of the element |

<a name="Question"></a>

## Question
React class to render a Dialog question

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| variant | <code>string</code> | Theme variant name to be added to the component |
| okayVariant | <code>string</code> | Theme variant name to be applied to the dialog okay button |
| cancelVariant | <code>string</code> | Theme variant name to be applied to the dialog cancel button |
| title | <code>string</code> | the title of the popup |
| okay | <code>string</code> | the text that will be on the okay button |
| cancel | <code>string</code> | the text that will be on the cancel button |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| show | <code>boolean</code> | if true, the popup will be displayed on the page |
| onOkay | <code>function</code> | function to be run on hitting okay |
| onCancel | <code>function</code> | function to be executed when the cancel button on the popup is clicked |
| message | <code>string</code> | text or react element to be displayed to the user |
| children | <code>node</code> | React children of the element |

<a name="Dropdown"></a>

## Dropdown
React class that renders a dropdown element and allows for the selection of one item

**Kind**: global class  
**See**: [https://jquense.github.io/react-widgets/api/DropdownList/](https://jquense.github.io/react-widgets/api/DropdownList/)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| children | <code>node</code> | internal component children, will be handled by react |
| sendValueField | <code>boolean</code> |  |
| onChange | <code>function</code> | function to be called when the button is clicked |
| valueField | <code>string</code> | key corresponding to the value field in the data |
| textField | <code>string</code> | key corresponding to the text field in the data |
| value | <code>any</code> | value to be assigned to the input |
| data | <code>array</code> | array of objects with a value and a text, the keys of which should correspond to valueField and textField |
| selectIcon | <code>string</code> | string corresponding to a font class for the icon desired |

<a name="Dropdown+onSelect"></a>

### dropdown.onSelect
(Internal) calls the onChange prop with an object with value and data

**Kind**: instance property of [<code>Dropdown</code>](#Dropdown)  
<a name="Flex"></a>

## Flex
React class that renders a div with display flex

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| direction | <code>string</code> | flex-direction css property |
| wrap | <code>string</code> | flex-wrap css property |
| inline | <code>boolean</code> | if true will change the display property to be inline-flex |
| vFill | <code>boolean</code> | if true, minHeight is set to 100% |
| align | <code>string</code> | align-items css property |
| alignSelf | <code>string</code> | align-self css property |
| alignContent | <code>string</code> | align-content css property |
| justify | <code>string</code> | justify-content css property |
| style | <code>object</code> | css styles object |
| children | <code>node</code> | react children |

<a name="Header"></a>

## Header
React class that renders a Hx html tag

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| level | <code>number</code> | html header level |

<a name="Label"></a>

## Label
React class that renders a label element

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |

<a name="Item"></a>

## Item
The Item represents a clickable and/or selectable element in the List. An
Item that supplies an item prop is selectable and clickable. An Item that 
supplies an eventData prop without an item prop will be clickable but not
selectable.

**Kind**: global class  
<a name="Item+onClick"></a>

### item.onClick
onClick - (Internal) onClick of the element

**Kind**: instance property of [<code>Item</code>](#Item)  
<a name="Dynamic"></a>

## Dynamic
This takes an items array and a factory and produces item elements for the list.
The Factory.create() will be called with an item and props ( onClick, onEvent, selected )
and should return a List.Item (if the item should be selectable/clickable) or other
React component

**Kind**: global class  
<a name="List"></a>

## List
React class that renders a List element

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| [selector] | <code>object</code> | either null (no selection), SingleSelector, MultiSelector, or a custom selector |
| selector.onSelect | <code>function</code> | called with an object containing { value : <item>, data : <item's eventData>, listData : <List's eventData>, sourceEvent }. This function should control the state of the selection. |
| selector.isSelected | <code>function</code> | returns true if the given item is selected |

<a name="SingleSelector"></a>

## SingleSelector
The SingleSelector will manage a state variable in you're controlling components
state. This will allow at most one item to be selected. Meta-click will unselect
a selected item.

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| component | <code>Component</code> | the component whose state is managed |
| stateKey | <code>string</code> | the name of the selection group in the state |
| options | <code>object</code> |  |
| options.onSelect | <code>function</code> | called with the item to select or null if remove is occurring. If this function returns false, the selection is cancelled. This will be invoked prior to calling component.setState() |
| [options.idFunc] | <code>function</code> | a function used to return item's id. The id will be stored in the selection group. |
| [options.idKey] | <code>string</code> | the key of the item's id. The id will be stored in the selection group. This is unused if idFunc is supplied |
| options.useMeta | <code>object</code> | if false, the use of meta to remove items will be disabled |

<a name="MultiSelector"></a>

## MultiSelector
The MultiSelector will manage a state variable in you're controlling components
state. This will allow multiple items to be selected. Meta-click will unselect
a selected item.

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| component | <code>Component</code> | the component whose state is managed |
| stateKey | <code>string</code> | the name of the selection group in the state |
| options | <code>object</code> |  |
| options.onSelect | <code>function</code> | called with three arguemnts: the array of the new selections ids, the item being added or removed, and true or false indicating if the event is an add or remove. If this function returns false, the selection is cancelled. This will be invoked prior to calling component.setState() |
| [options.idFunc] | <code>function</code> | a function used to return item's id. The id will be stored in the selection group. |
| [options.idKey] | <code>string</code> | the key of the item's id. The id will be stored in the selection group. This is unused if idFunc is supplied |

<a name="Login"></a>

## Login
React login widget with several input and methods

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| headerClassName | <code>string</code> | css class to be applied to the header component |
| userClassName | <code>string</code> | css class to be applied to the username input |
| passwordClassName | <code>string</code> | css class to be applied to the password input |
| loginClassName | <code>string</code> | css class to be applied to the login button |
| resetClassName | <code>string</code> | css class to be applied to the reset password button |
| warningClassName | <code>string</code> | css class to be applied to the warning/error text |
| forgotClassName | <code>string</code> | css class to be applied to the forgot password button |
| backClassName | <code>string</code> | css class to be applied to the back button |
| paneVariant | <code>string</code> | Theme variant name to be applied to the pane element |
| headerVariant | <code>string</code> | Theme variant name to be applied to the header |
| usernameVariant | <code>string</code> | Theme variant name to be applied to the username input |
| passwordVariant | <code>string</code> | Theme variant name to be applied to the password input |
| warningVariant | <code>string</code> | Theme variant name to be applied to the warning text |
| forgotVariant | <code>string</code> | Theme variant name to be applied to the forgot button |
| backVariant | <code>string</code> | Theme variant name to be applied to the back button |
| userText | <code>string</code> | text to be displayed above the username input |
| userHint | <code>string</code> | text to be the username input placeholder |
| emailText | <code>string</code> | text to be displayed above the email input |
| emailHint | <code>string</code> | text to be the email input placeholder |
| passwordText | <code>string</code> | text to be display above the password input |
| passwordHint | <code>string</code> | text to be the password input placeholder |
| loginText | <code>string</code> | text to be on the login button |
| resetText | <code>string</code> | text to be on the reset button |
| forgotText | <code>string</code> | text to be on the forgot password button |
| backText | <code>string</code> | text to be on the back button |
| errorText | <code>string</code> | text to be displayed in red |
| onLogin | <code>function</code> | function to be run when the user clicks on the login button |
| onLogout | <code>function</code> | function to ensure the user is logged out when they switch between login mode, or reset mode |
| onResetPassword | <code>function</code> | function to be ran when the user submits a password reset |
| logo | <code>any</code> | displayed at the top of the ui-element, usually an img elemet or react element with an image |
| loginInstruction | <code>any</code> | text or react element to be displayed at the top of the login pane |
| resetInstruction | <code>any</code> | text or react element to be displayed at the top of the reset password pane |


* [Login](#Login)
    * [.onInput](#Login+onInput)
    * [.onSubmit](#Login+onSubmit)
    * [.toggleMode](#Login+toggleMode)

<a name="Login+onInput"></a>

### login.onInput
(Internal) onChange method of the inputs, maintians state and where focus is

**Kind**: instance property of [<code>Login</code>](#Login)  
<a name="Login+onSubmit"></a>

### login.onSubmit
(Internal) onClick method of the buttons keeps track of which mode the widget is in and performs the appropriate funcionality

**Kind**: instance property of [<code>Login</code>](#Login)  
<a name="Login+toggleMode"></a>

### login.toggleMode
(Internal) maintains the correct mode the widget is in

**Kind**: instance property of [<code>Login</code>](#Login)  
<a name="MultiSelect"></a>

## MultiSelect
React class that renders a multiselect widget

**Kind**: global class  
**See**: [https://jquense.github.io/react-widgets/api/Multiselect/](https://jquense.github.io/react-widgets/api/Multiselect/)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| eventData | <code>any</code> | data to be included with events |
| onChange | <code>function</code> | function to be executed with the widget's onChange |
| onCreate | <code>function</code> | function to be executed with the widget's onCreate |
| children | <code>node</code> | internal component children, will be handled by react |
| selectIcon | <code>string</code> | font icon string of the icon to be used for dropdown arrow |


* [MultiSelect](#MultiSelect)
    * [.onSelect](#MultiSelect+onSelect)
    * [.onCreate](#MultiSelect+onCreate)

<a name="MultiSelect+onSelect"></a>

### multiSelect.onSelect
(Internal) onChange of the element, add event data to the payload and calls onChange

**Kind**: instance property of [<code>MultiSelect</code>](#MultiSelect)  
<a name="MultiSelect+onCreate"></a>

### multiSelect.onCreate
(Internal) onCreate of the element, adds eventData to the onCreate call

**Kind**: instance property of [<code>MultiSelect</code>](#MultiSelect)  
<a name="NumericInput"></a>

## NumericInput
React class that renders an Input that only accepts numbers

**Kind**: global class  
**See**: [TextInput](#TextInput) Class derived from  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| onChange | <code>function</code> | function to be called with the widgets onChange |
| changeOnBlur | <code>boolean</code> |  |
| changeOnReturn | <code>boolean</code> |  |
| hint | <code>string</code> | hint text for the widget |
| min | <code>number</code> | minimum value that the input can be |
| max | <code>number</code> | maximum value that the input can be |
| maxLength | <code>number</code> |  |
| size | <code>number</code> |  |
| focus | <code>boolean</code> |  |
| float | <code>boolean</code> | determines if the value can be a float or not |


* [NumericInput](#NumericInput)
    * [.onChange](#NumericInput+onChange)
    * [.acceptKey](#NumericInput+acceptKey)
    * [.validator](#NumericInput+validator)

<a name="NumericInput+onChange"></a>

### numericInput.onChange
(Internal) onChange of the element, calls the onChange prop

**Kind**: instance property of [<code>NumericInput</code>](#NumericInput)  
<a name="NumericInput+acceptKey"></a>

### numericInput.acceptKey
(Internal) - determines which key presses to accept this method filters out all non-numbers

**Kind**: instance property of [<code>NumericInput</code>](#NumericInput)  
<a name="NumericInput+validator"></a>

### numericInput.validator
(Internal) validation function that well not let invalid values be submitted

**Kind**: instance property of [<code>NumericInput</code>](#NumericInput)  
<a name="Pane"></a>

## Pane
React class that renders a pane

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| inline | <code>boolean</code> | adds inline properties to the pane |
| variant | <code>string</code> | Theme variant name to be added to the component |

<a name="Item"></a>

## Item
react class that renders an anchor tag with an onClick

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| close | <code>boolean</code> | if true will call the onClose function |
| onClick | <code>function</code> | called when the element is clicked with event data and value |
| eventData | <code>any</code> | passed into the onClick function when it is triggered |
| value | <code>any</code> | passed into the onClick function |
| onClose | <code>function</code> | called when the element is clicked and close is true |
| className | <code>string</code> | className of the element |
| children | <code>node</code> | React children of the element |

<a name="Item+onClick"></a>

### item.onClick
onClick - (Internal) onClick of the element

**Kind**: instance property of [<code>Item</code>](#Item)  
<a name="Popup"></a>

## Popup
React class to render a popup

**Kind**: global class  
**See**: [https://github.com/danreeves/react-tether](https://github.com/danreeves/react-tether)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| title | <code>string</code> \| <code>node</code> | to be rendered at the top of the popup |
| trigger | <code>function</code> | by default, a ToggleButton is used to render the button to surface the popup. If this function is supplied, its result will be used instead. The function is given and object containing { ref, onToggle, setOpened, isOpened }. The Ref needs to be assigned to the top most DOM element |
| style | <code>object</code> | css style object to be applied to the ToggleButton |
| id | <code>string</code> | unique id of the ToggleButton |
| variant | <code>string</code> | Theme variant name to be added to the popup component |
| toggleVariant | <code>string</code> | Theme variant name to be added to the ToggleButton component |
| onChange | <code>function</code> | called when the element is clicked with event data and value |
| eventData | <code>any</code> | passed into the onClick function when it is triggered |
| value | <code>any</code> | passed into the onClick function |
| children | <code>node</code> | React children of the element |
| render | <code>function</code> | if this is supplied, the function will be invoked with a close callback and the return value will be placed into the popup. |


* [Popup](#Popup)
    * [.onToggle](#Popup+onToggle)
    * [.setOpened](#Popup+setOpened)
    * [.onDocumentClick](#Popup+onDocumentClick)
    * [.addEvents()](#Popup+addEvents)
    * [.removeEvents()](#Popup+removeEvents)

<a name="Popup+onToggle"></a>

### popup.onToggle
(Internal) flips the isOpened property of the state

**Kind**: instance property of [<code>Popup</code>](#Popup)  
<a name="Popup+setOpened"></a>

### popup.setOpened
(internal) sets the isOpened property of the state

**Kind**: instance property of [<code>Popup</code>](#Popup)  
<a name="Popup+onDocumentClick"></a>

### popup.onDocumentClick
(Internal) closes the popup

**Kind**: instance property of [<code>Popup</code>](#Popup)  
<a name="Popup+addEvents"></a>

### popup.addEvents()
(internal) adds a click event to the page

**Kind**: instance method of [<code>Popup</code>](#Popup)  
<a name="Popup+removeEvents"></a>

### popup.removeEvents()
(internal) removes a click event to the page

**Kind**: instance method of [<code>Popup</code>](#Popup)  
<a name="RadioButton"></a>

## RadioButton
Creates a Radio button element in react

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | a class to be assigned to the element |
| variant | <code>string</code> | a global class to be assigned to the element |
| iconOn | <code>string</code> | the icon displayed when the radio value === on |
| iconOff | <code>string</code> | the icon displayed when radio value !== on |
| on | <code>any</code> | value is compared to this to determine if the radio is selected |
| onChange | <code>function</code> | callback called when element is clicked |
| eventData | <code>any</code> | data fed to the onChange function |
| value | <code>any</code> | a value used to determine if button is in an on state |
| id | <code>string</code> | to be used by the element |
| disabled | <code>boolean</code> | determines if the element is disabled or not |
| on | <code>any</code> | @default [true] if equal to value, button is in and on state, defaults to true |

<a name="RadioButton+onClick"></a>

### radioButton.onClick
(Internal) the onChange of the element, calls the onChange prop

**Kind**: instance property of [<code>RadioButton</code>](#RadioButton)  
<a name="ResetPassword"></a>

## ResetPassword
React class that renders a widget to reset a user's password

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Them variant name to be added to the component |
| logo | <code>any</code> | text or react element to be rendered at the top of the widget |
| resetInstruction | <code>any</code> | text or react element to be rendered below the logo |
| headerVariant | <code>string</code> | variant to be applied to the element header |
| headerClassName | <code>string</code> | css class to be applied to the element header |
| headerText | <code>string</code> | text to be rendered in the header |
| passwordClassName | <code>string</code> | css class to be applied to the password inputs |
| passwordVariant | <code>string</code> | Theme variant to be applied to the password inputs |
| passwordHint | <code>string</code> | text to be the password input hint |
| confirmPasswordHint | <code>string</code> | text to be the confirm password hint |
| resetClassName | <code>string</code> | css class to be applied to the button |
| resetVariant | <code>string</code> | Theme variant to be applied to the button |
| resetText | <code>string</code> | text for the button |
| errorVariant | <code>string</code> | Theme variant to be applied to the error text |
| errorClassName | <code>string</code> | css class to be applied to the error text |
| errorText | <code>string</code> | text to be displayed as the error |
| onSubmit | <code>function</code> | function to be called when the form is submitted |


* [ResetPassword](#ResetPassword)
    * [.onInput](#ResetPassword+onInput)
    * [.onSubmit](#ResetPassword+onSubmit)

<a name="ResetPassword+onInput"></a>

### resetPassword.onInput
(Internal) onChange method of the inputs, maintians state and where focus is

**Kind**: instance property of [<code>ResetPassword</code>](#ResetPassword)  
<a name="ResetPassword+onSubmit"></a>

### resetPassword.onSubmit
(Internal) onClick method of the buttons keeps track of which mode the widget is in and performs the appropriate funcionality

**Kind**: instance property of [<code>ResetPassword</code>](#ResetPassword)  
<a name="Slider"></a>

## Slider
React class that renders a Slider

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| onChange | <code>function</code> | function to be called when the button is clicked |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| min | <code>number</code> \| <code>string</code> | the minimum value of the slider range |
| max | <code>number</code> \| <code>string</code> | the maximum value of the slider range |
| value | <code>number</code> \| <code>string</code> | the current value of the slider |

<a name="Slider+onChange"></a>

### slider.onChange
(Internal) onClick of the element just adds the eventData prop to the event, and then calls the onClick prop

**Kind**: instance property of [<code>Slider</code>](#Slider)  
<a name="SplitPane"></a>

## SplitPane
React class that renders a SplitPane

**Kind**: global class  
**See**: [https://github.com/tomkp/react-split-pane](https://github.com/tomkp/react-split-pane) is the base widget this uses  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| split | <code>&#x27;vertical&#x27;</code> \| <code>&#x27;horizontal&#x27;</code> |  |
| minSize | <code>number</code> | sets the minimum size of the primary pane |
| maxSize | <code>number</code> | sets the maximum size of the primary pane |
| defaultSize | <code>number</code> | sets the default size of the primary pane |
| onChange | <code>function</code> | function to be called with the onChange method |
| autoSaveKey | <code>function</code> | key which saves the last value to local storage |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |

<a name="SplitPane+onChange"></a>

### splitPane.onChange
(Internal) gets called by the widget's onChange. sets the last pane size to local storage and calls the onChange prop with eventData

**Kind**: instance property of [<code>SplitPane</code>](#SplitPane)  
<a name="Table"></a>

## Table
React class that renders a table

**Kind**: global class  
**See**: [https://github.com/tannerlinsley/react-table](https://github.com/tannerlinsley/react-table)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| tableRef | <code>any</code> | react reference |
| data | <code>array</code> | the data to be displayed on the table |
| columns | <code>array</code> | array of objects the defines the column header and which portion of the data to display |

<a name="Tab"></a>

## Tab
react class to render a tab for the tab pane

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| tabId | <code>string</code> | id of the tab |
| tabName | <code>string</code> | name that will be displayed on the tab button |
| className | <code>string</code> | css class to be applied to this component |

<a name="TabPane"></a>

## TabPane
React class for a component with as many tabs as desired. manages which tab is displayed

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| activeTab | <code>string</code> | id of the tab that should be active when the component is created |
| variant | <code>string</code> | Theme variant name to be added to the component |
| className | <code>string</code> | css class to be applied to this component |
| activeId | <code>string</code> | id of the tab that will be active |
| defaultId | <code>string</code> | id of the tab that will be active if there isn't an activeId specified |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| onTabClicked | <code>function</code> | function to be executed when a Tab gets clicked |

<a name="TabPane+onTabClicked"></a>

### tabPane.onTabClicked
(Internal) sets the activeTab, then calls onTabClicked with an object with a value property and data property
the value property is the tabId of the tab clicked, and the data is the eventData prop

**Kind**: instance property of [<code>TabPane</code>](#TabPane)  
<a name="Text"></a>

## Text
React class to render a block of text

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |

<a name="TextArea"></a>

## TextArea
React class to render a block of text

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |

<a name="TextInput"></a>

## TextInput
This TextInput field will allow you to install a function
to prohibit keys, validate the input, and to fire changes
only on a carriage return or blur.

**Kind**: global class  
**Properties**

| Name | Type |
| --- | --- |
| onChange | <code>function</code> | 
| onfocus | <code>function</code> | 
| validator | <code>function</code> | 
| acceptKey | <code>function</code> | 
| changeOnReturn | <code>boolean</code> | 
| changeOnBlur | <code>boolean</code> | 
| alwaysFireOnReturn | <code>boolean</code> | 
| placeCaretAtEnd | <code>boolean</code> | 
| focus | <code>boolean</code> | 
| disabled | <code>boolean</code> | 
| hint | <code>string</code> | 
| placeholder | <code>string</code> | 
| value | <code>string</code> | 
| maxLength | <code>number</code> | 
| size | <code>number</code> | 

<a name="ToggleButton"></a>

## ToggleButton
React class that renders a button with an on and an off state

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| className | <code>string</code> | css class to be applied to this component |
| variant | <code>string</code> | Theme variant name to be added to the component |
| onChange | <code>function</code> | function to be called when the button is clicked |
| eventData | <code>any</code> | will be passed through as the data key to the onClick function |
| value | <code>boolean</code> | tells the button if it is an on or off state |
| on | <code>node</code> | react element to be displayed if value is true |
| off | <code>node</code> | react element to be displayed if value is false |
| iconOn | <code>string</code> | string of font to be displayed if value is true |
| iconOff | <code>string</code> | string of font to be displayed if value is false |
| children | <code>node</code> | internal component children, will be handled by react |

<a name="ToggleButton+onClick"></a>

### toggleButton.onClick
(Internal) onClick of the element just adds the eventData prop to the event, and then calls the onClick prop

**Kind**: instance property of [<code>ToggleButton</code>](#ToggleButton)  
<a name="create"></a>

## create()
**Kind**: global function  

* [create()](#create)
    * [~getData()](#create..getData)
    * [~setDefaultData()](#create..setDefaultData)
    * [~getDefaultData()](#create..getDefaultData)
    * [~applyErrorState(data, name, err, isSubmit)](#create..applyErrorState)
    * [~dataToForm()](#create..dataToForm)
    * [~isValid()](#create..isValid)
    * [~dataProps()](#create..dataProps) ⇒ <code>object</code>
    * [~hasChanges()](#create..hasChanges)
    * [~getFromData(type, name)](#create..getFromData)
    * [~message()](#create..message)

<a name="create..getData"></a>

### create~getData()
Returns the current form data, either from the
component state or from the currentData
return {FormData}

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..setDefaultData"></a>

### create~setDefaultData()
Sets the current (external) data. This is the default
state and the revert state

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..getDefaultData"></a>

### create~getDefaultData()
Gets the current (external) data

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..applyErrorState"></a>

### create~applyErrorState(data, name, err, isSubmit)
Applys the error condition to the data

**Kind**: inner method of [<code>create</code>](#create)  

| Param | Type | Description |
| --- | --- | --- |
| data | <code>\*</code> | the data to modify |
| name | <code>\*</code> | the name of the item to change |
| err | <code>\*</code> | if false, this indicates and error. If a string it indicates and error with a message |
| isSubmit | <code>\*</code> | if true, this is for submit validators |

<a name="create..dataToForm"></a>

### create~dataToForm()
Converts the value object into a { values : { }, errors : { }, msgs : { } }

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..isValid"></a>

### create~isValid()
Returns true if there are no immediate errors. Normally this
is used to enable the submit button. This only checks the
states of the immediate validators, not the submit validators

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..dataProps"></a>

### create~dataProps() ⇒ <code>object</code>
**Kind**: inner method of [<code>create</code>](#create)  
**Returns**: <code>object</code> - an object that contains data-error : true
if the named component is in an error state.  
<a name="create..hasChanges"></a>

### create~hasChanges()
Returns true if the the users has made
changes to the values

**Kind**: inner method of [<code>create</code>](#create)  
<a name="create..getFromData"></a>

### create~getFromData(type, name)
Returns the value for the named form elements field.

**Kind**: inner method of [<code>create</code>](#create)  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>string</code> | one of 'errors', 'msgs', 'values' |
| name | <code>string</code> | the name of the attribute |

<a name="create..message"></a>

### create~message()
Returns the message for the named field. If the name
is not supplied or is null, the overall error message
will be returned

**Kind**: inner method of [<code>create</code>](#create)  
<a name="classes"></a>

## classes(component, type, variant, ...rest) ⇒ <code>string</code>
Returns the classnames needed for the component's type and variant.

**Kind**: global function  
**Returns**: <code>string</code> - the classname  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| type | <code>string</code> | the part of the component to get. eg "button" |
| variant | <code>string</code> | the variant name to requsest. eg "small" |
| ...rest | <code>strings</code> | other strings to add to the classname |

<a name="subclasses"></a>

## subclasses(component, type, ...rest) ⇒ <code>string</code>
Returns the classnames needed for the component's sub element. The variant
is not needed here because it will be in the css rule as a parent.

**Kind**: global function  
**Returns**: <code>string</code> - the classname  

| Param | Type | Description |
| --- | --- | --- |
| component | <code>string</code> | the name of the component type. eg "Button" |
| type | <code>string</code> | the sub-component of the component to get. eg "button" |
| ...rest | <code>strings</code> | other strings to add to the classname |

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

<a name="renderLayout"></a>

## renderLayout(theme, layout, children)
Renders the layouts

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| theme | <code>Theme</code> |  |
| layout | <code>string</code> | the layout name |
| children | <code>array</code> | the react children to place |

<a name="ensureHierarchy"></a>

## ensureHierarchy(theme, results, parents, options, name)
Makes sure that the parent layouts have been created and are in the
layout children arrays or the top level results array

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| theme | <code>Theme</code> | the theme, used to get the layout's classname |
| results | <code>Array</code> | the top level results array |
| parents | <code>Object</code> | the top level parent layout lookup object |
| options | <code>Object</code> | the options for the particular layout |
| name | <code>string</code> | the name of the element we need to place. |

<a name="createSublayouts"></a>

## createSublayouts(elem)
Creates React elements from the sublayout object

**Kind**: global function  

| Param | Type | Description |
| --- | --- | --- |
| elem | <code>Object</code> | the sublayout object created in ensureHistory |

<a name="FormData"></a>

## FormData
**Kind**: global typedef  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| values | <code>object</code> | object containing current values |
| errors | <code>object</code> | object containing error states for each value |
| msgs | <code>object</code> | object containing error messages for each value |
| hasChanges | <code>boolean</code> | true if the user has modified the values |
| hasError | <code>boolean</code> | true if the there is an error |

