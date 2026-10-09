# 03 — Övningar

**Omfång:** `README.md` med tre svar och en reflektion, pushad till samma publika repo som `index.html`. Kuvertet heter `docs: besvara teorifragor och reflektion i README`. Du pekar på raderna under Commits. Minst 6 commits på GitHub. Inga nya kommandon. Ingen ny linje, ingen hämtning hem.

Saknar du de fem första commits (startfil, `.gitignore`, tre funktioner): gör först [02 — lådan och montern](../02-github-push/03-ovningar.md).

---

## Uppgift 1 — Skriv om den tunna meningen

**Mål:** Fråga 1 är din, 2–4 meningar.

**Scenario:** Någon har klistrat in: “Git är versionshantering och det är viktigt i team.” Den meningen säger inte vad som händer med måndagens rad.

**Krav:**
1. Skapa `README.md` i `git-uppgift`, bredvid `index.html`.
2. Rubrik för fråga 1. Skriv problemet med bara senaste filen, och vad ett förseglat läge bevarar.
3. Stäng filen. Säg svaret högt. Fastnar du: skriv om en mening.

**Klart-check (peka i DIN fil):**
- [ ] 2–4 meningar, inte en definition ur en ordlista
- [ ] Du sa dem utan att titta
- [ ] Ingen har pushat än i den här uppgiften, med flit. Kortet ligger bara hemma

---

## Uppgift 2 — De andra två, och reflektionen

**Mål:** Hela kortet, fortfarande bara på datorn tills uppgift 3.

**Krav:**
1. Fråga 2: arbetsyta, `git add`, `git commit`. Säg vad status gör och inte gör.
2. Fråga 3: lådan mot montern, och vad `git push` bär.
3. Reflektion, 3–5 meningar. Använde du AI: ett förslag du ändrade. Använde du det inte: vad du läste om, vad du testade, och vad `git status` visade.

**Klart-check:**
- [ ] Tre frågor, ungefär 2–4 meningar var
- [ ] Reflektionen har ett konkret tillfälle, inte bara “jag körde fast”
- [ ] Du kan peka på en egen mening och säga vilken fråga den hör till

---

## Uppgift 3 — Kortet till montern

**Mål:** README syns i repot på GitHub. Historiken visar minst 6 commits på GitHub. Den sjätte är kortet, med prefixet `docs:`.

**Krav:**
1. `git status`. `README.md` ska synas som ospårad eller ändrad.
2. `git add README.md`
3. `git commit -m "docs: besvara teorifragor och reflektion i README"`
4. `git push`
5. Öppna repot. Kortet ska gå att läsa där. Öppna Commits. Klicka den allra äldsta. Alla tre `TODO` ska fortfarande synas.

`docs:` är standarden för dokumentationsändringar. Samma prefix som startfilen. `feat:` är funktionerna. `chore:` är commit 2, `.gitignore`.

**Klart-check (peka på GitHub):**
- [ ] README syns utan att du öppnar den lokala filen
- [ ] Minst 6 commits på GitHub, i den här ordningen, äldst först:
  1. `docs: initiera projekt med startkod och tre TODO`
  2. `chore: lägg till gitignore för loggar och miljöfiler`
  3. `feat: implementera hamtaNamn`
  4. `feat: implementera addera`
  5. `feat: implementera statusForTal`
  6. `docs: besvara teorifragor och reflektion i README`
- [ ] Den äldsta visar alla tre TODO
- [ ] Sidan visar ditt namn, Summa: 12 och ok
- [ ] Säg ändra, add, commit, push för README-raden, och säg varför prefixet är `docs:`

**Ägarskap:** Peka på en `feat:`-rad. Säg funktionen. Kan du inte det, är kortet inte klart även om texten är lång.

---

## Peka högt — inför examinationen

Gör rundan två gånger. Första gången med Commits öppen. Andra gången med `README.md` stängd. Säg meningarna högt. Räkna med ungefär 45–60 minuter om du tar båda varven utan att läsa innantill.

**Varv 1 — filen får vara öppen.** Peka på varje commit och säg prefix, vad som ändrades, och en mening du kan stå för.

1. Äldsta, `docs:`: öppna den. Peka på alla tre `TODO`. Säg att starten sparades innan du löste funktionerna.
2. Commit 2, `chore:`: peka på `.gitignore`. Säg att `*.env`, `*.log` och `.DS_Store` slutar synas i `git status` och inte följer med i push. Filerna ligger kvar på disken.
3. `feat: implementera hamtaNamn`: säg vad funktionen lämnar tillbaka nu, och att TODO 1 är borta i den här committen.
4. `feat: implementera addera`: säg att `7 + 5` blir 12, och att bara den funktionen ändrades.
5. `feat: implementera statusForTal`: säg att 12 är större än 10, så sidan visar ok.
6. `docs: besvara teorifragor och reflektion i README`: säg att `docs:` är standarden för dokumentation, och peka på ett av dina tre svar.

**Varv 2 — stäng kortet.** Säg fråga 1, fråga 2 och fråga 3 utan att titta. Öppna bara om du fastnar, skriv om en mening, och säg den igen.

**Klart-check:**
- [ ] Du sa alla sex commits med prefix, utan att läsa meddelandet först på varv 2
- [ ] Du öppnade den äldsta och såg alla tre TODO
- [ ] Du sa vad commit 2 gör, och att den inte raderar filer från disken
- [ ] Du sa ett `feat:`-meddelande och funktionen det hör till
- [ ] Du sa varför README-kuvertet börjar med `docs:`

---

## Innan länken lämnas

Kryssa mot ditt repo. Länken lämnas in samma vecka som examinationen. Den här listan är vad länken ska öppna.

- [ ] Publikt repo
- [ ] `index.html` finns, den allra äldsta committen visar fortfarande alla tre TODO
- [ ] Minst 6 commits på GitHub: startfil, `.gitignore` som commit 2, tre funktioner, README
- [ ] Meddelandena använder `docs:`, `chore:` och `feat:`
- [ ] Sidan: ditt namn, Summa: 12, ok
- [ ] README på GitHub: tre svar och reflektionen, commit `docs: besvara teorifragor och reflektion i README`
- [ ] Du kan säga ändra, add, commit, push, och peka på en rad medan du säger den

---

## Stretch — gå närmare en rad

Frivilligt, samma repo.

Välj en commit som inte är den äldsta och inte är README. Skriv tre korta meningar: vilket prefix och vilken ändring, vad `git add` gjorde som committen inte gjorde ensam, och vad du skulle läsa först om nästa push blev röd.

**Klart-check:** Säg dem högt mot Commits, inte mot webbläsarens sida.
