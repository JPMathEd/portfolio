# Canvas-Safe Announcement Starter Template
### Companion file to the PD handout — *Engaging Canvas Announcements with HTML + AI*

Two copy-paste assets below:

1. **The AI constraint block** — paste this at the start of any new AI conversation before building Canvas content.
2. **The starter template** — a complete, Canvas-safe announcement. Swap the two brand colors (`#12294B` navy, `#C05A00` accent), replace every `[PLACEHOLDER]`, and paste into Canvas's HTML editor (the `</>` button).

---

## 1. AI Constraint Block

```
Before we build this, hard constraints for Canvas's editor: when
Canvas saves content it strips <style> blocks, external font imports,
<script> tags, and <html>/<head>/<body> wrappers. Only inline
style="..." attributes on individual elements survive. So:
 1. No <style> block -- every rule goes inline on the element itself.
 2. No external fonts -- use system stacks (Georgia,serif or
    Arial,sans-serif).
 3. No CSS variables -- hardcode real values on each element.
 4. No :hover / pseudo-classes -- static styling only.
 5. No @media queries -- for mobile-friendly layouts use
    display:flex;flex-wrap:wrap or grid repeat(auto-fit,minmax(...)).
 6. No JavaScript -- everything static.
 7. No page wrapper -- output a content fragment; one outer <div> max.
 8. Whole-pixel values only (no 0.5px borders).
Give me the result as a single HTML fragment I can paste into the
Canvas HTML editor.
```

---

## 2. Starter Template

Structure at a glance:

```
Outer card <div>
├── HEADER            course label + week number, announcement title
├── BODY
│   ├── Intro paragraph
│   ├── EXAM ALERT    (exam weeks only — delete otherwise)
│   ├── COVERAGE CARD
│   │   ├── Day One   subheader + description
│   │   └── Day Two   subheader + description
│   ├── RESOURCES     flex grid of linked cards
│   ├── OFFICE HOURS  with booking link
│   └── REMINDER      left-accented "questions welcome" box
└── FOOTER            sign-off + Email Me button
```

Full template (line breaks inside `style="..."` attributes are legal HTML — the wrapping is only for readability):

