
### Képernyő 0: Landing Page (Érkezési oldal új látogatóknak)

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?**
Egy modern, hosszan görgethető, marketing fókuszú weboldal.
    - **Header (Fejléc):** Bal oldalon az alkalmazás logója, jobb oldalon egy diszkrét „Belépés” gomb.
    - **Hero Section (Fő banner):** A képernyő felső részét egy dinamikus, egész képernyős mountain bike-os háttérkép vagy videó uralja. Rajta egy nagy, figyelemfelkeltő címsor (pl. *„Hozd ki a maximumot a bringádból mérnöki diploma nélkül!”*), alatta egy rövid értékajánlat (Value Proposition), és egy hatalmas, kontrasztos „Kezdd el ingyen” gomb.
    - **Features (Funkciók) szekció:** Lejjebb görgetve 3 dizájnos ikon/kártya mutatja be a fő funkciókat: *„1. Intelligens javaslatok”, „2. Közösségi beállítások”, „3. Virtuális garázs”*.
- **Milyen interaktív elemek vannak?**
    - **Fejléc „Belépés” gomb (Secondary Button):** A már regisztrált felhasználóknak szóló gyors link a jobb felső sarokban.
    - **Hero Section „Kezdd el ingyen / Regisztráció” gomb (Primary CTA):** A leginkább kiemelt, pulzáló vagy élénk színű konverziós gomb a képernyő közepén, amely az új érdeklődőket célozza.
    - **Függőleges görgetés (Scroll):** A felhasználó lefelé görgetve felfedezheti a funkciókat bemutató információs blokkokat.
    - **„Próbáld ki most” gomb az oldal alján (Bottom CTA):** A görgetés végén egy ismételt regisztrációs felhívás, hogy ne kelljen visszagörgetni a tetejére.
- **Mi történik a gombnyomás után?**
    - A fejléc **„Belépés”** gombjára kattintva a rendszer a **Képernyő 1-re (Kezdőlap és Autentikáció)** irányítja a felhasználót, és automatikusan a *„Bejelentkezés”* fület (Tab-ot) teszi aktívvá.
    - A Hero szekcióban lévő **„Kezdd el ingyen”**, illetve az oldal alján lévő **„Próbáld ki most”** gombokra kattintva a rendszer szintén a **Képernyő 1-re** ugrik, de úgy, hogy a *„Regisztráció”* (Fiók létrehozása) fül lesz az aktív, felgyorsítva ezzel az onboarding folyamatot, hogy azonnal megadhassa az adatait.

### Képernyő 1: Kezdőlap és Autentikáció

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Felül az alkalmazás logója. Alatta két nagyméretű, váltható fül (Tab): „Bejelentkezés” és „Regisztráció”. Középen szöveges beviteli mezők, alul egy hangsúlyos elsődleges (Primary) gomb.
- **Milyen interaktív elemek vannak?**
    - **Bejelentkezés / Regisztráció fülek:** Kattintásra a képernyőn belül cseréli az űrlapot (nincs oldalváltás).
    - **Email és Jelszó mezők (Input text/password):** Ide gépeli be a felhasználó az adatait.
    - **„Elfelejtett jelszó” szöveges link:** Egy felugró (Modal) ablakot nyit meg a jelszó-visszaállításhoz.
    - **„Belépés” / „Fiók létrehozása” gomb:** Elküldi az adatokat az API-nak.
- **Mi történik a gombnyomás után?**
    - Regisztráció esetén (új fiók, nincs még kerékpár): a rendszer a **Képernyő 3-ra (Új Kerékpár Hozzáadása)** irányít.
    - Bejelentkezés esetén (létező fiók): a rendszer a **Képernyő 2-re (Dashboard)** irányít.


### Képernyő 2: Főoldal (Dashboard) és Garázs

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Felül a jelenleg aktív kerékpár nagy kártyája (kép, név, aktív beállítás neve). Alatta egy görgethető rácsos lista a mentett pályák kártyáival. A képernyő jobb alsó sarkában egy lebegő akciógomb (FAB), alul pedig egy fix navigációs sáv (Navbar).
- **Milyen interaktív elemek vannak?**
    - **„Új kerékpár hozzáadása” ikon (Navbar vagy Header):** Átirányít a **Képernyő 3-ra**.
    - **Aktív kerékpár kártyáján lévő „Szerkesztés” (Ceruza ikon):** Átirányít a **Képernyő 8-ra (Manuális szerkesztés)**.
    - **„Mentett Pályáim” kártyák (pl. Mátra Enduro):** Egy konkrét kártyára bökve a rendszer a **Képernyő 7-re (Pályára érkezés)** ugrik.
    - **Lebegő Akciógomb (FAB) „Új visszajelzés” ikonnal:** Elindítja a hibakeresést, átirányít a **Képernyő 9-re (Intelligens visszajelzés)**.
    - **Alsó Navbar „Közösség” gomb:** Átirányít a **Képernyő 5-re (Közösségi Felfedező)**.


