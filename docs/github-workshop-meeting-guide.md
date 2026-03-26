# GitHub Workshop – Meeting Útmutató (Előadói Vázlat)

> **Időkeret:** ~45–60 perc | **Célközönség:** Csapattagok, akik már ismerik az alapokat (commit, push, PR)

---

## 🎯 Ív és sorrend

A meeting felépítése egy logikus fejlesztői munkafolyamatot követ:
> **Feladat megszületése → Fejlesztés → Projekt nyomon követése → Hibák elkerülése/kezelése**

```
[1] Issue → Branch    →    [2] Templates (megelőzés)    →    [3] Projects nézetek    →    [4] Merge Conflict
```

---

## ⏱️ Időbeosztás (ajánlott)

| Sorrend | Téma | Idő |
|---|---|---|
| Intro | Miért fontos ez? | 3 perc |
| 1. | Branch issue-ból | 10 perc |
| 2. | Issue template-ek | 10 perc |
| 3. | Project nézetek | 12 perc |
| 4. | Merge conflict feloldás | 12 perc |
| Zárás | Kérdések, összefoglalás | 5 perc |

---

## 🔵 INTRO – Miért vagyunk itt? (3 perc)

**Mondanivaló vázlata:**
- "Ma négy olyan GitHub funkciót nézünk meg, amik a napi munkát érezhetően megkönnyítik."
- "Nem elméleti áttekintés – mindent élőben megmutatom."
- "Ha közben kérdés van, bátran szóljatok!"

**Kulcsszavak:** workflow, produktivitás, csapatmunka, élő demo

---

## 🟢 1. TÉMA: Branch létrehozása Issue-ból (10 perc)

### Felütés (1 perc)
> *"Ki szokott kézzel branch-et csinálni és aztán utólag linkelni az issue-hoz? Ezt most megspóroljuk."*

### Kulcspontok
- **Probléma:** Kézzel létrehozott branch-ek nem kapcsolódnak automatikusan az issue-hoz → követhetetlen munka
- **Megoldás:** A GitHub issue jobb oldalán lévő "Development" panel → "Create a branch" gomb
- **Előny:** Branch neve automatikusan generálódik (pl. `42-fix-login`), az issue linkelt, PR merge után az issue lezárul

### Élő demo lépései
1. Megnyitok egy issue-t
2. Jobb panel → "Create a branch"
3. Megmutatom a névgenerálást és a checkout opciót
4. Branch megjelenik a repository-ban

### Amit érdemes kiemelni
- `Closes #42` a PR leírásban → automatikus issue-zárás
- Branch neve tartalmazzon issue számot!
- Összekötött branch látható az issue oldalán

### Kérdés a csapatnak
> *"Valaki szokta már így csinálni? Mi volt a tapasztalat?"*

---

## 🟡 2. TÉMA: Issue Template-ek (.github mappa) (10 perc)

### Felütés (1 perc)
> *"Kaptatok már olyan issue-t, amiből nem lehetett érteni, mi a probléma? Ezt lehet megelőzni."*

### Kulcspontok
- **Probléma:** Üres, hiányos, érthetetlen issue-k → felesleges kérdezés, lassulás
- **Megoldás:** `.github/ISSUE_TEMPLATE/` mappában `.md` fájlok
- **Eredmény:** Amikor valaki új issue-t nyit, sablonból indul → strukturált, teljes információ

### Élő demo lépései
1. Settings → Issues → "Set up templates" megmutatása (GUI út)
2. A generált `.github/ISSUE_TEMPLATE/bug_report.md` fájl megmutatása
3. Egy kész template megnyitása issue-nyitásnál → látszik a sablon
4. (Opcionális) `config.yml` gyors bemutatása – blank issues tiltása

### Amit érdemes kiemelni
- A fájlok csak a **default branch**-en (main) érvényesek
- Frontmatter: `name`, `about`, `labels`, `assignees` mezők
- `.yml` kiterjesztéssel Issue Forms is készíthető (legördülő, checkbox mezők)

### Kérdés a csapatnak
> *"Milyen template-eket használnátok szívesen? Bug report? Feature request?"*

---

## 🟠 3. TÉMA: Project nézetek – Table, Board, Roadmap (12 perc)

