---
created: 2025-05-10 05:31:26
author: Cong Le
version: "1.0"
license(s): MIT, CC BY 4.0
copyright: Copyright (c) 2025 Cong Le. All Rights Reserved.
---



# Designing in general
> This content is dual-licensed under your choice of the following licenses:
> 1.  **MIT License:** For the code implementations in Swift and Mermaid provided in this document.
> 2.  **Creative Commons Attribution 4.0 International License (CC BY 4.0):** For all other content, including the text, explanations, and the Mermaid diagrams and illustrations.

---


Configuration setting file: 
https://mermaid.js.org/schemas/config.schema.json

We can override the setting and value of Mermaid variables in the configuration scheme JSON file.


We can values of the properties in this file: [[json-schema for Mermaid variables and settings]]

Example usage: 

```mermaid
%%{
  init: {
    'additionalProperties': true,
    'look': "handDrawn",
    'fontFamily': 'Monaco',
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#8229',
      'primaryTextColor': '#000',
      'primaryBorderColor': '#4128',
      'lineColor': '#F8B229',
      'textColor': '#FFF',
      'fontSize': '20px'
    }
  }
}%%
stateDiagram
    state "Flag Bits" as FB {
        [*] --> noUndefs : Bit 0
        noUndefs --> incrLink : Bit 1
        incrLink --> dyldLink : Bit 2
        dyldLink --> bindAtLoad : Bit 3
        bindAtLoad --> prebound : Bit 4
        prebound --> splitSegs : Bit 5
        splitSegs --> lazyInit : Bit 6
        lazyInit --> twoLevel : Bit 7
        twoLevel --> forceFlat : Bit 8
        forceFlat --> ... : ...
        ... --> pie : Bit 22
        pie --> deadStrippableDylib : Bit 23
        deadStrippableDylib --> [*]
    }
    
```






---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>
---

<!-- - **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/). -->