```html
<!-- ==============================================================
     WEEKLY ANNOUNCEMENT TEMPLATE  (Canvas-safe: all styles inline)
     WEEKLY CHECKLIST -- this comment never displays to students:
     [ ] Week number + title (header)
     [ ] Intro paragraph
     [ ] Day One / Day Two topics + descriptions
     [ ] EXAM ALERT box -- keep on exam weeks, DELETE otherwise
     [ ] Resource links -- replace every [CANVAS LINK]
     [ ] Replace [YOUR EMAIL] in the footer (first week only)
     ============================================================== -->

<div style="max-width:660px;margin:0 auto;background:#f5f4f0;
  border:1px solid #ccc9c0;border-radius:12px;overflow:hidden;
  font-family:Georgia,serif;">

  <!-- HEADER -->
  <div style="background:#12294B;padding:1.8rem 2.2rem 1.5rem;
    border-top:5px solid #C05A00;">
    <p style="font-size:11px;letter-spacing:0.13em;text-transform:uppercase;
      color:#b8cfe8;margin:0 0 0.45rem;font-weight:500;
      font-family:Arial,sans-serif;">[COURSE NAME] &nbsp;&middot;&nbsp;
      Week [WEEK NUMBER]</p>
    <h1 style="font-family:Georgia,serif;font-size:26px;font-weight:600;
      color:#ffffff;margin:0;line-height:1.3;">[ANNOUNCEMENT TITLE]</h1>
  </div>

  <!-- BODY -->
  <div style="padding:1.7rem 2.2rem 1.8rem;background:#f5f4f0;">

    <!-- INTRO: keep to 1-2 sentences -->
    <p style="font-size:15.5px;line-height:1.78;color:#2a2825;
      margin:0 0 1.2rem;font-family:Georgia,serif;">
      [INTRO -- welcome line and a one-sentence preview of the week.]
    </p>

    <!-- EXAM ALERT (exam weeks only -- delete this block otherwise) -->
    <div style="background:#fdf6e3;border:1px solid #e0c060;
      border-radius:8px;padding:0.8rem 1.1rem;margin:0 0 1.2rem;
      font-size:14px;color:#5a4500;font-family:Georgia,serif;">
      <strong>EXAM:</strong> [Exam name] on [date]. [One logistics line.]
    </div>

    <!-- COVERAGE CARD -->
    <div style="border:1px solid #d4cfc6;border-radius:10px;
      overflow:hidden;margin:0 0 1.2rem;background:#ffffff;">
      <div style="background:#12294B;padding:0.55rem 1.1rem;">
        <span style="font-size:12px;letter-spacing:0.1em;
          text-transform:uppercase;color:#ffffff;font-weight:600;
          font-family:Arial,sans-serif;">Coverage</span>
      </div>

      <!-- DAY ONE -->
      <div style="background:#C05A00;padding:0.35rem 1.1rem;">
        <span style="font-size:11px;letter-spacing:0.1em;
          text-transform:uppercase;color:#ffffff;font-weight:600;
          font-family:Arial,sans-serif;">Day One &mdash; [SECTION #:
          TOPIC]</span>
      </div>
      <div style="padding:0.85rem 1.1rem;">
        <p style="font-size:14px;color:#2a2825;line-height:1.65;margin:0;
          font-family:Georgia,serif;">[Brief description of Day One.]</p>
      </div>

      <!-- DAY TWO -->
      <div style="background:#C05A00;padding:0.35rem 1.1rem;">
        <span style="font-size:11px;letter-spacing:0.1em;
          text-transform:uppercase;color:#ffffff;font-weight:600;
          font-family:Arial,sans-serif;">Day Two &mdash; [SECTION #:
          TOPIC]</span>
      </div>
      <div style="padding:0.85rem 1.1rem;">
        <p style="font-size:14px;color:#2a2825;line-height:1.65;margin:0;
          font-family:Georgia,serif;">[Brief description of Day Two.]</p>
      </div>
    </div>

    <!-- RESOURCES: duplicate a card per resource; if the grid ends
         uneven, add an empty filler div to balance it -->
    <p style="font-size:13px;letter-spacing:0.08em;text-transform:uppercase;
      color:#12294B;font-weight:600;margin:0 0 0.6rem;
      font-family:Arial,sans-serif;">This Week's Resources</p>
    <div style="display:flex;flex-wrap:wrap;gap:10px;margin:0 0 1.2rem;">

      <a href="[CANVAS LINK]" aria-label="Open [RESOURCE NAME] in Canvas"
        style="flex:1 1 180px;display:flex;flex-direction:column;
        align-items:center;gap:8px;padding:14px 10px;background:#ffffff;
        border:1px solid #d4cfc6;border-radius:12px;text-decoration:none;
        text-align:center;">
        <span style="width:36px;height:36px;background:#12294B;
          border-radius:8px;display:flex;align-items:center;
          justify-content:center;font-size:11px;font-weight:700;
          color:#ffffff;font-family:Arial,sans-serif;">[BADGE]</span>
        <span style="font-size:12px;font-family:Georgia,serif;
          font-weight:600;color:#12294B;line-height:1.35;">
          [RESOURCE NAME]</span>
      </a>
      <!-- ...more resource cards... -->

    </div>

    <!-- OFFICE HOURS -->
    <p style="font-size:13px;letter-spacing:0.08em;text-transform:uppercase;
      color:#12294B;font-weight:600;margin:0 0 0.5rem;
      font-family:Arial,sans-serif;">Office Hours</p>
    <p style="font-size:14px;color:#2a2825;line-height:1.7;
      margin:0 0 1.2rem;font-family:Georgia,serif;">
      [Days] &middot; [Times] &middot; [Location]. <a href="[BOOKING LINK]"
      aria-label="Schedule an office hours appointment"
      style="color:#a34f00;font-weight:600;">Schedule an appointment.</a>
    </p>

    <!-- REMINDER -->
    <div style="border-left:3px solid #C05A00;background:#ffffff;
      border-top:1px solid #d4cfc6;border-right:1px solid #d4cfc6;
      border-bottom:1px solid #d4cfc6;border-radius:0 8px 8px 0;
      padding:0.85rem 1.1rem;font-size:14px;color:#2a2825;
      line-height:1.65;font-family:Georgia,serif;">
      <strong style="color:#12294B;">Questions are always welcome.</strong>
      If anything is unclear or you hit a snag, my inbox is open.
    </div>

  </div>

  <!-- FOOTER -->
  <div style="background:#12294B;padding:0.95rem 2.2rem;display:flex;
    align-items:center;justify-content:space-between;flex-wrap:wrap;
    gap:12px;">
    <span style="font-size:13px;color:#c8daf0;
      font-family:Arial,sans-serif;">Have a great week!</span>
    <a href="mailto:[YOUR EMAIL]" aria-label="Email your instructor"
      style="font-size:13px;font-weight:600;color:#ffffff;
      background:#a34f00;border:1px solid #c46000;padding:5px 16px;
      border-radius:20px;text-decoration:none;
      font-family:Arial,sans-serif;">&#9993;&nbsp; Email Me Anytime</a>
  </div>

</div>
```

---

## Before You Post — Quick Checklist

- [ ] Every `[PLACEHOLDER]` replaced (search the code for `[` to be sure)
- [ ] Exam alert kept or deleted as appropriate
- [ ] All links tested in Student View
- [ ] Colors swapped to your institution's palette
- [ ] Accessibility spot-check: contrast, descriptive link text, no emoji-as-content
