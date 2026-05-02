# GEMINI.md

Instructions for maintaining this profile README.

## What this repo is

GitHub profile README at `tothKarolyDavid/tothKarolyDavid`. Single file: `README.md`. Renders on `https://github.com/tothKarolyDavid`.

## Style direction

**Professional & Clean.** Waving banner header, custom 2-col project cards, `tokyonight` theme for stats, focused socials.

Brand color: `#0078D4` (.NET Blue). Card label background: `#1a1b27`.

## Structure (top-to-bottom)

1. **Banner** — `capsule-render` SVG, name + tagline
2. **Social chips** — LinkedIn, GitHub, Email (shields.io `for-the-badge`)
3. **whoami** — Professional summary and focus areas
4. **whatihavebuilt** — 6 featured projects in 3×2 HTML table
5. **techstack** — Skills categorized by area
6. **stats for nerds** — 4 `github-profile-summary-cards`
7. **Footer** — Inline links to site, LinkedIn, and resume

## Card template

Each project cell uses this pattern:

```md
### [Name](https://github.com/tothKarolyDavid/<repo>)
One-line pitch. Core features.

![lang](https://img.shields.io/badge/<Lang>-<hex>?style=flat&labelColor=1a1b27) ![badge](https://img.shields.io/badge/<label>-<color>?style=flat&labelColor=1a1b27)
```

Wrap pairs of cells in `<table><tr><td width="50%" valign="top">…</td><td width="50%" valign="top">…</td></tr></table>`.

## Updating content

### Add / swap a featured project
Replace one `<td>` block in the `whatihavebuilt` table. Keep 2-col 3-row grid. Use brand colors for language badges (.NET: `512bd4`, Laravel: `ff2d20`, Python: `3776ab`).

### Change tagline / banner desc
Edit URL fragment after `desc=` in the `capsule-render` `<img>`. URL-encode spaces as `%20`.

### Change theme
Search-replace `tokyonight` → other theme. Verify compatibility with `github-profile-summary-cards`.

## External services used

| Service | Purpose |
|---|---|
| `capsule-render.vercel.app` | Header banner SVG |
| `img.shields.io` | All badges |
| `github-profile-summary-cards.vercel.app` | 4 stats cards (theme: `tokyonight`) |

## Verification before committing

- All image URLs return 200.
- All 6 project titles are clickable.
- Stats cards load correctly.
- Mobile viewport: tables stack cleanly.

## Don't do

- Don't use lowercase-only section headers (maintained professional case: `whoami`, `whatihavebuilt`, `techstack`, `stats for nerds`).
- Don't use plain GitHub pin cards.
- Don't add emojis to main section headers.
