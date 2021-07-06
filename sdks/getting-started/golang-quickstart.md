---
layout: sdks
title: GoLang Quickstart
permalink: /sdks/getting-started/golang-quickstart
---

Most of the docs-as-code solutions use lightweight markup syntax, often Markdown. So let's learn a bit more about Markdown. Markdown is a shorthand syntax for HTML. Instead of using `ul` and `li` tags, for example, you use asterisks (`*`). Instead of using `h2` tags, you use hashes (`##`). There's a Markdown tag for most of the commonly used HTML elements, but not all of them.

{% if site.format == "web" %}
* TOC
{:toc}
{% endif %}

## Sample Markdown syntax

To get a sense of the Markdown syntax, look at this sample:

```
## Heading 2

This is a bulleted list:

* fireStructuredText item
* second item
* third item

This is a numbered list:

1. Click this **button**.
2. Go to [this site](http://www.example.com).
3. See this image:

![My alt tag](myimagefile.png)
```

Markdown is meant to be kept simple, so there isn't a comprehensive Markdown tag for each HTML tag. For example, if you need `figure` elements and `figcaption` elements, you'll need to use HTML. What's nice about Markdown is that if the Markdown syntax doesn't provide the tag you need, you can just use HTML.

## Development by popular demand versus by committee

John Gruber, a blogger, created Markdown as a way to simplify HTML (see his [Markdown documentation here](http://daringfireball.net/projects/markdown/)). Others adopted it, and many made modifications to include the syntax they needed. As a result, there are various "flavors" of Markdown, such as [Github-flavored Markdown](https://help.github.com/articles/github-flavored-markdown/), [Multimarkdown](http://fletcherpenney.net/multimarkdown/), [kramdown](https://kramdown.gettalong.org/), [CommonMark](https://commonmark.org/), and more.

In contrast, DITA is a committee-based XML architecture derived from a committee. There aren't lots of different flavors and spinoffs of DITA based on how people customized the tags. There's an official DITA spec that is agreed upon by the DITA OASIS committee. Markdown doesn't have that kind of committee, so it evolves on its own as people choose to implement it.

## Why developers love Markdown

In many development tools (particularly [static site generators](https://www.staticgen.com/)) that you use for publishing documentation, many of them will use Markdown. For example, Github uses Markdown. If you upload files containing Markdown and use an md file extension, Github will automatically render the Markdown into HTML.

Markdown has appeal (especially with developers) for various reasons:

* You can work in text-file formats using your favorite code editor.
* You can treat the Markdown files with the same workflow and routing as code.
* Markdown is easy to learn, so you can focus on the content instead of the formatting.

## Why not use a more semantically rich markup?

Why not use a more semantically rich markup language like DITA? Although you can also work with DITA in a text editor, it's a lot harder to read the code with all the XML tag syntax. For example, look at the tags required by DITA for a simple instruction about printing a page:

```xml
<task id="task_mhs_zjk_pp">
    <title>Printing a page</title>
    <taskbody>
<steps>
        <stepsection>To print a page:</stepsection>
    <step>
        <cmd>Go to <menucascade>
            <uicontrol>File</uicontrol><uicontrol>Print</uicontrol>
        </menucascade></cmd>
    </step>
    <step>
        <cmd>Click the <uicontrol>Print</uicontrol> button.</cmd>
    </step>
</steps>
    </taskbody>
</task>
```

Now compare the same syntax with Markdown:

```markdown
## Print a page

1. Go to **File > Print**.
2. Click the **Print** button.
```
