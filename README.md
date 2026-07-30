# claudeway-site

Landing page for [Claudeway](https://github.com/JordanNewell/claudeway) — verifiable multi-agent consensus for Claude.

Live at **https://jordannewell.github.io/claudeway-site/**

## What's in here

- `index.html` — self-contained landing page. No build step, no framework, no JS bundler. Fonts via Google Fonts CDN, crypto via `@noble/curves` ESM CDN.
- `assets/og.png` — social card.
- `assets/favicon.svg` — canonical NEWELL N mark.

## Architecture

Hand-rolled HTML/CSS. NEWELL Brand System tokens inlined as CSS custom properties at `:root`. Layout is grid-based (8px spacing). Typography is Space Grotesk (display + body) + JetBrains Mono (code/technical).

The page is a single `index.html` (~2100 lines including styles). Section anchors in nav are all `#id` references — no client-side router, no SPA.

## Local preview

Open `index.html` in a browser. That's it. No server required for the static content. The interactive receipt verifier fetches `@noble/curves` from `esm.sh` so you'll want network access for that one feature.

## Deploy

GitHub Pages, main branch, root directory. The repo has no build step — push to main, Pages serves it.

To use a custom subdomain (e.g. `claudeway.jordannewell.com`):

1. Add a `CNAME` file containing `claudeway.jordannewell.com`
2. At your DNS provider, add a CNAME record: `claudeway.jordannewell.com → jordannewell.github.io`
3. Wait for HTTPS provisioning (~10 minutes)
4. Update the `og:image` and `og:url` meta tags in `index.html` to the new domain

## Editing

Just edit `index.html`. Brand tokens live at `:root` at the top of the `<style>` block. Section structure is commented with `<!-- =========== SECTION NAME =========== -->` markers.

## Sibling repos

- **[claudeway](https://github.com/JordanNewell/claudeway)** — the SDK, MCP server, adapters, and full docs at `jordannewell.github.io/claudeway/`. This landing links there for everything beyond the pitch.

## Brand

NEWELL Brand System. Canonical source: `e:/vaults/anything.xyz/50_Projects/brand-system/`. Pre-flight before shipping visual changes.

## License

MIT — same as the Claudeway SDK.
