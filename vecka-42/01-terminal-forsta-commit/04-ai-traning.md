# 04 — AI-träning: äga kommandona

AI kan rada upp Git på några sekunder. Det betyder inte att du äger ordningen. Här tränar du det examinationen senare frågar: se vad som är svagt, ändra, förklara.

Det är inte magi att granska ett förslag. Det är samma ordning som i teoriguiden. Ett läge, en sak, en mening.

---

## Scenario — problem först

Du ber AI: *“Spara historiken för lapp.txt.”*  
Du får tillbaka något i den här stilen:

```text
cd mina-lappar
git add .
git commit
git log
git push
```

Och meddelandet den föreslår, om du frågar efter ett, är `fix`.

Det kan låta färdigt. Flera rader hör inte hemma i det här materialet, och en rad öppnar en editor utan mening på fliken.

**Vad du tränar:** Feedback på ett förslag, och kommandon du själv kan säga.  
**Varför:** Du ska kunna peka på status, add och commit och säga vad var och en gör.  
**Vad det INTE är:** “AI skrev raderna, alltså kör jag dem.”

---

## Din uppgift (ca 30–45 min)

### Steg 1 — Läs förslaget mot din mapp

Ha `mina-lappar` öppen. Jämför raderna med det du redan gjort i övningarna. Du behöver inte köra förslaget.

### Steg 2 — Granska

- [ ] Står du i rätt mapp, eller antar förslaget det?
- [ ] Väljer `git add .` en namngiven fil, eller allt som ligger där?
- [ ] Har `git commit` en mening efter `-m`?
- [ ] Finns ett kommando som listar lådan, fast kvittot redan kommer från commit?
- [ ] Finns ett kommando som skickar lådan vidare, fast kuverten ska stanna på din dator?
- [ ] Säger meddelandet `fix` vilken rad som ändrades?

Skriv **minst tre** rader:

`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Skriv om, och äg det

Skriv de kommandon du faktiskt skulle köra för en ny rad i `lapp.txt`. En fil, namngiven. En mening som säger ändringen. `git status` före och efter.

Kör dem bara om arket verkligen har en ny rad. Annars räcker det att du kan läsa din omskrivning högt.

### Steg 4 — Reflektion (3–5 meningar)

Vad föreslog texten som du tog bort? Vad satte du i stället, och varför stämmer det med status, add och commit?

<details>
<summary>Facit-riktning, efter din egen granskning</summary>

`git commit` utan `-m` öppnar en editor. Meningen ska sitta i kommandot. `git add .` tar allt i mappen. Här räcker `git add lapp.txt`. `git log` behövs inte: utskriften från commit är kvittot. `git push` skickar lådan vidare, och det hör inte hemma här. `fix` säger inte vilken rad som ändrades.

En omskrivning som räcker:

```text
git status
git add lapp.txt
git commit -m "Lade till att anteckningar ska tas med"
git status
```

</details>
