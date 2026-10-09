# 02 — Visuellt: kortet följer med

Samma bild som i teoriguiden. `README.md` är kortet i mappen. Push bär det till glasmontern tillsammans med kuverten. En text som bara säger “Git” pekar inte på en rad.

---

## Tunn text, din text

```mermaid
flowchart LR
  T["Git och staging och push"] --> V["Kan vara vem som helst"]
  D["Måndagens rad försvinner utan kuvert"] --> E["Pekar på din låda"]
```

**Kom ihåg:** 2–4 meningar. Stäng filen och säg dem.

---

## Tre frågor, ett kort

```mermaid
flowchart TD
  F1["1. Varför historik"] --> K["README.md i mappen"]
  F2["2. Ark, add, commit"] --> K
  F3["3. Låda, monter, push"] --> K
  R["Reflektion: ett förslag du ändrade"] --> K
  K --> P["git add README.md"]
  P --> C["docs: besvara teorifragor och reflektion i README"]
  C --> M["Kortet syns i repot"]
```

**Kom ihåg:** `docs:` är standarden för dokumentation. Kortet hemma är inte inlämnat.

---

## Vad du pekar på

```mermaid
flowchart LR
  C["Commits, inte den äldsta raden"] --> F["Säg funktionen"]
  F --> O["ändra, add, commit, push"]
```

**Kom ihåg:** Sidan med namn, Summa: 12 och ok är kontrollen. Raden är förklaringen.

---

## Minst 6 commits på GitHub

```mermaid
flowchart TD
  A["1. docs: index.html med alla tre TODO"] --> B["2. chore: .gitignore"]
  B --> C["3. feat: hamtaNamn"]
  C --> D["4. feat: addera"]
  D --> E["5. feat: statusForTal"]
  E --> F["6. docs: README med svar och reflektion"]
```

**Kom ihåg:** Klicka den allra äldsta. Där ska alla tre TODO fortfarande synas. Commit 2 är `.gitignore`.

---

När kartan sitter: [03 — Övningar](./03-ovningar.md).
