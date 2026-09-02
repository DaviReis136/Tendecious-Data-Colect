# EST011 — Introduction to Statistics Assignment (Group 1, Activity A)

**National School of Statistical Sciences (ENCE-IBGE)** — 2026-2

<img width="2518" height="416" alt="ence_LOGO" src="https://github.com/user-attachments/assets/0b048c6f-592b-4ddb-846a-eebeb3514ac0" />

This repository contains a LaTeX report for an introductory statistics assignment. The project ran a small **online survey experiment** to measure how question wording (neutral vs. biased phrasing) affects response rates, using an automated randomized redirect built with a static HTML page.

---

## 👥 Authors

- Arthur Togi
- Branca Azevedo
- Daniele Nogueira
- Davi Reis
- Guilherme Souza
- Jorge Henrique
- Marcos Vinícios

---

## 📋 What the project does

Two versions of the same survey question were created:

- **Version A (neutral):**
  > "Do you think the university needs to carry out reforms to its facilities?"

- **Version B (biased):**
  > "Do you think the university should carry out reforms to its facilities in order to better meet your needs?"

A small HTML page (hosted on Netlify) randomly redirected respondents to one of two Google Forms links — one per question version — so assignment to A or B was automated rather than manual. The survey ran from **08/24/2026 to 08/26/2026** and was shared with ENCE-IBGE students and alumni via WhatsApp.

---

## 📁 Repository structure

```
.
├── report_english.tex     # Main LaTeX source (English version)
├── ence_LOGO.jpg           # ENCE-IBGE logo — used in the page header
├── Grafico_A.png            # Chart of responses to Version A
├── Grafico_B.png            # Chart of responses to Version B
└── README.md               # This file
```

> ⚠️ **Note:** the three image files are not included by default. Add your own `ence_LOGO.jpg`, `Grafico_A.png`, and `Grafico_B.png` to the same folder as the `.tex` file, or compilation will fail at the `\includegraphics` commands.

---

## 🖼️ Images used in the document

| File | Where it appears | Purpose |
|------|-------------------|---------|
| `ence_LOGO.jpg` | Page header (top-left, every page after the table of contents) | Institutional logo of ENCE-IBGE |
| `Grafico_A.png` | "Charts" section | Response distribution for the neutral question (Version A) |
| `Grafico_B.png` | "Charts" section | Response distribution for the biased question (Version B) |

---

## 🔣 Symbols and formulas

The report defines two formulas in LaTeX math mode. In plain-text form:

**Sample proportion of "yes" answers, per version:**

```
p̂_A = n_A(yes) / n_A        p̂_B = n_B(yes) / n_B
```

**Difference in proportions between versions:**

```
d = p̂_A − p̂_B
```

These only use base LaTeX math mode (`\hat{}`, `\frac{}{}`) — no extra math package is required.

---

## 📊 Data summary

| Metric | Version A | Version B |
|--------|-----------|-----------|
| Answered yes | 19 | 6 |
| Total approached | 25 | 26 |
| Proportion of yes | 0.76 | 0.80 |
| Difference (A − B) | — | −0.04 |

---

## ⚙️ Requirements to compile

- A LaTeX distribution: **TeX Live**, **MiKTeX**, or **MacTeX**.
- Standard packages (included in any full install): `graphicx`, `url`, `babel`, `inputenc`, `verbatim`, `listings`, `xcolor`, `indentfirst`, `fancyhdr`, `lipsum`, `booktabs`, `hyperref`.
- This `.tex` file does **not** require `sbc-template.sty` — the few commands from that package (`\inst`, `\address`, `\email`) are redefined locally at the top of the file in plain LaTeX.

---

## ▶️ How to compile

```bash
pdflatex report_english.tex
pdflatex report_english.tex   # run twice, for the table of contents and cross-references
```

Or open the project in [Overleaf](https://www.overleaf.com) and upload all four files (`.tex` + 3 images) together.

---

## 📄 License

Academic assignment — for coursework use.
