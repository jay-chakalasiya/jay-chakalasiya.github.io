---
title: "How to Use Markdown in Jekyll Posts"
   
excerpt: "The usage of markdown in jekyll posts with code examples"
excerpt_separator: "<!--more-->"
modified: 2016-09-09T09:55:10-04:00

header:
    overlay_filter: "0.8"

tags: 
  - Jekyll
  - Markdown
  - Tutorial
---
## Front Matter
```yaml
  layout: single #splash, posts, archive
  classes: #wide
  author_profile: true

  read_time: true
  comments: # true
  share: true
  related: true
  show_date: true

  search: true

  toc:  true
  toc_sticky: true # to make toc move with the scrolling
  toc_label:  "Table of Contents"
  toc_icon: "fas fa-scroll"

  header:
    overlay_image:/assets/images/defaults/default-header.jpg
    caption:  "Photo credits"
    overlay_filter: "0.5" # by default black; can also use colors like: rgba(255, 0, 0, 0.5)
    actions:    # to create a button in the overaly, (may be to point to code repo or reference)
        - label: "More Info"
          url: "https://unsplash.com"
  
  excerpt: "Please Add a Good Excerpt Here"

  title: "An Awesome post title"
  tags:
    - First Tag
  categories:
    - First category
```

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

### Text-Alignment
```markdown
Some Text

Some Text
{: style="text-align: left;"}

Some Text
{: style="text-align: center;"}

Some Text
{: style="text-align: right;"}

Some Text
{: style="text-align: justify;"}
```

Some Text

Some Text
{: style="text-align: left;"}

Some Text
{: style="text-align: center;"}

Some Text
{: style="text-align: right;"}

Some Text
{: style="text-align: justify;"}


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


## GitHub Gist Embed

```html
{% raw %}{% gist jay-chakalasiya/1400a5264cfcc394efae3130542d23dd %}{% endraw %}

<script src="https://gist.github.com/jay-chakalasiya/1400a5264cfcc394efae3130542d23dd.js"></script>
```
{% gist jay-chakalasiya/1400a5264cfcc394efae3130542d23dd %}

<script src="https://gist.github.com/jay-chakalasiya/1400a5264cfcc394efae3130542d23dd.js"></script>


## Images
```markdown
![Some Image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/sample.jpg)
```
![Some Image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/sample.jpg)

```markdown
<img src="{{ site.url }}{{ site.baseurl }}/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/sample.jpg" alt="">
```
<img src="{{ site.url }}{{ site.baseurl }}/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/sample.jpg" alt="">

## Image Alignments
```markdown
![left-aligned-image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/small-image.png){: .align-left}    
The written after the image will take up the right space left in the rendering.
``` 
<center>or</center>     
```html
<img src="/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/small-image.png" class="align-left" alt="">    
The written after the image will take up the right space left in the rendering.
``` 
![left-aligned-image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/small-image.png){: .align-left}    
The written after the image will take up the right space left in the rendering.

Just make sure that image is squarish & small enough to give some writing space on the right side, else it might take up whole space

Other options   
```markdown
![center-aligned-image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/small-image.png){: .align-center}
![right-aligned-image](/assets/images/2020-11-16-How-to-Use-Jekyll-Posts/small-image.png){: .align-right}
``` 
Html code can also be used juse replace `align-left` with `align-center` & `align-right` in the provided html code above. 


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

### Internal Content Links
```markdown
{% raw %}[Random Post][random-post]
[random-post]: {{ base_path }}{% post_url 2020-11-16-How-to-Use-Jekyll-Posts %} {% endraw %}
```
[Random Post][random-post]

[random-post]: {{ base_path }}{% post_url 2020-11-16-How-to-Use-Jekyll-Posts %}

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



## Buttons
```html
<a href="#" class="btn btn--primary">Primary Button</a>
<a href="#" class="btn btn--success">Success Button</a>
<a href="#" class="btn btn--warning">Warning Button</a>
<a href="#" class="btn btn--danger">Danger Button</a>
<a href="#" class="btn btn--info">Info Button</a>
```
<a href="#" class="btn">Primary Button</a>          
<a href="#" class="btn btn--success">Success Button</a>         
<a href="#" class="btn btn--warning">Warning Button</a>         
<a href="#" class="btn btn--danger">Danger Button</a>           
<a href="#" class="btn btn--info">Info Button</a>           

```markdown
[Default Button Text](#link){: .btn}
[Primary Button Text](#link){: .btn .btn--primary}
[Success Button Text](#link){: .btn .btn--success}
[Warning Button Text](#link){: .btn .btn--warning}
[Danger Button Text](#link){: .btn .btn--danger}
[Info Button Text](#link){: .btn .btn--info}
[Inverse Button](#link){: .btn .btn--inverse}
[Light Outline Button](#link){: .btn .btn--light-outline}
```
[Default Button Text](#link){: .btn}        
[Primary Button Text](#link){: .btn .btn--primary}      
[Success Button Text](#link){: .btn .btn--success}      
[Warning Button Text](#link){: .btn .btn--warning}      
[Danger Button Text](#link){: .btn .btn--danger}        
[Info Button Text](#link){: .btn .btn--info}        
[Inverse Button](#link){: .btn .btn--inverse}       
[Light Outline Button](#link){: .btn .btn--light-outline}       

```markdown
[X-Large Button](#link){: .btn .btn--primary .btn--x-large}
[Large Button](#link){: .btn .btn--primary .btn--large}
[Default Button](#link){: .btn .btn--primary }
[Small Button](#link){: .btn .btn--primary .btn--small}
```
[X-Large Button](#link){: .btn .btn--primary .btn--x-large}     
[Large Button](#link){: .btn .btn--primary .btn--large}     
[Default Button](#link){: .btn .btn--primary }      
[Small Button](#link){: .btn .btn--primary .btn--small}     


## Notices
```markdown
**Some Notice:** Notice Paragraph will go here...  
{: .notice}
```
**Some Notice:** Notice Paragraph will go here...  
{: .notice}

### Primary     
`{: .notice--primary}`       

**Some Notice:** Notice Paragraph will go here...  
{: .notice--primary}

### Info    
`{: .notice--info}`       

**Some Notice:** Notice Paragraph will go here...  
{: .notice--info}

### Warning     
`{: .notice--warning}`       

**Some Notice:** Notice Paragraph will go here...  
{: .notice--warning}

### Danger     
`{: .notice--danger}`       

**Some Notice:** Notice Paragraph will go here...  
{: .notice--danger}

### Success     
`{: .notice--success}`       

**Some Notice:** Notice Paragraph will go here...  
{: .notice--success}

### Longer Notices      
Wrap them into capture elemets
```html
{% raw %}{% capture notice-2 %}
#### Some Heading element inside    
* You can have lists as well
{% endcapture %}{% endraw %}

<div class="notice">{% raw %}{{ notice-2 | markdownify }}{% endraw %}</div>
```
{% capture notice-2 %}
#### Some Heading element inside    
* You can have lists as well
{% endcapture %}
<div class="notice">
    {{ notice-2 | markdownify }}
</div>


## File Structrue Tree
```bash
    tree /a /f > output.txt
```

## References
All the referecnes attached above will be visible at the end of the document.

