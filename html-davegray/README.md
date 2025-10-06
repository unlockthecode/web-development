# HTML Learning Notes

These notes represent exactly what I’ve learned so far while studying HTML from [Dave Gray’s HTML Full Course for Beginners](https://youtu.be/mJgBOIoGihA). This README is here for transparency, tracking, and sharing the scope of my current HTML understanding.

---

## General Concepts

- `index.html` is commonly served by web servers as the root, but it’s not strictly required.
- Begin each document with `<!DOCTYPE html>` and set the `lang` attribute on `<html>`.
- Use `<meta charset="UTF-8">` inside the `<head>` to define character encoding.
- Use the [W3C Markup Validation Service](https://validator.w3.org) to check for valid HTML.

---

## Visual Studio Code Setup

**Extensions Used:**
- `Live Server` – Live preview in the browser.
- `HTML CSS Support` – Enhanced autocomplete and linting.
- `vscode-icons`, `GitHub Theme` – Optional for UI improvements.

---

## VS Code Shortcuts Learnt

| Shortcut             | Action                           |
| -------------------- | -------------------------------- |
| `element + Tab`      | Expand tag (e.g. `html + Tab`)   |
| `Alt + L`, `Alt + O` | Open with Live Server            |
| `Alt + Z`            | Toggle word wrap                 |
| `Shift + Alt + ↓/↑`  | Duplicate or move selected lines |
| `Ctrl + D`           | Select next occurrence           |
| `Shift + Alt + F`    | Format document                  |
| `Shift + Alt + I`    | Add cursor to line ends          |
| `Ctrl + H`           | Find and replace                 |
| `Ctrl + Shift + I`   | Open GitHub Copilot Chat         |
| `"input:text" + Tab` | Autocomplete input field         |
| `Shift + Alt + A`    | Comment/uncomment selected lines |

---

## Extra Resources

* [https://placehold.co](https://placehold.co)
* [https://unsplash.com](https://unsplash.com)
* [https://www.pexels.com](https://www.pexels.com)
* [https://pixabay.com](https://pixabay.com)
* [https://canva.com](https://canva.com)
* [https://tinypng.com](https://tinypng.com)
* [https://coolors.co](https://coolors.co)

---

## Basic HTML Document Structure

```html
<html lang="en">
  <head>
    <!-- Metadata, title, links, scripts, styles -->
  </head>
  <body>
    <!-- Visible content -->
  </body>
</html>
````

---

## Key HTML Elements & Usage I Know

| Element     | Purpose                                               |
| ----------- | ----------------------------------------------------- |
| `<head>`    | Metadata, links, scripts, styles (not visible)        |
| `<header>`  | Top section (e.g. logo, nav)                          |
| `<footer>`  | Bottom section (e.g. contact, copyright)              |
| `<nav>`     | Navigation links (use `aria-label` for accessibility) |
| `<main>`    | Main page content                                     |
| `<aside>`   | Sidebar or related content                            |
| `<section>` | Thematic grouping of content                          |
| `<article>` | Self-contained content                                |
| `<div>`     | Generic block-level container                         |
| `<span>`    | Generic inline container                              |

---

## Text & Semantic Elements

* Use one `<h1>` per page, followed by `<h2>`, `<h3>`, etc.
* Use `<p>` for paragraph content.
* `<hr>` for thematic breaks, `<br>` for line breaks (sparingly).
* Common block-level elements: `<div>`, `<p>`, `<section>`, `<article>`, `<header>`, `<footer>`, `<form>`, `<table>`, `<blockquote>`.
* Common inline elements: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<input>`, `<button>`, `<code>`, `<small>`, `<sub>`, `<sup>`.
* Semantic tags: `<em>`, `<strong>`, `<abbr>`, `<address>`, `<mark>`, `<time>`, `<code>`.
* Comments: `<!-- Comment -->`

---

## Lists

* `<ol>` – Ordered list
* `<ul>` – Unordered list
* `<li>` – List item
* `<dl>` – Description list

  * `<dt>` – Term
  * `<dd>` – Description

---

## 🔗 Links

```html
<a href="https://example.com">Basic link</a>
<a href="#section-id">Internal link</a>
<a href="https://example.com" target="_blank">New tab</a>
```

---

## Images & Figures

```html
<img src="image.jpg" alt="Description" width="300" height="200" loading="lazy" />

<figure>
  <img src="..." />
  <figcaption>Caption text</figcaption>
</figure>

<code>&lt;h1&gt;Hello World!&lt;/h1&gt;</code>
```

---

## Collapsible Content

```html
<details>
  <summary>Click to expand</summary>
  <p>Hidden content</p>
</details>
```

---

## Tables

```html
<table>
  <caption>Table Caption</caption>
  <thead>
    <tr><th scope="col">Header</th></tr>
  </thead>
  <tbody>
    <tr><td>Data</td></tr>
  </tbody>
  <tfoot>
    <tr><td>Footer</td></tr>
  </tfoot>
</table>
```

* Use `colspan` or `rowspan` to span columns or rows.

---

## Forms & Inputs

**Testing form submissions:** [https://httpbin.org/post](https://httpbin.org/post)

```html
<form action="https://httpbin.org/post" method="post">
  <fieldset>
    <legend>Group Name</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required />
  </fieldset>
  <input type="submit" value="Submit" />
</form>
```

**Common Input Types:**

* text, email, tel, number, date, password, checkbox, radio
* submit, reset, file, hidden, button, color, range, search
* time, url, week, month

**Important Attributes:**

* `type`, `id`, `name`, `value`, `placeholder`, `required`, `pattern`, `min`, `max`, `step`, `minlength`, `maxlength`, `autocomplete`

**Other Form Elements:**

```html
<select id="color" name="color" multiple>
  <option value="red">Red</option>
  <option value="green">Green</option>
</select>

<textarea name="message"></textarea>
```

---

## 🎨 Styling & CSS Tips

* Use classes for layout/spacing instead of `&nbsp;`

```html
<p class="indented">Indented text</p>
```

```css
.indented { margin-left: 20px; }
```

* Remove default paragraph spacing in containers:

```css
.container p {
  margin: 0;
  padding: 0;
  line-height: 1.4;
}
```

* Add spacing to the last paragraph in a section:

```css
.section p:last-child {
  margin-bottom: 1em;
}
```

* Keep link color consistent:

```css
a, a:visited, a:active, a:focus {
  color: whitesmoke;
}
```

---

## Problems & Solutions I've Encountered

* Use `<span title="...">` for tooltips when `<abbr>` doesn’t fit the use case.
* Avoid `&nbsp;` — use CSS classes for spacing and indentation.
* Control spacing with CSS instead of relying on extra `<p>` or `<br>`.
* Use `target="_blank"` to open links in a new tab.
* Update the `<link>` to your CSS file per page if needed.

---

## Webpage Layout Terms

| Section      | Tag        |
| ------------ | ---------- |
| Navigation   | `<nav>`    |
| Main Content | `<main>`   |
| Sidebar      | `<aside>`  |
| Footer       | `<footer>` |

---

## Final Notes

This README reflects **only** what I’ve learned so far — no more, no less. It will evolve as I continue learning HTML and building on this foundation.