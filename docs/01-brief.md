# Project brief – Rezervace místa na kurzu keramiky

> Vzor. Projekt, lidé, rozhovory i odpovědi AI jsou smyšlené.

## Tři možné oblasti projektu

1. **Rezervace místa na kurzu keramiky v malém studiu – VYBRÁNO.** Uživatel: dospělý zájemce o jednorázový kurz. Úkol: najít volný termín a zarezervovat si místo.
2. **Půjčování deskových her v komunitním centru.** Uživatel: návštěvník centra. Úkol: zjistit, jestli je hra volná, a zamluvit si ji.
3. **Přihlašování dobrovolníků na úklidové akce.** Uživatel: dobrovolník. Úkol: vybrat akci a přihlásit se.

## Vybraný námět

- **Pro koho:** dospělí, kteří chtějí vyzkoušet jednorázový kurz keramiky a studio zatím neznají.
- **Hlavní úkol:** najít termín s volným místem a zarezervovat si ho.
- **Proč je rozsah realistický:** jedna skupina uživatelů, jeden úkol, platba probíhá na místě, nepracuje se s citlivými údaji a stačí jméno a e-mail.

## Role a odpovědnosti

| Role | Odpovědnost v tomto projektu |
|---|---|
| Zadavatel | Rozhoduje, které kurzy a termíny se nabízejí a kolik je v nich míst. |
| UX designer | Navrhuje cestu od seznamu kurzů po potvrzení rezervace a ověřuje ji s lidmi. |
| UI designer | Navrhuje vzhled karty kurzu, formuláře a stavů (plno, chyba, potvrzeno). |
| Webdesigner | Skládá obrazovky do responzivních stránek a hlídá jejich soudržnost. |
| Copywriter | Píše názvy kurzů, texty tlačítek, chybová hlášení a potvrzení. |
| Vývojář | Implementuje seznam termínů, formulář a ukládání rezervací. |

**Překrytí rolí:** v malém týmu dělá UX i UI jeden člověk. Odpovědnosti se přesto nemají zaměňovat: UX rozhodnutí (kolik kroků má rezervace) se ověřuje s uživateli, UI rozhodnutí (jak vypadá tlačítko) se ověřuje proti návrhovým pravidlům.

## Pracovní postup

| Krok | Artefakt | Typ |
|---|---|---|
| Porozumění problému | poznámky z rozhovoru se zadavatelkou | důkaz |
| Zadání | tento brief | výstup |
| Vymezení rozsahu | seznam „mimo rozsah“ | rozhodnutí |
| Výzkum | výzkumný plán a syntéza | důkaz |
| Návrh | wireframy a prototyp ve Figmě | výstup |
| Implementace | funkční aplikace | výstup |
| Ověření | záznam z testu s uživatelem | důkaz |

## Bezpečnost a pracovní prostředí

1. **Pracovní místo:** monitor jsem posunula kolmo k oknu, aby se v něm neodráželo světlo.
2. **Technika a kabely:** nabíječka vedla přes průchod. Přepojila jsem ji do zásuvky za stolem.
3. **Ochrana účtu:** na GitHubu a ve Figmě mám zapnuté dvoufázové ověření.
4. **Žádost o klíč:** pokud mě někdo požádá o zaslání API klíče, neposílám ho, ani jeho část. Ověřím žádost u lektorky jiným kanálem.

## Organizace Figmy a FigJamu

- **Před:** FigJam se jmenoval „Untitled“.
- **Po:** „Keramika – 01 Research“.
- **Přínos:** kolega pozná z názvu, ke kterému projektu a fázi prostor patří.

## Stakeholdeři

| Role | Potřeba, rozhodnutí nebo odpovědnost |
|---|---|
| Zákazník / zadavatel | Majitelka studia. Potřebuje zaplnit kurzy bez vyřizování e-mailů. |
| Hlavní uživatel | Zájemce o kurz. Potřebuje vědět, jestli je volno, a mít jistotu místa. |
| Provozovatel | Majitelka studia. Potřebuje přehled, kdo na který termín přijde. |
| Správce obsahu | Majitelka studia. Zadává termíny, kapacitu a popisy kurzů. |
| Osoba rozhodující o prioritách | Majitelka studia. Rozhoduje, co je nutné pro první verzi. |

Jedna osoba zde zastává čtyři role. Rozhodnutí proto zapisujeme podle role, ne podle osoby.

