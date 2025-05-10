
---


# Designing graphic art in Mermaid syntax



## Flow-chart node that shows an inline image



Mermaid allows basic HTML in node labels.  
That means you can embed an `<img>` tag:

```mermaid
flowchart LR
    %% A plain text start node
    A([Start])

    %% A node whose label is an <img> tag
    B(["<img src='https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/main/my_octocat.png?raw=true' width='80'/>"])

C(["<img src='https://raw.githubusercontent.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/refs/heads/Designing_graphic_syntax/I_Asked_AI_Bots.jpg' width='80'/>"])

    %% Show normal edges
    A --> B
    B --> C
    C --> D([Done])
```

What you get  
• Node B renders as the Octocat icon instead of text.  
• The image travels with the diagram; it is **not** a background for the page.

---


## Sequence diagram with avatars as participants

```mermaid
%% Replace the two avatar URLs with your own if you like
sequenceDiagram
    participant Alice as <img src="https://avatars.githubusercontent.com/u/583231" width="50"/>
    participant Bob   as <img src="https://avatars.githubusercontent.com/u/9919" width="50"/>

    Alice->>Bob: Hi Bob!
    Bob-->>Alice: Hi Alice!
```

Each participant heading shows the picture you supply.


----



## Diagram-level background image (CSS injected via init)

This technique attaches a CSS rule to the SVG root that Mermaid outputs.  
Only the diagram canvas gets the background, not the whole README.

```mermaid
%%{ init: {
      "theme": "base",
      "themeCSS": ".mermaid svg {
                     background-image:url(https://raw.githubusercontent.com/github/explore/main/topics/mona-lisa/mona-lisa.png);
                     background-size:cover;
                     background-position:center;
                   }"
    } }%%
graph TD
    A[Top] --> B[Bottom]
```

Tips  
• Large images may slow down the first render because GitHub caches them on demand.  
• `background-size:cover` keeps the image edge-to-edge inside the SVG.  
• All other styles (grid lines, fonts, etc.) still obey the chosen Mermaid theme.

---


## Node with an SVG logo loaded via a data-URI


Inlining a small image as a data URI avoids separate HTTP requests and guarantees the asset loads even if someone clones your repo privately.

```mermaid
%% Tiny black square (10×10) encoded as an inline SVG data URI
flowchart TD
    X["<img src='data:image/svg+xml;utf8,\
<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2210%22 height=%2210%22>\
<rect width=%2210%22 height=%2210%22 fill=%22black%22/></svg>'/>"] --> Y(Next)
```

---


## Combining images and regular text in one node




```mermaid
flowchart TD
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME/My-meme-orange_2.png?raw=true", label: "CongLeSolutionX", pos: "t", w: 200, h: 150, constraint: "on" }

```


---


```mermaid
graph LR
    node1(["<p style='margin:0'><img src='https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/main/MY_MEME/My-meme-orange.png?raw=true' width='40'/><br/>CongLeSolutionX</p>"])
    node2(["Ăn uống gì chưa ngừi đẹp?"])
    node1 --- node2
```


---



```mermaid
flowchart LR
    node1(["<p style='margin:0'><img src='https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/main/MY_MEME/My-meme-orange.png?raw=true' width='40'/><br/>CongLeSolutionX</p>"])
    node2(["Ăn uống gì chưa ngừi đẹp?"])
    node1 --- node2
```

---


```mermaid
flowchart TD
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME/My-meme-orange-microphone.png?raw=true", label: "CongLeSolutionX", pos: "b", w: 200, h: 150, constraint: "on" }

```



---



```mermaid
---
title: "CongLeSolutionX"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  layout: dagre
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%%%%%%% Available curve styles include the following keywords:
%% basis, bumpX, bumpY, cardinal, catmullRom, linear, monotoneX, monotoneY, natural, step, stepAfter, stepBefore.
%%{
  init: {
    'flowchart': { 'htmlLabels': false, 'curve': 'linear' },
    'fontFamily': 'Comic Sans MS',
    'themeVariables': {
      'primaryColor': '#ffcc80',
      'primaryTextColor': '#111111',
      'lineColor': '#e0e0e0',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#81c784',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'fontSize': '10px'
    }
  }
}%%
flowchart TD
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME/My-meme-orange-microphone.png?raw=true", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }

```

---



```mermaid
---
title: "CongLeSolutionX"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'flowchart': { 'htmlLabels': false },
    'fontFamily': 'Brush Script MT',
    'themeVariables': {
      'primaryColor': '#fc82',
      'primaryTextColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#81c784',
      'secondaryTextColor': '#6C3483',
      'fontSize': '15px'
    }
  }
}%%
flowchart TD
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME_ICONS/Orange-Cloud-Search-Icon-Base-Color-Black-1024x1024.png?raw=true", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }

```


