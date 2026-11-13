# Arytmetyka nie-Newtonowska z członem synergii

Notatka (preprint) ze źródłem LaTeX i zbudowanym PDF. Wcześniejszy tytuł roboczy: TPFAS.

**Autor:** Maciej Szulia | **Wersja:** listopad 2026 | **Objętość:** 5 stron

## O czym jest

Praca dodaje do arytmetyki nie-Newtonowskiej (Grossman, Katz) człon sprzężenia
ze środowiskiem i definiuje operator synergiczny:

```
a ⊕_s b = g⁻¹( g(a) + g(b) + 2√(s·(g(a)+g(b))) )
a ⊖_s b = g⁻¹( (√(g(a)+s) − √s)² − g(b) )
```

Dla `s = 0` operator jest zwykłym przeniesieniem struktury. Dla `s > 0` operator
jest przemienny i nie jest łączny. Praca zawiera też zestawienie 7 wariantów
działania, 4 klasy generatorów (energetyczna, saturacji, hybrydowa, ziarnista),
wynik testów numerycznych IEEE 754 oraz 3 propozycje zastosowań: sterowanie pompą
kotła na drewno bez instrukcji warunkowych, zmianę współrzędnej radialnej we
wnętrzu czarnej dziury i opis układów otwartych.

## Pliki

```
tpfas_szulia_paper.tex   # źródło (pdfLaTeX, babel polish, tabularx)
tpfas_szulia_paper.pdf   # zbudowany artykuł
```

## Budowanie

```bash
pdflatex -interaction=nonstopmode tpfas_szulia_paper.tex
pdflatex -interaction=nonstopmode tpfas_szulia_paper.tex   # spis treści
pdflatex -interaction=nonstopmode tpfas_szulia_paper.tex   # odsyłacze
```

Wymagany TeX Live z pakietami: `babel-polish`, `lmodern`, `amsmath`, `amsthm`,
`booktabs`, `tabularx`, `microtype`, `hyperref`.

## Status i zakres

To dokument teoretyczny autora, nie artykuł recenzowany. Propozycje zastosowań są
hipotezami modelowymi, a nie dowiedzionymi twierdzeniami fizycznymi:

* generator saturacji we wnętrzu czarnej dziury jest *zmianą współrzędnej*,
  a nie rozwiązaniem równań Einsteina;
* „sterowanie bez instrukcji warunkowych” oznacza, że bariery są wpisane
  w dziedzinę dekodera `g⁻¹`, a nie że regulator jest odporny na awarie czujników;
* brak łączności `⊕_s` jest własnością algebraiczną (sprawdzalną numerycznie);
  interpretacja fizyczna tej własności wymaga modelu kalibracyjnego.

## Zobacz też

Repozytorium [function-generated-arithmetics](https://github.com/maciejszulia/function-generated-arithmetics)
zawiera pomiar własności operatora synergicznego: dla `s > 0` operator nie ma
elementu neutralnego i nie jest łączny.

## Prawa

Tekst: © Maciej Szulia, 2026. Repozytorium publiczne do wglądu i cytowania;
brak licencji na redystrybucję zmienionych wersji.
