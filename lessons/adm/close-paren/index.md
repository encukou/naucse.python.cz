# Zapomenutá závorka

Občas se stane, že v interaktivním režimu Pythonu zapomeneš uzavřít závorku:

```python
>>> quit(
...
```

Python pak se pomocí `...` ptá na pokračování příkazu.
Python totiž umožňuje rozepsat případný obsah závorek na víc řádků
a dokud závorku neukončíš (nebo nevyvoláš chybu), neukončí.

Cesta ven je klávesová zkratka <kbd>Ctrl</kbd>+<kbd>C</kbd>,
která ukončí zadávaný příkaz a nechá tě zadat nový:

```python
>>> quit(
... # (Zmáčknu Ctrl+C)
KeyboardInterrupt
>>> 
```

V „grafických“ programech typicky <kbd>Ctrl</kbd>+<kbd>C</kbd>
znamená *kopírovat*, ale v příkazové řádce má starší význam: ukončení.
Python ukončení pomocí klávesové zkratky nazývá `KeyboardInterrupt`:
