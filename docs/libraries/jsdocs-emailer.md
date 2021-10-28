---
id: jsdocs-emailer
title: Emailer
---
## Functions

<dl>
<dt><a href="#create">create(options, to, cc, bcc, subject, text, html, template, context, attachments)</a> ⇒</dt>
<dd><p>Returns a object that uses NodeMailer MailGun to send emails.
This object will have a send( msg, callback ) method.</p>
</dd>
<dt><a href="#checkRecipient">checkRecipient(r, templateId, limiter, onFirst)</a> ⇒</dt>
<dd><p>The checkRecipient function is exposed here to facilitate testing with
the new Limit logic.</p>
</dd>
</dl>

<a name="create"></a>

## create(options, to, cc, bcc, subject, text, html, template, context, attachments) ⇒
Returns a object that uses NodeMailer MailGun to send emails.
This object will have a send( msg, callback ) method.

**Kind**: global function  
**Returns**: an object containing a send() method. This will accept
a message with te following paramters.  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | the node mailer options for mailgun and limiter |
| to | <code>string</code> \| <code>array</code> | the recipents' email addresses |
| cc | <code>string</code> \| <code>array</code> | the carbon copy email list |
| bcc | <code>string</code> \| <code>array</code> | the blind carbon copy email list |
| subject | <code>string</code> | the subject line |
| text | <code>string</code> | optional message in plain text format |
| html | <code>string</code> | optional message in html format |
| template | <code>string</code> | the id of the template to use |
| context | <code>object</code> | the object to give to the template |
| attachments | <code>array</code> | the attachment list |
| attachments[n].filename | <code>string</code> | the name of the attachment that the recipents will see |
| attachments[n].url | <code>string</code> | the source of a file to send as attachment |
| attachments[n].content | <code>string</code> | the base64 encoded content. Dont use this if url is specified |
| attachments[n].encoding | <code>string</code> | normally "base64". If not specified, it assumes base64 |
| attachments[n].contentType | <code>string</code> | the content type |
| attachments[n].knownLength | <code>string</code> | the length of the content |

<a name="checkRecipient"></a>

## checkRecipient(r, templateId, limiter, onFirst) ⇒
The checkRecipient function is exposed here to facilitate testing with
the new Limit logic.

**Kind**: global function  
**Returns**: an array of email targets  

| Param | Type | Description |
| --- | --- | --- |
| r |  | recipients in the form of a string or an array |
| templateId | <code>string</code> | the id of the template or null if one doesnt exist |
| limiter |  | the actual Limit instance to use |
| onFirst |  | a callback on the first time the limit occurs for a target |

<a name="checkRecipient..filterLimited"></a>

### checkRecipient~filterLimited()
Iterates over the array, checking each target to see if it has been
limited from email.

**Kind**: inner method of [<code>checkRecipient</code>](#checkRecipient)  
