---
math: true  # enable math mode
title: Notes for using this theme(Chirpy)
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [chirpy,note,en]     # TAG names should always be lowercase
render_with_liquid: false
---

## Good Front Matter (updating):

```
---
math: true  # enable math mode
title: Notes for using this theme(Chirpy)
date: YYYY-MM-DD HH:MM:SS +0800 #UTC+8
categories: [Note]
tags: [chirpy,note,en]     # TAG names should always be lowercase
---
```

## Insert an Image:
```
![img-description](/assets/img/sample/my_img.png){: w="700" h="400" .left}
```
Here, `left` can also be `right` and `normal`.

## Filepath Highlight
```
`/path/to/a/file.extend`{: .filepath}
```

## URL Link
```
[text](http://your/link/)
```

## Prompt
```
{: .prompt-info}
```
where `info` can be replaced by `tip`, `warning` and `danger`.
> this is a tip
{: .prompt-tip}
> this is a info
{: .prompt-info}
> this is a warning
{: .prompt-warning}
> this is a danger
{: .prompt-danger}

## Insert Videos

```liquid
{% include embed/{Platform}.html id='{ID}' %}
```
```liquid
{% include embed/bilibili.html id='BV1GJ411x7h7' %}
```
> if you don't want the above parts to be rendered, using `render_with_liquid: false` in the **Front Matter**
{: .prompt-tip}

## Useful Link
a possible useful link is [https://blandalpha.github.io/posts/Hello_World/](https://blandalpha.github.io/posts/Hello_World/)

## Some Advanced Markdown Tricks
you can draw many kinds of diagrams with 'mermaid' plugin that is already in chirpy theme:

```mermaid
flowchart LR
  A --> B
```
and also almost any kinds of charts you want. See [tutorial of Mermaid](https://mermaid.js.org/intro/syntax-reference.html) for further information.
