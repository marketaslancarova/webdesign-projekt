# AI work log

> Vzor. Projekt, lidé, rozhovory i odpovědi AI jsou smyšlené.

## Lekce 1 – orientační dotaz

**Účel:** zjistit, kam v projektu patří budoucí dokumenty. AI nesmí nic měnit.

**Vstupní podklady:** struktura složky projektu.

**Prompt:**

**Shrnutí odpovědi vlastními slovy:** AI doporučila složku `docs/`, protože obsahuje projektovou dokumentaci, a navrhla číslovaný název souboru.

**Kontrola výstupu**

| AI položka | Zdroj | Rozhodnutí | Důvod |
|---|---|---|---|
| Výzkum patří do `docs/` | struktura složky | accepted | Ve složce už je `01-brief.md`, odpovídá to účelu. |
| Navržený název `research.md` | – | corrected | Použiji číslovaný název podle zadání kurzu. |

**Lidské rozhodnutí:** žádný soubor se nezměnil. Ověřila jsem pohledem do složky, že AI nic nevytvořila.

---

## Lekce 2 – hledání nejasností v briefu

**Účel:** najít mezery a rozpory v briefu. AI nesmí doplňovat fakta, čísla ani funkce.

**Vstupní podklady:** anonymizovaný popis projektu z `01-brief.md`.

**Prompt:** převzat z domácího úkolu lekce 2 („Pracuj pouze s anonymizovaným popisem projektu níže…“).

**Kontrola výstupu**

| AI položka | Zdroj | Rozhodnutí | Důvod |
|---|---|---|---|
| „Není jasné, co se stane při zrušení rezervace.“ | brief, podmínky | accepted | Zapsáno jako otevřená otázka. |
| „Chybí informace, kdo zadává termíny.“ | brief, stakeholdeři | accepted | Doplněna role správce obsahu. |
| Kritérium „80 % uživatelů dokončí rezervaci do dvou minut“ | žádný | rejected | Číslo nemá oporu v žádných datech a nemáme jak ho měřit. |

**Kontrola návrhu AI**
- **Návrh AI:** 80 % uživatelů dokončí rezervaci do dvou minut.
- **Rozhodnutí:** odmítnuto
- **Důvod:** vymyšlená hodnota bez metodiky a bez dat.
- **Upravené kritérium nebo další krok:** „Uživatel, který aplikaci vidí poprvé, dokončí rezervaci bez pomoci.“ Ověřím pozorováním při testu.

**Lidské rozhodnutí:** do briefu jsem doplnila dvě otevřené otázky a kritérium úspěchu v upravené podobě.

---

## Lekce 3 – třídění poznámek z rozhovoru

**Účel:** roztřídit poznámky na potvrzené informace, předpoklady, konflikty a otevřené otázky. AI nesmí přidávat nové informace ani návrhy řešení.

**Vstupní podklady:** `03-feedback-notes.md`, poznámky N1–N10 bez identifikujících údajů.

**Prompt:** převzat z domácího úkolu lekce 3 („Pracuj pouze s uvedenými poznámkami…“).

**Kontrola výstupu**

| AI item | Source note ID | Decision | Reason |
|---|---|---|---|
| Rezervace probíhají e-mailem a zprávami (confirmed) | N1 | accepted | Odpovídá doslovnému výroku. |
| Kapacita je osm míst (confirmed) | N4 | accepted | Odpovídá doslovnému výroku. |
| Zákazníci jsou nespokojení s čekáním (confirmed) | N2 | corrected | N2 je moje interpretace, ne výrok. Přeřazeno do předpokladů. |
| Telefon je povinný údaj (confirmed) | N8 | rejected | N8 říká „hodil by se“ a je v rozporu s N7. Zapsáno jako konflikt. |
| Není známa četnost rušení (open question) | N9 | accepted | Odpovídá poznámce. |
| Studio potřebuje platební bránu (assumption) | – | rejected | Žádná poznámka to neuvádí, N6 říká opak. |

**Lidské rozhodnutí:** do briefu jsem přenesla tři potvrzená zjištění, jeden konflikt a jednu otevřenou otázku. Dvě položky AI jsem nepoužila.

---

