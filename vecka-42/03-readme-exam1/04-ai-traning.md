# 04 — AI-träning: ett kort som låter färdigt

AI skriver gärna en README som låter som en lärobok, och en historik som säger `Klart`. Här tar du bort det du inte kan säga, och behåller en mening du kan peka på i montern.

Räkna med ungefär 3–4 timmar om du gör alla steg och båda pekrundorna högt. Hoppa inte till facit.

---

## Scenario A — problem först

Du ber AI: *“Skriv README till min Git-examination.”*  
Du får tillbaka något i den här stilen:

> Git skapades för att hantera stora kodbaser. Staging area är indexet där blobbar lagras. Push synkar lådan med montern och löser historiken automatiskt. Använd git log för att visa fyra commits. Commit-meddelandet kan vara “Skrev README”.

Reflektionen den föreslår: “Jag använde AI och det gick bra.”

Texten är lång. Den är inte din låda. Den påstår att push löser historiken åt dig. Den räknar fel, och den tappar prefixet `docs:`.

**Vad du tränar:** Minst tre feedback-rader, och ett omskrivet svar på fråga 2.  
**Varför:** Examinationen godtar inte ett kort du inte kan förklara.  
**Vad det INTE är:** Att klistra in stycket och pusha.

---

## Steg 1 — Lägg texten bredvid din README (ca 20 min)

Jämför stycke för stycke med de tre frågorna. Kör inga nya kommandon från texten.

## Steg 2 — Granska (ca 25 min)

- [ ] Kan du säga meningen när filen är stängd?
- [ ] Pekar den på senaste filen mot förseglade lägen, eller på verktygets historia?
- [ ] Blandar den ihop add och commit?
- [ ] Säger den att push löser historiken åt dig?
- [ ] Ber den om fyra commits, när montern ska visa minst 6?
- [ ] Saknar meddelandet prefixet `docs:`?
- [ ] Har reflektionen ett förslag som faktiskt ändrades?

Skriv **minst tre** rader:

