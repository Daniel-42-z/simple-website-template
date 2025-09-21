---
layout: default
title: Sample Article Page
permalink: /articles/sample-page/
---

# Sample Article Page

You can write new pages using the *markdown* format, with html support for more advanced features. Compare the source of this file at `articles/sample-page.md` and the preview to learn how to add the most important styling and content types.

___

## Headings

# Main heading

## Subheading

### Level 3 heading

___

## Lists

- Bullet points with line break

	Same paragraph

- Second point
	1. Nested lists
	2. Different types of lists can be nested
		- Use either tabs or 4 spaces for indentation, but be consistent
	1. List numbering continues automatically even if the wrong number is used in the source
	
	Non-list paragraph

	1. Insert a non-list paragraph to restart from number 1
	2. Like this

___

## Styling

*Italic* **bold** ~~crossed out~~ ~~**use multiple styling**~~ ***at once***

`inline code`

```python
print("insert code block with proper highlighting")
```

Use latex for equations

Inline: $x$ $\int$ $\frac{1}{2}$

Display:

$$\int\frac{1}{\tan x}\mathrm{d}x$$

___

## Media and Links

[Link name](https://github.com/)

Local image:

![Photo](/media/summer_1am.jpg){: width="50%"}

Web image:

![Arch Linux](https://archlinux.org/static/logos/archlinux-logo-dark-scalable.svg){: width="75%"}

Image with captions (both local and web):

<figure>
	<img src="http://www.winstonhall.org/assets/images/logos/3blue1brown.png" width="30%">
	<figcaption>3Blue1Brown logo</figcaption>
</figure>

Local video:

<video width="75%" height=auto controls>
	<source src="/media/2d-coords-project-to-1d.mp4" type="video/mp4">
</video>
