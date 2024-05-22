# Uživatelská rozhraní.

> Uživatelská rozhraní. Principy návrhu a vývoje uživatelského rozhraní v moderních softwarových systémech, vč. webových, mobilních. Proces vývoje uživatelského rozhraní a zásady kvality. User experience (UX), interaction design, prototypování, wireframování, uživatelský výzkum, testování použitelnosti. Technologie a nástroje. Příklady z praxe pro vše výše uvedené. (PV182 || PV247 || PV278)

*Fun fact: v PV247 se toho o této otázce (vyjma základů Reactu) moc nedozvíte. Ostatní předměty jsem neměl, tak jen z vlastních zkušeností*

## Zakladne pojmy

User Interface (UI) - priestor kde prebiehaju interakcie medzi ludmi a strojmi, i.e. rozhranie clovek-stroj
User Experience (UX) - ako sa citi uzivatel pri pouzivani produktu/servicy/systemu
User Experience ako disciplina -> disciplina ktora sa zaobera navrhom end-to-end experience pri pouzivani konkretneho produktu/servicy/systemu

V UI riesime vizualnu stranku - color theory, typography, design, animacie, interaktivita (e.g., po kliknuti buttonu dostaneme vizualny feedback ze skutocne sa nieco stalo)
V UX riesime sa aplikacia dobre pouzivala a splnala poziadavky na funkcionalitu - e.g. layout design na lahku orientaciu, nepretazit uzivatela mnozstvom dat a moznosti,...

## Principy návrhu a vývoje uživatelského rozhraní v moderních softwarových systémech, vč. webových, mobilních.

Na vytvorenie dobreho UI aj UX zaroven musime vediet sa vcitit do predstav zakaznikov, spolupracovat so zakaznikom, ziskavat a adaptovat feedback, prototypovat, mat oko pre user-friendly design.

**Design thinking**
- user-centric pristup myslenia, cielom ktoreho pochopit ludske/zakaznikove potreby a navrhnut efektivne riesenia na ich naplnenie
- cyklicke fazy, casto aj vzajomne medzi sebout (neni nutne takto linearny)
    1. empathize - vnimat zakaznikov a ich potreby
    2. define - na zaklade danych vnemov pevne sformulovat problem - co treba vyriesit, komplikacie/problemy, co uzivatel potrebuje, persony...
    3. ideate - vymysliet riesenia problemu - brainstorming, storyboarding, mind mapping, prioritizacia
    4. prototype - realizacia a skusanie konkretnych navrhov - keep it simple, fail fast, iterate quickly
    5. test - otestovanie produktu, ziskavanie feedbacku od uzivatelov, aplikovanie feedbacku, roleplay - refining finalneho navrhu

**Design proces fazy a jeho metody**
Design process vedie k vytvoreniu produktu/servicy/systemu ktory riesi dany problem uzivatelov, aplikujeme v nom design thinking

Fazy a metody pouzivane pocas nich:
1. Discover
    - pochopenie daneho fieldu/cielovky (rozhovory s expertami z fieldu + s uzivatelmi + vlastny research z available materialov (desk research))
    - vystupom je zhrnutie hlavnych poznatkov ohladom problemu
2. Define 
    - **"How might we" otazky** na zadefinovanie problemov a navrh riesenia (bridge medzi define a ideate fazami design thinkingu)
    - **identifikujeme persony** uzivatelov produktu/servicy/systemu ktoru navrhujeme
    - sformujeme **concept statement** - dokument ktory sumarizuje business idea a presviedca o tom ze riesenie je viable (oplati sa realizovat)
    - **SWOT analyza** - identifikujeme strengths, weaknesses, opportunities a threats tykajuce sa produktu v kontexte podnikatelskeho napadu - co nam ulahci pracu, co nas moze spomalit, co mozeme nove priniest/zaujat dalsiu skupinu users,...
    - **stakeholders map** - vizualizujeme vsetky zainteresovane osoby v kontexte produktu a vztahy medzi nimi -> zistime kto je klucovy, kde sa zamerat na budovanie vztahov a comms, etc.
    - dokopy je teda vystupom pevne zadefinovanie problemu
3. Develop
    - sformulovat konkretne navrhy na riesenie
    - prototypovanie navrhov
    - testovanie s users
    - roleplaying
    - celkovo by mal byt vystupom konkretny navrh riesenia
