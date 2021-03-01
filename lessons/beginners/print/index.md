# Print a chybové hlášky

Otevři si v editoru svůj soubor `ahoj.py`, ve kterém máš napsáno:

```python
print("Ahoj světe!")
```

Program spusť:
* pokud ti už na začátku příkazové řádky nesvítí `(venv)`,
  aktivuj si virtuální prostředí,
* pomocí `cd` donaviguj do adresáře s programem,
* zadej `python ahoj.py`.

Funguje? Doufám, že stále ano.

Zkus přidat další řádek, aby program vypadal takhle:

```python
print("Ahoj světe!")
print("Jak se máš?")
```

Program spusť znovu.
Zjistíš, že se vypsaly dva řádky.

Abys nemusel{{a}} v příkazové řádce stále dokola psát `python ahoj.py`,
zkus zmáčknout na klávesnici šipku nahoru, <kbd>↑</kbd>.
Vrátíš se tak k předchozímu příkazu, který stačí „odklepnout“ pomocí
<kbd>Enter</kbd>.


## Jak funguje program

Teď, když program běží, se můžeme podívat, co se při
jeho spuštění vlastně děje.
Je to zatím docela jednoduché: v souboru jsou příkazy,
příkazy se provádějí jeden po druhém,
odshora dolů.
Program je jako recept na vaření nebo návod na skříňku z IKEA:
seznam instrukcí, které říkají co je potřeba udělat.

Zanedlouho budou tvoje programy mnohem složitější,
ale základní myšlenka bude stále stejná:
počítač „čte“ odshora dolů a provádí příkazy jeden po druhém.


## Print: vypisování a výrazy

A z jakých že instrukcí se náš „recept“ skládá?

Můžeš použít jakýkoli příkaz, který napíšeš do interaktivního módu Pythonu
(t.j. za `>>>` v příkazové řádce).
U programu v souboru ovšem Python nevypisuje výsledek každého zadaného příkazu.
Když do souboru napíšeš třeba řádek `1 + 2` (bez `print`), Python
sice spočítá výsledek, ale nikde ho neukáže.
Proč?
Velké programy obsahují tisíce příkazů; kdyby se každý mezivýsledek vypisoval,
nebylo by to vůbec přehledné.

Proto když v programu chceš říct Pythonu aby nějaký výsledek vypsal,
musíš použít `print`.
Zkus si {{gnd('sám','sama')}} pustit `python` interaktivně a ověřit,
že tenhle příkaz funguje stejně jako v programu:
```pycon
>>> print("ahoj!")
ahoj!
>>> quit()
```

To `print` (a i `quit`) je *funkce*.
O funkcích se obecně budeme bavit později;
teď stačí vědět, že když napíšeš `print` a za to něco do závorky,
Python to vypíše,


## Jak číst chyby

Často zjistíš, že program, který napíšeš, nebude fungovat hned napoprvé.
Počítač je hloupý stroj; pokud instrukce nenapíšeš přesně podle pravidel jazyka
Python, neumí si domyslet, co po něm chceš.
Ale nevěš hlavu, stává se to všem programátorům.
Důležité je vědět, jak chybu najít.
A k tomu ti pomůžou chybové výpisy.

Kdybys třeba v příkazu `print(Jak se máš?)` zapomněl{{a}} uvozovky,
dostaneš následující hlášku:

<pre>
  File "<span class="plhome">~/naucse-python</span>/01/ahoj.py", line <span class="err-lineno">11</span>
    print(Jak se máš?)
              ^
<span class="err-exctype">SyntaxError</span>: invalid syntax
</pre>

Při chybě Python napřed zmíní jméno souboru a
<span class="err-lineno">číslo řádku</span>, na kterém si chyby všimnul.
Potom vypíše celý řádek s chybou
a nakonec oznámí <span class="err-exctype">druh chyby</span>
(v tomto případě je to „syntaktická chyba“)
a případně nějaké bližší upřesnění.

> [note] Pro zvídavé
> Jak se od téhle chyby liší ta, která nastane, když zkusíš sečíst číslo a řetězec?
> Nebo když zkusíš dělit nulou?
> Nebo když zapomeneš jen uvozovku za textem?

Chybové hlášky můžou být ze začátku těžko pochopitelné,
zvyknout se na ně dá asi jenom praxí.
Pro tebe bude ze začátku důležité hlavně ono číslo řádku.
Když víš, že chyba je na řádku <span class="err-lineno">11</span>,
můžeš se podívat na tento řádek a zkusit chybu najít.

Když chyba není na daném řádku, může být ještě
o pár řádků výš nebo níž:
Python občas nesdílí lidské představy o tom, kde přesně chyba *je*.
Ukáže jen, kde si jí sám *všimnul*.

V našem případě je chyba v tom, že kolem řetězce *Jak se máš?* nejsou uvozovky.
Přidej je a program znovu spusť.
Jestli funguje, gratuluji!
Jinak chybu opět oprav a opakuj, dokud to nebude fungovat :)


## Další příkazy

Zkus do programu postupně, po jednom, přidávat další řádky.
Po přidání každého dalšího `print` program znovu spusť a vyzkoušej
co dělá.

```python
print("Ahoj světe!")
print("Jak se máš?")

print(1)
print(1, 2, 3)
print(1 + 1)
print(3 * 8, 10 - 2.2)
print(3 + (4 + 6) * 8 / 2 - 1)
print("Součet čísel 3 a 8 je", 3 + 8)
```

Proč jsou některé hodnoty v uvozovkách a některé ne?
Pokud chceš v Pythonu pracovat s *textem*, musíš ho obalit do uvozovek,
aby Python věděl, že se k němu má chovat jinak než k *instrukcím* jako `print`.
Více se dozvíš později, zatím si zapamatuj, že se takovýto text označuje v programovací
hantýrce jako `řetězec`.

Obecně může být v závorkách za `print` několik *výrazů*
(angl. *expressions*) oddělených čárkou.
A co že je ten výraz?
V našem programu máš několik příkladů:
výraz je číslo, řetězec nebo nějaká (třeba matematická) operace
složená z více výrazů.
Třeba výraz `3 + 8` sčítá výrazy `3` a `8`.

> [style-note] Typografická vsuvka
> Všimni si stylu zápisu: jako v češtině se po otevírací závorce a před
> uzavírací závorkou nepíše mezera; na rozdíl od češtiny ale mezera není
> mezi `print` a závorkou.
> Nejde o vsuvku.
> ```python
> print("Ahoj!")
> ```
>
> S čárkou je to jako v češtině: mezeru píšeme po čárce, ale ne před ní:
> ```python
> print(1, 2, 3)
> ```
>
> Kolem operátorů jako `+` a `/` se obyčejně píše jedna mezera zleva a
> jedna zprava. Někdy je ale přehlednější obě vynechat:
> ```python
> print(2 + 8)
> print("Jedna a půl je", 1 + 1/2)
> ```
>
> Tyhle zásady jsou tu jen proto, aby se program dobře četl ostatním lidem.
> Samotný Python mezery kolem slov ignoruje (když nejsou v uvozovkách).
> Můžeš klidně napsat něco jako:
>
> ```
> print      (   "Ahoj světe!"
>                                 )
> ```
> Ale budoucí kolegové tě pak nejspíš nebudou mít rádi.
