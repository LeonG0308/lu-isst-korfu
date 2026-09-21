# Lu & Carla – Korfu

Privater Restaurant-Finder für Roda, Nord-Korfu (22.–29.09.2026). Eine einzige HTML-Datei, gehostet über GitHub Pages:
**https://leong0308.github.io/lu-isst-korfu/**

## KI-Suche (Anthropic / Claude)

Die Suche „Worauf habt ihr Lust?“ schickt die Frage plus alle Speisekarten direkt aus dem Browser an die Anthropic-API (Standard: Claude Haiku 4.5).

Der API-Schlüssel steht **nicht** in diesem Repo. Er liegt als Repository-Secret `ANTHROPIC_KEY` und wird beim Deploy (`.github/workflows/pages.yml`) in die Seite eingesetzt. Dadurch funktioniert die KI-Suche auf jedem Gerät, ohne dass jemand einen Schlüssel eingeben muss.

Schlüssel setzen oder wechseln (einmalig, vom eigenen Rechner):

```
gh secret set ANTHROPIC_KEY --repo LeonG0308/lu-isst-korfu
gh workflow run Deploy --repo LeonG0308/lu-isst-korfu
```

Oder im Browser: Repo → Settings → Secrets and variables → Actions → `ANTHROPIC_KEY`, danach Actions → „Deploy“ → „Run workflow“.

Hinweis: Die veröffentlichte Seite enthält den Schlüssel (leicht verschleiert). Wer den Quelltext der Seite liest, kann ihn benutzen. Deshalb einen **eigenen Schlüssel nur für diese App** mit **Ausgabenlimit** anlegen (console.anthropic.com → Settings → Limits) und ihn nach dem Urlaub löschen.
