# Vítejte na kurzu!

## Co je to programování?

Na začátek vás požádám, abyste se zamysleli nad touhle otázkou:
*co je to programování*?
Co se tady vlastně chcete naučit? Proč jste se přihlásili?

Zapauzujte teď video a zkuste dát v rámci týmu dohromady odpověď.
A jestli jste tým odvážný, podělte se o svou odpověď v diskusi – nejlíp ještě
dřív než vám prozradím tu svoji.
Neexistují žádné špatné odpovědi – ptám se na vaši aktuální představu.

Tak, čas na pauzu …
Jestli jste nezapauzovali, opravdu to doporučuju udělat!

---

Správných odpovědí je spousta – programovat dokonce můžete i jiné věci
než počítače – programování je třeba i sestavování programu koncertu
nebo festivalu, kde program předem říká co se bude dít – kdo zahraje které
skladby kterých autorů a jak půjdou po sobě.

My se ale budeme bavit o programování počítačů, které stručně shrnu takhle:
programovat je *říkat strojům, co mají dělat*.
Počítač je totiž jen stroj.
Je hloupý: dělá jen a pouze a přesně to, co mu programátor řekne.
Dělá to extrémně rychle a bezchybně, ale nemá vlastní vůli.
Umí jen plnit příkazy.
Veškerou chytrost vašich zařízení i softwarové chyby na které narazíte mají
na svědomí programátoři, kteří strojům precizně řekli co mají dělat.

Prvním programovatelným počítačům se příkazy zadávaly přepojováním drátů,
které propojovaly jednotlivé komponenty – sčítačky, násobičky, integrátory –
tak, aby stroj počítal složité matematické příklady.
Odtud máme označení „počítač“.

Později někdo připojil počítač k psacímu stroji a tiskárně a komponenty
propojil tak, aby se příkazy daly zadávat pomocí textu.
To bylo pro lidi mnohem jednodušší a umožnilo to zadávat složitější příkazy.

A pomocí složitějších příkazů někdo stroje naučil to, že se po připojení
obrazovky objeví třeba ikonky, na které se pomocí myši dá kliknout.
Nebo to, že si jednotlivé počítače mezi sebou umí posílat soubory, takže se
můžete dívat na video, které jsem pro vás natočil.
Všechno tohle někdo naprogramoval – řekl strojům, co mají dělat.

A ačkoli dnes už stroje umí ovládání dotykem nebo hlasem, ono programování –
zadávání instrukcí – se dělá nejlíp pomocí textu.
Text se totiž dá jednoduše upravovat, porovnávat, kopírovat a posílat.
Takže i když programátoři dnes používají spoustu klikacích ikonek
a grafických zlepšováků, obecně platí, že když budete tvořit něco nového,
co pro vás ještě někdo nepřipravil, budete psát text.


### Jazyky

Ten text budete psát v nějakém *programovacím jazyce*.
To je způsob, jak počítači předat instrukce.
Programovacímu jazyku rozumí jak lidi – programátoři – tak i počítače.
Když je jazyk dobrý, počítač pochopí instrukce tak jak to programátor zamýšlel.
Programovacích jazyků je spousta, každý má svoje výhody a nevýhody, ale platí,
že když se naučíš jeden, ten další je pak jednodušší.
Jazyk je totiž jen způsob zápisu; důležitější než konkrétní
abeceda je se naučit programátorsky myslet – tedy jaké instrukce počítači dát,
aby dělal to co chceš.

Jak už jsem říkal v úvodu, my použijeme jazyk Python.
Jako většině jiných jazyků ale Pythonu počítače nerozumí rovnou od výroby –
napřed si budeš muset nainstalovat program, který to tvůj počítač naučí.
A kromě toho si nainstaluješ *editor*, neboli nástroj na úpravu textu,
který začneme používat hned na příští lekci.


## Úvod k instalaci

Tahle instalace je ale z jednoho pohledu nejložitější část kurzu.
Na každý druh systému se totiž instaluje trošku jinak,
takže vám budu muset dát k dispozici různé instrukce pro různé operační
systémy: Linux, Windows a macOS.

Co je ještě horší je, že já mám jenom jeden systém – a nemůžu dost dobře
natočit videa pro ty ostatní.
Zeptám se dobrovolníků, jestli by něco nenatočili i pro další systémy,
ale stejně se může stát, že pro tebe budou instalační instrukce jen v textové
verzi.
Ty textové instrukce už pár let je používáme a zkoušíme, takže myslím že s nimi
nebude problém, ale stejně mě trochu mrzí že tenhle videokurz pro tebe možná
začne bez videa.

Každopádně: kdybys měl{{a}} jakékoli problémy, dej vědět v diskusi!
Každý počítač je nastavený trochu jinak, systémy se stále mění a aktualizují,
ale na Discordu jsme připravení pomoct právě a konkrétně tobě.
Ještě jednou – instalace je z jednoho pohledu nejsložitější část kurzu.
Neboj se požádat o pomoc.

Kdybys instalaci konzultoval{{a}} s odborníkem, možná přijdete na to, že
instrukce jsou trochu složitější než by mohly být.
Je to proto, že až bude nainstalováno, chceme aby se všechny počítače
všech účastníků chovaly stejně.
Pro tvůj systém určitě existují nějaké zkratky a my o nich možná i víme,
ale schválně je nepoužíváme.
Až je v budoucnu objevíš, budeš mít o to větší radost :)


### Příkazová řádka

Než začneme se samotnou instalací, seznámím vás se způsobem,
jak ovládat počítač pomocí textu.

Pomocí takzvané *příkazové řádky* (angl. *command line*) můžeš pouštět
programy nebo otevírat soubory ne klikáním na ikonky, ale tak, že napíšeš
příkaz a počítač vypíše odpověď.

Dá se začít i bez ní a ačkoli já řádku používám denně, znám i programátory
kteří ji prakticky nespouští.
Téměř každý programátor ale s příkazovou řádkou umí pracovat a myslím si,
že v rámci tříměsíčního kurzu stojí za to se s ní tochu seznámit.

Na každém systému ale příkazová řádka funguje trochu jinak,
a tak tady skončím a poprosím tě, aby sis v popisku vybral{{a}} svoji variantu.
A až ji projdeš, pokračuj svojí variantou instalace Pythonu a editoru.
