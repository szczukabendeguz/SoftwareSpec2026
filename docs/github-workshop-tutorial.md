# GitHub Workshop – Oktatási Anyag

> **Cél:** A csapattagok megismerkedjenek négy fontos GitHub funkcióval, amelyek a napi fejlesztői munkát megkönnyítik.

---

## 1. Branch létrehozása Issue-ból

### Mi ez és miért hasznos?
Ahelyett, hogy kézzel hoznánk létre egy branch-et, a GitHub lehetővé teszi, hogy közvetlenül egy Issue-ból indítsunk el egy új fejlesztési ágat. Így a branch automatikusan össze van kötve az Issue-val, és a PR merge-elésekor az Issue is automatikusan lezárható.

### Lépések
1. Navigálj a repository **Issues** fülére.
2. Kattints a megfelelő issue-ra.
3. A jobb oldali panelben, a **"Development"** szekció alatt kattints a **"Create a branch"** gombra.
4. Állítsd be a branch nevét (pl. `42-fix-login-bug`) és válaszd ki a kiindulási branch-et (általában `main`).
5. Válaszd ki, hogy a branch-et **GitHub-on nyisd meg** (`Checkout locally` vagy `Open in GitHub Desktop`).
6. Kattints **"Create branch"** – kész!

### Tipp
- A branch neve automatikusan az issue számából és nevéből generálódik.
- Ha a branch neve tartalmazza az issue számát (pl. `fix/42-...`), a GitHub automatikusan linkeli.
- PR merge után a hozzárendelt issue lezárul, ha a PR leírásában szerepel: `Closes #42`.

