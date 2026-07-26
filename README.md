# brandondavidcole.com

Personal bio site for Brandon David Cole. One static page, no build step.
Its job: rank #1 for "Brandon Cole" / "Brandon David Cole" and anchor the
professional first page of Google.

**Live:** https://brandondavidcole.com

## Stack

- Single `index.html` — plain HTML/CSS, fonts from Google Fonts.
- Hosted on GitHub Pages (`main` branch, root).
- Custom domain via the `CNAME` file in this repo.

## Files

| File         | Purpose                                              |
|--------------|------------------------------------------------------|
| `index.html` | The whole site.                                      |
| `CNAME`      | Tells GitHub Pages the custom domain. Do not delete. |
| `README.md`  | This file.                                           |

## Deploy / update

It's a static file, so updating = replacing it.

1. Edit `index.html` (or upload a new version).
2. Commit to `main`.
3. GitHub Pages redeploys in ~1 min. Hard-refresh to bust cache.

## First-time setup (already done, kept for reference)

**GitHub:** Settings → Pages → Source: *Deploy from branch*, `main` / root.
Custom domain: `brandondavidcole.com`. Then enable **Enforce HTTPS** once the
DNS check goes green.

**Namecheap** (Advanced DNS) — delete the default parking + redirect records first, then:

| Type  | Host | Value                             |
|-------|------|-----------------------------------|
| A     | @    | 185.199.108.153                   |
| A     | @    | 185.199.109.153                   |
| A     | @    | 185.199.110.153                   |
| A     | @    | 185.199.111.153                   |
| CNAME | www  | YOUR-GITHUB-USERNAME.github.io    |

DNS can take minutes to ~24h to propagate.

## Before calling it done — swap these placeholders in `index.html`

Search the file for `REPLACE`:

- [ ] `REPLACE@YOURDOMAIN.com` — contact email (top-right + footer schema)
- [ ] `linkedin.com/in/REPLACE-ME` — LinkedIn URL (**highest priority** — the
      `sameAs` schema uses this to tell Google your LinkedIn and this page are
      the same person; that link fuses your first page together)
- [ ] `REPLACE-WITH-AGENCY-URL` — VDO Aigency URL

IMDb link is already live. Family office is intentionally unnamed — add it only
if you want your search results tied to theirs.

## SEO notes

- The `<title>`, meta description, and JSON-LD `Person` schema are the parts that
  rank. Keep the name in the title and H1.
- Cross-link both ways: LinkedIn → this site, this site → LinkedIn/IMDb.
- Keep it on the apex domain (`brandondavidcole.com`) — the domain name matching
  your name is doing real ranking work. Don't bury it on a subpath.
