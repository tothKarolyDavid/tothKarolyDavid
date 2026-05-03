# GEMINI.md

Instructions for maintaining this profile README.

## What this repo is

GitHub profile README at `tothKarolyDavid/tothKarolyDavid`. Single file: `README.md`. Renders on `https://github.com/tothKarolyDavid`.

## Style direction

**Professional & Clean with a Synthwave/Hacker Edge.** Animated terminal glitch banner header, custom 2-col project cards, `tokyonight` theme for stats, focused socials.

Brand colors: Primary `#421a8d` (Deep Purple), Accents `#ff00ff` (Magenta) & `#00ffff` (Cyan). Card label background: `#1a1b27`.

## Structure (top-to-bottom)

1. **Banner** — Animated terminal glitch header from `gitbanner.saviru.me`.
2. **Social chips** — LinkedIn (shields.io `for-the-badge`)
3. **whoami** — Professional summary and focus areas
4. **whathaveibuilt** — 6 featured projects in 3×2 HTML table
5. **whatdoiusetobuild** — Skills categorized by area

## Card template

Each project cell uses this exact pattern:

```md
### [Name](https://github.com/tothKarolyDavid/<repo>)
One-line pitch. Core features.
```

Wrap pairs of cells in `<table><tr><td width="50%" valign="top">…</td><td width="50%" valign="top">…</td></tr></table>`.

## Updating content

### Add / swap a featured project
Replace one `<td>` block in the `whathaveibuilt` table. Keep 2-col 3-row grid (6 total). Use brand colors for language badges (.NET: `512bd4`, Laravel: `ff2d20`, Python: `3776ab`).

### Change tagline / banner desc
Edit URL fragment after `desc=` in the `gitbanner` `<img>`. URL-encode spaces as `%20`, pipes/dots left as-is. Verify URL returns 200 before committing.

### Change theme
Search-replace `tokyonight` → other supported theme name (e.g. `radical`). Verify compatibility with `github-profile-summary-cards` (accepts `tokyonight`, rejects `tokyo_night`).

## External services used

| Service | Purpose | Notes |
|---|---|---|
| `gitbanner.saviru.me` | Terminal glitch banner | Params: name, desc, theme, glitch |
| `img.shields.io` | All badges | `for-the-badge` for chips, `flat` for cards |
| `github-profile-summary-cards.vercel.app` | 4 stats cards | Theme `tokyonight` (no underscore) |

## Verification before committing

```bash
# Verify all image URLs return 200
grep -oE 'https?://[^")]+\' README.md | sort -u | while read u; do
 printf '%s -> %s\n' "$u" "$(curl -sIL -o /dev/null -w %{http_code} --max-time 10 "$u")"
done
```

Then open `https://github.com/tothKarolyDavid` in browser. Toggle GitHub light/dark theme. Confirm:
- Banner renders, no broken-image icon
- All 6 project card titles are clickable links
- Mobile viewport: tables stack OK

## Don't do

- Don't add emoji to section headers (kept lowercase, dryly named: whoami, whathaveibuilt, whatdoiusetobuild).
- Don't use plain GitHub pin cards — custom 2-col table is the established style.