# Vyhodnocování výrazů

Už víš, že Python se dá použít jako kalkulačka: dokáže spočítat
hodnotu *výrazu* (angl. *expression*) jako `3 * (5 + 2)`.
Jak to ale vlastně dělá?
Jak se vyhodnocují výrazy?

Pro základní výrazy je to tak, jak to možná znáš ze školy.
U `3 * (5 + 2)` nejdřív spočítáš to, co je v závorkách: `(5 + 2)` je `7`.
Výsledek dosadíš do původního výrazu místo závorky: `3 * 7`.
Stejně fungují výrazy v Pythonu.

Možná to zní jednoduše, ale protože budeme ten samý postup používat
i na složitější výrazy, hodí se ho umět „rozepsat“:

```python
vysledek = 3 * (5 + 2)
#              ╰──┬──╯
vysledek = 3 *    7
#          ╰─┬────╯
vysledek =  21
```

Když Python potřebuje vyhodnotit *proměnnou*, dosadí její hodnotu.
Pokud je zrovna v proměnné <var>a</var> číslo 4, za `a` se dosadí `4`:

```python
a = 4
b = 5

vysledek = (a + b) / a
#           |   |    |
vysledek = (4 + 5) / 4
#          ╰──┬──╯
vysledek =    9    / 4
#             ╰────┬─╯
vysledek =        2.25
```

Python dodržuje *prioritu operátorů*: např. násobení vyhodnotí dřív než
sečítání.
Záleží přitom vždy na operátoru (znaménku).
Násobení čísel (`*`) a opakování řetězců (taky `*`) má vyšší prioritu;
sečítání čísel (`+`) a spojování řetězců (taky `+`) ji má nižší.

```python
vysledek = 4 + 2 * 3
#              ╰─┬─╯
vysledek = 4 +   6
#          ╰──┬──╯
vysledek =  10

vyzva = "Volejte třikrát: " + "Sláva! " * 3
#                             ╰─────┬─────╯
vyzva = "Volejte třikrát: " + "Sláva! Sláva! Sláva! "
#       ╰────────────────────┬──────────────────────╯
vyzva = "Volejte třikrát: Sláva! Sláva! Sláva! "
```

Python nemá problém se složitými výrazy – vyhodnocování funguje vždy stejně.
Jen člověk, který program čte či píše, se ve výrazech může lehce ztratit.
Když opravdu potřebuješ napsat složitý výraz, je dobré jej rozdělit na několik
menších nebo vysvětlit pomocí komentáře.

Je ale dobré mít povědomí o tom, jak složité výrazy „fungují“,
aby ses jich nemusel{{a}} bát.
Měl{{a}} bys být schopn{{gnd('ý', 'á')}} vysvětlit, co se stane,
když se Pythonu zeptáš, kolik je (-<var>b</var> + (<var>b</var>² -
4<var>a</var><var>c</var>)⁰·⁵) / (2<var>a</var>), abys pak věděl{{a}}, co za
tebe Python dělá.

```python
a = 2
b = 5
c = 3


x = (-b + (b ** 2 - 4 * a * c) ** 0.5) / (2 * a)
#     |    |            |   |                 |
x = (-5 + (5 ** 2 - 4 * 2 * 3) ** 0.5) / (2 * 2)
#          ╰──┬─╯   ╰─┬─╯                ╰──┬──╯
x = (-5 + (  25   -   8   * 3) ** 0.5) /    4
#                     ╰───┬─╯
x = (-5 + (  25   -      24  ) ** 0.5) /    4
#         ╰───────┬──────────╯
x = (-5 +         1            ** 0.5) /    4
#                 ╰──────┬──────────╯
x = (-5 +                1)            /    4
#    ╰────────────┬──────╯
x =              -4                    /    4
#                 ╰────────────┬────────────╯
x =                           -1.0
```

Výrazy se používají na více místech Pythonu než jen v přiřazování
do proměnných.
Třeba pro porovnání dvou hodnot.
Ale o tom zase příště.
