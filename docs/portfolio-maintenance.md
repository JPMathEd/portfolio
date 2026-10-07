# Curated portfolio

The custom design remains a Jekyll site and uses the existing GitHub Pages deployment.
No new service, build workflow, JavaScript dependency, or authentication is required.

## Editing

- Shared layout: `_layouts/portfolio.html`
- Visual system and responsive rules: `assets/css/portfolio.css`
- Navigation: `_data/navigation.yml`
- Homepage: `_pages/about.md`
- Projects index: `_pages/projects.md`
- Project overviews: `_pages/accessible-and-rigorous.html` and `_pages/ai-error-coach.html`
- Complete HTML editions: `_pages/accessible-and-rigorous-toolkit.html` and `_pages/ai-error-coach-capstone.html`
- Course portfolios: `_pages/inst-7100.html` and `_pages/inst-7800.html`
- Shared project cards: `_includes/portfolio-case-studies.html`
- Shared course cards: `_includes/portfolio-courses.html`
- Curated CV: `_pages/cv.md`
- Research and publications: `_pages/publications.html`
- Reusable feature card: `_includes/portfolio-feature.html`

Keep `url: https://jpmathed.github.io` and `baseurl: /portfolio` in `_config.yml`.
Use Liquid's `relative_url` filter for internal paths. Do not hardcode `/Portfolio`.

Unused template examples are excluded from the build, not deleted. Their source
remains available for later adaptation. Only remove an exclusion after replacing
all sample names, titles, and links with real content.

## Source and publication decisions

The October 2026 uploaded CV is the source of truth for the curated CV page.
The previous webpage listed appointments/dates not present in this version; those
were not carried forward without confirmation. The public PDF at
`files/portfolio/Joshua_Plummer_CV.pdf` preserves the supplied CV's professional
content but removes the street address and telephone number. Review professional
contact details and date ranges before merging.

The October 7, 2026 toolkit PDF and its matching LaTeX are the current sources.
The complete HTML edition preserves the seven parts, three sessions, twelve
worksheets, six tables, and 36 references, adapting layout and navigation for
the web. It is available at `/projects/accessible-and-rigorous/toolkit/`.
Worksheet spaces are reading and printing aids, not interactive form fields.

The current download is `files/inst-7100/accessible-and-rigorous-toolkit.pdf`
(56 pages, 393,737 bytes; label as PDF, 393.7 kB). It is an unchanged copy of the
supplied publication. Its metadata reports document tags; this alone does not
establish complete accessibility conformance. HTML remains the primary reading
format. The course page, project overview, and full HTML edition use this PDF.
The older image archive remains in the repository for existing direct links,
but is no longer the featured download.

Toolkit previews are rendered from the current PDF: cover on page 1, announcement
comparison on page 23, and AI Prompt Frame on page 42. The previews link to the
corresponding HTML content. When replacing the PDF, update those images, page
numbers, the complete HTML content, and all download-size labels together.

The case study distinguishes planned sessions from the one-to-one July 17, 2026
delivery of *Your Page, Rebuilt*. The pilot supported a facilitation revision, not
a claim about measured student outcomes or validation of the entire toolkit.
The current toolkit's page 24 is the source for that reflection.

## Adding a project

Create `_pages/short-project-name.html` with front matter:

```yaml
---
layout: portfolio
title: Project title
section: projects
permalink: /projects/short-project-name/
description: A concise description of the project.
---
```

Use the project overviews as structural models: problem, audience, role,
design decisions, artifacts, evidence, and reflection. Label designed, piloted,
and measured results accurately. Add a link from `_pages/projects.md`.

## Verification

The production build is the repository's existing GitHub Pages/Jekyll build.
Locally, with Ruby and the Gemfile dependencies installed:

```sh
bundle install
bundle exec jekyll build
bundle exec jekyll serve
```

Test at `/portfolio/`, `/portfolio/projects/`, `/portfolio/cv/`, and
`/portfolio/projects/accessible-and-rigorous/`. Check narrow screens, keyboard
navigation, the skip link, downloads, and internal anchors. The curated pages use
no client-side JavaScript. A public PDF is not necessarily a tagged PDF; HTML is
the primary accessible reading format.

## Course portfolios and page hierarchy

The homepage and Projects page both include the shared project and course cards.
Edit those cards once in `_includes/portfolio-case-studies.html` or
`_includes/portfolio-courses.html` so their descriptions stay consistent.

- INST 7100 collects adult learning and professional development coursework.
  Accessible & Rigorous is its featured project. The course page currently
  links to the project overview, complete HTML toolkit, and current PDF, with
  a note that further coursework will be added.
- INST 7800 collects AI in Education coursework. Its five required sections stay
  in order: Introduction, Major Projects/Artifacts, Certificates, Reflections,
  and Final Capstone Project. The AI Error Coach overview links to its complete
  HTML capstone and the original PDF.
- Keep project overviews brief. Put detailed evidence in the linked source
  documents or full HTML edition, and label tested, piloted, and proposed work.
- The capstone and toolkit article bodies and submitted PDFs are source documents. A navigation
  or layout update should not rewrite them.

### Adding INST 7100 coursework later

1. Upload public-ready files to `files/inst-7100/` and images to
   `assets/images/portfolio/inst-7100/`. Use lowercase names with hyphens, without
   spaces. Create these directories only when there are files to upload.
2. In `_pages/inst-7100.html`, add each artifact under Major Projects/Artifacts
   with an h3 title, a short first-person summary, and a descriptive link.
3. Use `relative_url` on every internal path. Put file type and size in each
   download link, and disclose untagged PDFs beside the links. HTML summaries
   do not replace a full text alternative for inaccessible source documents.
4. Replace the More coursework note when additional material is ready. Add a
   Reflections section and its section-navigation link when there is actual
   reflection text to publish. Do not invent module names or required sections.
5. Check that both the course page and project overview link to each other.

For the full toolkit, verify all nine main contents links, all twelve worksheet
links, the six tables, and the reciprocal links to the course and overview.
Confirm the PDF has 56 pages and opens from each reading route. The current PDF
has tags; the separate companion PDFs and INST 7800 PDFs retain their existing
accessibility notes. Do not apply one document's tagging status to all downloads.
