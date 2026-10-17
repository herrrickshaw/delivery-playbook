# The Delivery Playbook

A field guide to software delivery: classic SDLC models (Waterfall, V-Model, Incremental, Spiral, RAD),
the Agile family (Scrum, Kanban, XP, Lean/Lean Startup, Crystal, SAFe/LeSS), DevOps/CALMS, a
volatility-vs-criticality fit-finder for picking a model, six named process anti-patterns, ten
computer-science-theory results applied to product/tooling decisions (Conway's Law, Little's Law, CAP
theorem, Amdahl's Law, Postel's Law, computational complexity, undecidability, Shannon entropy,
mechanism design, Byzantine fault tolerance), Domain-Driven Design (strategic + tactical), and TOGAF's
ADM cycle — plus a section grounding several of these in how `global-market-scanners` and
`global-stock-screener` actually run SDLC + SAFe + TOGAF together, and a further-reading table pulled
from a personal Zotero/Dropbox document catalog.

**Read it live:** https://claude.ai/artifact/9fGPDJMxVpKfifNeZ55MXj

This repo is the versioned source for that page (`index.html`, a single self-contained file). The
claude.ai link is the canonical place to *read* it — it renders live and supports both light/dark theme;
this repo exists so the content has real git history and can be diffed, reviewed, and reused elsewhere
(e.g. served via GitHub Pages) independent of the artifact platform.

## Updating

Edit `index.html` directly — it's one self-contained HTML file (fonts loaded from Google Fonts, no build
step, no dependencies). After editing here, the live claude.ai copy needs to be republished separately
from the same content; the two aren't auto-synced.

## Status

Living document — not a point-in-time snapshot. Indexed in
[`repo-traffic-analytics/artifacts.yaml`](https://github.com/herrrickshaw/repo-traffic-analytics/blob/main/artifacts.yaml)
alongside the account's other published reference artifacts.

## Further reading (2026-10 update)

Primary sources only. Each URL returned HTTP 200 on 2026-10-17 (checked with curl).

- [DORA research](https://dora.dev/research/) — the program behind the four delivery-performance metrics cited in the Lineage section; the place to check current definitions rather than relying on secondary summaries.
- [Team Topologies: key concepts](https://teamtopologies.com/key-concepts) — the four team types and three interaction modes; the practical follow-on to the Conway's Law item in the CS-theory section.
- [The Scrum Guide](https://scrumguides.org/scrum-guide.html) — the authoritative definition of Scrum, useful for checking the Agile-family section against the source.
- [The Open Group: TOGAF Standard](https://pubs.opengroup.org/togaf-standard/) — official publication of the ADM and its supporting content, backing the TOGAF section.
- [Google SRE Book (table of contents)](https://sre.google/sre-book/table-of-contents/) — free primary text on SLOs, error budgets and toil, extending the DevOps and continuous-delivery section.

Not included: the SAFe framework site (framework.scaledagile.com) returned HTTP 403 to curl, so it could not be verified from this environment.
