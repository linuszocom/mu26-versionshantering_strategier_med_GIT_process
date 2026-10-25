# 01 — Teoriguide: samma rad, sedan kortet

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt, med gruppens repo öppet. Tar du materialet från noll: läs klart, gör sedan [03 — Övningar](./03-ovningar.md). Montern, sidofacket och frågan gäller fortfarande. Inget nytt kommando utöver valet när två sidofack rört samma rad. Ingen ny roll.

Vi börjar med två frågor som båda vill skriva samma rad. Sedan skriver ni kortet så att det pekar på just den raden.

---

## Två sidofack, samma rad

Många tänker nu: “Git blir trasigt när det tar stopp.” Andas. Stoppet är ett val, inte en söndrig fil.

**Metafor:** Två sidofack klipptes från **samma** glas, samma `main`. Båda bytte `return` i `hamtaNamn`, till olika namn. Den första frågan gick in. Glaset har nu en mening på den raden. Den andra frågan stannar, för den vill lägga en annan mening på en rad som redan ändrats.

**Vad det är:** En merge-konflikt. Samma rad, två sidofack, samma utgångsläge.  
**Varför det finns:** Git gissar inte vilket namn gruppen menade.  
**Om det saknas / vad det INTE är:** Olika funktioner krockar inte. Stoppet betyder inte att repot är förstört, och det löses inte med rebase.

**Målsvar (säg högt / skriv i README):** *“Två sidofack från samma main bytte samma return-rad. Första frågan gick in. Den andra stannade, för glaset redan hade en annan mening där.”*

---

## HEAD är raden som redan ligger i glaset

När den andra frågan stannar visar filen tre markörer. Exempel, med era namn i stället:

```text
<<<<<<< HEAD
      return "Norrsken";
=======
      return "Fjäll";
>>>>>>> feature/johan
```

**HEAD** låter som en chef. Här är det raden som redan ligger i glaset, på `main`, efter den första frågan. Under strecket står sidofackets rad, med namnet efter pilarna.

Ingen av dem vinner för att den står överst. Sprintmålet har redan en mening om vad sidan ska visa. Behåll det namnet. Ta bort de tre markörerna. Lämna en `return`.

På GitHub, på den andra frågan: **Resolve conflicts**, när filen går att öppna där. Sedan **Mark as resolved** och **Commit merge**. Någon annan Approve igen. Först därefter **Merge pull request**.

Öppnar GitHub inte filen: samma markörer ligger i filen på det andra sidofacket. En rad, inga markörer, `git add`, `git commit`, `git push`. Sedan nytt Approve och knappen.

**Vad det är:** Ett val mellan två meningar på en rad, sedan samma fråga som förut.  
**Varför det finns:** Historiken ska visa vilken mening som blev kvar, och att någon annan läste den nya raden.  
**Om det saknas:** Att ta den övre raden för att den heter HEAD är en gissning. Rebase och mergetool hör inte hit.

**Målsvar (säg högt / skriv i README):** *“HEAD var raden som redan låg i glaset. Vi behöll namnet från sprintmålet, tog bort markörerna, och någon annan sa ja till den nya raden.”*

---

## Notisen — vilken rad, varför

Skriv i `README.md` **eller** som kommentar på frågan som stannade. Några meningar. Vad som krockade. Vilket namn ni behöll. Varför, kopplat till sprintmålet.

Svagt: “Vi löste en konflikt.”  
Starkare: “anna och johan bytte båda return i hamtaNamn. Vi behöll Norrsken, för den meningen står i sprintmålet.”

**Vad det är:** En pekning, inte ett kvitto på att ni blev klara.  
**Varför det finns:** Någon ska kunna fråga varför just den raden ligger i glaset.  
**Om det saknas:** “Löst” går inte att peka på.

**Målsvar (säg högt / skriv i README):** *“Notisen säger vilken rad, vilka två sidofack, vilket namn som blev kvar, och att sprintmålet redan hade valt det.”*

---

## Kortet pekar på er historik

