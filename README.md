# EST011 — Introduction to Statistics Assignment (Group 1, Activity A)

**National School of Statistical Sciences (ENCE-IBGE)** — 2026-2

<img width="2518" height="416" alt="ence_LOGO" src="https://github.com/user-attachments/assets/0b048c6f-592b-4ddb-846a-eebeb3514ac0" />

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

### Code:

```


<!DOCTYPE html>
2 <html>
3 <head>
4 <meta charset="utf-8"/>
5 <title>Redirecionando</title>
6 <meta id="encurtador" http-equiv="refresh" content="5; url=/"
/>
7 </head>
8 <body>
9 <h1>Trabalho de Introduc¸˜ao `a Estat´ıstica</h1>
10 <h2>Redirecionando para o FORMS</h2>
11 <script>
12 var links = [
13 Array(’https://docs.google.com/forms/d/e/1
FAIpQLSd2wiAGmTh1TdIA53nGkhIkKpfWZR4fvpKMl2QsqDH_Ht2_ZA/
viewform?usp=dialog’,’https://docs.google.com/forms/d/e/1
FAIpQLSdAjuKGauA-w98E1IFzQi_46LdCfZUriVqT3byf4R21nltXSw/
viewform?usp=dialog’)
14 document
15 .getElementById("encurtador")
16 setAttribute("content", "5; URL=" + links[Math.floor(
Math.random()*links.length)]);
17 </script>
18 </body>
19 </html>
C ´odigo 1. Linguagem HTML


```

### Website:


<img width="1919" height="921" alt="image" src="https://github.com/user-attachments/assets/c669db96-f4d0-4dbe-8c44-b8f0dc78ae46" />

*Note*: Introdution to Statics College project<br> 
Redirecting to forms

### What we change in Version B

We mentioned the student's individual needs regarding accommodations, rather than simply generalizing the need for accommodations.

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
| Answered yes | 19 | 21 |
| Total approached | 25 | 26 |
| Proportion of yes | 0.76 | 0.80 |
| Difference (A − B) | — | −0.04 |

---

## Conclusion

Mentioning needs creates certainty.

## 🗣 Note 

This repository contains a LaTeX report for an introductory statistics assignment. The project ran a small **online survey experiment** to measure how question wording (neutral vs. biased phrasing) affects response rates, using an automated randomized redirect built with a static HTML page.

---

## 📄 License

Academic assignment — for coursework use.


