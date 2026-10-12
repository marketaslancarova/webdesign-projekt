# AI check

> Záznamy na vstupu jsou skutečné (z `docs/audit_matrix.md`). Výstup AI je ukázkový: je sestavený tak, aby na něm byla vidět podložená i nepodložená tvrzení.

## Prompt

```text
Pracuj pouze s vloženými anonymizovanými záznamy.
1. Shrň shody a rozdíly mezi službami.
2. Uveď rozpory nebo chybějící důkazy.
3. Navrhni otázky k ověření ve veřejně dostupném zdroji.
Nedoplňuj nepozorované funkce, obrazovky, metriky ani chování uživatelů.
Ke každému tvrzení uveď identifikátor zdrojového záznamu.
Každé tvrzení bez zdrojové opory označ jako „nejisté“.
Odděl pozorování od interpretace.
```

## Anonymizovaný vstup

Názvy služeb a adresy jsou odstraněny. Služby jsou označené X, Y a Z.

| Záznam | Služba | Krok | Pozorování | Interpretace |
|---|---|---|---|---|
| record-01 | X | seznam kurzů | Karty kurzů mají název s datem, text s cenou, datum a tlačítko „VÍCE“. Počet volných míst na kartách není. | Dostupnost může uživatel zjistit až po otevření detailu. |
| record-02 | X | detail kurzu | Blok „Vstupenky“ s textem „6 zbývajících míst“, cenou, volbou množství a tlačítkem „Get Tickets“. Na stránce je oddíl „Co je v ceně“ a věta „Místo máte jisté až po zaplacení kurzu“. | Počet míst může pomoci rozhodnout se bez dotazu. Anglický text tlačítka může část uživatelů zarazit. |
| record-03 | Y | stránka klubu | Souvislý text s časem klubu, cenami a větou „Nutné přihlášení předem!“. Hlásit se lze telefonicky nebo e-mailem. Formulář ani údaj o volných místech klubu na stránce nejsou. | O volném místě se uživatel nejspíš dozví až z odpovědi. |
| record-04 | Y | blok „Dnes probíhá“ | Karty jiných kroužků se štítkem „VOLNO“ nebo „OBSAZENO“. Karty se štítkem „VOLNO“ mají tlačítko „ONLINE PŘIHLÁŠKA“. | Online přihláška existuje pro kroužky, u klubu pro dospělé ji stránka nenabízí. |
| record-05 | Z | seznam termínů | Řádky seskupené podle dne: čas, sál, název, štítky a tlačítko s cenou. | Termíny lze rychle projít a cena je vidět bez otevření detailu. |
| record-06 | Z | dnešní termíny | U dvou termínů je místo tlačítka s cenou šedý štítek „Vyprodáno“. Vyprodané termíny v seznamu zůstávají. | Nedostupný termín lze poznat před kliknutím. |

## Výstup AI

1. Služby X a Z ukazují dostupnost přímo v seznamu termínů. (record-01, record-06)
2. Služba X pošle po zaplacení potvrzení e-mailem. (record-02)
3. Služba Z ponechává vyprodané termíny v seznamu. (record-06)
4. Služba Y má pro jiné aktivity online přihlášku, pro klub dospělých ji na stránce nenabízí. (record-03, record-04)
5. Anglické tlačítko u služby X snižuje počet dokončených nákupů. (record-02)
6. U služby X je počet zbývajících míst uveden v detailu kurzu. (record-02)

Otázky k ověření, které AI navrhla: Co se stane u služby X s kurzem, který je plný? Uvádí služba Y, do kdy na přihlášku odpoví?

## Kontrola tvrzení

| # | Stav | Záznam | Poznámka |
|---|---|---|---|
| 1 | nejisté | – | U služby Z to platí (record-06). U služby X je to v rozporu s record-01: v seznamu počet míst není, je až v detailu. |
| 2 | nejisté | – | Record-02 o potvrzení nic neříká. Nic jsem nekupovala, takže nevím, co služba pošle. |
| 3 | podložené | record-06 | Odpovídá pozorování. |
| 4 | podložené | record-03, record-04 | Odpovídá pozorováním. |
| 5 | nejisté | – | Record-02 říká jen „může část uživatelů zarazit“. Počet nákupů z veřejného webu nezjistím. |
| 6 | podložené | record-02 | Odpovídá pozorování. |

## Co z toho používám

- Tvrzení 3, 4 a 6 používám v `competitive_review.md`.
- Tvrzení 1 opravuji: dostupnost v seznamu ukazuje jen služba Z, služba X až v detailu.
- Tvrzení 2 a 5 nepoužívám jako závěr.
- Otázku „Co se stane u služby X s plným kurzem?“ jsem zapsala do srovnání jako „nezjištěno“. Žádný plný termín jsem na veřejných stránkách neviděla.
