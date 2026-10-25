# 02 — Visuellt: samma rad, sedan kortet

Samma bild som i teoriguiden. Två sidofack från samma glas. Båda byter samma rad. Första frågan går in. Den andra stannar. HEAD är raden som redan ligger i glaset. Sprintmålet väljer namnet. Kortet pekar på den raden.

---

## Varför den andra frågan stannar

```mermaid
flowchart TD
  M["Samma main"] --> A["Sidofack anna<br/>return Norrsken"]
  M --> J["Sidofack johan<br/>return Fjäll"]
  A --> I["Första frågan in i glaset"]
  I --> S["Andra frågan stannar"]
  J --> S
```

**Kom ihåg:** Olika funktioner ger inget sådant stopp. Samma rad gör det.

---

## Valet

```mermaid
flowchart TD
  H["HEAD: raden som redan ligger i glaset"] --> V{"Vad säger sprintmålet?"}
  F["Sidofackets rad"] --> V
  V --> K["Ett namn. Inga markörer."]
  K --> R["Nytt Approve. Merge pull request."]
```

**Kom ihåg:** Den övre raden vinner inte för att den står först.

---

## Kortet mot Closed

```mermaid
flowchart LR
  T["Tunt: vi löste en konflikt"] --> X["Går att flytta till ett annat repo"]
  S["anna och johan, hamtaNamn, Norrsken, sprintmålet"] --> C["Går att peka på i Closed"]
```

**Kom ihåg:** En mening som kan vara vilken grupp som helst är inte ert svar.
