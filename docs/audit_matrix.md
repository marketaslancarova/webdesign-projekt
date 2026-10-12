# Audit matrix

> Služby v této matici jsou skutečné. Pozorování a screenshoty jsou z veřejných stránek dne 12. 10. 2026. Weby se mění, proto má každý záznam čas přístupu. Nic jsem nevyplňovala ani neodesílala.

- Hlavní úkol uživatele (z `01-brief.md`): najít termín kurzu s volným místem a zarezervovat si ho.
- Scénář, který procházím: zájemce chce místo na nejbližším jednorázovém kurzu pro začátečníky.

## 1. Vybrané služby

| # | service_name | service_type | url | Vazba na hlavní úkol | Krok k ověření |
|---|---|---|---|---|---|
| 1 | Dílna Matilda, Brno | přímá konkurence | https://dilna-matilda.cz/keramicke-kurzy-2/ | Uživatel si zde může vybrat termín jednorázového kurzu keramiky a koupit na něj místo. | Seznam kurzů a detail kurzu s nákupem místa. |
| 2 | DDM Praha 6, Keramika pro dospělé | nepřímá alternativa | https://www.ddmp6.cz/kluby/?id=7 | Uživatel se dostane na keramiku, ale bez rezervace na webu: hlásí se předem e-mailem nebo telefonicky. | Jak se dozví o volném místě a jak se přihlásí. |
| 3 | Kino Světozor, program | mezioborový benchmark | https://www.kinosvetozor.cz/ | Uživatel vybírá termín ze seznamu podle dostupnosti, stejně jako u kurzu. | Seznam projekcí a označení vyprodaných termínů. |

## 2. Matice pozorování

Jeden řádek je jedno pozorování na jedné obrazovce nebo v jednom kroku.

| # | service_name | service_type | url | scenario | screen_or_step | observation | interpretation | evidence_link | accessed_at | risk_or_opportunity | confidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| record-01 | Dílna Matilda | přímá konkurence | https://dilna-matilda.cz/keramicke-kurzy-2/ | místo na jednorázovém kurzu pro začátečníky | seznam kurzů | Nahoře je sedm filtrů (například „Točení na kruhu“, „Jednodenní“). Pod nimi jsou karty kurzů: fotografie, štítky, název s datem v závorce, text s cenou, datum a tlačítko „VÍCE“. Počet volných míst na kartách uveden není. | Uživatel v seznamu pozná datum a cenu, ale dostupnost může zjistit až po otevření detailu. | docs/evidence/service-01-step-01.png | 2026-10-12T17:06:31+02:00 | Příležitost: ukázat volná místa už v seznamu termínů. | high |
| record-02 | Dílna Matilda | přímá konkurence | https://dilna-matilda.cz/etn/🎯-jednorazove-toceni-na-kruhu-pro-neznalky-8-9/ | místo na jednorázovém kurzu pro začátečníky | detail kurzu, blok „Vstupenky“ (nic nevybráno, neodesláno) | Vpravo je blok „Vstupenky“ s textem „kurz točení na kruhu jednorázový 16/10 (6 zbývajících míst)“, cenou 1 980,00 Kč, volbou množství a šedým tlačítkem „Get Tickets“. V textu stránky jsou oddíly „Co je v ceně“ a „Rezervace & storno“ s větou „Místo máte jisté až po zaplacení kurzu“. | Počet zbývajících míst může pomoci rozhodnout se bez dotazu. Anglický text tlačítka na české stránce může část uživatelů zarazit. | docs/evidence/service-01-step-02.png | 2026-10-12T17:07:46+02:00 | Příležitost: říct předem, co je v ceně a kdy je místo jisté. Riziko: nejasně pojmenovaná hlavní akce. | medium |
| record-03 | DDM Praha 6 | nepřímá alternativa | https://www.ddmp6.cz/kluby/?id=7 | přihlášení na keramiku pro dospělé | stránka „Keramika pro dospělé“ | Stránka je souvislý text: keramický klub se schází každé úterý od 18 do 20 hodin, jsou uvedeny ceny (1000 Kč / 4 lekce, 300 Kč / lekce) a věta „Nutné přihlášení předem!“. Níže je tučně „Na tyto akce je nutné se hlásit předem telefonicky nebo e-mailem“. Pod textem je rámeček s kontaktem. Přihlašovací formulář ani údaj o volných místech klubu na stránce nejsou. | Uživatel se o volném místě nejspíš dozví až z odpovědi na e-mail nebo telefonát. | docs/evidence/service-02-step-01.png | 2026-10-12T17:07:52+02:00 | Riziko: bez údaje o dostupnosti musí uživatel čekat. Shoduje se s tématem 1 ve výzkumu. | medium |
| record-04 | DDM Praha 6 | nepřímá alternativa | https://www.ddmp6.cz/kluby/?id=7 | přihlášení na keramiku pro dospělé | blok „Dnes probíhá“ ve spodní části téže stránky | V bloku jsou karty jiných kroužků. Každá má štítek „VOLNO“ (zeleně, se zatržítkem) nebo „OBSAZENO“ (červeně, s křížkem). Karty se štítkem „VOLNO“ mají tlačítko „ONLINE PŘIHLÁŠKA“, obsazené ho nemají. | Organizace online přihlášku pro kroužky používá, u keramického klubu pro dospělé ji ale stránka nenabízí. Stav je sdělen textem a ikonou, ne jen barvou. | docs/evidence/service-02-step-02.png | 2026-10-12T17:07:06+02:00 | Příležitost: stav termínu sdělovat slovem a ikonou a akci nabízet jen u volných. | high |
| record-05 | Kino Světozor | mezioborový benchmark | https://www.kinosvetozor.cz/ | výběr termínu podle dostupnosti | program, celý seznam | Program je seznam řádků seskupených podle dne („Dnes“, „Zítra“, „St 14/10“). Každý řádek má čas, sál, název filmu, případné štítky (například „ENG“) a vpravo tlačítko s ikonou vstupenky a cenou (například „170 Kč“). Nad seznamem jsou čtyři filtry. | Uživatel může termíny rychle projít podle dne a času a cenu vidí bez otevření detailu. | docs/evidence/service-03-step-01.png | 2026-10-12T17:07:58+02:00 | Příležitost: seskupit termíny podle data a cenu ukázat přímo v řádku. | high |
| record-06 | Kino Světozor | mezioborový benchmark | https://www.kinosvetozor.cz/ | výběr termínu podle dostupnosti | program, dnešní projekce | U dvou dnešních projekcí (20:15 a 20:30) je místo tlačítka s cenou šedý štítek „Vyprodáno“. Vyprodané projekce v seznamu zůstávají. | Uživatel může poznat nedostupný termín ještě před kliknutím a vidí, že existoval. | docs/evidence/service-03-step-02.png | 2026-10-12T17:07:58+02:00 | Příležitost: obsazené termíny neskrývat, ale označit jako obsazené. | high |

