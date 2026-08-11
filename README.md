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

## Editing

Plain HTML — open a file and edit the text. Shared styling is in `assets/styles.css`, which uses a
small set of CSS custom properties at the top for colour and spacing, and supports light and dark
appearance automatically.

To preview locally:

```
python3 -m http.server 8000
```

then open <http://localhost:8000>.
