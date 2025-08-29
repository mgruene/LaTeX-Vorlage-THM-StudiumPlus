# Leitfaden zum THM-Template (Richtlinie 02/2025)

## Systemvoraussetzungen
- **LaTeX-Distribution**: **TeX Live** empfohlen. Eine Distribution bündelt Compiler (pdfLaTeX), Pakete und Tools.
  - **Linux (Debian/Ubuntu)**: `sudo apt install texlive-full`
    - Minimal: `sudo apt install texlive-latex-recommended texlive-latex-extra texlive-lang-german`
  - **Windows/macOS**: TeX Live Installer von tug.org verwenden (Standardauswahl).
- **Editor/IDE**: **TeXmaker** (frei, plattformübergreifend). Alternativen: TeXstudio, Kile, Overleaf.

### Texmaker kurz einrichten
1. **Optionen → Texmaker konfigurieren → Schnellübersetzung**: „pdfLaTeX“ wählen.
2. `document.tex` öffnen, mit **F1** kompilieren.
3. Literatur: **pdfLaTeX → BibTeX → pdfLaTeX → pdfLaTeX**.

## Vorgabenkonforme Formatierung
- **Schrift**: Vorlage bevorzugt **Arial**. Da Arial nicht garantiert vorhanden ist, lädt das Template automatisch `uarial` *falls verfügbar*, sonst **Helvetica** als Fallback.  
  - Arial aktivieren: Paket **`uarial`** installieren (unter Ubuntu via `sudo apt install texlive-fonts-extra`). Keine proprietären TTF-Dateien erforderlich.
- **Schriftgrößen**: Fließtext 12 pt, **Fußnoten 10 pt**.
- **Zeilenabstand**: 1,5-zeilig.
- **Ränder**: links 4,0 cm, rechts 1,5 cm, oben 3,0 cm, unten 2,0 cm.
- **Papier/Seiten**: DIN A4, einseitig.

## Struktur & zusätzliche Bestandteile
- **Sperrvermerk**: im Template via `\lockMark` vorgesehen (optional laut Richtlinie).
- **Vorwort**: als `Inhalt/0_Vorwort.tex` eingefügt, **nicht** im Inhaltsverzeichnis.
- **Gender-Disclaimer**: als `Inhalt/0_Gender.tex` nach den Verzeichnissen, **nicht** im Inhaltsverzeichnis.
- **Versicherung**: durch `\makeinsurance` am Ende bereits enthalten.

## Literatur mit Zotero + BetterBibTeX
1. **Zotero** installieren, Plugin **BetterBibTeX** hinzufügen.
2. Sammlung exportieren: Rechtsklick → **Export** → **Better BibTeX** → Option *Keep updated* aktivieren → Datei `source.bib` im Projekt belassen.
3. Zitieren im Text mit `\cite{}`. Bibliographie wird mit `\printbibliography` ausgegeben.
4. Kompilierfolge: pdfLaTeX → BibTeX → pdfLaTeX → pdfLaTeX.
5. **Fachrichtungs‑Hinweis**: Ingenieur-/Naturwissenschaften verwenden nummerierte Verweise; BWL/WI oft Fußnoten‑Kurzbelege (ggf. mit Betreuenden abstimmen).

## Hinweise
- **Nichts löschen**: Die Vorlage behält alle Originaldateien und ergänzt nur zusätzliche `.tex`‑Bestandteile.
- **Times‑Alternative**: Falls Times gewünscht: Preamble‑Zeile `\usepackage{mathptmx}` aktivieren und `\renewcommand{\familydefault}{\rmdefault}` setzen (auskommentiert belassen, wenn Arial/Helvetica genutzt wird).