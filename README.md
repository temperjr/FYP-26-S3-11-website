# The Daily Loop — Project Website

Marketing and progress website for **The Daily Loop**, the CSIT321 Final Year Project of
group **FYP-26-S3-11** (topic CSIT-26-S3-21, News Release System Design and Implementation),
SIM Global Education / University of Wollongong.

This is the **project website** required by the subject: a site marketing the project group and
the system being developed. It is **not** the product. The Daily Loop application itself lives in a
separate, private repository.

## Pages

| Page | Purpose |
|---|---|
| `index.html` | Landing page — objective, the problem, what makes the product different, plans, call to action |
| `team.html` | Who is who: the four members, their responsibilities and how the group works |
| `documentation.html` | Deliverables, status and where the project stands |

## Publishing

Static HTML and CSS with no build step and no external dependencies, so it can be served directly
by GitHub Pages.

1. Push this repository to GitHub (it must be **public** for GitHub Pages on a free account).
2. **Settings → Pages → Source:** deploy from a branch, `main`, folder `/ (root)`.
3. The site appears at `https://<user-or-org>.github.io/<repo>/` within a minute or two.

If a paid custom domain is ever used, the subject requires the site to stay live for at least one
month after the final presentation.

## Two rules for this repository

1. **Never commit assessment documents here.** The University treats uploading an assessment item
   to a website as academic misconduct. `documentation.html` links to the group's access-controlled
   shared drive; it does not host the files. The `.gitignore` blocks the common document formats as
   a safety net.
2. **Keep the product code out.** The application source belongs in the private product repository.

## Design system

The site is built on the project design system (documented in TDM Section 6). It is deliberately
small so four people can keep to it:

- **Six colours** — red `#D81F26` (logo, developing, errors), ink `#111111` (text, rules, buttons),
  grey `#5F6672`, line `#E3E6EA`, panel `#F7F8FA`, green `#1E6B3A` (done). Red is only ever the
  brand or a "developing" state; it is never used for ordinary buttons or links.
- **Two typefaces** — Anton for the logo only, Source Sans 3 for everything else. Both are SIL Open
  Font License and self-hosted in `assets/fonts/`, so there is no external font request.
- **Six text sizes, five spacing steps (4/8/16/24/40), three screen sizes** (phone, tablet, desktop).

The header lockup is the masthead capsule reduced to header size, and chips reuse the same capsule
shape, which is what ties the site back to the product identity.

## Editing

Plain HTML — open a file and edit the text. Shared styling is in `assets/styles.css`; the custom
properties at the top of that file are the whole design system. Do not introduce a colour, size or
spacing value that is not already defined there.

To preview locally:

```
python3 -m http.server 8000
```

then open <http://localhost:8000>.
