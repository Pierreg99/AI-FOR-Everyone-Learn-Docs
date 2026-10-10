<div align="center">

<img src="assets/readme-banner.svg" alt="AI for Everyone — Lernen. Entwickeln. Hinterfragen. Ein Projekt von Pierreg99." width="100%">

# AI for Everyone

**Grundlagen verstehen. Agenten entwickeln. KI-Systeme betreiben.**

Ein offener Lern-Guide mit 36 aufeinander abgestimmten Kapiteln auf Deutsch und Englisch.

[![Ausgabe 2.2](https://img.shields.io/badge/Ausgabe-2.2-102e28?style=flat-square&labelColor=1d3e35)](package.json) [![36 Kapitel](https://img.shields.io/badge/Kapitel-36-102e28?style=flat-square&labelColor=1d3e35)](docs/de/README.md) [![Deutsch und Englisch](https://img.shields.io/badge/Sprachen-DE_%2B_EN-102e28?style=flat-square&labelColor=1d3e35)](docs/language-map.md) [![Validierung](https://github.com/Pierreg99/AI-FOR-Everyone-Learn-Docs/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/Pierreg99/AI-FOR-Everyone-Learn-Docs/actions/workflows/ci.yml)

**[Auf Deutsch lesen →](https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/de/)** &nbsp; · &nbsp; **[Read in English →](https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/en/)**

[Deutsche Kapitel](docs/de/README.md) · [English chapters](docs/en/README.md) · [English README](README.md)

</div>

---

Ein Projekt von [Pierreg99](https://github.com/Pierreg99). **Der vereinheitlichte Codex-Guide auf `main` ist die Hauptausgabe.** Die maßgeblichen Quellen liegen in [`docs/de/`](docs/de/README.md) und [`docs/en/`](docs/en/README.md).

## Finde deinen Einstieg

| Dein Ziel | Was du lernst | Hier starten |
| --- | --- | --- |
| **KI verstehen** | Modelle, Machine Learning, Transformer, Sprachmodelle, generative KI und RAG | [KI-Grundlagen](docs/de/01-ai-fundamentals.md) · 6 Kapitel |
| **Agenten entwickeln** | Werkzeuge, Gedächtnis, Kontext, Berechtigungen, Architektur und Tests | [KI-Agenten](docs/de/07-ai-agents.md) · 10 Kapitel |
| **Systeme betreiben** | Beobachtbarkeit, Daten, Inferenz, Recovery, Evaluation, Datenschutz und Kosten | [Beobachtbarkeit](docs/de/19-observability.md) · 12 Kapitel |

Beginne mit dem [Schnellstart](docs/de/getting-started.md), folge einem Lernpfad auf der Website oder stöbere in [allen 36 Kapiteln](docs/de/README.md). Die übrigen Kapitel vertiefen Architektur und Forschungsgrenzen. AGI und ASI sind Fähigkeits- beziehungsweise hypothetische Zukunftskonzepte, keine garantierten Entwicklungsschritte.

## Dein eigener Lernraum

<a href="https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/de/">
  <img src="assets/readme-preview-de.jpg" alt="Deutsche Lern-Website mit Pierreg99-Logo, Kapitelnavigation und Lernfortschritt" width="100%">
</a>

*Die tatsächliche Lern-Website, gebaut aus diesem Repository.*

| Lesen und verstehen | Erkunden und den Überblick behalten |
| --- | --- |
| Jedes Kapitel enthält Lernziel, Beispiel, Grenzen, Übung, Lösung und Originalquellen | Volltextsuche, Themenfilter und drei Lernpfade |
| Deutsche und englische Seiten mit Links zum passenden Kapitel | Gemeinsamer Fortschritt und Lesezeichen für beide Sprachen im selben Browser |
| Responsive helle/dunkle Oberfläche, Kapitelübersicht und Lesefokus (`F`) | Lokaler JSON-Export/Import des Fortschritts und ein persönlicher nächster Lernschritt |
| Kapitel und Navigation bleiben ohne JavaScript lesbar | Architektur-Explorer und beispielhafte Kosten- und Zuverlässigkeitsrechner |

Die Website benötigt weder Konto noch Analyse-Dienst, externe Schriftart oder Laufzeit-API. Fortschritt bleibt im Browser-Speicher; falls dieser nicht verfügbar ist, gilt er nur für die Sitzung. Sicherungsdateien werden lokal verarbeitet. Suche, gespeicherter Fortschritt und interaktive Werkzeuge benötigen JavaScript. Preise in den Rechnern sind Beispielannahmen, keine Anbieterpreise.

## Lernen durch Ausprobieren

Drei kleine Python-Beispiele verwenden nur die Standardbibliothek. Führe sie mit Python 3.10+ im Repository-Verzeichnis aus:

```sh
python examples/retrieval.py --lang de --query "Rückgabe"
python examples/durable_job.py
python examples/evaluate.py
```

Probiere eine einfache Retrieval-Baseline aus, wiederhole eine Operation ohne doppelten Datenbankeffekt und vergleiche Evaluationsergebnisse nach Sprache. Die [Praxisprojekte](docs/de/projects.md) erklären, was du prüfen und wie du die Übungen erweitern kannst.

## Website lokal starten

**Voraussetzungen:** Node.js 22+ und npm. Für `npm run check` wird auch Python 3.10+ benötigt, da es die Beispieltests ausführt.

```sh
npm ci
npm run check
npm run dev
```

Öffne **http://127.0.0.1:4173/**. `npm run build` erzeugt die statische Website in `dist/`; baue sie nach einer Kapiteländerung erneut. Die veröffentlichte Website benötigt keinen Node.js-Prozess.

Für Desktop-/Mobil-Browsertests und Barrierefreiheitsprüfungen:

```sh
npx playwright install chromium
npm run test:e2e
```

## Ein Guide, klare Quelldateien

```text
docs/
├── de/                  Deutsche Kapitel und Referenzseiten
└── en/                  Passende englische Kapitel und Referenzseiten
data/chapters.json       Gemeinsame Kapitelreihenfolge, Themen und Vorwissen
assets/                  Styles, Browser-Skripte und Bilder
scripts/                 Statischer Build, Vorschau-Server und Deployment-Prüfung
examples/                Drei ausführbare Python-Übungen
tests/                   Inhalts-, Link-, Beispiel- und Browsertests
index.html               Website-Vorlage
dist/                    Generierte Ausgabe — von Git ignoriert
```

Bearbeite die maßgeblichen Sprachdateien gemeinsam. Frühere V1.2-Übersichten und Kapitel-Adressen verweisen auf den aktuellen Guide. GitHub Pages veröffentlicht das generierte `dist/`-Artefakt über [den Pages-Workflow](.github/workflows/pages.yml); als Deployment-Quelle muss **GitHub Actions** eingestellt sein.

## Nachschlagen oder mitwirken

| Lesen | Pflegen |
| --- | --- |
| [Schnellstart](docs/de/getting-started.md) | [Mitwirken](CONTRIBUTING.de.md) |
| [Glossar](docs/de/glossary.md) | [Website und Deployment](WEBSITE.md) |
| [Quellen und Vertiefung](docs/de/sources.md) | [Spracharchitektur](docs/language-map.md) |
| [Praxisprojekte](docs/de/projects.md) | [Roadmap](ROADMAP.md) |

Verbessere eine Erklärung, probiere eine Übung aus oder korrigiere eine Quelle. Halte fachlichen Umfang, Beispiele, Übungen und Quellen zwischen Deutsch und Englisch synchron.

---

<div align="center">

**[Jetzt loslernen →](https://pierreg99.github.io/AI-FOR-Everyone-Learn-Docs/de/)**

<sub>AI for Everyone · Pierreg99 · Ausgabe 2.2</sub>

</div>