### Képernyő 3: Új Kerékpár és Felfüggesztés Hozzáadása

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Egy letisztult, lefelé görgethető űrlap, amely lépésről lépésre kéri be a hardveres adatokat.
- **Milyen interaktív elemek vannak?**
    - **Kerékpár márka/modell, Villa, Rugóstag legördülő menük (Dropdown/Searchable Select):** A felhasználó rákereshet és kiválaszthatja a SQL adatbázisban szereplő gyári elemeket.
    - **„Testsúly felszerelésben” számmező (Number input):** Numerikus billentyűzetet hoz fel a pontos KG megadásához.
    - **„Vissza” gomb a bal felső sarokban:** Változtatások nélkül visszadob a **Képernyő 2-re**.
    - **„Mentés és Alapbeállítás lekérése” (Nagy, kiemelt gomb):** Validálja az űrlapot.
- **Mi történik a gombnyomás után?** Az adatok rögzülnek a felhasználói profilhoz, és a rendszer továbbléptet a **Képernyő 4-re (Gyári Alapbeállítások)**.


### Képernyő 4: Gyári Alapbeállítások (Base Setup)

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Nagy, jól olvasható számok paneljei (pl. „Villa: 75 PSI”, „Rugóstag: 180 PSI”). A paraméterek mellett kis információs ikonok találhatók.
- **Milyen interaktív elemek vannak?**
    - **Információs („i”) ikonok:** Rábökve egy Tooltip (kicsi felugró buborék) magyarázza el röviden, mi az a PSI vagy a Rebound.
    - **„Adatok módosítása” másodlagos gomb:** Visszavisz a **Képernyő 3-ra**, ha a felhasználó elírta a súlyát.
    - **„Beállítottam, mehetünk!” (Nagy, zöld gomb):** Véglegesíti az első lépéseket.
- **Mi történik a gombnyomás után?** Az alkalmazás ezeket az értékeket menti el „Alapértelmezett” faként, beállítja az aktuális fizikai állapotnak, majd átirányít a **Képernyő 2-re (Dashboard)**.


### Képernyő 5: Közösségi Felfedező (Social Setup Explorer)

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Legfelül egy keresősáv, alatta vízszintesen görgethető szűrő-címkék (Chips). A képernyő nagy részét a többi felhasználó által feltöltött beállításokat mutató listakártyák teszik ki.
- **Milyen interaktív elemek vannak?**
    - **Keresősáv (Search bar):** Szöveges keresés pályanevekre (pl. „Schladming”). Beírásra a lista azonnal szűrődik.
    - **Szűrő-címkék (Toggle Chips):** Pl. „Csak az én bringám”, „+- 5kg súlykülönbség”. Rányomva aktív/inaktív állapotba váltanak, a backend azonnal újrafrissíti a kártyákat.
    - **Közösségi beállítás kártya:** Rákattintva a kártya lenyílik (Accordion), és megmutatja a konkrét teleszkóp értékeket.
    - **„Beállítás Importálása” gomb a lenyílt kártyán belül:** Ezzel indítható el a mentési folyamat.
- **Mi történik a gombnyomás után?** Az importálás gomb azonnal átirányít a **Képernyő 6-ra (Pályaspecifikus Mentés)**, magával víve a kiválasztott értékeket.


### Képernyő 6: Pályaspecifikus Beállítás Mentése

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Egy mentési összesítő űrlap. Felül egy szövegmező, alatta a menteni kívánt értékek listája, legalul pedig láthatósági beállítások.
- **Milyen interaktív elemek vannak?**
    - **„Pálya / Terep neve” mező (Text input):** Ide írja be a felhasználó az azonosítót (pl. „János-hegy esős”).
    - **Láthatóság kapcsoló (Toggle/Switch):** Átkapcsolható „Privát” (csak én látom) és „Publikus” (Közösségi térben megjelenik) között.
    - **„Mégsem” gomb:** Megszakítja a folyamatot, visszavisz az előző képernyőre.
    - **„Pálya Profil Mentése” elsődleges gomb:** Végrehajtja a mentést.
