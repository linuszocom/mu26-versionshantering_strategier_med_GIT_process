# 04 — AI-träning: en röd push och ett för brett kuvert

AI kan skriva en svit som ser färdig ut. Här äger du vilka rader som får köras, och att en funktion är ett kuvert.

---

## Scenario — problem först

Du ber AI: *“Lägg upp index.html på GitHub och fixa alla TODO.”*  
Du får tillbaka något i den här stilen:

```text
git pull
git checkout -b fix
git add .
git commit -m "Klart"
git push
```

Och i filen har den ändrat både det funktionerna lämnar tillbaka och raderna under funktionerna.

Det låter som en genväg. Flera rader hör inte hemma här. Ett kuvert med texten `Klart` går inte att peka på.

**Vad du tränar:** Tre feedback-rader, och en omskrivning du kan säga.  
**Varför:** Commits ska visa en funktion per rad, och push ska gå till montern du skapade tom.  
**Vad det INTE är:** Att köra listan för att den är kort.

---

## Din uppgift (ca 30–45 min)

### Steg 1 — Håll förslaget oläst mot din monter

Öppna Commits om du redan har pushat. Jämför med raderna ovan. Kör dem inte.

### Steg 2 — Granska

- [ ] Hämtar förslaget hem ett papper du inte har i lådan?
- [ ] Skapar det en ny linje vid sidan av `main`?
- [ ] Tar `git add .` mer än den fil du just ändrade, till exempel en `.env` som `.gitignore` skulle ha stoppat?
- [ ] Säger meningen `Klart` vilken funktion som ändrades, med prefixet `feat:`?
- [ ] Rör förslaget raderna under funktionerna?
- [ ] Saknas `-u`, `origin` och `main` om det här vore första pushen?

Skriv **minst tre** rader:

`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Skriv om en funktion

Skriv kommandona för **bara** `addera`, från ändrad fil till en rad under Commits. Meningen ska vara `feat: implementera addera`. Använd `git push` om adressen redan sitter. Använd `git push -u origin main` om det är första gången, efter `git branch -M main`.

### Steg 4 — Reflektion (3–5 meningar)

Vilken rad tog du bort, och vad satte du i stället? Peka på en riktig rad under dina Commits om du har den, och säg funktionen.

<details>
<summary>Facit-riktning, efter din egen granskning</summary>

`git pull` hämtar hem något. Den röda pushen i det här materialet löses med ett tomt repo och en ny adress, inte genom att ta in det andra pappret. En ny linje vid sidan av `main` hör inte hemma. `Klart` byts mot `feat: implementera addera`. Raderna under funktionerna lämnas. `git add index.html` räcker. `.gitignore` ska redan ligga i ett eget `chore:`-kuvert, så att `git add .` inte kan dra med en `.env`.

En omskrivning som räcker, när origin redan finns och lådan heter `main`:

```text
git diff
git add index.html
git commit -m "feat: implementera addera"
git push
```

</details>
