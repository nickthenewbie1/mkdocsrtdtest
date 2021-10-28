---
id: ui-redux
title: UI Redux
---

UI-redux contains some commonly used front end functionality and integrates it with redux to make it easily used across and app.

## Installation

```
npm install @leverege/ui-redux --save
```

## Reducer Setup

When creating the reducers, include the InterfaceReducer

```
import { combineReducers } from 'redux' 
import { SelectReducer, UIReducer } from 'ui-redux'
...

const reducers = combineReducers( {
  ...
  select : Select,
  ui : UI
} )

export default reducers

```

## Actions and Access

### select

`select` is a reducer responsible for maintaining arrays (groups) of items that have been selected. 

```
import { select } from '@leverege/ui-redux'

dispatch( select.add( UUID, myGroup ) )
```

the methods on `select` are

1. add( ids, group ) - adds ids to the specified group
2. set( ids, group ) - changes the group to be the ids provided
3. remove( ids, group ) - removes the ids from the group
4. toggle( ids, group ) - if in group, removes id, if not in group adds id; for each id
5. clear( group ) - resets the group to no selection
6. clearAll() - resets all groups to no selection
7. isSelected( groupData, id ) - checks if an item is in a group
8. count( groupData ) - count of the number of items in a group
9. isEmpty( groupData ) - checks if group is empty

### UI

`UI` is a simple reducer that maintains keys.

```
import { UI } from '@leverege/ui-redux'

dispatch( UI.set( myKey, myValue ) )
```

the `UI` methods are

1. set( key, value ) - sets the value of the key
2. multiSet( keyValue ) - object that has all of its keys and values set
