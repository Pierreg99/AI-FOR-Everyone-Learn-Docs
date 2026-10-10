# Language architecture

The unified Codex guide on `main` is the canonical edition. The repository entry points are [English](../README.md) and [German](../README.de.md); the complete chapter indexes are [English](en/README.md) and [German](de/README.md).

Every numbered chapter has its canonical German Markdown source at `docs/de/{slug}.md` and its canonical English source at `docs/en/{slug}.md`. The ordered metadata lives in `data/chapters.json`. Both editions share chapter numbers, technical coverage, examples, exercises, limits, and references. Localized titles and summaries are read directly from the Markdown. German and English index, quick-start, glossary, sources, and projects pages follow the same directory structure.

Legacy root Markdown files and the original first 24 chapters in `docs/` point to the canonical locations; these links are deliberately preserved. The V1.2 index files point to the current full indexes. New links should target the canonical editions.

The build outputs HTML in `dist/docs/de/` and `dist/docs/en/`, with stable translation links between matched chapters. The site has no runtime translation service. A content check verifies all pairs, structural sections, and local links.

---

[Komplette Website: Deutsch](https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/de/) · [Full website: English](https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/en/)
