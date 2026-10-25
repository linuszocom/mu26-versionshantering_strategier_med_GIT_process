# 02 — Visuellt: sidofacket och frågan

Samma bild som i teoriguiden. Glasmontern är det gemensamma publika repot. Glaset är `main`. Sidofacket heter `feature/` och ditt namn. Lådan är klonen på din dator. Frågan är en Pull Request. Knappen heter Merge pull request.

---

## Från låda till glas

```mermaid
flowchart LR
  C["git clone"] --> L["Lådan<br/>main"]
  L --> P["git pull"]
  P --> F["feature och ditt namn"]
  F --> U["git push -u"]
  U --> Q["Fråga mot main"]
  Q --> A["Någon annan Approve"]
  A --> M["Merge pull request"]
```

**Kom ihåg:** Push ställer upp sidofacket. Glaset ändras vid knappen.

---

## Sidofacket kopierar lådan

```mermaid
flowchart TD
  S{"Ligger startfilen i lådans main?"}
  S -->|Nej| H["git checkout main och git pull"]
  H --> B["git checkout -b feature och ditt namn"]
  S -->|Ja| B
```

**Kom ihåg:** `checkout -b` läser inte glaset på skärmen. Den läser lådan.

---

## Frågans riktning

```mermaid
flowchart LR
  R["Rätt"] --> RM["Bas main"]
  RM --> RC["Compare feature och ditt namn"]
  V["Fel håll"] --> VM["Bas feature"]
  VM --> VC["Compare main"]
```

**Kom ihåg:** Läs bas och compare innan du skapar frågan. Någon annan Approve. Inte `git merge` i terminalen.
