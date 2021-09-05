# Interaktivní režim Pythonu

Chceš-li si začít hrát s Pythonem, otevři *příkazový řádek* a aktivuj virtuální prostředí.
Zkontroluj si, na začátku příkazové řádky ti svítí `(venv)`.

Je-li tomu tak, nezbývá než – konečně – pustit Python. K tomu použij příkaz `python`:

``` console
$ python
Python 3.6.6 (...)
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Příkaz vypíše několik informací. Z prvního řádku se můžeš ujistit že používáš Python 3.
(Vidíš-li číslo jako `2.7.18`, něco je špatně – popros o radu kouče.
Novější verze, např. `3.9.1`, je naopak v pořádku)

Třemi „zobáčky“ `>>>` pak Python poprosí o instrukce.
Je to jako v příkazové řádce, ale místo příkazů jako `cd` a `mkdir` sem budeš psát příkazy Pythonu.

Práci s příkazovým řádkem si můžeš představit jako telefonní konverzaci:
nejdřív ses s počítačem bavil{{a}} pomocí příkazů jako `cd`.
Příkaz `python` znamená „dej mi prosím k telefonu Python!“
Následující „konverzace“ bude s úplně jiným programem, i když okýnko s textem
vypadá skoro stejně.

Vyzkoušej si, že příkazy z příkazové řádky v Pythonu nefungují:

```pycon
>>> cd adresar
  File "<stdin>", line 1
    cd adresar
       ^
SyntaxError: invalid syntax
>>> whoami
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'whoami' is not defined
```

Tohle je *chybová hláška*, která se objeví vždycky
když Python nebude spokojený.
V průběhu kurzu jich uvidíš ještě spoustu,
takže si ji dobře prohlédni, ať ji příště poznáš.


## První příkaz

Zkusme radši příkazy, kterým Python rozumí.

Ze začátku použij Pythonu jako kalkulačku.
Za tři zobáčky napiš třeba `2 + 3` a zmáčkni <kbd>Enter</kbd>.

``` pycon
>>> 2 + 3
5
```

Zobrazila se ti správná odpověď?
Pokud ano, gratuluji! První příkaz v Pythonu máš za sebou.

Zkusíš i odečítání?

A jak je to s násobením?

Na kalkulačce bys zadal{{a}} `4 × 5`, což se na klávesnici píše špatně.
Písmeno `x` i tečku Python používá k jiným účelům.

Pro násobení proto Python používá symbol `*` (který možná znáš třeba z Excelu).

``` pycon
>>> 4 * 5
20
```

Znaménka jako `+`, `-` a `*` se odborně nazývají *operátory*.

> [style-note]
> Mezery mezi čísly a operátorem nejsou nutné: `4*5` i `4       * 5` dělá
> to samé co `4 * 5`.
> Je ale zvykem psát kolem operátoru jednu mezeru z každé strany – tak jako
> v těchto materiálech.
> Kód je pak čitelnější.

Operátor pro dělení je `/`.
Při dělení může vzniknout necelé číslo, třeba dva a půl.
Python vychází z angličtiny a používá desetinnou *tečku*, takže číslo 2,5 ukáže
jako `2.5`:

``` pycon
>>> 5 / 2
2.5
```

Z důvodů do kterých teď nebudeme zabíhat Python rozlišuje mezi celými a
reálnými čísly.
Desetinná tečka se proto objeví i když vyjde číslo celé:
``` pycon
>>> 4 / 2
2.0
```

Občas se hodí použít dělení se zbytkem, kdy podíl zůstane jako celé číslo.
Na to má Python operátory `//` (podíl) a `%` (zbytek):

``` pycon
>>> 5 // 2
2
>>> 5 % 2
1
```

Časem zjistíš že dělení se zbytkem je v programování překvapivě užitečné.
Jestli si děláš poznámky, `//` i `%` si do nich určitě přidej!


### Ukončení

Pokud ses dostal{{a}} až sem, gratuluji!
Python máš nejen nainstalovaný, ale taky ti funguje.
Stačí ho už jen zavřít.
To se dělá pomocí `quit()`, s prázdnými závorkami na konci.

<div class="highlight"><pre>
<span class="gp">&gt;&gt;&gt;</span> quit()
<span class="gp">(venv)$</span>
</pre></div>

Tím ukončíš konverzaci s Pythonem a „zavoláš k telefonu“
zpátky příkazovou řádku.
Zobáčky `>>>` se změnily na výzvu
příkazové řádky (která začíná `(venv)` a končí `$` nebo `>`).
Příkazy Pythonu, jako `1 + 2`, teď fungovat nebudou (dokud Python opět
nepustíš ke slovu pomocí příkazu `python`).
Zato příkazům jako `whoami` a `cd` teď počítač rozumět bude.

Teď můžeš okno s příkazovou řádkou zavřít – buď zavři její okýnko,
nebo na to můžeš použít textové příkazy.

virtuální prostředí můžeš ukončit příkazem `deactivate` – tentokrát bez
závorek:

```console
(venv)$ deactivate
```

A celou příkazovou řádku můžeš zavřít příkazem `exit`:

```console
$ exit
```

Pro cvik si zkus Python znovu spustit – nejdřív otevři příkazovou řádku,
pak donaviguj do adresáře s virtuálním prostředím,
aktivuj virtuální prostředí a nakonec spusť Python samotný.