## Cíle a návrhový problém

- **Obchodní cíl:** zaplnit vypsané kurzy bez ručního vyřizování rezervací.
- **Uživatelský cíl:** rychle zjistit, kdy je volno, a mít potvrzené místo.
- **Návrhový problém:** zájemce neví, které termíny jsou volné, dokud nenapíše e-mail a nepočká na odpověď.

## Scénář MVP

Zájemce otevře odkaz ze sociální sítě studia → vidí seznam nadcházejících kurzů s datem, cenou a počtem volných míst → vybere termín → vyplní jméno a e-mail → odešle → vidí potvrzení s názvem a datem kurzu.

## Priority

| Položka | Skupina | Zdůvodnění |
|---|---|---|
| Seznam termínů s počtem volných míst | nutné pro MVP | Bez něj uživatel v kroku výběru nemá z čeho vybírat. |
| Rezervační formulář s potvrzením | nutné pro MVP | Bez něj uživatel úkol nedokončí. |
| Stav „obsazeno“ | nutné pro MVP | Bez něj by šlo rezervovat plný termín. |
| Platba online | vhodné později | Rezervace funguje i s platbou na místě. |
| Zrušení rezervace uživatelem | vhodné později | První verze řeší zrušení e-mailem. |
| Hodnocení lektorů | mimo rozsah | Nesouvisí s hlavním úkolem. |
| Dárkové poukazy | mimo rozsah | Samostatný scénář s vlastními pravidly. |

## Podmínky

- **Omezení:** aplikace nezpracovává platby ani jiné údaje než jméno a e-mail.
- **Riziko:** dva lidé si rezervují poslední místo ve stejnou chvíli.
- **Závislost:** majitelka musí průběžně zadávat termíny a kapacitu.
- **Předpoklad:** zájemci rezervují večer z mobilu. Zatím nedoloženo.
- **Otevřená otázka:** jak často se rezervace ruší a co se má stát s uvolněným místem?

## Kritéria úspěchu

### Kritérium úspěchu 1
- **Scénář nebo požadavek:** hlavní scénář MVP
- **Kritérium:** uživatel, který aplikaci vidí poprvé, dokončí rezervaci bez pomoci.
- **Budoucí ověření:** moderovaný test v lekci 24.
- **Co přesně budeme pozorovat nebo měřit:** zda účastník dojde k potvrzení bez dotazu na moderátora.
- **Poznámka k předpokladu či omezení:** malý vzorek, výsledek není statistický odhad.

### Kritérium úspěchu 2
- **Scénář nebo požadavek:** stav „obsazeno“
- **Kritérium:** na plný termín nelze odeslat rezervaci a uživatel vidí proč.
- **Budoucí ověření:** ruční test s termínem nastaveným na nula míst.
- **Co přesně budeme pozorovat nebo měřit:** zda je akce nedostupná a zobrazí se text o obsazenosti.
- **Poznámka k předpokladu či omezení:** souběh dvou rezervací zatím netestujeme.

## Návrh rozhovoru se zadavatelem

| # | Oblast | Otázka | Které rozhodnutí odpověď ovlivní |
|---|---|---|---|
| 1 | Cíle | Co by se mělo po spuštění změnit ve vašem běžném týdnu? | Formulaci obchodního cíle. |
| 2 | Cíle | Podle čeho poznáte, že se to povedlo? | Kritéria úspěchu. |
| 3 | Uživatelé | Kdo se na kurzy nejčastěji hlásí a jak se o nich dozví? | Vstupní bod scénáře. |
| 4 | Uživatelé | Na co se vás lidé ptají, než se přihlásí? | Obsah karty kurzu. |
| 5 | Obsah | Jaké informace o kurzu dnes lidem posíláte? | Obsahový inventář. |
| 6 | Obsah | Kdo a jak často bude informace aktualizovat? | Rozsah správy obsahu. |
| 7 | Omezení | Co se nesmí stát za žádných okolností? | Rizika a chybové stavy. |
| 8 | Omezení | Jaké údaje od lidí potřebujete a které ne? | Pole formuláře. |
| 9 | Úspěch | Jak dnes zjišťujete, kolik míst zbývá? | Datový model. |
| 10 | Úspěch | Co by vás přimělo vrátit se k e-mailům? | Rizika a priority. |
