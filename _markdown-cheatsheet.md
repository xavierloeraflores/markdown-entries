---
title: "_Markdown Cheatsheet"
date: 2023-11-18T23:20:16-08:00
draft: true
categories: ["Meta"]
---

# Heading 1

## Heading 2

### Heading 3 w/ custom heading id {#custom-id}

#### Heading 4

##### Heading 5

---

Standard Text

**Bold Text**

_Italicized Text_

~~Strikethrough Text~~

&nbsp;Spaced Text

&nbsp;&nbsp;&nbsp;&nbsp;Indented Text

Footnoted Text[^1]

Hidden Text:

[Hidden Text]: #

---

> ⚠️ **Warning:** This is a warning

> 🗒️ **Note:** This is a note

> 💡 **Tip:** This is a tooltip

---

List w/ Dash:

- List Item 1
- List Item 2

List w/ Asterisk:

- List Item w/ Asterisk 1
- List Item w/ Asterisk 2

Numbered List:

1. Numbered List Item 1
2. Numbered List Item 2

---

`Code`

```
#code block
a := 1
b := 2
c := a + b
```

example.go:

```go
#code block with language support
a := 1
b := 2
c := a + b
```

---

> Quote

> Multiline Quote: This is an example of a multline quote that spans multiple lines. This can be used with large pieces of text and can indicate quotes from other sources.

> Quote
>
> > Nested Quote

---

[Link](/posts/_markdown-cheatsheet)

[Linking to Heading IDs](#custom-id)

Automatic URL Link: https://www.google.com

Disabled URL Link: `https://www.google.com`

Image:
![Image](/static/images/xavier.jpg)

[Read More on Images](/posts/_image)

Linked Image:

## [![Linked Image](/static/images/xavier.jpg)](/posts/_image)

Table:
| Header Col A | Header Col B |
| ----------- | ----------- |
| Row 1 A | Row 1 B |
| Row 2 A | Row 2 B |

Aligned Table:
| Header Col A | Header Col B | Header Col C |
| :--- | :----: | ---: |
| Row 1 A | Row 1 B | Row 1 C |
| Row 2 A | Row 2 B | Row 2 C |

---

Horizontal Rules

---

---

---

## Horizontal Rule with Heading

---

Task List:

- [x] Task List Item 1
- [ ] Task List Item 2

term
: definition

: definition with no term

Text with Footnote[^1]

[^1]: Footnote Definition
