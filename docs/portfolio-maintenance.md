# Curated portfolio

The custom design remains a Jekyll site and uses the existing GitHub Pages deployment.
No new service, build workflow, JavaScript dependency, or authentication is required.

## Editing

- Shared layout: `_layouts/portfolio.html`
- Visual system and responsive rules: `assets/css/portfolio.css`
- Navigation: `_data/navigation.yml`
- Homepage: `_pages/about.md`
- Projects index: `_pages/projects.md`
- Featured case study: `_pages/accessible-and-rigorous.html`
- Curated CV: `_pages/cv.md`
- Research and publications: `_pages/publications.html`
- Reusable feature card: `_includes/portfolio-feature.html`

Keep `url: https://jpmathed.github.io` and `baseurl: /portfolio` in `_config.yml`.
Use Liquid's `relative_url` filter for internal paths. Do not hardcode `/Portfolio`.

Unused template examples are excluded from the build, not deleted. Their source
remains available for later adaptation. Only remove an exclusion after replacing
all sample names, titles, and links with real content.

## Source and publication decisions

The September 2026 uploaded CV is the source of truth for the curated CV page.
The previous webpage listed appointments/dates not present in this version; those
were not carried forward without confirmation. The public PDF at
`files/portfolio/Joshua_Plummer_CV.pdf` preserves the supplied CV's professional
content but removes the street address and telephone number. Review professional
contact details and date ranges before merging.

The uploaded toolkit was a ZIP of 58 numbered PNG images, not a PDF. Its archive
is preserved as supplied at `files/portfolio/Accessible_and_Rigorous_Source_Pages.zip`.
The case study has a semantic HTML overview and explicitly labels the original
image archive's accessibility limitations. Replacing it with a properly tagged,
searchable source PDF is a worthwhile follow-up; do not describe this archive as
accessible or rename it to `.pdf`.

The case study distinguishes planned sessions from the one-to-one July 17, 2026
delivery of *Your Page, Rebuilt*. The pilot supported a facilitation revision, not
a claim about measured student outcomes or validation of the entire toolkit.
The provided toolkit's page 25 is the source for that reflection.

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

Use the featured case study as a structural model: problem, audience, role,
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