### Hivatalos dokumentáció
- 📄 [Creating a branch for an issue – GitHub Docs](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/creating-a-branch-for-an-issue)
- 📄 [About branches – GitHub Docs](https://docs.github.com/articles/about-branches)

---

## 2. Különböző nézetek a Projects fülön

### Mi ez és miért hasznos?
A GitHub Projects három különböző nézetben jeleníti meg ugyanazokat az adatokat (issue-k, PR-ok, feladatok). Minden nézet más perspektívát ad a projekt állásáról.

### A három nézet

| Nézet | Leírás | Mire jó? |
|---|---|---|
| **Table** (Táblázat) | Táblázatos, Excel-szerű nézet | Részletes áttekintés, szűrés, rendezés |
| **Board** (Tábla) | Kanban-stílusú oszlopos nézet | Sprint/státusz követés (To Do → In Progress → Done) |
| **Roadmap** (Ütemterv) | Idővonalas, Gantt-szerű nézet | Határidők, mérföldkövek vizualizálása |

### Nézet létrehozása / váltása
1. Nyisd meg a repository **Projects** fülét, majd válassz egy projektet.
2. A nézetek fülei a képernyő tetején jelennek meg.
3. Új nézet hozzáadásához kattints a **`+`** gombra a meglévő nézetek mellett.
4. Adj nevet az új nézetnek, majd a nézetfül melletti **`⌄`** (legördülő) ikonra kattintva, a **"Layout"** alatt válassz: **Table / Board / Roadmap**.
5. Az elrendezést bármikor megváltoztathatod anélkül, hogy az adatok elvesznének.

### Szűrés, csoportosítás, rendezés
- **Szűrés:** A keresőmezőbe írj pl. `assignee:username` vagy `label:bug`.
- **Csoportosítás:** A `Group by` opcióval csoportosíthatod az elemeket (pl. státusz, assignee szerint).
- **Mezők testreszabása:** Custom field-eket adhatsz hozzá (pl. prioritás, story points).

### Hivatalos dokumentáció
- 📄 [Customizing views in your project – GitHub Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project)
- 📄 [Changing the layout of a view – GitHub Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/changing-the-layout-of-a-view)
- 📄 [Customizing the board layout](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-board-layout)
- 📄 [Customizing the roadmap layout](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-roadmap-layout)

---

## 3. Issue Template-ek a `.github` mappában

### Mi ez és miért hasznos?
Issue template-ek segítségével előre meghatározott struktúrájú sablonokat adhatunk a csapattagoknak, amikor új issue-t nyitnak. Ezzel elkerülhető, hogy hiányos vagy érthetetlen hibajelentések szülessenek.

### Fájlstruktúra
```
.github/
└── ISSUE_TEMPLATE/
    ├── bug_report.md
    ├── feature_request.md
    └── config.yml        ← (opcionális) template chooser konfigurálása
```

### Template készítése – UI-on keresztül (ajánlott kezdőknek)
1. Menj a **Settings** → **Features** → **Issues** → **Set up templates**.
2. Válassz egy előre elkészített sablont (Bug report / Feature request) vagy kezdj egy üresből.
3. Szerkeszd a sablont a felületen, majd kattints **"Propose changes"** → commit.

### Template készítése – kézzel (fájlban)
Hozz létre egy `.md` fájlt a `.github/ISSUE_TEMPLATE/` mappában:

```markdown
---
name: 🐛 Bug Report
about: Hibajelentés benyújtása
title: "[BUG] "
labels: bug
assignees: ''
---

## 🐛 Mi a hiba?
Rövid leírás...

## 🔁 Reprodukálási lépések
1. ...
2. ...

## ✅ Elvárt működés
...

## 📸 Képernyőkép (ha van)
...

## 💻 Környezet
- OS: [pl. Windows 11]
- Browser: [pl. Chrome 120]
```

### `config.yml` – Template chooser testreszabása
```yaml
blank_issues_enabled: false
contact_links:
  - name: 📬 Kérdés / Ötlet
    url: https://github.com/orgs/community/discussions
    about: Általános kérdéseket ide írj!
```

### Fontos szabályok
- A template fájlok csak az **alapértelmezett branch**-en (pl. `main`) érvényesek.
- `.md` kiterjesztés szükséges (kivéve Issue Forms, ahol `.yml` kell).
- A fájlnév nem case-sensitive.

### Hivatalos dokumentáció
- 📄 [About issue and pull request templates – GitHub Docs](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)
- 📄 [Configuring issue templates for your repository](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)
- 📄 [Syntax for issue forms (yml)](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)

---

## 4. Merge Conflict feloldása a GitHub felületén

### Mi ez és miért hasznos?
Ha két branch ugyanazon fájl ugyanazon sorát módosítja, merge conflict keletkezik. A GitHub webes szerkesztőjével **egyszerű, sor-szintű konfliktusokat** közvetlenül böngészőből is fel lehet oldani – parancssor nélkül.

> ⚠️ **Fontos:** Csak sor-szintű konfliktusok oldhatók fel a webes felületen. Bináris fájlok (képek, stb.) vagy átnevezett fájlok esetén parancssort kell használni.

### Lépések
1. Nyisd meg a **Pull Requestet**, amelyen conflict van.
2. Kattints a **"Resolve conflicts"** gombra.
3. A webes szerkesztőben látni fogod a konfliktus-jelölőket:
   ```
   <<<<<<< feature-branch
   Az én változtatásom
   =======
   A main branch változtatása
   >>>>>>> main
   ```
4. **Döntsd el**, melyik változatot tartod meg (vagy kombinálj belőlük).
5. **Töröld ki** a konfliktus-jelölőket (`<<<<<<<`, `=======`, `>>>>>>>`).
6. Ha több fájlban is van konfliktus, a bal oldalon lévő fájllistán váltogathatsz közöttük.
7. Ha minden konfliktust feloldottál, kattints a **"Mark as resolved"** gombra.
8. Végül kattints a **"Commit merge"** gombra – a változtatások bekerülnek a branch-be.

### Tipp
- Ha konfliktus-feloldás közben összekeveredtél, a szerkesztőből kilépve elölről kezdheted.
- Komplex konfliktusokhoz használj lokális eszközt: VS Code beépített merge editor, vagy `git mergetool`.

### Hivatalos dokumentáció
- 📄 [Resolving a merge conflict on GitHub – GitHub Docs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)
- 📄 [Resolving a merge conflict using the command line](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)

---

## Összefoglaló táblázat

| Funkció | Hol érhető el? | Kulcslépés |
|---|---|---|
| Branch issue-ból | Issue → jobb panel → Development | "Create a branch" gomb |
| Projekt nézetek | Projects fül → nézet `⌄` ikon | Layout: Table / Board / Roadmap |
| Issue template | Settings → Issues → Set up templates | `.github/ISSUE_TEMPLATE/` mappa |
| Merge conflict | PR → "Resolve conflicts" gomb | Jelölők törlése + "Commit merge" |

---

> 📌 *Készítette: Bendegúz Szczuka – GitHub Workshop 2026*
