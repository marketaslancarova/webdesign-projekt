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
