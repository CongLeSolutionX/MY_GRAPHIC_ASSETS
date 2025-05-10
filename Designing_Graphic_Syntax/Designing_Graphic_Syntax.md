
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
graph LR
    node1(["<p style='margin:0'><img src='https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/main/MY_MEME/My-meme-orange.png?raw=true' width='40'/><br/>CongLeSolutionX</p>"])
    node2(["Ăn uống gì chưa ngừi đẹp?"])
    node1 --- node2
```



---


## Key limitations (current GitHub renderer)



1. Markdown itself still has no notion of “page background.”  
2. GitHub strips any `<style>` blocks that you put *outside* Mermaid; only the `themeCSS` JSON key is honoured.  
3. Only HTTPS or `data:` images render—no `file:` or `blob:` links.  
4. All CSS you inject is scoped to the `<svg class="mermaid">…</svg>` element of that diagram, so it cannot leak into the rest of the README.