- **Mi történik a gombnyomás után?** Az alkalmazás elmenti az új profilt az adatbázisba, megjeleníti a Dashboardon, és átirányít a **Képernyő 2-re**.


### Képernyő 7: Pályára Érkezés és Alkalmazás (Delta / Abszolút Nézet)

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Felül a kiválasztott pálya neve. Alatta két hatalmas fül (Tab), amik a képernyő módját váltják. Középen a konkrét utasítások listája (pl. „Nyomás: -5 PSI”).
- **Milyen interaktív elemek vannak?**
    - **„Mit tekerjek? (Különbség)” Tab:** Erre kattintva a lista azt mutatja, mennyit kell csavarni a *jelenlegi* beállításhoz képest (pl. +2 kattintás).
    - **„Teljes értékek (Abszolút)” Tab:** Erre kattintva a lista a teljesen zárt állapottól számított teljes értékeket mutatja (pl. 8 kattintás).
    - **„Kész, beállítottam a bringán!” (Jóváhagyó gomb):** Nyugtázza a fizikai módosítást.
- **Mi történik a gombnyomás után?** A szoftver felülírja a „jelenlegi fizikai állapotot” a memóriában ezekre az értékekre, így a rendszer szinkronba kerül a valósággal. Átirányít a **Képernyő 2-re**.


### Képernyő 8: Paraméterek Manuális Szerkesztése

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Haladó nézet. Egy hosszú lista minden lehetséges paraméterről (HSC, LSC, HSR, LSR, PSI), mellettük növelő/csökkentő gombokkal.
- **Milyen interaktív elemek vannak?**
    - **Plusz (+) és Mínusz (-) gombok minden paraméternél (Stepper):** Kattintásonként növelik/csökkentik az adott értéket.
    - **„Mentés jelenlegi állapotként” gomb:** Arra szolgál, ha a felhasználó intelligens asszisztens nélkül állítgatott a hegyen, és ezt akarja rögzíteni.
    - **„Mentés új pályaként” másodlagos gomb:** Ha a most kikísérletezett érték olyan jó lett, hogy külön elmentené.
- **Mi történik a gombnyomás után?**
    - A „Jelenlegi állapotként” gomb menti a módosítást és visszavisz a **Képernyő 2-re**.
    - Az „Új pályaként” gomb átirányít a **Képernyő 6-ra (Mentés)**.


### Képernyő 9: Intelligens Visszajelzés (Ride Feedback)

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Panaszkártyák (címkék) rácsos elrendezésben, alatta egy szabadszöveges mező.
- **Milyen interaktív elemek vannak?**
    - **Gyorspanasz címkék (Multi-select Chips):** Pl. „Felüt az ugrásnál”, „Kevés tapadás”. Több is kiválasztható, rákattintva színt váltanak (aktívak lesznek).
    - **„Egyéb megjegyzés” mező (Textarea):** Ide saját szavakkal lehet gépelni.
    - **„Elemzés és Javaslat kérése” (Kiemelt gomb):** Elküldi az adatokat a backendnek elemzésre.
- **Mi történik a gombnyomás után?** Megjelenik egy 1-2 másodperces töltőképernyő (animáció), amíg az algoritmus kiszámolja a megoldást, majd megnyílik a **Képernyő 10 (Javaslat)**.


### Képernyő 10: Intelligens Javaslat és Véglegesítés

[KÉPERNYŐKÉP BEILLESZTÉSE IDE]

- **Hogyan néz ki?** Egy „Előtte -> Utána” táblázat vizuális megjelenítése a változó paramétereknél. Felette szöveges magyarázat. Alul két gomb (Elfogad / Elvet).
- **Milyen interaktív elemek vannak?**
    - **„Miért javasoljuk ezt?” lenyíló fül (Accordion):** Rákattintva szövegesen elmagyarázza, miért kell a kompresszión állítani a felütés ellen.
    - **„Módosítások elvetése” másodlagos gomb:** Ha a felhasználónak nem tetszik a javaslat, megszakítja a folyamatot.
    - **„Javaslat alkalmazása a [Pálya Neve] beállításra” elsődleges gomb:** Jóváhagyja az utasításokat.
- **Mi történik a gombnyomás után?**
    - Az elvetés visszavisz a **Képernyő 2-re**.
    - Az alkalmazás gomb megnyomásával az új értékek felülírják a pálya eddigi profilját az adatbázisban, és a rendszer ezt állítja be aktív fizikai állapotnak, majd átirányít a **Képernyő 2-re**.

