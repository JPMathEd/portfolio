# Accessibility Checklist
### Verify before you publish — every page, every time

The four criteria below match the session outcome exactly. A page passes when all four pass.

---

**☐ 1. Heading hierarchy.**
Headings are real heading tags (`<h2>`, `<h3>`) in logical order, starting at `<h2>` — never bolded paragraph text doing a heading's job, and never an `<h1>` (Canvas already renders the page title as the h1).
*Pass test:* Run the accessibility checker in the Canvas editor toolbar; the heading outline reads like a table of contents.

**☐ 2. Color contrast.**
Every text/background pair meets WCAG 4.5:1. Watch for the two usual offenders: light gray "fine print" and text lightened with `opacity`.
*Pass test:* Check the actual hex pairs at webaim.org/resources/contrastchecker. Decorative borders and accents are exempt; readable text is not.

**☐ 3. Alternative text.**
Every image has meaningful alt text written by a human.
*Pass test:* No `[DESCRIBE IMAGE]` placeholders survive, and no alt text merely repeats the file name. If the page has no images, this criterion passes by absence.

**☐ 4. Canvas-ready inline styling.**
The page saves and renders intact: inline styles only, no `<style>` or `<script>` blocks, no document wrapper — Canvas strips them, and what depends on them breaks silently.
*Pass test:* Save, then view the page as a student (Student View), once on a phone or narrow window.

**Riding along with every check:** link text says where the link goes ("Get MyMathLab login help," never "click here"), and emoji decorate but never carry meaning alone.

---

> **The principle this list exists for:** An AI's statement that a page is accessible is not evidence that it is. The prompt asks; this checklist verifies; you own what gets published.

*Part of "Accessibility for the Modern Learner" — Toolkit Section 5.*
