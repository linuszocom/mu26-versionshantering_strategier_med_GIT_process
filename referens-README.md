# Projekt: Agilt Teamarbete (Gruppnamn: CodeCrafters)

## Scrum-roller
* **Product Owner:** Anna Andersson (även Utvecklare)
* **Scrum Master:** Björn Berg (även Utvecklare)
* **Utvecklare:** Cecilia Carlsson, David Dahl

---

## Sprintmål
När sprinten är klar ska systemet ha ett komplett och verifierat användarflöde där nya besökare kan registrera ett konto, verifiera sina uppgifter och logga in i applikationen.

### Agil motivering
Genom att arbeta i korta, iterativa cykler kan vi testa dellösningar tidigt. Fördelen är att vi kan upptäcka tekniska hinder eller hantera förändrade kundkrav under en Daily Standup och anpassa backloggen utan att missa leveransdatumet.

---

## Produktbacklog

### US-1: Visa gruppens identitet
* **User Story:** Som en besökare vill jag se teamets namn på sidan för att veta vem som skapat applikationen.
* **Acceptanskriterier:** Funktionen `hamtaNamn()` returnerar strängen `"CodeCrafters"` så att rubriken visar teamets namn.
* **Ansvarig:** Anna Andersson

### US-2: Summera beräkning
* **User Story:** Som en användare vill jag få två tal summerade automatiskt för att slippa räkna manuellt.
* **Acceptanskriterier:** `addera(a, b)` returnerar summan av `a + b` så att sidan visar `Summa: 12`.
* **Ansvarig:** Björn Berg

### US-3: Kontrollera statusindikator
* **User Story:** Som en administratör vill jag se en statusbedömning av summan för att snabbt avgöra om värdet är godkänt.
* **Acceptanskriterier:** `statusForTal(tal)` returnerar `"ok"` om värdet överstiger 10, annars `"för låg"`.
* **Ansvarig:** Cecilia Carlsson

### US-4: Analysera textlängd
* **User Story:** Som en redaktör vill jag se längden på ett ord för att kontrollera att det ryms i mobilvyn.
* **Acceptanskriterier:** `raknaTecken(text)` returnerar antalet tecken i strängen (ignorerar mellanslag) så att inputen `"git"` visar `Tecken: 3`.
* **Ansvarig:** David Dahl

---

## Daily Standup & Sprint-anpassning

### Standup-notering
Under morgonens 5-minuters Daily Standup rapporterade alla status på sina funktioner. Inga blockers fanns på logiken, men kunden inkom med en kravändring gällande textanalysen.

### Sprint-anpassning (Kravändring)
* **Vad:** Kunden meddelade att mellanslag ska ignoreras vid teckenräkning för att undvika layoutfel.
* **Vem:** Product Owner tog emot ändringen och uppdaterade acceptanskriteriet för US-4. David Dahl implementerade logiken så att mellanslag filtreras bort.
* **Varför sprintmålet håller:** Eftersom vårt sprintmål testas med ordet `"git"` (som inte innehåller mellanslag) visar sidan fortfarande `Tecken: 3`. Sprintmålet är därmed oförändrat.
