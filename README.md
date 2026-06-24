# Markdown zu PDF mit GitHub Actions

Dieses Mini-Projekt zeigt eine einfache Pipeline:

```text
Markdown-Datei ändern
-> Commit
-> Push
-> GitHub Actions startet
-> HTML und PDF werden erzeugt
-> Ergebnis liegt als Artefakt bereit
```

## Ordner

```text
md-pdf-github-action-demo/
├── docs/
│   └── kursnotiz.md
├── .github/
│   └── workflows/
│       └── markdown-pdf.yml
├── .gitignore
└── README.md
```

## Benutzung

1. Eine Markdown-Datei in `docs/` ändern oder neu anlegen.
2. Änderung committen.
3. Nach GitHub pushen.
4. In GitHub unter `Actions` den Workflow `Markdown zu PDF` öffnen.
5. Das Artefakt `markdown-ausgabe` herunterladen.
6. PDF oder HTML öffnen.

## Was macht die Pipeline?

Die Pipeline:

- startet bei Änderungen an Dateien in `docs/`
- installiert `pandoc` und `wkhtmltopdf`
- erzeugt aus jeder Markdown-Datei eine HTML-Datei
- erzeugt daraus eine PDF-Datei
- lädt die Ergebnisse als Artefakt hoch

## Warum so einfach?

Für den Einstieg ist wichtig, dass die Teilnehmenden den Ablauf verstehen:

- Trigger
- Runner
- Job
- Befehle
- Artefakt

Das Projekt verzichtet deshalb bewusst auf komplexe Styles, Testframeworks oder Deployment.

## Unterrichtsidee

Gute Fragen an die Teilnehmenden:

- Was löst die Pipeline aus?
- Welche Werkzeuge werden im Runner installiert?
- Warum liegt das PDF als Artefakt vor?
- Was passiert, wenn eine Markdown-Datei fehlerhaft ist?
- Wäre das schon Continuous Deployment oder nur Continuous Integration?
