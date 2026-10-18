# Visual brief: mdz logo cuts

## Source

- Topic: Phase 5 brand SVGs for mdz (page → LLM-ready markdown)
- Source files: `assets/icon.svg`, `assets/icon-animated.svg`, `assets/logo.svg`, `assets/logo-animated.svg` in `/root/mdz`, plus `design/tokens.json` (dark palette)
- Audience: someone about to run the `logo-kit-svg` skill on a CLI/MCP/extension repo
- Platform and dimensions: README embed 904×256 banner, extension icon 512×512

## Evidence pack

| Claim or asset | Status | Source | Limitation |
|---|---|---|---|
| Product converts arbitrary web pages to structured markdown locally | verified | `/root/mdz/README.md` | tagline paraphrased |
| Dark theme tokens are the only allowed brand hexes | verified | `/root/mdz/design/tokens.json` | light set unused in marks |
| Shipped four SVGs under repo `assets/` | verified | `/root/mdz/assets/*.svg` | |
| Extension store icon must match square mark | verified | `/root/mdz/apps/extension/assets/icon.png` | raster derived from `icon.svg` |
| README embed uses animated banner | verified | `/root/mdz/README.md` | |
| Mark reduced to a folded page plus one blue hash after four review rounds | verified | git 132120..aa19c7f in `/root/mdz` | earlier versions dropped |

## Five-second takeaway

After five seconds, the viewer should read a folded page carrying one blue hash, understand that mdz ships as CLI, MCP, and browser extension, and see the banner's real terminal line showing what the tool prints.

## Visual decision

- Primary job: identify (app icon) and orient (README banner)
- Information topology: folded page → one hash; banner adds wordmark, tagline, three delivery pills, and a terminal panel
- Layout family: icon-in-panel + horizontal README strip (mark left, type right, hairline rule at right edge)
- Why this structure fits: mdz is not a diff tool; the mark sells "a page becomes structure" with one glyph instead of a diagram
- Dominant visual element: `#` in `primary` — only saturated shape in the 16px icon
- Accent color and its function: `#2f6feb` marks markdown syntax emerging from muted body lines
- Rejected ideas: (1) git branch / hunk diff metaphor (reads as ApplyDiff, not mdz); (2) `M↓Z` arrow monogram (illegible at 16px); (3) full-page browser chrome in the icon (cluttered favicon); (4) gradients, glow, or drop shadows (forbidden by design spec and token discipline)
- Production method: hand-authored SVG with SMIL on animated pair only

## Cuts

Four rounds, each rejected on a real defect:

1. **Page with two grey text lines, `#` and `-` in blue.** Rejected: two focal points fighting, and the grey bars turn to mush below 32px.
2. **Dog-ear page, hash built from four straight bars.** Rejected: the hash read as a 4-cell grid because the verticals were upright with no overhang, i.e. it looked like a calendar.
3. **Page + hash, tile with a stroked border.** Rejected: double frame (tile edge plus page edge) competed with the glyph; the page also read as a phone because the aspect was 1:1.65 with a 23% corner radius.
4. **Shipped: folded page, one hash, one frame.** Tile is fill-only. Page is 3:4 with small radius so it reads as paper. Flap gets its own darker fill so the fold reads as folded rather than a clipped corner. Hash uses round caps and the lighter `accent` blue at 5.3:1 against the page.

Measured contrast in the shipped icon: page/tile 1.41:1, border/page 2.07:1, hash/page 5.3:1. Every hex comes from `design/tokens.json`; no filter, no gradient, no shadow.
