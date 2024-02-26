#calculator
##JanLetecky

##index.html:
Tvoříří formulář pomocí značky <form> s atributy method="post" a action="main.php". Z formuláře budou odeslána pomocí HTTP POST na soubor main.php pro zpracování.
Uživatel má možnost zadat první číslo, vybrat operátor ze select boxu a zadat druhé číslo.
Po odeslání formuláře se data odešlou do souboru main.php pro výpočet a zobrazení výsledku.


##main.php:
Skript začíná kontrolou, zda byl formulář odeslán pomocí podmínky if ($_SERVER["REQUEST_METHOD"] == "POST").
Pokud byl formulář odeslán, skript získává data z formuláře pomocí pole $_POST.
Proměnné $num1, $num2 a $operator obsahují první číslo, druhé číslo a operátor z formuláře.
Pomocí příkazu switch se vyhodnotí hodnota operátoru. V závislosti na operátoru se provede matematická operace a výsledek se uloží do proměnné $result.
Pokud je vybrán operátor dělení a druhé číslo je nula, skript nastaví výsledek na "Nelze dělit nulou".
Pokud je vybrán neplatný operátor, skript nastaví výsledek na "Neplatný operátor".
Nakonec se výsledek vypíše pomocí echo v HTML formátu jako <h3> nadpis.