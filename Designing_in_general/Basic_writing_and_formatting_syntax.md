---
created: 2025-05-10 05:31:26
author: Cong Le
version: "1.0"
license(s): MIT, CC BY 4.0
copyright: Copyright (c) 2025 Cong Le. All Rights Reserved.
source: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
---



# Basic writing and formatting syntax - Sketch notebook
> This content is dual-licensed under your choice of the following licenses:
> 1.  **MIT License:** For the code implementations in Swift and Mermaid provided in this document.
> 2.  **Creative Commons Attribution 4.0 International License (CC BY 4.0):** For all other content, including the text, explanations, and the Mermaid diagrams and illustrations.

---

## [Headings](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#headings)


To create a heading, add one to six \# symbols before your heading text. The number of \# you use will determine the hierarchy level and typeface size of the heading.


````
# A first-level heading
## A second-level heading
### A third-level heading
````

The rendered result is:

# A first-level heading
## A second-level heading
### A third-level heading

---


## [Styling text](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#styling-text)

**The syntax for the table is:**

````
| Style                   | Syntax                              | Keyboard shortcut                               | Example                                 | Output                                  |
|-------------------------|-------------------------------------|-------------------------------------------------|-----------------------------------------|-----------------------------------------|
| Bold                    | `** **` or `__ __`                  | Command+B (Mac) or Ctrl+B (Windows/Linux)       | **This is bold text**                   | **This is bold text**                   |
| Italic                  | `* *` or `_ _`                      | Command+I (Mac) or Ctrl+I (Windows/Linux)       | _This text is italicized_               | _This text is italicized_               |
| Strikethrough           | `~~ ~~` or `~ ~`                    | None                                            | ~~This was mistaken text~~              | ~~This was mistaken text~~              |
| Bold and nested italic  | `** **` and `_ _`                  | None                                            | **This text is _extremely_ important**  | **This text is _extremely_ important**  |
| All bold and italic     | `*** ***`                           | None                                            | ***All this text is important***        | ***All this text is important***        |
| Subscript               | `<sub> </sub>`                     | None                                            | This is a <sub>subscript</sub> text     | This is a <sub>subscript</sub> text     |
| Superscript             | `<sup> </sup>`                     | None                                            | This is a <sup>superscript</sup> text     | This is a <sup>superscript</sup> text     |
| Underline               | `<ins> </ins>`                     | None                                            | This is an <ins>underlined</ins> text  | This is an <ins>underlined</ins> text  |
````

**The rendered result table is** 


| Style                   | Syntax                              | Keyboard shortcut                               | Example                                 | Output                                  |
|-------------------------|-------------------------------------|-------------------------------------------------|-----------------------------------------|-----------------------------------------|
| Bold                    | `** **` or `__ __`                  | Command+B (Mac) or Ctrl+B (Windows/Linux)       | **This is bold text**                   | **This is bold text**                   |
| Italic                  | `* *` or `_ _`                      | Command+I (Mac) or Ctrl+I (Windows/Linux)       | _This text is italicized_               | _This text is italicized_               |
| Strikethrough           | `~~ ~~` or `~ ~`                    | None                                            | ~~This was mistaken text~~              | ~~This was mistaken text~~              |
| Bold and nested italic  | `** **` and `_ _`                  | None                                            | **This text is _extremely_ important**  | **This text is _extremely_ important**  |
| All bold and italic     | `*** ***`                           | None                                            | ***All this text is important***        | ***All this text is important***        |
| Subscript               | `<sub> </sub>`                     | None                                            | This is a <sub>subscript</sub> text     | This is a <sub>subscript</sub> text     |
| Superscript             | `<sup> </sup>`                     | None                                            | This is a <sup>superscript</sup> text     | This is a <sup>superscript</sup> text     |
| Underline               | `<ins> </ins>`                     | None                                            | This is an <ins>underlined</ins> text  | This is an <ins>underlined</ins> text  |



**Explanation of Changes and Formatting:**

1.  **Table Structure:** The content is formatted using Markdown's pipe table syntax (`|` for columns, `---` for the header separator).
2.  **Syntax Column:** The Markdown syntax examples (e.g., `** **`, `* *`) are enclosed in backticks (`` ` ``) to display them as literal code snippets rather than rendering them as styled text. The extraneous em spaces from the original "Italic" syntax line were removed as they were likely for visual alignment in the source text.
3.  **Example Column:** This column shows the Markdown syntax as you would type it.
4.  **Output Column:** This column shows how the Markdown in the "Example" column would render.
5.  **HTML Tags:** HTML tags like `<sub>`, `<sup>`, and `<ins>` are used directly, as Markdown supports inline HTML for functionalities not natively covered. These will render correctly on GitHub.
6.  **Strikethrough Syntax:** The `Syntax` column lists `~~ ~~` or `~ ~` as per your input. Note that `~~text~~` is standard for GitHub Flavored Markdown, while `~text~` typically is not used for strikethrough in GFM. The example correctly uses `~~This was mistaken text~~`.




----

## [Quoting text](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#quoting-text)


You can quote text with a \>, using the syntax below:

````
Text that is not a quote

> Text that is a quote
````

As a result, the quote will be rendered as below:

Text that is not a quote

> Text that is a quote


---




---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>
---

<!-- - **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/). -->
