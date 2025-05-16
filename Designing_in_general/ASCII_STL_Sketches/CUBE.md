---
created: 2025-05-10 05:31:26
author: NA
version: "TBD"
license(s): NA
copyright: NA
source: https://people.math.sc.edu/Burkardt/data/stla/stla.html
---



# CUBE
<!-- > This content is dual-licensed under your choice of the following licenses:
> 1.  **MIT License:** For the code implementations in Swift and Mermaid provided in this document.
> 2.  **Creative Commons Attribution 4.0 International License (CC BY 4.0):** For all other content, including the text, explanations, and the Mermaid diagrams and illustrations. -->

---


CUBE is a cube using 12 triangular faces.

```stl
solid MYSOLID
  facet normal  0.0   0.0  -1.0    
    outer loop
      vertex    0.0   0.0   0.0    
      vertex    1.0   1.0   0.0    
      vertex    1.0   0.0   0.0    
    endloop
  endfacet
  facet normal  0.0   0.0  -1.0    
    outer loop
      vertex    0.0   0.0   0.0 
      vertex    0.0   1.0   0.0    
      vertex    1.0   1.0   0.0    
    endloop
  endfacet
  facet normal -1.0   0.0   0.0    
    outer loop
      vertex    0.0   0.0   0.0
      vertex    0.0   1.0   1.0
      vertex    0.0   1.0   0.0
    endloop
  endfacet
  facet normal -1.0   0.0   0.0    
    outer loop
      vertex    0.0   0.0   0.0
      vertex    0.0   0.0   1.0
      vertex    0.0   1.0   1.0
    endloop
  endfacet
  facet normal  0.0   1.0   0.0    
    outer loop
      vertex    0.0   1.0   0.0
      vertex    1.0   1.0   1.0
      vertex    1.0   1.0   0.0
    endloop
  endfacet
  facet normal  0.0   1.0   0.0    
    outer loop
      vertex    0.0   1.0   0.0
      vertex    0.0   1.0   1.0
      vertex    1.0   1.0   1.0
    endloop
  endfacet
  facet normal  1.0   0.0   0.0    
    outer loop
      vertex    1.0   0.0   0.0
      vertex    1.0   1.0   0.0
      vertex    1.0   1.0   1.0
    endloop
  endfacet
  facet normal  1.0   0.0   0.0    
    outer loop
      vertex    1.0   0.0   0.0
      vertex    1.0   1.0   1.0
      vertex    1.0   0.0   1.0
    endloop
  endfacet
  facet normal  0.0  -1.0   0.0    
    outer loop
      vertex    0.0   0.0   0.0
      vertex    1.0   0.0   0.0
      vertex    1.0   0.0   1.0
    endloop
  endfacet
  facet normal  0.0  -1.0   0.0    
    outer loop
      vertex    0.0   0.0   0.0
      vertex    1.0   0.0   1.0
      vertex    0.0   0.0   1.0
    endloop
  endfacet
  facet normal  0.0   0.0   1.0    
    outer loop
      vertex    0.0   0.0   1.0
      vertex    1.0   0.0   1.0
      vertex    1.0   1.0   1.0
    endloop
  endfacet
  facet normal  0.0   0.0   1.0    
    outer loop
      vertex    0.0   0.0   1.0
      vertex    1.0   1.0   1.0
      vertex    0.0   1.0   1.0
    endloop
  endfacet
endsolid MYSOLID
```



<!-- ---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>
--- -->

<!-- - **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/). -->
