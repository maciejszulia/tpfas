# TPFAS — Teoria Programowalnej Fizyki i Algebry Synergii

Artykuł (preprint) wraz ze źródłem LaTeX i zbudowanym PDF.

**Autor:** M. Szulia · **Wersja:** listopad 2026 · **Objętość:** 5 stron

## O czym jest

Praca rozwija arytmetykę nie-Newtonowską (Grossman–Katz) o człon sprzężenia
ze środowiskiem i definiuje **Generator M. Szulia**:

```
a ⊕_s b = g⁻¹( g(a) + g(b) + 2√(s·(g(a)+g(b))) )
a ⊖_s b = g⁻¹( (√(g(a)+s) − √s)² − g(b) )
```

Dla `s = 0` wracamy do zwykłego transportu struktury (TPFAS 1.0); dla `s > 0`
operator staje się niełączny i modeluje synergię (TPFAS 2.0). Dalej: taksonomia
siedmiu „iskier" (zachowawcza, synergii, Tsallisa, ekstremalna, równowagi,
fraktalna, falowa), cztery klasy przestrzeni (energetyczna, saturacji,
hybrydowa, ziarnista), audyt numeryczny IEEE 754 oraz dwa wdrożenia: sterowanie
kotłem na drewno bez instrukcji warunkowych i regularyzacja osobliwości
w metryce Schwarzschilda.

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

To dokument teoretyczny autora, nie artykuł recenzowany. Część tez ma charakter
postulatów modelowych, a nie dowiedzionych twierdzeń fizycznych — w
szczególności:

* „eliminacja osobliwości" czarnej dziury przez generator saturacji jest
  *zmianą współrzędnych* w metryce, a nie rozwiązaniem równań Einsteina;
* „sterowanie bezwarunkowe" oznacza, że bariery są wpisane w dziedzinę
  dekodera `g⁻¹`, a nie że regulator jest odporny na awarie czujników;
* niełączność `⊕_s` jest własnością algebraiczną (sprawdzalną numerycznie),
  ale jej fizyczna interpretacja jako „zysku kaskadowego" wymaga modelu
  kalibracyjnego.

Te zastrzeżenia nie unmniejszają konstrukcji — porządkują, co jest matematyką,
a co hipotezą.

## Prawa

Tekst: © M. Szulia, 2026. Repozytorium publiczne do wglądu i cytowania;
brak licencji na redystrybucję zmienionych wersji.
