# Competitive review

> Rozbor vychází ze skutečných veřejných stránek navštívených 12. 10. 2026. Důkazy jsou v `docs/audit_matrix.md` a `docs/evidence/`.

## 1. Vybraná služba a její typ

Dílna Matilda v Brně, přímá konkurence: studio, které na webu nabízí jednorázové kurzy keramiky s nákupem místa.

## 2. Vazba scénáře na hlavní úkol

Hlavní úkol mého uživatele je najít termín kurzu s volným místem a zarezervovat si ho. U Dílny Matilda jsem procházela stejný scénář: seznam kurzů a detail jednorázového kurzu točení na kruhu. U DDM Praha 6 (nepřímá alternativa) jsem sledovala, jak se dospělý přihlásí na keramiku bez rezervace na webu. U Kina Světozor (benchmark) jsem ověřovala jeden krok: jak seznam termínů sděluje dostupnost.

## 3. Tři poznatky podložené důkazy

1. Dílna Matilda uvádí počet zbývajících míst až v detailu kurzu („6 zbývajících míst“), v seznamu kurzů ne (record-01, record-02). Uživatel tak musí otevírat jednotlivé termíny.
2. DDM Praha 6 u keramického klubu pro dospělé nenabízí formulář ani údaj o volných místech, přihlásit se lze e-mailem nebo telefonicky (record-03). Na téže stránce přitom jiné kroužky mají štítek „VOLNO“ nebo „OBSAZENO“ a online přihlášku (record-04).
3. Kino Světozor ukazuje dostupnost přímo v seznamu: u volné projekce tlačítko s cenou, u plné šedý štítek „Vyprodáno“ (record-05, record-06).

## 4. Dvě konvence nebo patterny napříč službami

- **Krátký štítek stavu u termínu:** „VOLNO“ / „OBSAZENO“ u DDM (record-04), „Vyprodáno“ u kina (record-06). Dílna Matilda používá text „6 zbývajících míst“, ale až v detailu (record-02).
- **Akce jen u volných termínů:** u DDM má tlačítko „ONLINE PŘIHLÁŠKA“ jen karta se štítkem „VOLNO“ (record-04), u kina je tlačítko s cenou nahrazeno štítkem „Vyprodáno“ (record-06). Plné termíny přitom ze seznamu nemizí.

## 5. Riziko a příležitosti

- **Riziko:** nejasně pojmenovaná hlavní akce. U Dílny Matilda je tlačítko „Get Tickets“ anglicky na české stránce (record-02). Jak na to uživatelé reagují, z veřejného webu nevím.
- **Příležitost 1:** ukázat volná místa už v seznamu termínů, ne až v detailu (record-01, record-02, record-06).
- **Příležitost 2:** dát uživateli jistotu místa hned, bez čekání na odpověď e-mailem (record-03).

## 6. Návrhové principy

1. Budeme ukazovat počet volných míst u každého termínu už v seznamu, protože u přímé konkurence je vidět až v detailu a uživatel musí termíny otevírat po jednom.
   Důkaz: record-01, record-02, record-06.
2. Budeme obsazené termíny nechávat v seznamu a označovat je jako obsazené, protože uživatel má poznat nedostupnou volbu před kliknutím.
   Důkaz: record-04, record-06.
3. Budeme stav termínu sdělovat slovem, ne jen barvou, protože obě služby, které stav ukazují, používají text.
   Důkaz: record-04, record-06.
4. Nebudeme rezervaci vázat na e-mail nebo telefonát, protože se pak uživatel dozví o volném místě se zpožděním.
   Důkaz: record-03.
5. Budeme na kartě kurzu uvádět, co je v ceně, protože účastníci výzkumu to chtěli vědět před rezervací.
   Zdroj: `03-research-findings.md`, téma 3, source A-04 a C-04. Jistota: medium. Shoduje se s record-02, kde má přímá konkurence oddíl „Co je v ceně“.

Žádný z principů nepřebírá texty, barvy ani rozvržení porovnávaných služeb.
