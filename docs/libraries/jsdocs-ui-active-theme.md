---
id: jsdocs-ui-active-theme
title: UI Active Theme
---
## Functions

<dl>
<dt><a href="#props">props(component, variant)</a> ⇒ <code>object</code></dt>
<dd><p>Returns any default props for the supplied Component and Variant.
If the third argument is an object, it will be overlaid on top of
the component&#39;s default props and the component&#39;s variant props.</p>
<p>If the second argument is an object, it is considered to be the
React component&#39;s actual props object, and the variant is looked
up from it. This means from render, you can invoke:
  const { markClass } = theme.props( &#39;Checkbox&#39;, this.props )</p>
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
<dt><a href="#onAppearanceLoaded">onAppearanceLoaded()</a></dt>
<dd><p>Invoked on the initial download of the firebase appearance</p>
</dd>
<dt><a href="#styleToCss">styleToCss()</a></dt>
<dd><p>Turn component.style into cssText</p>
</dd>
<dt><a href="#extractStyleSheet">extractStyleSheet()</a></dt>
<dd><p>Walk the style model to extract css. Form is
[ { selector, value } | { type : &#39;conditional&#39;, selector, rules [ ] }]</p>
</dd>
<dt><a href="#objToCss">objToCss()</a></dt>
<dd><p>Turn each key/value in obj into a css attribute</p>
</dd>
</dl>

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

<a name="onAppearanceLoaded"></a>

## onAppearanceLoaded()
Invoked on the initial download of the firebase appearance

**Kind**: global function  
<a name="styleToCss"></a>

## styleToCss()
Turn component.style into cssText

**Kind**: global function  
<a name="extractStyleSheet"></a>

## extractStyleSheet()
Walk the style model to extract css. Form is
[ { selector, value } | { type : 'conditional', selector, rules [ ] }]

**Kind**: global function  
<a name="objToCss"></a>

## objToCss()
Turn each key/value in obj into a css attribute

**Kind**: global function  
