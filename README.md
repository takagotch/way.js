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

way.set("someData", "hello")

way.set("someData", "hello");
way.registerTransform("lolify", function(data){
  return data + " lol";
});

way.set("some.list", ["I", "am", "list"]);

$("#clickToRemove").click();
$("#clickToPush").click();
way.get("some.list");
>> ["I", "am", null]

way.set("image.url", "somethingThatsNotAnImageURL");

way.dom("#someForm").toStorage()
way.dom("#someForm").formStorage()

way.dom("#someForm").toJSON()

way.dom("#soemForm").formJSON({name:"John Doe"})
way.dom("#someForm").getValue()
way.dom("#someForm").setValue({name:"John Doe"})

way.dom("#someForm").setDefault()
>> {
  its: "values",
  serialized: {
    in: "a json"
  }
}

way.setDefaults()

way.dom().getOptions()

way.get("some.path");

way.set("some.path", "bonjour!");

way.clear("some.path");
way.get("some.path");
>> undefined

way.clear();
way.get();
>> {}

way.backup();

way.restore();

way.registerBindings()

way.updateBindings("formData.name")

way.registerRepeats()

way.updateRepeats("somethingToBeLooped")

way.watch("some.data", function(value){
  console.log("Data has been updated to value: " + value);
});

way.watchAll(function(selector, value){
  console.log("The data " + selector + "has been changed.", value);
});

way.options.persistent = true

way.options.timeoutInput = 50

way.options.timeoutDOM = 500
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

<div id="clickToRemove" way-action-remove=""></div>
<div id="clickToPush" way-action-push="some.list"></div>

<img way-data="image.url">

```