### Felütés (1 perc)
> *"Mindenki tudja, hogy van Projects fül, de sokan csak az alapnézetet ismerik. Megmutatom, mire képes."*

### Kulcspontok
- **3 nézet, 1 adathalmaz** – ugyanazok az issue-k, de más perspektívából
- **Table:** Táblázatos nézet, szűrhető, rendezhető – jó áttekintéshez
- **Board:** Kanban tábla – sprint követéshez, állapot alapján (To Do / In Progress / Done)
- **Roadmap:** Idővonalas nézet – határidőkhöz, mérföldkövekhez

### Élő demo lépései
1. Megnyitok egy projektet
2. Megmutatom a Table nézetet: szűrés, csoportosítás
3. Új nézet hozzáadása (`+` gomb) → Board nézet beállítása
4. Board oszlopok testreszabása
5. Roadmap nézet létrehozása → dátummezők beállítása

### Amit érdemes kiemelni
- Minden nézetnek lehet saját neve és beállítása
- Custom field-ek hozzáadhatók (prioritás, story points, etc.)
- A szűrők és csoportosítások nézetenként menthetők
- A Project-et össze lehet kötni a repository-val → auto-hozzáadás

### Kérdés a csapatnak
> *"Melyik nézet tűnik a leghasznosabbnak a mi munkamódszerünkhöz?"*

---

## 🔴 4. TÉMA: Merge Conflict feloldása a GitHub felületén (12 perc)

### Felütés (1 perc)
> *"Mindenki találkozott már merge conflicttal. A jó hír: nem kell mindig terminál ahhoz, hogy megoldjuk."*

### Kulcspontok
- **Mikor keletkezik?** Két branch ugyanazon fájl ugyanazon sorát módosítja
- **Mit tud a GitHub webes felület?** Sor-szintű konfliktusokat fel tud oldani
- **Mit NEM tud?** Bináris fájlok, átnevezett fájlok, komplex refaktorok → ott parancssor kell

### Élő demo lépései
1. Megnyitok egy PR-t, amin conflict van (vagy élőben létrehozom)
2. Megmutatom a "Resolve conflicts" gombot
3. A webes editorban látszanak a jelölők: `<<<<<<<`, `=======`, `>>>>>>>`
4. Kiválasztjuk a helyes verziót, töröljük a jelölőket
5. "Mark as resolved" → "Commit merge"

### Amit érdemes kiemelni
- A conflict marker szintaxis magyarázata (`HEAD` = aktuális branch, a másik = beolvasztandó)
- "Mark as resolved" csak akkor aktív, ha az összes jelölőt töröltük
- Több fájl conflict esetén fájlonként kell végigmenni
- Komplex esetekre: VS Code merge editor, `git mergetool`

### Kérdés a csapatnak
> *"Volt már olyan conflict, ami nem oldódott meg könnyen? Mi volt a helyzet?"*

---

## 🏁 ZÁRÁS (5 perc)

### Összefoglaló – 1 mondat per téma
- **Branch issue-ból:** Issue jobb panel → "Create a branch" → összekapcsolt, követhető munka
- **Issue template:** `.github/ISSUE_TEMPLATE/` → strukturált hibajelentések, feature requestek
- **Project nézetek:** Table / Board / Roadmap → mindenki azt a nézetet használja, ami illik a munkájához
- **Merge conflict:** PR → "Resolve conflicts" → jelölők törlése → commit

### Call to action
> *"Próbáljátok ki még a héten: nyissatok egy issue-t, csináljatok belőle branch-et, és nézzétek meg a projekt board nézetet."*

### Linkek megosztása
- 📄 Részletes tutorial: `docs/github-workshop-tutorial.md` (ez a repo)
- 🌐 GitHub Docs: https://docs.github.com

---

## 📋 Gyorslista: Fontos linkek az előadáshoz

| Téma | Link |
|---|---|
| Branch issue-ból | https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/creating-a-branch-for-an-issue |
| Project nézetek | https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project |
| Nézet layout váltás | https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/changing-the-layout-of-a-view |
| Issue template-ek | https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository |
| Merge conflict (web) | https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github |

---

> 📌 *Előadói vázlat – Bendegúz Szczuka – GitHub Workshop 2026*