4. Deliver
    - navrh lean business modelu, blueprint, finalna architektura
    - navrh customer journey - predpokladany plan ako potencialny zakaznik pride do kontaktu s produktom, co ho presvedci k pouzivaniu, aby ostal zakaznikom neskor,...
    - navrh touchpoints - zvolit "miesta" kde zakaznik pride do kontaktu s produktom - v kontexte tejto otazky to moze byt mobilna appka/web UI, vseobecny business kontext riesi socialne media/email newsletter/in-person a pod.
    - celkovo je vystupom riesenie problemu

Klíčem k úspěchu UI je uživatelská přívětivost a snadné použití rozhraní. Našlapaný systém s tunou pokročilých funkcionalit bude k ničemu, pokud se nedá jednoduše používat koncovými uživateli. Běžní uživatelé obvykle dokáží systémum s dobrým UI prominout i některé funkcionální nedostatky.

Návrh rozhraní může ovlivňovat
- jedná se i interní, nebo veřejný systém (musí s ním uživatelé pracovat, nebo s ním pracují jen když chtějí?)
- úroveň odbornosti uživatelů
- nutnost možnosti přizpůsobení
- nutnost vícejazyčnosti aplikace (problém mohou dělat třeba odlišné druhy písma)
- nutnost přístupnosti (accessibility) pro uživatele s nějakým omezením (zrakové či sluchové specifické potřeby, nutnost používat pro ovládání pouze myš/pouze klávesnici)
- platforma

UI se obvykle vyvíjí jako monolit, ale je možné dělat i microfrontendy (i.e., mat frontend rozdeleny na samostatne mensie komponenty, ktore sa builduju samostatne, analogicke k microservices).

Je fajn brát v potaz
- uživatelskou přívětivost (složité formuláře je fajn dělit na vícero částí, mít pole top-down (ne tabulka polí))
- bezpečnost - pro aplikace, na které mohou cílit útočníci je fajn stránku uživateli přizpůsobit, třeba jeho fotkou, aby bylo těžké stránku napodobit
    - skrývání hesel
- používání vhodných input polí
- rozhraní by mělo být jednotné
- responsivity - fungování aplikace na různě velkých obrazovkách

V současnosti je nejuniverzálnějším způsobem tvorby UI HTML+CSS+JS. Aktuálně jsou populární frontend js frameworky (React, Vue, Solid, Svelte, Angular..). Lze je použít v prohlížeči, jako desktopovou aplikaci (Electron - přibalí se k aplikaci chromium, nebo s využitím native webview třeba Tauri), pro mobilní aplikace (Progressive Web App - aplikacia, ktora je vytvorena pomocou web technologies ale funguje ako keby bola aplikaciou nativnou pre danu platformu, je schopna s nou interagovat a to aj offline - priklad: Qerko, mam pocit ze pracujem s nativnou mobile appkou, ale pritom sa nemusi stahovat mobilna appka z appstore), případně mají vlastní verze nativní mobilním zařízení (React Native, Svelte Native...). Tyto technologie mají obvykle dobře řešené věci jako accessibility či lokalizace, existují pro ně solidní komponentové knihovny (MaterialUI, Patternfly,...).

Aktuálním trendem se zajímavým potenciálem je WebAssembly, které umožňuje použití kompilovaného jazyka -> napise sa aplikacia v nejakom jazyku, skompiluje sa pomocou dedicated toolu do WASM a WASM binarka je spustitelne a podporovana v hocijakom z mainstream browsers. Výsledná aplikace je typicka rychlejší, než JS. WASM podporuje 2 mody - práci s DOM, nebo přímé vykreslování na canvas (používá třeba Figma). Priklad - Blazor C#

Alternativou může být použití multiplafrormního frameworku Flutter (používá jazyk Dart, podporuje android, ios, web), který umožňuje vývoj pro vícero platform z jednoho zařízení.
MAUI v C# je dobry priklad as well.

Nativními jazyky pro mobilní aplikace jsou swift (ios) a java/kotlin (android).

Pro desktopové aplikace je možné použít i technologie jako GTK (existují bindingy na různé jazyky) nebo Qt (C++), JavaFx/swing, pre C# WPF/WinForms/MAUI/Avalonia...

