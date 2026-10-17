# tractum-site

Landing page for [Tractum](https://github.com/JordanNewell/tractum) — verifiable multi-agent consensus.

Live at **https://tractum.dev/**

## What's in here

- `index.html` — self-contained landing page. No build step, no framework, no JS bundler. Fonts via Google Fonts CDN, crypto via `@noble/curves` ESM CDN.
- `assets/og.png` — social card (regenerate from `og.html` with headless Chrome at 1200×630).
- `assets/tractum-lockup.svg` + `assets/tractum-mark.svg` — canonical marks from the brand kit.
- `og.html` — source for the social card.

## Architecture

Hand-rolled HTML/CSS. Tractum Brand tokens inlined as CSS custom properties at `:root` (Seal Amber `#FFB000` on `#0A0A0A`). Layout is grid-based (8px spacing). Typography is JetBrains Mono (display) + Space Grotesk (body).

The page is a single `index.html` (~2400 lines including styles). Section anchors in nav are all `#id` references — no client-side router, no SPA.

## Local preview

Open `index.html` in a browser. That's it. No server required for the static content. The interactive receipt verifier fetches `@noble/curves` from `esm.sh` so you'll want network access for that one feature.

## Deploy

Cloudflare Pages, direct upload or git-connected, custom domain `tractum.dev` (zone in CF account).

## Editing

Just edit `index.html`. Brand tokens live at `:root` at the top of the `<style>` block. Section structure is commented with `<!-- =========== SECTION NAME =========== -->` markers.

## Sibling repos

- **[tractum](https://github.com/JordanNewell/tractum)** — the SDK, MCP server, adapters, and full docs at `jordannewell.github.io/tractum/`. This landing links there for everything beyond the pitch.

## Brand

Tractum Brand System v0.1 (Seal Amber). Canonical source: `10_PROJECTS/tractum/brand/` in the vault. Pre-flight before shipping visual changes: amber is `#FFB000`, ≤10% of any surface, no gradients/glow/indigo.

## License

BUSL-1.1 — same as the Tractum SDK. Source-available; converts to MIT on 2030-10-12. See [LICENSE](LICENSE).


<p align="right">
  <a href="https://jordannewell.com" title="Built by Jordan Newell">
    <img src="assets/newell-badge.png" alt="Built by Jordan Newell" width="48" height="48">
  </a>
</p>
