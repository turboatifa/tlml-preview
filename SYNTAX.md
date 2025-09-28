# TLML — Syntax Reference ✨📄

This file documents **TLML (TLML (Text Layout Markup Language)

---

## 📑 Table of Contents

1. 🔠 Headings
2. ✍️ Paragraphs and line breaks
3. 🎨 Inline formatting (bold, italic, monospace, colors)
4. 📋 Lists (unordered & ordered)
5. 💬 Blockquotes
6. 💻 Code blocks & syntax highlighting
7. 📊 Tables
8. 🖼️ Links, images, audio & video (media)
9. 📂 Collapsible sections
10. 📝 Comments
11. 🔖 Footnotes
12. 🧩 Special blocks / fallback rule

---

## 1. 🔠 Headings

Use leading slashes to indicate heading level. One slash = H1, two = H2, three = H3.

```
/ This is H1
// This is H2
/// This is H3
```

---

## 2. ✍️ Paragraphs and line breaks

A blank line separates paragraphs. To force a single-line break inside a paragraph, end the line with two spaces.

```
This is a paragraph.  
This is the same paragraph but on the next line.

This starts a new paragraph.
```

---

## 3. 🎨 Inline formatting

**Bold**: wrap text with percent signs.

```
%bold text%
```

**Italic**: wrap text with carets.

```
^italic text^
```

**Monospace / inline code**: use commas with backtick style.

```
`,code,`
```

**Colors**: add `[color]` before the element.

```
[red] Red text
[green]%bold green text%
```

**Font size**:

```
[size=20px] Big text here
```

---

## 4. 📋 Lists

**Unordered lists**:

```
_ Item one
_ Item two
```

**Ordered lists**:

```
1 First item
2 Second item
```

Nested:

```
_ Parent
  _ Child
    _ Grandchild
```

---

## 5. 💬 Blockquotes

```
* This is a quote *
```

---

## 6. 💻 Code blocks & syntax highlighting

````
```python
print("Hello TLML")
```
````

Inline: `,inline code,`

---

## 7. 📊 Tables

```
/table
| Name | Age |
| Ali  | 13  |
| Sara | 14  |
/end
```

---

## 8. 🖼️ Media

**Links**: `[Click here](https://example.com)`
**Image**: `![Alt](url)`
**Audio**: `[audio](url.mp3)` 🎵
**Video**: `[video](url.mp4)` 🎬

---

## 9. 📂 Collapsible sections

```
/collapse Title
Hidden content here...
/endcollapse
```

---

## 10. 📝 Comments

```
: This line won’t show
```

---

## 11. 🔖 Footnotes

```
Here is a note[1].

[1]: This is the footnote.
```

---

## 12. 🧩 Fallback rule

Unknown lines are treated as paragraphs. Exporters should safely render or ignore unknown tags.

---

## 🌟 Quick TLML Example

```
/ TLML Quick Example
%Bold% and ^italic^ and `,inline,` all work!

/table
| Key | Value |
| TLML | Markup |
/end

_ List item
  _ Nested item

/collapse More info
Extra hidden text here!
/endcollapse
```

---

## ✅ Notes for developers

* 🎨 Colors accept both names and hex.
* 🎵 Media placeholders let you add assets later.
* 🔒 Exporters should sanitize input.

✨ That’s it — TLML is lightweight, fun, and ready to use! 🚀
