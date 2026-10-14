# Lekce 7 – Praktická cvičení

**Obsahová strategie, UX writing a práce s obsahem pomocí AI**


> **Tři pravidla pro všechna cvičení**
>
> 1. Každé faktické tvrzení musí mít oporu v `01-brief.md`. Co v briefu není, zapište jako **ověřit s klientem**.
> 2. Instrukce nesmí záviset jen na barvě, ikoně nebo poloze na obrazovce.
> 3. Do AI nevkládejte osobní údaje, hesla, neveřejné obchodní informace ani celý brief.

 **ukázkový projekt Fakturka** níže.

---

## Ukázkový brief: Fakturka (fiktivní projekt)

Webová aplikace pro jednoduchou fakturaci. Řešíme registraci zkušební verze – typický vstupní scénář moderní webové aplikace, ve kterém se snadno schovají podmínky („co se stane po skončení zkušební doby?“) a kde se často zaměňuje *účet vytvořen* za *účet aktivní*.


```markdown
# 01-brief.md — Fakturka

## Klient
Fakturka s.r.o. – webová aplikace pro jednoduchou fakturaci (fiktivní).

## Cílový uživatel
OSVČ (například grafik, lektor nebo řemeslník), která vystavuje několik faktur
měsíčně. Dnes je píše ve Wordu nebo v Excelu a chce mít faktury na jednom místě.

## Hlavní uživatelský úkol
Založit si 30denní zkušební verzi aplikace.

## Schválený rozsah
- Stránka „Vyzkoušet zdarma“: nabídka + registrační formulář.
- Formulář: e-mail, heslo, IČO.
- Obrazovka po odeslání registrace a aktivační e-mail.
- Mimo rozsah: výběr placeného tarifu, platba, import faktur, mobilní aplikace.

## Ověřená fakta
- F1: Zkušební verze trvá 30 dní, je zdarma a má všechny funkce tarifu Plus.
- F2: K registraci není potřeba platební karta.
- F3: Po 30 dnech se účet automaticky přepne na bezplatný tarif Start
  (nejvýše 5 faktur měsíčně). Nic se neplatí, dokud si uživatel sám nezvolí tarif Plus.
- F4: Tarif Plus stojí 199 Kč měsíčně bez DPH (neomezený počet faktur,
  vlastní logo, automatické upomínky).
- F5: Podle IČO aplikace načte z veřejného registru ARES název nebo jméno
  a adresu sídla. Uživatel je může upravit.
- F6: Po registraci přijde e-mail s aktivačním odkazem. Odkaz platí 24 hodin.
  Bez aktivace se nelze přihlásit.
- F7: Heslo musí mít alespoň 10 znaků.
- F8: Faktury lze stáhnout jako PDF a poslat e-mailem přímo z aplikace.
- F9: Vystavené faktury zůstávají uložené i po přechodu na tarif Start.

## Neověřeno (ověřit s klientem)
- Zda aplikace umí QR platbu na faktuře.
- Zda podporuje plátce DPH.
- Export do účetních programů.
- Co se stane, když uživatel účet do 24 hodin neaktivuje.
- Zda lze pokračovat bez IČO, pokud ho ARES nenajde.

## Interní poznámky (uživateli se nezobrazují)
- Registrace z podzimní kampaně označit „podzim-osvc-b“.
- Nové účty s IČO předat obchodnímu týmu do CRM jako „warm lead“.
```

---

## Cvičení 0 – Diagnostika: co je tu další krok?

**Blok 1 · samostatně, pak společně**

Přečtěte si tři bloky textu. Ke každému napište jedno slovo – **další krok**, **podpůrné** nebo **interní** – a jednou větou zdůvodněte, komu text pomáhá.

| Blok | Text | Zařazení | Proč (komu text pomáhá?) |
|---|---|---|---|
| A | „Rekvalifikační kurz pro změnu kariéry. Připravte se na práci s moderními digitálními službami.“ Tlačítko: *Zobrazit program kurzu* | | |
| B | „Výuku vede lektor a účastník pracuje na vlastním projektu. Před přihlášením si přečtěte podmínky účasti.“ | | |
| C | „Interní poznámka: pro podzimní kampaň použít označení segmentu R-04.“ | | |


