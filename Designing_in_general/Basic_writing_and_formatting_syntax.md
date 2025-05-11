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


# [Creating and highlighting code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)


## [Fenced code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#fenced-code-blocks)


You can create fenced code blocks by placing triple backticks ``` before and after the code block.

```
function test() {
  console.log("notice the blank line before this function?");
}
```

---


To display triple backticks in a fenced code block, wrap them inside quadruple backticks.


````
```
Look! You can see my backticks.
```
````


---


## [Syntax highlighting](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting)


You can add an optional language identifier to enable syntax highlighting in your fenced code block.

Syntax highlighting changes the color and style of source code to make it easier to read.

For example, to syntax highlight Ruby code:

````
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
````

This will display the code block with syntax highlighting as below:


```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

GitHub use [Linguist](https://github.com/github-linguist/linguist) to perform language detection and to select [third-party grammars](https://github.com/github-linguist/linguist/blob/main/vendor/README.md) for syntax highlighting. 


We can find out which keywords are valid in [the languages YAML file](https://github.com/github-linguist/linguist/blob/main/lib/linguist/languages.yml).


---

## [Supported color models](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#supported-color-models)


In issues, pull requests, and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

```
The background color is `\#ffffff` for light mode and `\#000000` for dark mode.

```

![Screenshot of rendered GitHub Markdown showing how HEX values within backticks create small circles of color, here white and then black.](https://docs.github.com/assets/cb-11643/images/help/writing/supported-color-models-rendered.png)





Here are the currently supported color models.

**The syntax for the table is:**

````
| Color Model | Syntax          | Example                 | Output                                                                                                                               |
|-------------|-----------------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| HEX         | `` `#RRGGBB` ``   | `` `#0969DA` ``          | ![Screenshot of rendered GitHub Markdown showing how HEX value #0969DA appears with a blue circle.](https://docs.github.com/assets/cb-1558/images/help/writing/supported-color-models-hex-rendered.png)    |
| RGB         | `` `rgb(R,G,B)` `` | `` `rgb(9, 105, 218)` `` | ![Screenshot of rendered GitHub Markdown showing how RGB value 9, 105, 218 appears with a blue circle.](https://docs.github.com/assets/cb-1962/images/help/writing/supported-color-models-rgb-rendered.png)  |
| HSL         | `` `hsl(H,S,L)` `` | `` `hsl(212, 92%, 45%)` ``| ![Screenshot of rendered GitHub Markdown showing how HSL value 212, 92%, 45% appears with a blue circle.](https://docs.github.com/assets/cb-2066/images/help/writing/supported-color-models-hsl-rendered.png) |
````

**The rendered result table is:**

| Color Model | Syntax          | Example                 | Output                                                                                                                               |
|-------------|-----------------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| HEX         | `` `#RRGGBB` ``   | `` `#0969DA` ``          | ![Screenshot of rendered GitHub Markdown showing how HEX value #0969DA appears with a blue circle.](https://docs.github.com/assets/cb-1558/images/help/writing/supported-color-models-hex-rendered.png)    |
| RGB         | `` `rgb(R,G,B)` `` | `` `rgb(9, 105, 218)` `` | ![Screenshot of rendered GitHub Markdown showing how RGB value 9, 105, 218 appears with a blue circle.](https://docs.github.com/assets/cb-1962/images/help/writing/supported-color-models-rgb-rendered.png)  |
| HSL         | `` `hsl(H,S,L)` `` | `` `hsl(212, 92%, 45%)` ``| ![Screenshot of rendered GitHub Markdown showing how HSL value 212, 92%, 45% appears with a blue circle.](https://docs.github.com/assets/cb-2066/images/help/writing/supported-color-models-hsl-rendered.png) |



**Explanation of Changes and Formatting:**

1.  **Table Structure:** The content is formatted using Markdown's pipe table syntax (`|` for columns, `---` for the header separator).
2.  **Column Headers:** I've named the columns "Color Model", "Syntax", "Example", and "Output" based on the pattern of the input data.
3.  **Code Formatting:**
    *   The `Syntax` and `Example` values (like `#RRGGBB` or `#0969DA`) are enclosed in double backticks ` `` ` as per your input format. This creates an inline code span and also allows literal backticks inside if needed, though for these simple cases single backticks ` ` ` would also work fine in standard Markdown. GitHub Flavored Markdown renders ` ``code`` ` a bit differently, often with a red font by default in their documentation style. If you prefer standard monospaced rendering, single backticks (` `code` `) are more common. I've kept ` `` ` to match your input style more closely.
4.  **Image Links:** The Markdown for the images (`![alt text](url)`) is kept as is, so they will render as images in the "Output" column when viewed on GitHub.





---



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

## [Quoting code](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#quoting-code)


You can call out code or a command within a sentence with single backticks. 

````
Use `git status` to list all new or modified files that haven't yet been committed.
````

Use `git status` to list all new or modified files that haven't yet been committed.

---

To format code or text into its own distinct block, use triple backticks.


````
Some basic Git commands are:
```
git status
git add
git commit
```
````

Some basic Git commands are:
```
git status
git add
git commit
```


For more information, see [Creating and highlighting code blocks](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).



---

## [Links](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#links)


You can create an inline link by wrapping link text in brackets `[ ]`, and then wrapping the URL in parentheses `( )`. You can also use the keyboard shortcut Command+K to create a link. When you have text selected, you can paste a URL from your clipboard to automatically create a link from the selection.

You can also create a Markdown hyperlink by highlighting the text and using the keyboard shortcut `Command`+`V`. If you'd like to replace the text with the link, use the keyboard shortcut `Command+Shift`+`V`.


````
This site was built using [GitHub Pages](https://pages.github.com/).
````

This site was built using [GitHub Pages](https://pages.github.com/).

---

## [Section links](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#section-links)


You can link directly to any section that has a heading. To view the automatically generated anchor in a rendered file, hover over the section heading to expose the  icon and click the icon to display the anchor in your browser.

![Screenshot of a README for a repository. To the left of a section heading, a link icon is outlined in dark orange.](https://docs.github.com/assets/cb-55933/images/help/repository/readme-links.png)

If you need to determine the anchor for a heading in a file you are editing, you can use the following basic rules:

* Letters are converted to lower-case.
* Spaces are replaced by hyphens (`-`). Any other whitespace or punctuation characters are removed.
* Leading and trailing whitespace are removed.
* Markup formatting is removed, leaving only the contents (for example, `_italics_` becomes `italics`).
* If the automatically generated anchor for a heading is identical to an earlier anchor in the same document, a unique identifier is generated by appending a hyphen and an auto-incrementing integer.

----




---
>**Licenses:**
>
>- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
>
---

<!-- - **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/). -->