## Lekce 4 – kritika výzkumného plánu

**Účel:** najít naváděcí otázky a nesoulad mezi cílem, otázkami a metodou. AI nesmí vytvářet data, respondenty ani persony.

**Vstupní podklady:** výzkumný cíl, metoda a scénář z `02-research-plan.md`.

**Prompt:** převzat z domácího úkolu lekce 4 („Zkontroluj tento výzkumný cíl, metodu a scénář…“).

- **Připomínka AI nebo kolegy:** otázka „Co vám na tom vadilo?“ předpokládá, že něco vadilo.
- **Rozhodnutí:** přijímám
- **Důvod:** shoduje se s tím, co ukázal pilot, účastnice odpověděla „nic“.
- **Změna v `02-research-plan.md`:** otázka přepsána na „Co bylo nejtěžší nebo nejpomalejší?“

- **Připomínka AI nebo kolegy:** doporučení přidat dotazník pro 50 respondentů.
- **Rozhodnutí:** odmítám
- **Důvod:** cílem je porozumět průběhu a důvodům, ne měřit četnost. Dotazník by neodpověděl na výzkumné otázky.
- **Změna v `02-research-plan.md`:** žádná.

---

## Lekce 5 – oponentura affinity mapy

- **Date:** lekce 5
- **Tool and mode:** Codex, režim bez zápisu
- **Anonymization and settings check:** poznámky obsahují jen `source_id`, typ a text bez identifikujících údajů. Zkontrolováno před vložením.
- **Purpose:** získat alternativní seskupení karet a najít rozpory.
- **Input scope:** dvanáct poznámek z `pilot-notes.md`.
- **AI proposal:** (1) sloučit témata 1 a 2 do jednoho „Nejistota“; (2) vytvořit téma „Mobilní uživatelé“ z B-03; (3) označit C-01 jako rozpor s tématem 1.
- **Decision:**
  - (1) rejected – čekání na volné místo a nejistota po odeslání jsou dvě různé chvíle na cestě uživatele.
  - (2) rejected – téma by stálo na jedné kartě a C-03 mu odporuje.
  - (3) accepted – C-01 doplněna jako výjimka u tématu 1.
- **Checked against source_id:** A-01, B-01, B-02, B-03, C-01, C-03
- **Reason:** každé rozhodnutí jsem ověřila proti textu karet.
- **Contradictions or limits:** AI nabídla téma podložené jedinou kartou. U tří účastníků nelze mluvit o „mobilních uživatelích“ jako o skupině.

---

## Lekce 6 – kontrola shrnutí konkurenční analýzy

**Účel:** shrnout shody a rozdíly mezi třemi službami a najít chybějící důkazy. AI nesmí doplňovat nepozorované funkce, metriky ani chování uživatelů.

**Vstupní podklady:** šest anonymizovaných záznamů `record-01` až `record-06` z `docs/audit_matrix.md`, bez názvů služeb a adres.

**Prompt:** převzat z domácího úkolu lekce 6, celý je v `docs/ai_check.md`.

**Kontrola výstupu**

| AI položka | Zdroj | Rozhodnutí | Důvod |
|---|---|---|---|
| X a Z ukazují dostupnost přímo v seznamu | record-01, record-06 | corrected | U služby X to odporuje record-01: počet míst je až v detailu. Platí jen pro Z. |
| Služba X pošle po zaplacení potvrzení e-mailem | – | rejected | Nic jsem nekupovala, v záznamech to není. |
| Z ponechává vyprodané termíny v seznamu | record-06 | accepted | Odpovídá pozorování. |
| Y má online přihlášku pro jiné aktivity, pro klub dospělých ne | record-03, record-04 | accepted | Odpovídá pozorováním. |
| Anglické tlačítko snižuje počet nákupů | – | rejected | Metrika, kterou z veřejného webu nezjistím. |
| U služby X je počet míst v detailu kurzu | record-02 | accepted | Odpovídá pozorování. |

**Lidské rozhodnutí:** do `docs/competitive_review.md` jsem použila tři podložená tvrzení a jedno opravené. Otázku AI na plný kurz u služby X jsem nedokázala ověřit a zapsala ji do srovnání jako „nezjištěno“.
