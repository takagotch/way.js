### way.js
---
https://github.com/gwendall/way.js

```
npm install way-js
```

```js
import 'way-js';

way.set("someScope", { with: { something: "hello" }})

way.dom("#someDIV").scope()
>> "someScope.with"

way.set("some.list", [
  {name:"Pierre"},
  {name:"Paul"},
  {name:"Jacques"}
]);

way.set("""se")
```

```
<script src="dist/way.js"></script>

<form way-data="some.form" way-pick="some,propertyies,that,can.be.nested">
<form way-data="some.form" way-omit="dont,want.those">
<img way-data="some.form" way-omit="dont,want.those">
<pre way-data="some.json" way-json="true"></pre>

<div way-scope="someScope">
  <div way-scope="with">
    <div way-data="something"></div>
  </div>
</div>

<div way-scope="someScope">
  <div way-scope-break="true">
    <div way-data="someScope.with.something"></div>
  </div>
</div>

<div way-scope="someScope">
  <div way-scope="with">
    <div way-data="something" id="someDIV"></div>
  </div>
</div>

<div way-repeat="some.list">
  $$key - <span way-data="name"></span>
</div>

<div way-scope="some.list">
  <div way-scope="0">
    0 - <span way-data="name">Pierrre</span>
  </div>
  <div way-scope="1">
    1 - <span way-data="name">Paul</span>
  </div>
  <div way-scope="2">
    2 - <span way-data="name">Jacques</span>
  </div>
</div>


```

