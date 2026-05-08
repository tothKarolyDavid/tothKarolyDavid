# AGENTS.md

Technical specification and maintenance manifest for the profile `README.md`.

## Metadata & Inspiration

- **Owner:** [tothKarolyDavid](https://github.com/tothKarolyDavid)
- **Inspiration:** [andrasbacsai/andrasbacsai](https://github.com/andrasbacsai/andrasbacsai)
- **Design Philosophy:** Professional, Clean, Synthwave Edge. Minimalist section headers.

## Content Breakdown

| Section | Content Description | Implementation |
| :--- | :--- | :--- |
| **Banner** | Animated waving header with name. | `capsule-render.vercel.app` (SVG) |
| **Socials** | LinkedIn badge. | `img.shields.io` (for-the-badge) |
| **whoami** | Professional summary and tech focus. | Plain Markdown |
| **whathaveibuilt** | 6 featured projects in a 3×2 grid. | HTML `<table>` with custom labels |
| **whatdoiusetobuild** | Skill matrix by area. | Markdown Table |
| **mystats** | GitHub activity and language metrics. | `github-profile-summary-cards` |

## External Services & Credits

This profile utilizes the following tools and services:

1.  **[capsule-render](https://github.com/kyechan9k/capsule-render)**: Dynamic SVG header generation.
2.  **[Shields.io](https://shields.io/)**: Badge generation for socials and project labels.
3.  **[github-profile-summary-cards](https://github.com/vn7n24fzkq/github-profile-summary-cards)**: Visualizing GitHub stats and activity.

## Maintenance Guidelines

- **Typography:** Section headers must be `###` lowercase (e.g., `### whoami`).
- **Color Palette:**
  - Primary Accent: `#3d1c9f` (Deep Purple)
  - Label Background: `#1a1b27`
- **Project Cards:**
  - Use 50% width `<td>` blocks.
  - Languages: .NET (`512bd4`), Laravel (`ff2d20`), Python (`3776ab`).
- **Validation:**
  - Verify all image URLs return `200` before committing.
  - Test responsiveness on mobile viewports (tables should stack or scale gracefully).

---
*This file is intended for use by AI agents and maintainers to ensure consistency with the established profile style.*
