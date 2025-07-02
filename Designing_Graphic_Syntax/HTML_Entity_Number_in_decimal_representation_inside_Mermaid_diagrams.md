---
created: 2025-07-01 05:31:26
author: Cong Le
version: "1.0"
license(s): MIT, CC BY-SA 4.0
copyright: Copyright © 2025 Cong Le. All Rights Reserved.
---


> ⚠️🏗️🚧🦺🧱🪵🪨🪚🛠️👷
> 
> This is a working draft in progress
> 
> ![Loading...](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExMXVjejV3dnVjc2o5MXd3eXBvcDR1cHlzbHQ1Z2R6YjY0ZHpmdjJ6OCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/hL9q5k9dk9l0wGd4e0/giphy.gif)
>
> gif image is provided by [Giphy](https://giphy.com)
> 
> ⚠️🏗️🚧🦺🧱🪵🪨🪚🛠️👷


----


# HTML Entity Number in decimal representation inside Mermaid diagrams
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



----

## 📜 Overview: What are HTML Special Characters?

In HTML, certain characters are "reserved" because they are part of the language's syntax (like `<` and `>`). To display these characters literally, or to show symbols not found on a standard keyboard (like © or €), we use special codes called **HTML Entities**. Think of them as a "secret code" the browser understands to render a specific symbol correctly.

Let's start with a mind map to see the big picture.

```mermaid
---
title: "What are HTML Special Characters?"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY-SA 4.0"
copyright: "Copyright © 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'fontFamily': 'American Typewriter, monospace',
    'logLevel': 'fatal',
    'mindmap': {
	    'nodeAlign': 'center',
	    'padding': 20
    },
    'themeVariables': {
      'primaryColor': '#FC82',
      'primaryTextColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#EBF3',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'fontSize': '20px'
    }
  }
}%%
mindmap
  root)"**HTML Special Characters**"(
    What_are_they))"**What are they?** 🧐"((
    ::icon(fa fa-commenting)
      Codes_for_special_symbols("Codes for special symbols")
      Also_called("Also called **HTML Entities** or **Character References**")
      Ensures correct display in browsers
    Why_use_them))"**Why use them?** 🤔"((
    ::icon(fa fa-question)
        Reserved Characters
        ::icon(fa fa-language)
            To avoid confusing the browser (e.g., `<` for tags)
        Non-Keyboard Characters
        ::icon(fa fa-keyboard)
            To display symbols like ©, ®, €, ™
        Accented Characters
        ::icon(fa fa-language)
            For letters like á, ñ, ü
        Cross-Browser Compatibility
        ::icon(fa fa-share)
            Guarantees consistent rendering everywhere
    How_to_write_them))"**How to write them?** ✍️"((
    ::icon(fa fa-pencil)
        All_entities["All entities start with `&` and end with `;`"]
        Three_primary_formats{{"3️⃣ primary formats"}}
            Entity_Name))"**Entity Name**"((
            ::icon(fa fa-font)
                Descriptive_and_readable("Descriptive & readable<br/>(e.g., `&copy;`)")
            Entity_Number))"**Entity Number** <br/>(Decimal)"((
            ::icon(fa fa-icon)
                Numeric_code["Numeric code<br/>(e.g., `#169;`)"]
            Entity_Number))"**Entity Number**<br/>(Hexadecimal)"((
            ::icon(fa fa-info)
                Hex_code["Hex code, starts with `&#x`<br/>(e.g., `&#xa9;`)"]

```

> [!note]
> As you can see, normal structure format of the HTML entity in decimal representation do not display properly when nested inside Mermaid mind map. The solution for this issue is below.

---

## ⚙️ The Anatomy of an HTML Entity

Every HTML entity follows a specific structure. Let's break it down visually using Graphviz DOT Language to see the components of the Copyright symbol (`©`) in both its named and numbered forms.

**1. Entity Name (`&copy;`)**

```dot
/*
 * title: The Anatomy of an HTML Entity Name
 * author: Cong Le
 * version: 1.0
 * license(s): MIT, CC BY-SA 4.0
 * copyright: Copyright © 2025 Cong Le. All Rights Reserved.
 */
graph {
    node [shape=record, style=filled, fillcolor=lightblue]
    rankdir=LR
    entity [label="{ <start> & | <name> copy | <end> ; }"]
    subgraph cluster_legend {
        label = "Structure of an Entity Name"
        style=dotted
        node [shape=plaintext]
        key [label="Start Delimiter | Entity Name | End Delimiter"]
    }
}
```

**2. Entity Number (`&#169;`)**

```dot
/*
 * title: The Anatomy of an HTML Entity Number
 * author: Cong Le
 * version: 1.0
 * license(s): MIT, CC BY-SA 4.0
 * copyright: Copyright © 2025 Cong Le. All Rights Reserved.
 */
graph {
    node [shape=record, style=filled, fillcolor=lightgreen]
    rankdir=LR
    entity [label="{ <start> & | <pound> # | <number> 169 | <end> ; }"]
     subgraph cluster_legend {
        label = "Structure of an Entity Number";
        style=dotted
        node [shape=plaintext]
        key [label="Start Delimiter | Numeric Identifier | Decimal Code | End Delimiter"]
    }
}
```

As you can see, the core structure is an `&` at the beginning and a `;` at the end, with the specific code sandwiched in between.

> [!note]
> The Structure of HTML Entity Number can be used in Mermaid mind map look like this example `#34;`

-----

## ❓ Developer's Decision Flowchart

When should you use an HTML entity? Here's a simple flowchart to guide your decision-making process.

```mermaid
---
title: "❓ Developer's Decision Flowchart"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY-SA 4.0"
copyright: "Copyright © 2025 Cong Le. All Rights Reserved."
config:
  layout: elk
  theme: base
  look: handDrawn
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%%%%%%% Available curve styles include the following keywords:
%% basis, bumpX, bumpY, cardinal, catmullRom, linear, monotoneX, monotoneY, natural, step, stepAfter, stepBefore.
%%{
  init: {
    'flowchart': { 'htmlLabels': true, 'curve': 'basis' },
    'fontFamily': 'American Typewriter, monospace',
    'logLevel': 'fatal',
    'themeVariables': {
      'primaryColor': '#22BB',
      'primaryTextColor': '#F8B229',
      'lineColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#E2F1',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'fontSize': '20px'
    }
  }
}%%
flowchart TD
    A["Start:<br/>I need to display a character"] --> B{"Is the character '<', '>', or '&'?"}
    B -->|Yes ✅| C["Use its HTML Entity Name! <br> <char>&lt;</char>, <char>&gt;</char>, <char>&amp;</char>"]
    B -->|No ❌| D{"Is the character on a standard keyboard?"}
    D -->|Yes ✅| E["You can type it directly.<br/>e.g., 'A', '1', '$'"]
    D -->|No ❌| F{"Is it a common symbol <br> like ©, ®, or ™?"}
    F --> |Yes ✅| G["Use its a Entity Name for readability.<br> <char>&copy;</char>, <char>&reg;</char>, <char>&trade;</char>"]
    F --> |No ❌| H["Find its Decimal or Hex code and use that in the various format below:<br/>e.g., '#8594;' is the same symbol as <char>#8594;</char>, and the final rendered symbol is →"]

    subgraph Output["Output"]
    style Output fill:#F2F2,stroke:#333,stroke-width:1px, color: #FFFF
    direction LR
        C --> Z["End:<br/>Character displays correctly"]
        E --> Z
        G --> Z
        H --> Z
    end

    style C fill:#9e92,stroke:#333,stroke-width:2px
    style G fill:#9e92,stroke:#333,stroke-width:2px
    style H fill:#fcb2,stroke:#333,stroke-width:2px
```

---

## ⭐ Example: Displaying an Asterisk (`*`)

The asterisk is a good example because while it's on the keyboard, it can sometimes be a special character in programming contexts (like CSS or JavaScript). Using an entity guarantees it's treated as plain text.

Here are the three ways to display it, as shown in the original document:

1.  **HTML Entity Name:** `&ast;`
2.  **HTML Entity Number (Decimal):** `&#42;`
3.  **HTML Entity Number (Hexadecimal):** `&#x2a;`

Here is how you'd write it in your HTML file:

```html
<!-- Using the Entity Name -->
<p>This is a required field&ast;</p>

<!-- Using the Decimal Number -->
<p>This is a required field&#42;</p>

<!-- Using the Hexadecimal Number -->
<p>This is a required field&#x2a;</p>
```

All three lines of code will produce the exact same visual output for the user:

> This is a required field*

---

## 📋 Common Special Characters Table

Here is a handy reference table of some of the most frequently used special characters and their entity codes.

| Result | Description           | Entity Name | Entity Number |
| :----: | --------------------- | :---------: | :-----------: |
|  `<`   | Less than sign        |   `&lt;`    |    `&#60;`    |
|  `>`   | Greater than sign     |   `&gt;`    |    `&#62;`    |
|  `&`   | Ampersand             |   `&amp;`   |    `&#38;`    |
|  `"`   | Double quotation mark |  `&quot;`   |    `&#34;`    |
|  `'`   | Single quotation mark |  `&apos;`   |    `&#39;`    |
|  `©`   | Copyright sign        |  `&copy;`   |   `&#169;`    |
|  `®`   | Registered trademark  |   `&reg;`   |   `&#174;`    |
|  `€`   | Euro sign             |  `&euro;`   |   `&#8364;`   |
|  `™`   | Trademark sign        |  `&trade;`  |   `&#8482;`   |
|        | Non-breaking space    |  `&nbsp;`   |   `&#160;`    |
|  `–`   | En dash               |  `&ndash;`  |   `&#8211;`   |
|  `—`   | Em dash               |  `&mdash;`  |   `&#8212;`   |
|  `←`   | Left arrow            |  `&larr;`   |   `&#8592;`   |
|  `→`   | Right arrow           |  `&rarr;`   |   `&#8594;`   |

---

## HTML Entity Number Rendered inside a Mermaid Mind Map

Here is a mindmap created using Mermaid syntax that organizes all the special characters mentioned above, displaying each one using its `HTML Entity Number (Decimal)` format with a small adjustment, can you tell? 



```mermaid
---
title: "HTML Entity Number Rendered inside a Mermaid Mind Map"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY-SA 4.0"
copyright: "Copyright © 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'fontFamily': 'Fantasy',
    'logLevel': 'fatal',
    'mindmap': {
	    'nodeAlign': 'center',
	    'padding': 10
    },
    'themeVariables': {
      'primaryColor': '#FC82',
      'primaryTextColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#EBF3',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'fontSize': '20px'
    }
  }
}%%
mindmap
  root)"**HTML Special Characters by Decimal Code**"(
    HTML_Reserved_Characters))"**HTML Reserved Characters**"((
        Symbol_1["`#60;`"] %% < %% Less than sign
        Symbol_2["`#62;`"] %% > %% Greater than sign
        Symbol_3["`#38;`"] %% & %% Ampersand
    Punctuation_and_Quotes))"**Punctuation & Quotes**"((
        Symbol_1["`#34;`"] %% " %% Double quotation mark
        Symbol_2["`#39;`"] %% ' %% Single quotation mark
        Symbol_3["`#42;`"] %% * %% Asterisk symbol
    Common_Symbols))"**Common Symbols**"((
        Symbol_1["`#169;`"] %% © %% Copyright Symbol
        Symbol_2["`#174;`"] %% ® %% Registered Symbol
        Symbol_3["`#8482;`"] %% ™ %% Trademark Symbol
        Symbol_4["`#8364;`"] %% € %% Euro Symbol
    Spacing_and_Dashes))"**Spacing & Dashes**"((
        Symbol_1("`#160;`") %% Non-Breaking Space
        Symbol_2("`#8211;`") %% En Dash
        Symbol_3("`#8212;`") %% Em Dash
    Arrows))"**Arrows**"((
        Symbol_1["`#8592;`"] %% ← %% Left Arrow
        Symbol_2["`#8594;`"] %% → %% Right Arrow
    Accented_Characters))"**Accented Characters**"((
        Symbol_1["`#225;`"] %% á
        Symbol_2["`#241;`"] %% ñ
    Combining_Diacritical_Marks))"Combining Diacritical Marks"((
        Character_1{{"`Co#770;ng Le#770;`"}} %% Công Lê
    Currency_Symbols))"Currency Symbols"((
        Character_1{{"`#8383;`"}} %% ₿ %% Bitcoin Sign
    UTF_8_Miscellaneous_Symbols))"UTF-8 Miscellaneous Symbols"((
        Symbol_1["`#9728;`"] %% ☀ %% BLACK SUN WITH RAYS
        Symbol_2["`#9729;`"] %% ☁ %% CLOUD
        Symbol_3["`#9764;`"] %% ☤ %% CADUCEUS
        Symbol_4["`#9769;`"] %% ☩ %% CROSS OF JERUSALEM

```




----


<!-- 
```mermaid
%% Current Mermaid version
info
```  -->


```mermaid
---
title: "CongLeSolutionX"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY-SA 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%{
  init: {
    'flowchart': { 'htmlLabels': false },
    'fontFamily': 'Bradley Hand',
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
  My_Meme@{ img: "https://raw.githubusercontent.com/CongLeSolutionX/CongLeSolutionX/refs/heads/main/assets/images/My-meme-light-bulb-question-marks.png", label: "Ăn uống gì chưa ngừi đẹp?", pos: "b", w: 200, h: 150, constraint: "on" }

  Closing_quote@{ shape: braces, label: "...searching insights in the process of formulating better questions..." }

  Closing_quote ~~~ My_Meme

  Link_to_my_profile{{"<a href='https://github.com/CongLeSolutionX/CongLeSolutionX' target='_blank'>Click here if you care about my profile</a>"}}

  Closing_quote ~~~ My_Meme
  My_Meme animatingEdge@--> Link_to_my_profile
  
  animatingEdge@{ animate: true }



```

---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>- **Creative Commons Attribution-ShareAlike 4.0 International**: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) [![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-sa/4.0/) - Legal details in [LICENSE-CC-BY-SA-4.0](THE_PAST/LICENSE-CC-BY-SA-4.0) and at [Creative Commons official site](https://creativecommons.org/licenses/by-sa/4.0/).
>
---


### 📚 References

For a complete list of all available HTML character entities, you can consult these authoritative sources:

*   **Mozilla Developer Network (MDN):** [HTML character references](https://developer.mozilla.org/en-US/docs/Glossary/Entity)
*   **W3Schools:** [HTML Entity Reference](https://www.w3schools.com/html/html_entities.asp)

-----
