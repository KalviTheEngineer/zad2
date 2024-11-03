---
title: Instrukcja

---

# Lekcja 1 – Markdown lekki język znaczników

## Spis treści

1. [Lekcja 1 – Markdown lekki język znaczników](#lekcja-1--markdown-lekki-język-znaczników) ....................................... 1
   - [Wstęp](#wstęp) ........................................................................................... 1
   - [Podstawy składni](#podstawy-składni) ............................................................... 3
     - [Definiowanie nagłówków](#definiowanie-nagłówków) ............................... 3
     - [Definiowanie list](#definiowanie-list) ............................................................ 4
     - [Wyróżnianie tekstu](#wyróżnianie-tekstu) ..................................................... 4
     - [Tabele](#tabele) ..................................................................................... 5
     - [Odnośniki do zasobów](#odnośniki-do-zasobów) ................................. 5
     - [Obrazki](#obrazki) .................................................................................... 5
     - [Kod źródłowy dla różnych języków programowania](#kod-źródłowy-dla-różnych-języków-programowania) .......... 5
     - [Tworzenie spisu treści na podstawie nagłówków](#tworzenie-spisu-treści-na-podstawie-nagłówków) ............... 6
   - [Edytory dedykowane](#edytory-dedykowane) ........................................................ 7
   - [Pandoc – system do konwersji dokumentów Markdown do innych formatów](#pandoc--system-do-konwersji-dokumentów-markdown-do-innych-formatów) ..... 8

## Wstęp

Obecnie powszechnie wykorzystuje się języki ze znacznikami do opisywania dodatkowych informacji umieszczanych w plikach tekstowych. Z pośród najbardziej popularnych można wspomnieć o:

1. **HTML** – służącym do opisu struktury informacji zawartych na stronach internetowych,
2. **TeX (LaTeX)** – poznanym na zajęciach język do „profesjonalnego” składania tekstów,
3. **XML (Extensible Markup Language)** – uniwersalnym języku znaczników przeznaczonym do reprezentowania różnych danych w ustrukturalizowany sposób.

## Przykład kodu HTML i jego interpretacja w przeglądarce:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Przykład</title>
</head>
<body>
    <p>Jakiś paragraf tekstu</p>
</body>
</html>
```
![PrzykładHTML](https://hackmd.io/_uploads/H1uN_eBb1l.png)

Przykład kodu LaTeX i wygenerowanego pliku w formacie PDF:

```latex
\documentclass[]{letter}
\usepackage{lipsum}
\usepackage{polyglossia}
\setmainlanguage{polish}
\begin{document}
\begin{letter}{Szanowny Panie XY}
\address{Adres do korespondencji}
\opening{}
\lipsum[2]
\signature{Nadawca}
\closing{Pozdrawiam}
\end{letter}
\end{document}
```
![Latex](https://hackmd.io/_uploads/rkp4OxBZkx.png)
