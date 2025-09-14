# 📝 TLML Syntax Reference

**TLML (Turbo Lightweight Markup Language)** — lightweight markup made simple. 🌟
All TLML files convert to HTML automatically. 🚀

---

## 1️⃣ Headings

Use slashes to define heading levels:

```tlml
/ Heading 1      → <h1>
// Heading 2     → <h2>
/// Heading 3    → <h3>
```

> **Example:**

```tlml
/ Welcome to TLML
// Features
/// Advanced Tips
```

---

## 2️⃣ Text Formatting ✨

| Syntax         | Result                    |
| -------------- | ------------------------- |
| `%bold%`       | **Bold text**             |
| `^italic^`     | *Italic text*             |
| `` `inline` `` | `Inline code`             |
| `,code,`       | `Monospace / inline code` |

> **Example:**

```tlml
This is %bold% and ^italic^ text with `inline` code.
```

---

## 3️⃣ Lists 🗂️

### Unordered List

```tlml
* Item 1
* Item 2
_ Item 3
```

### Ordered List

```tlml
1. First
2. Second
3. Third
```

> Nesting not yet supported (planned for future updates).

---

## 4️⃣ Tables 📊

Use pipes `|` to define tables:

```tlml
| Name | Age | City |
| John | 20  | NYC  |
| Anna | 25  | LA   |
```

* Each row starts and ends with `|`
* Cells are separated by `|`
* TLML automatically converts it to `<table>` in HTML

---

## 5️⃣ Collapsible Sections ➡️

Use `++` to start and end collapsible sections:

```tlml
++ Section Title
This content will be hidden until expanded.
++
```

* HTML `<details>` and `<summary>` tags are generated automatically.

---

## 6️⃣ Colors 🎨

Wrap text in `[color]`...`[/]` for colored text:

```tlml
[red]Red Text[/]
[blue]Blue Text[/]
[#ff9900]Orange Text[/]
```

* Supports color names, hex codes, and `rgb()`/`rgba()` values.
* HTML `<span style="color:...">` is used.

---

## 7️⃣ Images 🖼️

Syntax:

```tlml
![Alt Text](path/to/image.png)
```

* Path can be relative or absolute.
* Maximum width automatically set to 100% for responsive display.

> **Example:**

```tlml
![Hello Kitty](assets/hello-kitty.png)
```

---

## 8️⃣ Inline Links 🔗

Currently TLML converts links as plain HTML anchor tags:

```tlml
[Google](https://www.google.com)
```

* Converts to: `<a href="https://www.google.com">Google</a>`

---

## 9️⃣ Code Blocks 💻

Use triple backticks for multi-line code:

```tlml
```

function hello() {
console.log("Hello TLML!");
}

```
```

* TLML converts it to `<pre><code>` in HTML.
* Syntax highlighting is up to HTML/CSS styling.

---

## 🔟 Notes & Limitations ⚠️

* TLML **currently only converts to HTML**.
* PDF, DOCX, or EPUB exports are not supported yet.
* Nesting of lists, tables inside collapsible sections, and advanced features may be limited.
* TLML is beginner-friendly and simple: write, preview, export.

---

**💡 Tip:** Use VS Code TLML Preview extension to live-preview your TLML file while editing.
