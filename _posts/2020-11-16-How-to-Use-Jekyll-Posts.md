---
title: "How to Use Markdown in Jekyll Posts"

excerpt: "The usage of markdown in jekyll posts with code examples"
excerpt_separator: "<!--more-->"
modified: 2016-09-09T09:55:10-04:00

tags: 
  - Jekyll
  - Markdown
  - Tutorial
---
## Front Matter

## Headings
### Test Heading
```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
Heading **has to come in order** to make them properly organized in Table Of Contents. Heading 2 is customized for this Jekyll site to be used as headings, It will automatically draw a horizontal ruler to make it look more appealing.

As best practices for the text/paragraph, `don't start with tab or spaces`. Add a blank line to add a linebreak in the rendered output or end the line with 2 or more spaces.

## Text-Formatting

| Emphasis               | Code                   |
| ---------------------- | ---------------------- |
| **Bold**               | `**Bold**`             |
| _Italic_               | `_Italic_`             |
| **_Bold & Italic_**    | `**_Bold & Italic_**`  | 
| `Inline code`          | ```Inline code```      |



## Blockquotes   
```markdown
> This is a Block Quote
```
> This is a Block Quote  

Block quotes could be written in multiple paragraphs, by staring all lines with `>`, There could be Quote inside quote using `>>`. Quotes can includes all other markdown elements as well.

## Lists
### Ordered List    
```markdown
1. First Item
    1. First Sub-Item    
       Can add Paragraph inside the listitem
    2. Second Sub-Item
       > can have blockquotes inside as well
2. Second Item
3. Third Item
4. Fourth Item
```
1. First Item
    1. First Sub-Item    
       Can add Paragraph inside the listitem
    2. Second Sub-Item
       > can have blockquotes inside as well
2. Second Item
3. Third Item
4. Fourth Item

### Unordered List
```markdown
- First Item
    - First Sub-Item    
      Can add Paragraph inside the listitem
    - Second Sub-Item
      > can have blockquotes inside as well
- Second Item
+ Third Item
* Fourth Item
```
- First Item
    - First Sub-Item    
      Can add Paragraph inside the listitem
    - Second Sub-Item
      > can have blockquotes inside as well
- Second Item
+ Third Item
* Fourth Item

Its best practice to use one delimiter in the unordered list, the example is just to show the possibilities.

## Code-Blocks
```markdown
\```python
    import numpy as np
    print(np.array([1,2,3]))
\```
```

```python
    import numpy as np
    print(np.array([1,2,3]))
```
Ignore the `\` symbol, Other laguages are also supported like ruby, java, c, markdown, etc.

GitHub Flavored Markdown [fenced code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/) are supported. To modify styling and highlight colors edit `/_sass/syntax.scss`.


## Images
```markdown
![Some Image](/assets/images/sample.jpg)
```
![Some Image](/assets/images/sample.jpg)

```markdown
<img src="{{ site.url }}{{ site.baseurl }}/assets/images/sample.jpg" alt="">
```
<img src="{{ site.url }}{{ site.baseurl }}/assets/images/sample.jpg" alt="">


## Referencing
```markdown
Some-text [^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>
```
Some-text [^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>


## Horizontal Rules
```markdown
***
___
____________________________________
```
***
---
____________________________________


## Links
```markdown
You are at [jay-chakalasiya.github.io](https://jay-chakalasiya.github.io).
```
You are at [jay-chakalasiya.github.io](https://jay-chakalasiya.github.io).


### Links with titles   
Or you can do this with adding title
```markdown
You are at [jay-chakalasiya.github.io](https://jay-chakalasiya.github.io "The best github blog, JK :p").
```
You are at [jay-chakalasiya.github.io](https://jay-chakalasiya.github.io "The best github blog").

### URLs & Email Addresses
```markdown
<https://jay-chakalasiya.github.io>
<sample@gnail.com>
```
<https://jay-chakalasiya.github.io>     
<sample@gmail.com>



## Tables

```markdown
| Align Left Column      | Align Center Column    | Align Right Column  |
| ---------------------- | :--------------------: | ------------------: |
| Row1                   | Row1                   | Row1                |
| Row2                   | Row2                   | Row2                |
| Row3                   | Row3                   | Row3                |
| Row4                   | Row4                   | Row4                |
```

| Align Left Column      | Align Center Column    | Align Right Column  |
| ---------------------- | :--------------------: | ------------------: |
| Row1                   | Row1                   | Row1                |
| Row2                   | Row2                   | Row2                |
| Row3                   | Row3                   | Row3                |
| Row4                   | Row4                   | Row4                |











### GitHub Gist Embed

An example of a Gist embed below.

{% gist mmistakes/6589546 %}