---




```mermaid
---
title: "CongLeSolutionX"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'flowchart': { 'htmlLabels': false },
    'fontFamily': 'Brush Script MT',
    'themeVariables': {
      'primaryColor': '#fc82',
      'primaryTextColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#81c784',
      'secondaryTextColor': '#6C3483',
      'lineColor': '#F8B229',
      'fontSize': '20px'
    }
  }
}%%
flowchart LR
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME_ICONS/Orange-Cloud-Search-Icon-Base-Color-Black-1024x1024.png?raw=true", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }

    Closing_quote@{ shape: braces, label: "Math and code work together to bring interactive art to life!" }

Closing_quote --- My_Meme

```

---





```mermaid
---
title: "CongLeSolutionX"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'flowchart': { 'htmlLabels': false },
    'fontFamily': 'Brush Script MT',
    'themeVariables': {
      'primaryColor': '#fc82',
      'primaryTextColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#81c784',
      'secondaryTextColor': '#6C3483',
      'lineColor': '#F8B229',
      'fontSize': '20px'
    }
  }
}%%
flowchart LR
    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME_ICONS/Orange-Cloud-Search-Icon-Base-Color-Black-1024x1024.png?raw=true", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }

    Closing_quote@{ shape: braces, label: "Math and code work together to bring interactive art to life!" }

My_Meme ~~~ Closing_quote

```


---



```mermaid
---
title: "CHANGE_ME_DADDY"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  layout: dagre
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%%%%%%% Available curve styles include the following keywords:
%% basis, bumpX, bumpY, cardinal, catmullRom, linear, monotoneX, monotoneY, natural, step, stepAfter, stepBefore.
%%{
  init: {
    'flowchart': { 'htmlLabels': false, 'curve': 'linear' },
    'fontFamily': 'Bradley Hand',
    'themeVariables': {
      'primaryColor': '#ffcc80',
      'primaryTextColor': '#000',
      'lineColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#81c784',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'tertiaryColor': '#ef9a9a',
      'fontSize': '15px'
    }
  }
}%%
flowchart TD
%% Nodes
    A("fab:fa-youtube Starter Guide")
    B("fab:fa-youtube Make Flowchart")
    n1@{ icon: "fa:gem", pos: "b", h: 24}
    
    C("fa:fa-book-open Learn More")
    D{"Use the editor"}
    n2(Many shapes)@{ shape: delay}
    
    E(fa:fa-shapes Visual Editor)
    F("fa:fa-chevron-up Add node in toolbar")
    G("fa:fa-comment-dots AI chat")
    H("fa:fa-arrow-left Open AI in side menu")
    I("fa:fa-code Text")
    J(fa:fa-arrow-left Type Mermaid syntax)

    My_Meme@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME_ICONS/Orange-Cloud-Search-Icon-Base-Color-Black-1024x1024.png?raw=true", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }



%% Edge connections between nodes
    A --> My_Meme --> B --> C --> n1 & D & n2
    D -- Build and Design --> E --> F
    D -- Use AI --> G --> H
    D -- Mermaid js --> I --> J

%% Individual node styling. Try the visual editor toolbar for easier styling!
    style E color:#FFFFFF, fill:#AA00FF, stroke:#AA00FF
    style G color:#FFFFFF, stroke:#00C853, fill:#00C853
    style I color:#FFFFFF, stroke:#2962FF, fill:#2962FF

%% You can add notes with two "%" signs in a row!
```



----



<!-- 
## Types of web font

Helvetica (sans-serif)
Arial (sans-serif)
Arial Black (sans-serif)
Verdana (sans-serif)
Tahoma (sans-serif)
Trebuchet MS (sans-serif)
Impact (sans-serif)
Gill Sans (sans-serif)
Times New Roman (serif)
Georgia (serif)
Palatino (serif)
Baskerville (serif)
Andalé Mono (monospace)
Courier (monospace)
Lucida (monospace)
Monaco (monospace)
Bradley Hand (cursive)
Brush Script MT (cursive)
Luminari (fantasy)
Comic Sans MS (cursive) 
-->




---


## Key limitations (current GitHub renderer)



1. Markdown itself still has no notion of “page background.”  
2. GitHub strips any `<style>` blocks that you put *outside* Mermaid; only the `themeCSS` JSON key is honoured.  
3. Only HTTPS or `data:` images render—no `file:` or `blob:` links.  
4. All CSS you inject is scoped to the `<svg class="mermaid">…</svg>` element of that diagram, so it cannot leak into the rest of the README.