## 3. Srovnání vedle sebe

| Krok úkolu | Dílna Matilda | DDM Praha 6 | Kino Světozor |
|---|---|---|---|
| Jak se uživatel dozví, co je volné | Až v detailu kurzu: „6 zbývajících míst“ (record-02). V seznamu ne (record-01). | U keramického klubu vůbec (record-03). U jiných kroužků štítek „VOLNO“ / „OBSAZENO“ (record-04). | Přímo v seznamu: cena, nebo „Vyprodáno“ (record-05, record-06). |
| Jak zahájí hlavní akci | Zvolí množství a tlačítko „Get Tickets“ (record-02). | Napíše e-mail nebo zavolá (record-03). | Tlačítko s ikonou vstupenky a cenou v řádku (record-05). |
| Co ví před dokončením | Cenu, co je v ceně a storno podmínky (record-02). | Cenu lekce a čas klubu (record-03). | Čas, sál a cenu (record-05). |
| Co se stane s plným termínem | Nezjištěno, žádný plný termín jsem neviděla. | U kroužků štítek „OBSAZENO“ bez tlačítka (record-04). | Zůstává v seznamu se štítkem „Vyprodáno“ (record-06). |

## 4. Co z toho plyne

- Opakující se konvence nebo pattern 1: dostupnost sdělená krátkým štítkem přímo u termínu (record-04, record-06).
- Opakující se konvence nebo pattern 2: akce se nabízí jen u volných termínů, obsazené zůstávají viditelné (record-04, record-06).
- Neobvyklé řešení nebo riziko: tlačítko hlavní akce „Get Tickets“ v angličtině na české stránce (record-02).
- Příležitost pro můj projekt 1: ukázat volná místa už v seznamu termínů, ne až v detailu (record-01, record-02).
- Příležitost pro můj projekt 2: dát uživateli jistotu místa bez čekání na odpověď člověka (record-03).
