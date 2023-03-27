---
layout: full
---

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<div class="grid grid-cols-2 gap-4">
<div>

# Protocol 1

One user sends batch of 2000 statements per requests to the LRS.


```mermaid
flowchart TB
    user("🏫🎓") -- 2000 statements --> lrs((LRS))
    lrs -- HTTP 200 OK--> user
```

 Duration of the test: 900 seconds


</div>
<div>

# Protocol 2 

Many users sends 1 statement per requests to the LRS


```mermaid {scale: 0.8}
flowchart
    user1("👨🏽‍🎓") -- 1 statement --> lrs((LRS))
    user2("🧑🏼‍🎓") -- 1 statement --> lrs
    user3("👩‍🎓") -- 1 statement --> lrs
    user4("👩🏾‍🎓") -- 1 statement ... --> lrs

```

 Duration of the test: 900 seconds

</div>
</div>

