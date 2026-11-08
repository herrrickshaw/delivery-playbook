# The Delivery Playbook

A field guide to software delivery, written for product and tooling people who have to pick a
process and defend it. It covers the classic SDLC models (Waterfall, V-Model, Incremental, Spiral,
RAD), the Agile family (Scrum, Kanban, XP, Lean/Lean Startup, Crystal, SAFe/LeSS), DevOps/CALMS,
a volatility-vs-criticality fit-finder for choosing a model, six named process anti-patterns, ten
computer-science results applied to product and tooling decisions (Conway's Law, Little's Law, CAP
theorem, Amdahl's Law, Postel's Law, computational complexity, undecidability, Shannon entropy,
mechanism design, Byzantine fault tolerance), Domain-Driven Design (strategic and tactical), TOGAF's
ADM cycle, essential build pillars for tooling, and a software testing playbook. The output is one
self-contained HTML page, `index.html`.

> Status: maintained — living document, not a point-in-time snapshot. Docs-only repo: one HTML
> file, no code, no data. Opinions are the author's; not professional advice.

**Read it live:** https://claude.ai/artifact/9fGPDJMxVpKfifNeZ55MXj

The claude.ai artifact is the canonical place to *read* the playbook (live render, light and dark
theme). This repo is the versioned source so the content has real git history and can be diffed,
reviewed, and reused elsewhere (for example served via GitHub Pages) independent of the artifact
platform.

## What it does
- Fourteen `<h2>` sections in `index.html`, from "Lineage" through "The software testing playbook".
- Grounds the theory in two real repos: a section shows how
  [`global-market-scanners`](https://github.com/herrrickshaw/global-market-scanners) and
  [`global-stock-screener`](https://github.com/herrrickshaw/global-stock-screener) run SDLC + SAFe +
  TOGAF together (Definition of Done, backlog hierarchy, the gap that closed).
- Names six failure modes: Scrummerfall, Zombie Scrum, Watermelon status, Cargo-cult DevOps, Dark
  agile, Spec-driven paralysis.
- "From your own library": a further-reading table pulled from the author's personal Zotero/Dropbox
  document catalog.
- Testing playbook (§13) with five testing anti-patterns (ice-cream cone, coverage theatre,
  flaky-test tolerance, testing implementation not behaviour, mocking everything).

## Quick start
```bash
git clone https://github.com/herrrickshaw/delivery-playbook.git
cd delivery-playbook
open index.html        # macOS; or double-click the file in any browser
```
There is no build step, no dependencies and nothing to install. Fonts (IBM Plex) are loaded from
Google Fonts, so the page renders in its fallback serif/sans when offline.

## How it works
| Stage | Where | Output |
|---|---|---|
| Author | edit `index.html` by hand (CSS variables at the top define light/dark tokens) | the page |
| Review | git diff / PR on this repo | history |
| Publish | republish the same content to the claude.ai artifact | live page |

The two copies are **not auto-synced**: after editing here, the claude.ai copy must be republished
separately from the same content. `index.html` carries no `<!doctype>` or `<html>` wrapper because
the artifact platform supplies that skeleton at publish time; browsers still render it directly.

## Repository layout
| Path | Purpose |
|---|---|
| `index.html` | The playbook — one self-contained file, no scripts |
| `HOW_TO_USE_WITH_AI.md` | Generic guide for non-programmers: hand the repo to an AI assistant |
| `.github/workflows/quality-gates.yml` | gitleaks secret scan on every push / PR (the only gate that applies; no code to lint) |
| `graphify-out/` | Generated knowledge-graph cache; not hand-edited |

## Limitations and known issues
- The artifact link and this repo can drift; the repo is authoritative for history, the artifact
  for what readers see. Check the commit log before assuming the live page is current.
- The further-reading table references a private Zotero/Dropbox catalog; the documents themselves
  are not in this repo.
- Google Fonts is an external dependency for typography only.

## Related repositories
- [repo-traffic-analytics](https://github.com/herrrickshaw/repo-traffic-analytics) — indexes this
  page in [`artifacts.yaml`](https://github.com/herrrickshaw/repo-traffic-analytics/blob/main/artifacts.yaml)
  alongside the account's other published reference artifacts.
- [global-market-scanners](https://github.com/herrrickshaw/global-market-scanners) and
  [global-stock-screener](https://github.com/herrrickshaw/global-stock-screener) — the worked
  examples in the "Applied" section.

## Licence
No licence file yet — all rights reserved.
