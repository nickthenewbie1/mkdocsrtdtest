---
id: api-patch-ops
title: API Patch Ops
---

# Install
```
npm install --save @leverege/api-patch-ops

const PatchOps = require( '@leverege/api-patch-ops' );

let patch = PatchOps( 'attr', value )
api.blueprint( id ).update( patch.ops() )

```


