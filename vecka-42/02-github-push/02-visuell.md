# 02 — Visuellt: lådan och montern

Samma bild som i teoriguiden. Lådan är mappen på din dator. Glasmontern är det publika repot. Adressen på luckan heter remote, smeknamn `origin`. `git push` bär kopian. En commit stannar hemma. `.gitignore` är lappen på locket: vissa papper följer inte med.

---

## Två rum

```mermaid
flowchart LR
  H["Lådan hemma<br/>commit"] --> P["git push"]
  P --> M["Glasmontern<br/>Commits på GitHub"]
```

**Kom ihåg:** Pilen går inte av sig själv. Utan push är montern tom eller gammal.

---

## Namnet main

```mermaid
flowchart TD
  I["git init"] --> M["git branch -M main"]
  M --> P["git push -u origin main"]
```

**Kom ihåg:** `-M` döper om lådan innan första båret. Du byter inte till ett annat gren-namn.

---

## Lappen på locket

```mermaid
flowchart TD
  F["hemligheter.env och debug.log syns i git status"] --> G[".gitignore med *.env, *.log och .DS_Store"]
  G --> S["git status: filerna syns inte längre"]
  S --> C["chore: lägg till gitignore för loggar och miljöfiler"]
  C --> P["Först därefter git push"]
```

**Kom ihåg:** Filerna ligger kvar på disken. De slutar synas i `git status` och följer inte med i push.

---

## Adressen

```mermaid
flowchart TD
  V["git remote -v"] --> T{"Syns en länk?"}
  T -->|Nej| A["git remote add origin och länken"]
  T -->|Ja| U["git push -u origin main"]
  A --> U
```

**Kom ihåg:** Tom lista är en saknad adress, inte en trasig fil.

---

## Röd push

```mermaid
flowchart TD
  R["Läs sista raden"] --> K{"Vad säger den?"}
  K -->|Rejected eller fetch first| N["Nytt tomt repo, utan README"]
  N --> B["git remote remove origin"]
  B --> C["git remote add origin, ny länk"]
  C --> P["git push -u origin main"]
  K -->|Ingen adress| A["Lägg till origin"]
  A --> P
  K -->|refspec main does not match| D["git branch -M main"]
  D --> P
```

**Kom ihåg:** Du byter monter, eller döper om lådan till `main`. Du hämtar inte hem pappret som redan låg där.

---

## Minst 5 commits

```mermaid
flowchart TD
  S["1. docs: index.html med alla tre TODO"] --> G["2. chore: .gitignore"]
  G --> A["3. feat: hamtaNamn"]
  A --> B["4. feat: addera"]
  B --> C["5. feat: statusForTal"]
  C --> H["Commits visar minst 5 meningar"]
```

**Kom ihåg:** Klicka den allra äldsta committen. Där ska alla tre TODO fortfarande synas.

---

När kartan sitter: [03 — Övningar](./03-ovningar.md).
