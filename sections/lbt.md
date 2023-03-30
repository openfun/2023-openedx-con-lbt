---
layout: two-cols
---

<style>
h3 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

# What is a Learning Record Store (LRS)?
Quick reminder with the example of Ralph

<br>

```mermaid {scale: 0.8}
flowchart LR
    subgraph LRS
        ralph(Ralph) -- xAPI --> es[(Elasticsearch)]
    end

    lms("LMS - Open edX 🎓") -- xAPI --> ralph
    marsha("Marsha 🎬") -- xAPI --> ralph
    ashley("Ashley 💬") -- xAPI --> ralph
    LRS --> grafana("Grafana 📈") 
    LRS --> superset("Superset 📈") 
```

::right::

<br>

### Some open source LRS

<style >
    .right {
  display: block;
  margin-left: auto;
  margin-right: 100;
}
    h3 {
        text-align: right;
    }
</style>

<br>

<img src="https://camo.githubusercontent.com/df989cf5db6c5f206e1f867c5bf1c5d2e799dca4f4f261432d94c831f2f3d323/68747470733a2f2f692e696d6775722e636f6d2f68503179464b4c2e706e67" width="170" class="right">  

<br>

<img src="https://yetanalytics.github.io/lrsql/images/doc_logo.png" width="150" class="right"> 

<br>

<img src="/images/traxlrs.png" width="100" class="right"> 

<br>

<img src="https://raw.githubusercontent.com/openfun/logos/main/ralph/ralph-color-light.png" width="130" class="right"> 

---
layout: full
class: text-center
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

.footer {
    position: fixed;     
    text-align: center;    
    bottom: 0px; 
    width: 100%;
}

.center {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);   
}
</style>

# Architecture of **L**RS **B**enchmarking **T**ool (LBT)

<div class="center">

```mermaid {scale: 1.1}
flowchart LR
    datasim("Datasim ①") -- xAPI --> locust("Locust ②") -- HTTP POST/GET --> lrs((LRS))
    lrs((LRS)) -- HTTP response --> locust
    locust -- collected metrics --> jup("Jupyter Notebook 📊 📉 📈")
```
</div>

<div class="footer">

[① datasim: xAPI Data Generation Tool](https://github.com/yetanalytics/datasim)

[② Python-based load testing framework](https://github.com/locustio/locust)
</div>