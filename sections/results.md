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

# Results for protocol 1
One user, 2200 statements per request

<div class="grid grid-cols-2 gap-4">
  <div>
    POST /statements
    <br/>
    <img src="/images/protocol_1_post.png" width="500" />
  </div>
  <div>
    GET /statements?limit=2200
  <img src="/images/protocol_1_get.png" width="500" />
  </div>
</div>

---
layout: full
---

# Results for protocol 2

1000 users, 1 statement per request

<div class="grid grid-cols-2 gap-4">
  <div>
    POST /statements
    <br/>
    <img src="/images/protocol_2_post.png" width="500" />
  </div>
  <div>
    GET /statements?id=
  <img src="/images/protocol_2_get.png" width="500" />
  </div>
</div>

