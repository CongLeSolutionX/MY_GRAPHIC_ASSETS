---
created: 2025-05-10 05:31:26
author: NA
version: "TBD"
license(s): NA
copyright: NA
source: https://en.wikipedia.org/wiki/GeoJSON
---



# CHANGE_ME
<details open>
<summary>Click to show/hide the full disclaimer.</summary>
   
> <ins>📢 **Disclaimer** 🚨</ins>
>
> This is a sketch book where I actively experiment and try new techniques<br/>
> and get result in realtime for faster development.</br>
> It's where I document my academic explorations,</br>
> share my findings with anyone interested,</br>
> and maintain a personal vault of my creative and technical journey.</br>
> I'm not sure the link for this repo being shared in the back by others,</br>
> since I havent plan for any analytics for this project yet.</br>
> ...and I'm actively looking for a job...</br>

> This document contains my personal notes on the topic,</br>
> compiled from publicly available documentation and various cited sources.
> 
> The materials are intended for educational purposes (<ins>sometimes, entertainment purposes</ins>), personal study, and technical reference.
> The content is dual-licensed:
> 1. **MIT License:** Applies to all code implementations (Swift, Mermaid, and other programming languages).
> 2. **Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0):** Applies to all non-code content, including text, explanations, diagrams, and illustrations.

</details>


---



```topojson
{
  "type":"Topology",
  "transform":{
    "scale": [1,1],
    "translate": [0,0]
  },
  "objects":{ 
    "two-squares":{
      "type": "GeometryCollection",
      "geometries":[
        {"type": "Polygon", "arcs":[[0,1]],"properties": {"name": "Left_Polygon" }},
        {"type": "Polygon", "arcs":[[2,-1]],"properties": {"name": "Right_Polygon" }}
      ]
    },
    "one-line": {
      "type":"GeometryCollection",
      "geometries":[
        {"type": "LineString", "arcs": [3],"properties":{"name":"Under_LineString"}}
      ]
    },
    "two-places":{
      "type":"GeometryCollection",
      "geometries":[
        {"type":"Point","coordinates":[0,0],"properties":{"name":"Origine_Point"}},
        {"type":"Point","coordinates":[0,-1],"properties":{"name":"Under_Point"}}
      ]
    }
  },
  "arcs": [
    [[1,2],[0,-2]],
    [[1,0],[-1,0],[0,2],[1,0]],
    [[1,2],[1,0],[0,-2],[-1,0]],
    [[0,-1],[2,0]]
  ]
}
```



<!-- ---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>
--- -->

<!-- - **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/). -->
