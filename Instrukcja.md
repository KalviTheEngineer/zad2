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
Przykład kodu XML – fragment dokumentu SVG (Scalar Vector Graphics):

```xml
<!DOCTYPE html>
<html>
<body>
<svg height="100" width="100">
  <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>
</body>
</html>
```
W tym przypadku mamy znacznik `<circle>` opisujący parametry koła, który może być właściwie zinterpretowany przez dedykowaną aplikację (np. przeglądarki www). 

Jako ciekawostkę można podać fakt, że również pakiet MS Office wykorzystuje format XML do przechowywania informacji o dodatkowych parametrach formatowania danych. Na przykład pliki z rozszerzeniem `.docx` to nic innego jak spakowane algorytmem zip katalogi z plikami XML.
Przykład rozpakowania zawartości pliku `test.docx` poleceniem: `unzip`

```bash
$ unzip -l test.docx
Archive: test.docx
Length   Date    Time    Name
--------- ---------- ----- ----
573      2022-03-20 08:55 _rels/.rels
731      2022-03-20 08:55 docProps/core.xml
508      2022-03-20 08:55 docProps/app.xml
531      2022-03-20 08:55 word/_rels/document.xml.rels
1288     2022-03-20 08:55 word/document.xml
2429     2022-03-20 08:55 word/styles.xml
853      2022-03-20 08:55 word/fontTable.xml
257      2022-03-20 08:55 word/settings.xml
1374     2022-03-20 08:55 [Content_Types].xml
```

Wszystkie te języki znaczników cechują się rozbudowaną i złożoną składnią, dlatego do ich edycji wymagają najczęściej dedykowanych narzędzi w postaci specjalizowanych edytorów.

By wyeliminować powyższą niedogodność, powstał **Markdown** - uproszczony język znaczników służący do formatowania dokumentów tekstowych (bez konieczności używania specjalizowanych narzędzi). Dokumenty w tym formacie można bardzo łatwo konwertować do wielu innych formatów: np. HTML, PDF, PS (PostScript), EPUB, XML i wiele innych.

Format ten jest powszechnie używany do tworzenia plików `README.md` (w projektach open source) i powszechnie obsługiwany przez serwery Gita. Język ten został stworzony w 2004 r., a jego twórcami byli John Gruber i Aaron Swartz.

W kolejnych latach podjęto prace w celu stworzenia standardu rozwiązania i tak w 2016 r. opublikowano dokument [RFC 7764](https://datatracker.ietf.org/doc/html/rfc7764), który zawiera opis kilku odmian tegoż języka:

- CommonMark,
- GitHub Flavored Markdown (GFM),
- Markdown Extra.
