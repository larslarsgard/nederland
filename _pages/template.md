---
layout: post
title: "Tufte Jekyll Feature Reference Post"
subtitle: "A complete cheatsheet for text, images, side notes, and math."
date: 2026-08-12
---

<span class="newthought">Starting a new section</span> with a small-caps opening phrase is a classic Tufte typographic choice. Use this HTML span at the start of major paragraphs to give your writing structure.

---

### 1. Typography & Basic Formatting

Standard Markdown formatting works exactly as expected:

* **Bold text** for emphasis.
* *Italicized text* for subtle highlights.
* `Inline code` for file paths or commands.
* Blockquotes for citations:

> "Design is not just what it looks like and feels like. Design is how it works."

---

### 2. Sidenotes & Margin Notes

Because standard GitHub Pages does not support custom Liquid tags, use these HTML snippets instead.

#### Sidenote (Numbered)
Sidenotes automatically assign a superscript number in the text<label for="sn-1" class="margin-toggle sidenote-number"></label><input type="checkbox" id="sn-1" class="margin-toggle"/><span class="sidenote">This is a numbered sidenote in the right margin. On mobile screens, tapping the number toggles this text directly under the line!</span> and place the commentary in the right-hand margin.

#### Margin Note (Unnumbered)
If you want an unnumbered note in the margin without a superscript in the main text, use a margin note.<label for="mn-1" class="margin-toggle">&#8853;</label><input type="checkbox" id="mn-1" class="margin-toggle"/><span class="marginnote">This is an unnumbered margin note. Notice there is no number in the body paragraph!</span>

---

### 3. Images & Media

Tufte Jekyll offers three distinct ways to display images:

#### Option A: Standard Centered Image
Use standard Markdown for regular inline photos.

![Studio workspace](/assets/images/workspace.jpg)

#### Option B: Margin Image
Place a small photo alongside your main body text in the right margin:

<label for="mn-img" class="margin-toggle">&#8853;</label><input type="checkbox" id="mn-img" class="margin-toggle"/><span class="marginnote"><img src="/assets/images/thumbnail.jpg" alt="Quick photo"/><br/>A quick snapshot alongside the main text.</span>

#### Option C: Full-Width Image
For high-resolution photos or panoramas, stretch the image across both the main text column and the right margin:

<figure class="fullwidth">
  <img src="/assets/images/panorama.jpg" alt="Panoramic view of the city" />
  <figcaption>A full-width figure that spans the entire layout grid.</figcaption>
</figure>

---

### 4. Code Blocks & Data Tables

#### Code Block
```python
def publish_post(title, date):
    file_name = f"_posts/{date}-{title.lower().replace(' ', '-')}.md"
    print(f"Creating post at: {file_name}")
