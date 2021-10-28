---
id: jsdocs-permissions
title: Permissions
---
<a name="has"></a>

## has()
Checks to see if Path.get( key, perm ) has the specific value in it. This uses
indexOf() to determine the answer. This can operate with either strings
or arrays:
   has( { x : 'rw' }, 'x', 'w' ) ==> true
   has( { x : ['r', 'w'] }, 'x', 'w' ) ==> true
   has( { x : 1 }, 'x', '1' ) ==> true
If the Path.get( key, perm ) does not have an indexOf function, Path.get( key, perm ) == val will 
be used instead

**Kind**: global function  