`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

## Steg 3 — Skriv fråga 2 själv (ca 20 min)

2–4 meningar. Arbetsyta, `git add`, `git commit`, och att status bara läser. Inga ord du inte kan peka på i din terminal. Stäng filen och säg dem.

## Steg 4 — Skriv fråga 1 och fråga 3 själv (ca 30 min)

Fråga 1: senaste filen mot ett förseglat läge. Fråga 3: lådan mot glasmontern, och vad `git push` bär. 2–4 meningar var. Säg båda med filen stängd. Fastnar du: skriv om en mening, inte hela kortet.

Reflektion, 3–5 meningar: vilken mening i förslaget tog du bort, vad satte du i stället, och var i repot du kan peka medan du säger den.

<details>
<summary>Facit-riktning för scenario A, efter din egen granskning</summary>

Verktygets historia och ord som blobbar hör inte hemma i svaret. Add väljer, commit förseglar, de är inte samma steg. Push bär en kopia. Den skriver inte om kuverten och löser inte en röd rad åt dig. En lista över lådan behövs inte: Commits på GitHub är vyn. Fyra commits räcker inte. Minst 6 commits på GitHub. README-kuvertet är `docs: besvara teorifragor och reflektion i README`, för `docs:` är standarden för dokumentation. Reflektionen behöver ett exempel du ändrade, inte att det “gick bra”.

En fråga 2 som räcker, om orden är dina:

Arbetsytan är filen jag sparar. git add väljer just den filen till nästa kuvert. git commit förseglar det och kräver en mening. git status talar om läget och sparar ingenting.

</details>

---

## Scenario B — ett kuvert som heter Klart (ca 40 min)

Du ber AI: *“Lägg upp examinationen på GitHub.”* Du får tillbaka:

```text
git add .
git commit -m "Klart"
git push
```

Och en kommentar: “Fyra rader räcker, startfilen plus funktionerna. README kan ligga i samma commit.”

**Krav:** Kör listan inte. Skriv om den till den tidslinje montern ska visa, äldst först. Ett kuvert per rad. Prefix på varje rad.

1. `docs: initiera projekt med startkod och tre TODO`
2. `chore: lägg till gitignore för loggar och miljöfiler`
3. `feat: implementera hamtaNamn`
4. `feat: implementera addera`
5. `feat: implementera statusForTal`
6. `docs: besvara teorifragor och reflektion i README`

**Klart-check:**
- [ ] Du sa högt varför `git add .` kan dra med en `.env` om `.gitignore` saknas
- [ ] Du sa att commit 2 är `.gitignore`, och att filerna ligger kvar på disken
- [ ] Du sa att README inte får dela kuvert med en funktion
- [ ] Du sa att `docs:` är dokumentation, `chore:` är skyddet, `feat:` är en funktion

---

## Peka högt, varv 1 — Commits öppen (ca 40 min)

Öppna fliken Commits på GitHub. Peka med fingret eller markören. Säg prefixet innan du läser meningen, så du märker om du bara rabblar.

1. Äldsta. Öppna filen i den committen. Peka på TODO 1, TODO 2 och TODO 3. Säg att starten sparades innan funktionerna löstes.
2. Commit 2. Peka på `.gitignore`. Läs `*.env`, `*.log` och `.DS_Store`. Säg att matchande filer försvinner ur `git status` och inte pushas. Öppna mappen på datorn och säg att en `.env` du skapade fortfarande ligger där, om du har en.
3. `feat: implementera hamtaNamn`. Säg ditt namn, och att raderna under funktionerna inte rördes.
4. `feat: implementera addera`. Säg `a + b`, och att sidan därför kan visa Summa: 12.
5. `feat: implementera statusForTal`. Säg villkoret: större än 10 ger ok, annars för låg.
6. `docs:` för README. Peka på ett svar i kortet på GitHub, inte i den lokala filen. Säg varför prefixet är `docs:`.

**Klart-check:** sex pekningar, och den äldsta visade alla tre TODO.

---

## Peka högt, varv 2 — kortet stängt (ca 40 min)

Stäng `README.md`. Stäng också fliken Commits. Säg sedan, i den här ordningen, utan att öppna:

1. Fråga 1, 2–4 meningar.
2. Fråga 2, med arbetsyta, add, commit och vad status inte gör.
3. Fråga 3, låda, monter, push.
4. Tidslinjen: sex meningar, med prefix. Commit 2 ska vara `.gitignore`.
5. En `feat:`-rad du väljer själv: funktionen, vad den lämnar tillbaka, och att du skulle köra `git diff` innan nästa kuvert.
6. Vad du läser först om push blir röd: sista raden, sedan `git status` eller `git remote -v`, sedan en sak.

Öppna Commits igen bara för att kontrollera. Rättade du en mening: `git add README.md` och, om du redan har `docs:`-kuvertet, ett nytt kuvert `docs: justera formuleringar for tydlighet`. Pusha. Kortet i montern ska vara det du kan säga.

**Klart-check:**
- [ ] Du sa fråga 1 utan filen
- [ ] Du rabblade inte “fyra rader”
- [ ] Du sa minst 6 commits på GitHub, med `.gitignore` som commit 2
- [ ] Du sa `docs: besvara teorifragor och reflektion i README` utan att titta på meddelandet först

---

## Sista kontrollen mot montern (ca 20 min)

Öppna repot i ett fönster där du inte är inloggad, om du kan. Annars öppna den publika sidan och låtsas att du är den som granskar.

- [ ] Kortet syns först, med tre svar och reflektionen
- [ ] Commits visar minst 6
- [ ] Den allra äldsta har alla tre TODO
- [ ] Commit 2 är `.gitignore`
- [ ] Sidan: ditt namn, Summa: 12, ok
- [ ] Du kan peka på en `feat:`-rad och säga funktionen på under tio sekunder
