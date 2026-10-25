# 03 — Övningar

**Omfång:** en krock ni tar fram med flit, på samma `return` i `hamtaNamn`. Valet på GitHub, eller samma val i filen med add, commit och push. Ny Approve, **Merge pull request**. Notis. Tre svar och reflektionen i kortet. En genomgång där var och en pekar. Ingen rebase. Inget mergetool. Ingen ny roll. Inga nya kommandon utöver det valet.

Arbeta i samma grupp som montern. Två personer skriver de två texterna. Alla ska kunna peka.

---

## Uppgift 1 — Samma rad, två texter

**Mål:** Den andra frågan stannar, och ni kan säga varför.

**Scenario:** Alla har redan var sin mergad fråga, på olika funktioner. Glaset tar emot dem utan stopp. Det är inte krocken.

**Krav:**
1. Två personer: `git checkout main`, `git pull`.
2. Varsitt nytt sidofack från den `main`, `feature/` och ett namn som inte redan finns. `feature/anna` som redan ligger i glaset går inte att ta igen.
3. Båda byter **bara** `return` i `hamtaNamn`, till olika namn. Rör inget annat.
4. Add, commit med en kort mening, `git push -u origin` och sidofackets namn. En fråga var. Bas `main`.
5. Någon annan Approve på den **första**. **Merge pull request**.
6. Öppna den andra frågan. Den ska visa att den inte kan gå in.

**Klart-check:**
- [ ] Båda sidofacken utgick från samma `main` innan den första frågan gick in
- [ ] Det är samma rad, inte två funktioner
- [ ] Du kan säga varför den andra stannade, utan att öppna sidan

---

## Uppgift 2 — Ett namn, inga markörer

**Mål:** Glaset har sprintmålets namn, och någon annan har sagt ja till den nya raden.

**Krav:**
1. Läs markörerna. **HEAD** är raden som redan ligger i glaset. Den andra är sidofacket.
2. Behåll namnet som sprintmålet redan har. Ta bort `<<<<<<<`, `=======` och `>>>>>>>`. En `return` ska vara kvar.
3. På GitHub: **Resolve conflicts**, **Mark as resolved**, **Commit merge**.
4. Öppnar inte GitHub filen: gör samma val i filen på det andra sidofacket. `git add`, `git commit`, `git push`.
5. Någon annan Approve igen. Sedan **Merge pull request**.
6. Skriv notisen i `README.md` eller som kommentar på den frågan: vilken rad, vilka två sidofack, vilket namn, varför.

**Klart-check (peka i filen och i frågan):**
- [ ] Inga markörer kvar
- [ ] Namnet är det sprintmålet säger
- [ ] Approve efter valet kommer från någon annan
- [ ] Notisen går att läsa mot den frågan

---

## Uppgift 3 — Kortet går inte att flytta

**Mål:** Tre svar och reflektionen pekar på er runda och er Closed.

**Krav:**
1. I `README.md`, ungefär 2–4 meningar per fråga.
   - Agil, kort, och fördelen: raden ni flyttade, meningen som låg kvar.
   - Scrum med minst två begrepp eller roller ni skrivit, och hur ni använde dem.
   - Git och GitHub med ett exempel: ett sidofack, en Approve, krocken.
2. Reflektion, 3–5 meningar. En mening ni ändrade, om ni använde AI.
3. `git checkout main`, `git pull`, sidofack `feature/kortet`, bara kortet, fråga, någon annan Approve, **Merge pull request**.
4. Öppna kortet på GitHub. Läs fråga 3 högt mot **Pull requests → Closed**.

**Klart-check:**
- [ ] Fråga 1 nämner en sak ni flyttade, inte bara ordet flexibelt
- [ ] Fråga 3 innehåller ett namn som finns i er historik
- [ ] Kortet syns i glaset, inte bara i någons låda

---

## Uppgift 4 — Femton minuter, var och en pekar

**Mål:** Du kan din fråga utan att de andra pratar åt dig.

**Krav:**
1. Gruppen tillsammans, ungefär 15 minuter. Repot öppet på Closed. Gärna terminalen eller VS Code.
2. Var och en: peka på din fråga, säg branch, push, PR, review, merge, och en mening om krocken eller om din roll.
3. Första meningen nämner Closed och din fråga. Öppna inte sidan som numret.
4. Den som vill närmare: varför den andra frågan stannade, vad HEAD var, vilket namn ni behöll, och notisen när planen ändrades.

**Klart-check:**
- [ ] Du pekade själv
- [ ] Du sa vem som Approve
- [ ] Sidan var inte det du öppnade först

Sidan ska fortfarande visa gruppnamn, Summa: 12, ok och Tecken: 3. Det är en kontroll efter valet, inte redovisningen.

---

## Stretch — under huven

Säg fyra meningar i följd, med Closed öppet: din fråga, vägen från sidofack till glas, varför krocken uppstod, och hur planen ändrades. Det är väl godkänt-blicken. Kortet ska kunna läsas bredvid det du säger.