---

## Cvičení 1 – Obsahový inventář a priorita

**Blok 3 · samostatně pak společně**

### Krok 1: Hlavní úkol

Dvěma větami si zapište, kdo je uživatel a čeho chce dosáhnout:

```markdown
Uživatel: [ověřený popis z briefu]
Hlavní úkol: [činnost uživatele, např. „založit si zkušební verzi“ – ne interní cíl typu „získat lead“]
Ověřený výsledek akce: [co systém nebo služba skutečně udělá]
```

### Krok 2: Doplňte inventář

Ke stávajícím položkám v `04-content-and-ia.md` doplňte **nejméně tři další**. U každé určete okamžik a typ.

| Okamžik | Položka obsahu | Účel pro uživatele | Typ | Zdroj faktu | Stav ověření |
|---|---|---|---|---|---|
| Před akcí | | | | | |
| Před akcí | | | | | |
| Během akce | | | | | |
| Během akce | | | | | |
| Po akci | | | | | |
| Interně | | | nezařazovat | | nezobrazovat |

- **Okamžik:** před akcí / během akce / po akci
- **Typ:** primární (vede k dalšímu kroku) / podpůrný (pomáhá rozhodnout) / provozní (vysvětluje stav systému)
- **Stav ověření:** ověřeno / ověřit s klientem

### Krok 3: Seřaďte podle priority

Seřaďte řádky v pořadí, v jakém je uživatel potřebuje. Ke každé **primární** položce dopište:

```markdown
- [položka] → uživatel díky ní pozná, že má [konkrétní další krok].
```

Interní položky přesuňte dolů a označte „nezobrazovat“.



**Kontrolní otázky:**

- [ ] Jaký další krok tato položka umožní?
- [ ] Co by se stalo, kdyby tu nebyla?
- [ ] Je pro uživatele, nebo pro interní provoz?
- [ ] Je neznámý údaj označený „ověřit s klientem“?

---

## Cvičení 2 – Přepis nabídky do konkrétního sdělení

**Blok 5 · samostatně, pak čtení nahlas**

Vyberte jeden blok hlavního scénáře (úvod stránky, nabídka služby, krok před formulářem). Napište čtyři řádky **jen z faktů v briefu**.

```markdown
### Hodnotová nabídka – pracovní verze
Nadpis: [co tu uživatel může udělat]
Podnadpis: [jaký užitek nebo co zjistí – ne opakování nadpisu]
Důkaz: [jeden ověřený fakt] — Zdroj: 01-brief.md — [název části]
CTA: [sloveso + předmět: co se stane po kliknutí]
```

**Zakázané:** „nejlepší“, „jedinečný“, „garantujeme“, „poslední šance“, „Klikněte zde“, „Zjistit více“, „Začít“ nebo „Pokračovat“ (pokud jde akci pojmenovat přesněji).

### Společně

Někdo přečte nahlas jen své čtyři řádky. **Autor nic dalšího nevysvětluje.** Ostatní odpoví na dvě otázky:

```markdown
Jako nabídku jsem pochopil/a: …
Po kliknutí na CTA očekávám: …
```

---

## Cvičení 3 – Mikrotexty pro akci, chybu a úspěch

**Blok 8 · samostatně, pak čtení nahlas**

Zvolte **jeden malý** formulář nebo krok se vstupem (registrace, žádost, rezervace, přihlášení k odběru). Napište šest textů:

| # | Prvek | Váš text | Zdroj / poznámka |
|---|---|---|---|
| 1 | Nadpis formuláře / kroku | | |
| 2 | Viditelný label | | |
| 3 | Nápověda (proč údaj chceme / jaký formát) | | |
| 4 | Konkrétní CTA | | |
| 5 | Zpráva pro jednu neplatnou hodnotu (co je špatně + jak opravit) | | |
| 6 | Potvrzení úspěchu + další krok | | |

Volitelně: **Placeholder** (jen příklad formátu, nikdy místo labelu): `…`

