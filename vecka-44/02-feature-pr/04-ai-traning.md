# 04 — AI-träning: en fråga som hoppar över glaset

AI kortar gärna vägen: hoppa över pull, merga i terminalen, godkänn dig själv. Här tar du bort genvägarna och behåller sidofacket, frågan och någon annans ja.

---

## Scenario — problem först

Du ber AI: *“Lägg in min funktion på main i gruppens repo.”*  
Du får tillbaka något i den här stilen:

> Hoppa över pull, den är för team som ligger efter. Kör `git checkout -b feature/anna` direkt, den hämtar senaste main från GitHub. Ändra alla TODO på en gång. Pusha till main. Merga sedan själv med `git merge feature/anna`. Godkänn din egen Pull Request så det går fort. Skriv “Klart” som text.

Det låter effektivt. Sidofacket kopierar lådan, inte glaset. Alla TODO i ett fack suddar ut vem som tog vilken rad. `git merge` och ett eget ja är inte frågan.

**Vad du tränar:** Minst tre feedback-rader, och en omskriven mening till Pull Request.  
**Varför:** Examinationen tittar på din fråga och på vem som godkände den.  
**Vad det INTE är:** Att köra stycket.

---

## Din uppgift (ca 30–45 min)

### Steg 1 — Lägg texten bredvid er historik

Jämför med sidofacket, basen och vem som klickade Approve. Inför inget nytt kommando.

### Steg 2 — Granska

- [ ] Kommer pull före `checkout -b`?
- [ ] Är det en rad per person, inte alla TODO i samma fack?
- [ ] Går push till `feature/` och ditt namn?
- [ ] Är bas `main` och compare ditt sidofack?
- [ ] Godkänner någon annan, under Files changed?
- [ ] Är vägen knappen **Merge pull request**, inte `git merge`?
- [ ] Säger frågetexten vilken rad, inte bara “Klart”?

Skriv **minst tre** rader:

`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Skriv om meningen

En mening du skulle klistra in i frågan. Den ska namnge raden.

**Målsvar (säg högt / skriv i README):** *“Pull hämtar glaset först. Sidofacket är feature och mitt namn. Någon annan Approve. Knappen lägger in raden. Frågetexten säger vilken.”*

### Steg 4 — Reflektion

3–5 meningar. Vilken mening i förslaget tog du bort, och vad skulle ha hänt i er monter om ni kört den?

---

## Facit — riktning

<details>
<summary>Visa riktning efter din egen granskning</summary>

Rimliga feedback-rader pekar på pull före sidofacket, en rad var, push till `feature/` och namnet, bas `main`, någon annans Approve, och knappen i stället för `git merge`.

En mening som håller: “hamtaNamn lämnar tillbaka gruppnamnet, så sidan visar namnet.”

Svagt om du behåller “Klart”, ett eget ja, eller terminalkommandot `git merge`.

</details>
