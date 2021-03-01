# První program

```pycon
>>> 3 + 4
7
```

Psaní příkazů přímo v Pythonu, <em>interaktivně</em>,
má jednu velkou nevýhodu:
to co napíšeš se ztratí jakmile zavřeš okno příkazové řádky.
Na jednoduché výpočty to nevadí, ale až budou tvoje programy složitější,
budeš je potřebovat nějak uložit.

Otevři editor.
(Ten bys měl{{a}} mít nainstalovaný, jestli ne, instrukce jsou v [předchozí
lekci]({{ lesson_url('beginners/install-editor') }}).)

V něm vytvoř nový soubor, do kterého napiš následující text:

```python
print("Ahoj světe!")
```

Pak soubor ulož jako `ahoj.py`:

* V adresáři, kde máš soubory ke kurzům Pythonu, si založ adresář pojmenovaný
  podle čísla lekce: `01`.
  Měl by být vedle tvého virtuálního prostředí.
* Do něj pak soubor ulož pod jménem `ahoj.py`.

Pokud máš v ukládacím okýnku možnost zvolit *kódování*, zvol `UTF-8`.
Můžeš–li zvolit typ souboru, zvol `.py` nebo „všechny soubory“.

Po uložení s příponou `.py` by měl editor program obarvit: text v uvozovkách
by měl mít jinou barvu než slovo `print`.
Barvy napovídají, jak bude Python souboru rozumět.
Až si na ně zvykneš, můžou ti pomoci najít překlepy.


## Spuštění

Otevři si příkazovou řádku.
Pomocí `cd` donaviguj do adresáře, kde máš soubory ke kurzům Pythonu,
tedy adresáře `venv` a `01`.

> [note]
> S příkazovou řádkou jsme se seznámil{{gnd('i', 'y', both='i')}}
> v [minulé lekci](../../beginners/cmdline/), která popisuje i změnu aktuálního
> adresáře pomocí příkazu `cd`.

Aktivuj si virtuální prostředí.

> [note]
> Příkaz k tomu jsme si ukázali na konci
> [návodu na tvorbu virtuálního prostředí](../venv-setup/); končí `activate`.

Pak pomocí `cd 01` zajdi do adresáře s programem.

A pak zadej tento příkaz:

```console
(venv)$ python ahoj.py
```

Pokud se vypíše hláška `Ahoj světe!`, gratuluji!
Napsal{{a}} a spustil{{a}} jsi svůj první program v Pythonu!

Jestli to nefunguje, zkontroluj, že:

* Máš zapnuté virtuální prostředí.
  (Na příkazové řádce se musí ukazovat <code>(venv)</code>;
  pokud tam není, použij příkaz „activate“ z [minula]({{ lesson_url('beginners/install') }}).)
* Jsi ve správném adresáři. Zkus `pwd` (Unix) nebo `cd` (Windows).
  Aktuální adresář musí být ten, do kterého jsi uložil{{a}}
  soubor s programem.
* Soubor se opravdu jmenuje `ahoj.py`.
  Pomocí `ls` (Unix) nebo `dir` (Windows) zkontroluj, že se soubor opravdu
  jmenuje `ahoj.py` a ne třeba `ahoj.py.txt`.
  Jestli ne, ulož ho znovu pod správným jménem.
* Soubor `ahoj.py` obsahuje správný příkaz, včetně všech uvozovek a závorek.
* Slovo `(venv)` ani znak `$` nezadáváš – v materiálech jsou proto, aby bylo
  poznat že jde o příkaz příkazové řádky.
  Na `$` (nebo, na Windows, `>`) končí dotaz, který vypíše sám počítač.
  Příkaz, který zadáváš ty, je jen `python ahoj.py`.

A jestli to pořád nefunguje, zeptej se
{% if var('coach-present') -%}
kouče.
{%- else -%}
zkušenějšího programátora. <!-- XXX: where to direct people? -->
{% endif %}