### Vaše pravidlo voice and tone

Napište jedno pravidlo, podle kterého jde upravit konkrétní větu (ne „buďte přátelští“):

```markdown
- [pravidlo]
```

### Čtení nahlas

Někdo přečte své texty nahlas v pořadí: nadpis → label → nápověda → CTA → chyba → oprava → potvrzení. Ostatní poslouchají jako uživatel a vlastními slovy řeknou, co mají udělat a co bude následovat.

### Kontrola

Po čtení nahlas si každý zkontroluje svůj text:

- [ ] Text odpovídá hlavnímu úkolu uživatele.
- [ ] Tón odpovídá pravidlům voice and tone.
- [ ] Význam je jasný bez barvy, ikony a odkazu na polohu („červené pole“, „ikona vpravo“).
- [ ] Potvrzení netvrdí víc, než systém podle briefu skutečně udělal.

Podtrhněte **jednu** formulaci, která při čtení nahlas zněla nejasně, a opravte ji.

---

## Cvičení 4 – Redakční kontrola

**Blok 9 · v rámci výkladu**

### 4a) Najděte a opravte tři chyby

```text
Zjistěte více o naší jedinečné nabídce.
Klikněte zde.
Vyplňte červeně označené údaje.
```

| Chyba | Proč je to problém | Váš přepis (pro svůj projekt nebo Fakturku) |
|---|---|---|
| 1 | | |
| 2 | | |
| 3 | | |

### 4b) Přepište formulář

```text
Přihlaste se
[ name@domain.com ]
[ •••••••• ]
Vyplňte červené údaje.
Odeslat
```

Váš přepis:

```text
Nadpis:
Label 1:
Label 2:
Placeholder (volitelně):
Chybová zpráva:
CTA:
```

### 4c) Title a meta description pro stránku hlavního scénáře

```markdown
Účel stránky:
Search intent (s jakým cílem člověk hledá):
Title:
Meta description:
H1:
H2 sekce:
```

### 4d) Kontrola faktů

Najděte ve svém textu jedno tvrzení o ceně, podmínce, omezení, dostupnosti nebo výsledku služby a doplňte zdroj:

```markdown
Tvrzení: „…“
Zdroj: 01-brief.md — [název části] / ověřit s klientem
```

---

## Cvičení 5 – AI varianty, redakční rozhodnutí a copy deck

**Blok 10 · samostatně**

### Krok 1: Prompt

Vyberte jeden mikrotext ze cvičení 3. Vyplňte šablonu **jen ověřenými a neosobními informacemi**:

```text
Kontext produktu: [stručný popis z 01-brief.md]
Cílový uživatel: [ověřený popis]
Úkol uživatele: [konkrétní akce]
Text k vytvoření: [např. chybová zpráva pro pole IČO]
Ověřená fakta: [pouze fakta z briefu]
Tón: [pravidla voice and tone]
Délkový limit: [např. jedna krátká věta]
Zakázané formulace: [negarantovat výsledek, nevytvářet nátlak, nepřidávat fakta]
Hodnoticí kritéria: srozumitelnost, konkrétní další krok, shoda s fakty,
soulad s tónem, význam nezávislý na barvě a ikoně.
Vytvoř tři odlišné varianty a u každé neuváděj žádná nová fakta.
```

### Krok 2: Tři varianty

```markdown
- Varianta A: „…“
- Varianta B: „…“
- Varianta C: „…“
```

Pokud AI vrátí méně než tři varianty nebo přidá nový fakt, upřesněte prompt nebo dopište vlastní variantu.

### Krok 3: Porovnání

| Kritérium | A | B | C |
|---|---|---|---|
| Drží se pouze ověřených faktů? | | | |
| Popisuje konkrétní akci nebo opravu? | | | |
| Odpovídá voice and tone projektu? | | | |
| Je srozumitelná bez barvy, ikony a polohy? | | | |
| Neobsahuje nátlak ani nepodložený slib? | | | |

Pokud žádná varianta neprojde všemi kritérii, nepřebírejte žádnou.
