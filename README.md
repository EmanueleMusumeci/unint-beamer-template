# UNINT Beamer Presentation Template

An **unofficial** LaTeX beamer template for presentations at UNINT — Università degli
Studi Internazionali di Roma.

Brand colours are taken from unint.eu: **`#0076CC`** (blue, `maincolor`) and
**`#C1001F`** (red, `unintred`).

## Usage

```tex
\documentclass{beamer}
\usetheme{unint}

\titlebackground*{assets/background}   % starred = split title page; unstarred = full bleed

\title{Titolo della lezione}
\subtitle{Sottotitolo}
\course{Master Executive in Intelligenza Artificiale per la PA}
\author{Emanuele Musumeci}
\date{a.a. 2025/2026}

\begin{document}
\maketitle
...
\end{document}
```

Build with `pdflatex main.tex` (run it twice so the table of contents settles).

### Options

* `noslidenumber`: disable slide numbering — `\usetheme[noslidenumber]{unint}`

### Fonts

The theme prefers Caladea + Carlito (metric-compatible with Cambria and Calibri). If
those are not installed it falls back to Helvetica automatically, so the template also
compiles on a bare TeX Live. To get the intended fonts on Debian/Ubuntu:

```bash
sudo apt install texlive-fonts-extra
```

Overleaf already ships them, so no fallback happens there.

### Assets

| File | Used for |
|---|---|
| `assets/logo_RGB.png` | full stacked logo, colour |
| `assets/logo_RGB_negative.png` | full stacked logo, all white |
| `assets/logo_mark.png` | compact `UNINT` wordmark, shown in the header of every slide |
| `assets/logo_mark_negative.png` | same wordmark in white, for dark slides |
| `assets/background.png` | title panel, UNINT blue with the white logo |
| `assets/background_negative.png` | title panel, white with the colour logo |

The logo is a raster asset derived from the one published on unint.eu; UNINT does not
publish a vector version. Keep it at or below the sizes used here, because it does not
survive heavy enlargement.

---

Derived from the [Sapienza Beamer
Template](https://github.com/andrea-gasparini/sapienza-beamer-template) by Andrea
Gasparini, itself based on [SINTEF
Presentation](https://www.overleaf.com/latex/templates/sintef-presentation/jhbhdffczpnx)
by Federico Zenith, with additions from
[Beamer-LaTeX-Themes](https://github.com/TOB-KNPOB/Beamer-LaTeX-Themes) by Liu Qilong.