**Specifika pro web**
- řešíme, kdy je stránka renderovaná
- Server side rendering - plně renderovaná na serveru, vhodné pro statické aplikace
- Client side rendering - renderovaná na straně klienta, data jsou do aplikace přidaná (pomocí dotazů na server)

- Tradičně aplikace fungovaly multi-page (přechod na stránku znamenal kompletně nový page load (e.g. PHP))
- Později se přešlo na single-page přístup pomocí client side rendering
- aktuálně je možné přístupy míchat (initial page load je SSR, následně CSR), což je fajn pro iniciální page load, friendly pro SEO roboty... (e.g. nextjs)

## Proces vývoje uživatelského rozhraní a zásady kvality.

Začneme uživatelským výzkumem, abychom pochopili skutečné požadavky na UI. Následuje návrh pomocí wireframů a prototypů, které můžeme použít pro zpětnou vazbu a jako předlohu pro vývojovou práci. Na konec je důležité provést uživatelské testování s různými typy uživatelů, abychom předešli problémům při nasazení aplikace.
Experimentaciou ziskavame feedback, uistujeme sa ze postupujeme spravnym smerom a robime progres. 

### Uživatelský výzkum, analýza
- Je důležité určit, kdo jsou naši uživatelé, jak dosud pracují se stávajícími systémy, co jim vyhovuje a co ne...
- Je důležité určit, co jsou požadavky na systém, jak se používá (můžeme se snažit o minimalizaci kliknutí pro dosažení operace...)
- s uživateli lze řešit i náš produkt ve **focus groups**
- lze použít A/B testování - každé skupině uživatelů prezentujeme určitou variantu produktu a sledujeme vliv

- vyskum je klasika - zadefinovanie ciela, sledovanych otazok, hypotezy, zozbierania vysledkov, analyza vysledkov, zaver
- analyza
    - kvalitativna - pytame sa preco? ako? - rozhovory s users, user testing - tocime sa okolo user dojmov -> hlbsie pochopenie
    - kvantitativna - kolko? - analyza poctu kliknuti, prechodov, etc. - tocime sa okolo cisel -> vseobecnejsie pochopenie, identifikacia bodov zaujmu

### Interaction design

Snažíme se pochopit, jakým způsobem uživatelé se systémem pracují či interagují a uzpůsobit tomu uživatelské rozhraní. 

### Wireframování

Vhodné pro návrh rozložení jednotlivých komponentů rozhraní, neřešíme barvy/styly, ale jen layout a hrubé rozložení obsahu.
Lahke na vyskusanie/iterovanie navrhov, low effort/time.

Medzikrok medzi wireframovanim a prototypovanim je mockup - obsahuje navyse uz zakladne farby/loga/styly, na lepsiu predstavu ci veci idu spravnym smerom

### Prototypování 

Pomocí návrhových nástrojů jako AdobeXD nebo Figma, lze vytvořit (z části i interaktnvní) prototyp, který lze použít pro prvotní uživatelské testování.
Zahrna design, loga, fonty, styling, etc. - vizualne hotovu sekciu produktu z vizualneho hladiska.
Casovo najnarocnejsie na implementaciu oproti wireframe/mockupu.

Prototyping techonologies - Figma, Miro, Draw.io,... - zavisi od range of features ake potrebujeme

## User experience (UX)

Je kombinací aspektů uživatelského rozhraní
- vizuální krása
- použitelnost (umožňuje fungovat i s omezeními)
- užitnost (umožňuje provádět chtěné akce)
- efektivita (usnadňuje provádění akcí), e.g.
    - uživatel by neměl být nucen do systému zadávat totožnou informaci vícekrát
    - pro časté akce je fajn umožnit použití dobře známých klávesových zkratek

Celkové user experience určuje, zda uživatelé budou chtít náš produkt používat.

## Testování použitelnosti

Může zahrnovat
- pozorování uživatelů při provádění úkonů v rámci systému
    - sledujeme jejich akce, reakce, potíže
    - na základě sledování lze navrhnout řešení
- evaluace experty z oblastí přístupnosti (accessability), lze také použít automatizované nástroje jako Lighthouse
- sledování očí uživatele při používání produktu, zjistíme tak, jaké části rozhraní nejvíce upoutají pozornost uživatelů, je k tomu potřeba souhlas uživatele
