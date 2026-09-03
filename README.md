# Apache Fineract — New Command Processing Infrastructure

GSoC 2026 project documentation site for [FINERACT-2169](https://issues.apache.org/jira/browse/FINERACT-2169).

**Live site:** `https://<your-github-username>.github.io/gsoc-2026-fineract/`

> Migrating Apache Fineract's legacy `JsonCommand` handlers to a typed, compile-safe command framework with Jakarta validation, URL-level security, and Resilience4j retry.

---

## Contents

```
gsoc-2026-fineract/
├── index.adoc                  Landing page (hero, stats, workflow, architecture, highlights, footer)
├── sections/
│   ├── 01-introduction.adoc
│   ├── 02-about-fineract.adoc
│   ├── 03-project-overview.adoc
│   ├── 04-problem-statement.adoc
│   ├── 05-existing-architecture.adoc
│   ├── 06-new-command-processing.adoc
│   ├── 07-my-contributions.adoc
│   ├── 08-implementation.adoc
│   ├── 09-testing.adoc
│   ├── 10-challenges.adoc
│   ├── 11-demo.adoc
│   ├── 12-results.adoc
│   ├── 13-future-work.adoc
│   ├── 14-lessons-learned.adoc
│   └── 15-acknowledgements.adoc
├── assets/
│   └── style.css               Custom stylesheet (Apache pastel palette)
├── images/
│   ├── fineract-logo.svg
│   ├── system-architecture.svg
│   ├── workflow-diagram.svg
│   ├── architecture-stack.svg
│   └── lines-per-module.svg
├── docinfo.html                <head> injection (favicon, meta description)
├── docinfo-footer.html         Post-content footer injection
├── .github/workflows/pages.yml GitHub Pages build workflow (Asciidoctor + Ruby)
└── README.md
```

---

## Local preview

Requires Ruby 3+ and Asciidoctor.

```bash
gem install asciidoctor
asciidoctor index.adoc -D _site
cp -r assets images _site
python3 -m http.server 8080 -d _site
# open http://localhost:8080
```

---

## Deploy

The site publishes automatically to GitHub Pages on every push to `main` via `.github/workflows/pages.yml`. Enable Pages once in **repo Settings → Pages → Source: GitHub Actions**.

---

## Editing content

Section content lives in `sections/*.adoc` (AsciiDoc). To edit the landing page hero, stats, workflow cards, or highlights: edit the passthrough HTML blocks inside `index.adoc`.

To restyle: edit `assets/style.css`.

---

## Credits

- **Contributor:** Nidhi Bhawari ([@nidhiii128](https://github.com/nidhiii128))
- **Mentor:** Alex Vidakovic
- **Upstream:** [apache/fineract](https://github.com/apache/fineract)
- **JIRA:** [FINERACT-2169](https://issues.apache.org/jira/browse/FINERACT-2169)

Apache®, Apache Fineract®, and the Fineract logo are trademarks of the Apache Software Foundation. This site is a GSoC 2026 project artifact, not an official ASF publication.
