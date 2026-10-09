# 02 — Visuellt: från ark till förseglat kuvert

Samma bild som i teoriguiden. Arket är filen du sparar. Kuvertet med öppen flik är staging. Det förseglade kuvertet, med en mening på fliken, är en commit. Lådan är det `git init` skapade i den här mappen.

---

## Platsen först

```mermaid
flowchart LR
  A["pwd<br/>var står jag"] --> B["ls<br/>vad ligger här"]
  B --> C["cd mina-lappar<br/>steg in"]
  C --> D["pwd igen<br/>rätt mapp"]
```

**Kom ihåg:** Tomt svar från `ls` betyder tom mapp. Det betyder inte att kommandot gick sönder.

---

## Ett ark som skriver över sig

```mermaid
flowchart TD
  M["Måndag: sparad rad"] --> O["Onsdag: samma fil, ny rad"]
  O --> K["Kvar på arket: bara onsdag"]
```

**Kom ihåg:** Spara byter ut arket. Måndagens rad finns inte kvar där.

---

## Tre lägen

```mermaid
flowchart LR
  S["Spara lapp.txt"] --> U["git status<br/>untracked"]
  U --> A["git add lapp.txt"]
  A --> G["git status<br/>changes to be committed"]
  G --> C["git commit -m<br/>en mening"]
  C --> R["git status<br/>nothing to commit"]
```

**Kom ihåg:** `git add` väljer. `git commit` förseglar. `git status` läser och sparar inget.

---

## Två kuvert, ett ark

```mermaid
flowchart TD
  K1["Kuvert 1: mötet är på onsdag"] --> K2["Kuvert 2: mötet flyttat till fredag"]
  K2 --> Ark["Arket visar bara fredag"]
```

**Kom ihåg:** Arket visar slutet. Meningarna på kuverten visar stegen. Kvittot är utskriften från varje commit, inte ett nytt list-kommando.

---

När kartan sitter: [03 — Övningar](./03-ovningar.md).