`README.md` är fortfarande kortet i mappen. Det har redan meningen, raderna, rollerna och notisen om planen. Nu lägger ni till tre svar, ungefär 2–4 meningar var, och en reflektion på 3–5 meningar. Egna ord. En person skriver. De andra säger meningarna.

Frågorna:

1. Vad är agil utveckling kort, och vilken fördel såg ni i er runda? Fördelen ska gå att peka på: en rad som flyttades, och att meningen låg kvar.
2. Beskriv Scrum med minst två begrepp eller roller ni faktiskt använt, och hur.
3. Hur samarbetade ni med Git och GitHub? Ett exempel från er historik: sidofack, fråga, review, och krocken.

Reflektionen: ett tillfälle ni körde fast. Använde ni AI: en mening ni ändrade innan den stämde hos er. “Vi frågade AI” är inte exemplet. Exemplet är meningen ni tog bort.

Kortet in i glaset på samma väg som raderna. `git checkout main`, `git pull`, ett sidofack, till exempel `feature/kortet`, bara `README.md`, fråga, någon annan Approve, **Merge pull request**.

**Vad det är:** Text som går att läsa mot Closed och mot sprintmålet.  
**Varför det finns:** Ett kort som kan vara vilken grupp som helst räcker inte.  
**Om det saknas:** Svaren ska inte kunna flyttas till ett annat repo utan att bli falska.

**Målsvar (säg högt / skriv i README):** *“Fråga 1 pekar på raden vi flyttade. Fråga 2 namnger två roller vi skrivit. Fråga 3 namnger ett sidofack, en Approve och krocken. Reflektionen säger vilken mening vi ändrade.”*

---

## De femton minuterna

Gruppen sitter tillsammans, ungefär 15 minuter. Betyget är ditt. Att de andra pratar räcker inte om du inte kan din del.

Ha repot öppet: **Pull requests → Closed**, frågan som hade krocken, och gärna terminalen eller VS Code. Första meningen nämner din fråga. Sidan i webbläsaren är en kontroll, inte numret ni visar.

Varje person pekar på sin egen fråga eller commit, säger branch, push, PR, review, merge, och säger något kort om krocken eller om sin roll.

Godkänt är den övergripande förklaringen: din fråga och din roll. Väl godkänt går närmare: varför den andra frågan stannade, vad HEAD var, vilket namn ni behöll och varför, och hur planen ändrades när någon inte kunde ta sin rad.

Inga nya kommandon när länken till montern lämnas in och ni sitter de minuterna.

**Målsvar (säg högt / skriv i README):** *“Jag öppnar Closed, pekar på min fråga och på den som sa ja, och säger raden. Sidan är inte numret.”*

---

## Metod — när du tvekar

1. Vilka två sidofack? Vilken rad? Står de kvar i Closed?
2. Vad visar sprintmålet att sidan ska heta? Det namnet är valet. Inte den rad som står överst.
3. Syns `<<<<<<<` kvar i filen? Då är valet inte inne än.
4. Saknas ett nytt Approve efter valet? Knappen väntar.
5. Kan meningen i kortet stå i ett annat repo? Skriv in ett namn från er lista.

**Målsvar (säg högt / skriv i README) — metod:** *“Jag läser sprintmålet, väljer det namnet, tar bort markörerna, och ber någon annan säga ja igen.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Olika funktioner, och inget stopp | Samma `return` i `hamtaNamn`, två texter |
| Den övre raden, för den heter HEAD | HEAD är glasets rad. Sprintmålet väljer |
| “Vi löste konflikten” | Vilken rad, vilket namn, varför |
| Rebase eller mergetool | Markörerna och en rad |
| Kortet kan vara vilken grupp som helst | Ett sidofack och ett namn från er Closed |
| Redovisningen öppnar sidan | Closed, din fråga, den som sa ja |
| Du säger inget, gruppen pratar | Betyget är ditt. Peka på din fråga |

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md) eller [03 — Övningar](./03-ovningar.md).
