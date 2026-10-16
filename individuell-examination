# Individuell examination: Git & GitHub

Du ska på egen hand visa att du behärskar det praktiska grundflödet i Git och GitHub via terminalen. Målet är inte att bygga en stor applikation eller skriva avancerad kod, utan att skapa en ren, spårbar och begriplig historik på GitHub.

Koden för funktionerna finns färdig i instruktionen så att du slipper fastna på JavaScript. Det som bedöms är hur du använder Git i terminalen, hur du bygger din historik och dina förklaringar i `README.md`.

Uppgiften bedöms helt skriftligt utifrån ditt publika GitHub-repo och din `README.md`.

---

## Arbetsgång steg för steg

### 1. Skapa repot och koppla ihop
- Skapa ett **publikt** repo på GitHub som heter `git-uppgift`. Lämna det helt tomt (bocka inte i README, .gitignore eller licens).
- Skapa mappen lokalt på din dator, initiera repot med `git init`, standardisera grennamnet till `main` (`git branch -M main`) och koppla repot till GitHub (`origin`).

### 2. Spara utgångsläget (Commit 1)
- Skapa filen `index.html` i din projektmapp och klistra in koden från avsnittet "Startkod" längst ner. Rör ingenting i koden än – alla tre `TODO` ska finnas kvar.
- Staga filen, skapa en commit med ett eget beskrivande meddelande om att startkoden lagts till, och pusha till GitHub med `-u origin main`.

### 3. Skydda projektet med .gitignore (Commit 2)
- Skapa filen `.gitignore` i samma mapp.
- Lägg till regler för att ignorera systemskräp och tillfälliga filer:
  ```text
  *.env
  *.log
  .DS_Store
  ```
- Staga filen, committa med ett eget tydligt meddelande om vad filen gör, och pusha till GitHub.

### 4. Lös funktionerna stegvis (Commit 3, 4 och 5)
Lös funktionerna i `index.html` en i taget. Baka inte ihop ändringarna – varje funktion ska få en egen commit och push!

*(Rör inte koden längst ner under funktionerna som hanterar utskriften på sidan.)*

#### Funktion 1: hamtaNamn (Commit 3)
1. Öppna `index.html` och byt ut funktionen `hamtaNamn()` mot följande kod (ersätt med ditt eget namn och ta bort `TODO 1`-kommentaren):
   ```javascript
   function hamtaNamn() {
     return "Ditt Förnamn Efternamn";
   }
   ```
2. Spara filen och granska ändringen i terminalen med `git diff`.
3. Staga filen, committa med ett beskrivande meddelande för vad ändringen gör, och pusha till GitHub.

#### Funktion 2: addera (Commit 4)
1. Byt ut funktionen `addera(a, b)` mot följande kod (ta bort `TODO 2`-kommentaren):
   ```javascript
   function addera(a, b) {
     return a + b;
   }
   ```
2. Spara filen och granska ändringen i terminalen med `git diff`.
3. Staga filen, committa med ett beskrivande meddelande, och pusha till GitHub.

#### Funktion 3: statusForTal (Commit 5)
1. Byt ut funktionen `statusForTal(tal)` mot följande kod (ta bort `TODO 3`-kommentaren):
   ```javascript
   function statusForTal(tal) {
     if (tal > 10) {
       return "ok";
     }
     return "för låg";
   }
   ```
2. Spara filen.
3. Öppna `index.html` i din webbläsare och kontrollera snabbt att sidan visar **ditt namn**, texten **Summa: 12** och ordet **ok**.
4. Staga filen, committa med ett beskrivande meddelande, och pusha till GitHub.

### 5. Dokumentera och analysera i README.md (Commit 6)
- Skapa filen `README.md` och besvara frågorna nedan med dina egna ord.
- Staga filen, committa med ett tydligt meddelande och pusha till GitHub.

---

## Instruktioner för README.md

<details>
<summary>💡 Klicka här för en snabb lathund i Markdown (för snyggare formatering) helt frivilligt och påverkar inte betyget</summary>

<br>

Formatera gärna din `README.md` med Markdown:

- **Rubriker:** Skriv `# Rubrik 1`, `## Underrubrik` eller `### Mindre rubrik`
- **Fet text:** Skriv `**fet text**`
- **Punktlista:** Starta raden med `- `
- **Numrerad lista:** Starta raden med `1. `, `2. ` osv.

</details>

<br>

Besvara följande frågor direkt i din `README.md` med egna ord (ca 2–4 meningar per fråga).

### Fråga 1: Versionshantering vs vanliga filer
- **För Godkänt (G):** Vad är versionshantering och vad är den stora skillnaden mellan att spara en fil via editorns vanliga sparaknapp och att spara ändringar i Git?
- **För Väl Godkänt (VG):** Förklara vad som menas med att Git sparar en tidslinje av frysta ögonblicksbilder (commits). Vad bevisar det faktum att du när som helst kan klicka på din allra första commit på GitHub och fortfarande se alla tre `TODO` kvar i koden, trots att filen på din dator ser helt annorlunda ut idag?

### Fråga 2: Arbetsytan, Staging och Commits
- **För Godkänt (G):** Beskriv vad kommandona `git status`, `git add` och `git commit` gör i det dagliga arbetsflödet och när du kör dem.
- **För Väl Godkänt (VG):** Förklara relationen mellan **arbetsytan (arket på skrivbordet)**, **staging (kuvertet)** och **commit (arkivlådan)**. Förklara också varför Git protesterar med `no changes added to commit` om man har ändrat filen i editorn och försöker köra `git commit` direkt utan `git add`.

### Fråga 3: Lådan hemma vs Montern på GitHub
- **För Godkänt (G):** Vad är skillnaden mellan mappen på din dator och repot på GitHub, och vad gör kommandot `git push`?
- **För Väl Godkänt (VG):** Förklara konceptet med **de två rummen / minnesytorna** (lådan hemma på datorn vs glasmontern på GitHub). Förklara varför `git push` svarar `Everything up-to-date` om du har ändrat i koden men glömt att staga och committa innan du kör push.

---

## Klart-check (kontrollera innan inlämning)

- [ ] Mitt GitHub-repo är **publikt** så att det går att granska.
- [ ] När jag dubbelklickar och öppnar `index.html` i webbläsaren syns mitt namn, texten **Summa: 12** och ordet **ok**.
- [ ] Fliken **Commits** på GitHub innehåller minst **6 commits** som visar utvecklingsresan steg för steg.
- [ ] Repot innehåller en committad `.gitignore` som exkluderar relevanta filer.
- [ ] `README.md` är ifylld med egna svar på frågorna.

---

## Betygskriterier

Bedömningen sker helt skriftligt utifrån ditt GitHub-repo och innehållet i `README.md`.

### Godkänt (G)
- Samtliga punkter i Klart-checken är uppfyllda.
- Historiken under Commits på GitHub visar att uppgiften lösts steg för steg (minst 6 commits med egna, begripliga meddelanden som beskriver vad som gjorts).
- `README.md` besvarar G-nivån på de tre frågorna med egna ord.

### Väl Godkänt (VG)
- Samtliga krav för Godkänt är uppfyllda.
- **Tydlig och ren historik:** Commit-meddelandena är genomgående informativa, konsekventa och beskriver vad varje ändring tillför. Ändringarna är isolerade per commit (atomära commits) och repot är skyddat av `.gitignore`.
- **Djupare systemförståelse:** `README.md` besvarar även VG-nivån på de tre frågorna och visar tydlig förståelse för Gits inre mekanik (ögonblicksbilder, relationen mellan arbetsyta/staging/arkiv, de två minnesytorna och varför fellägena uppstår).

---

## Inlämning

Lämna in genom att klistra in länken till ditt publika GitHub-repo i Moodle.

---

## Startkod (index.html)

Kopiera koden nedan exakt och spara som `index.html`:

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <title>Git-uppgift</title>
</head>
<body>
  <h1>Git-uppgift</h1>
  <p id="namn"></p>
  <p id="summa"></p>
  <p id="status"></p>
  <script>
    // TODO 1: Returnera ditt eget namn (just nu returneras "TODO").
    function hamtaNamn() {
      return "TODO";
    }

    // TODO 2: Returnera summan av a och b (just nu returneras alltid 0).
    function addera(a, b) {
      return 0;
    }

    // TODO 3: Returnera "ok" om talet är större än 10, annars "för låg".
    function statusForTal(tal) {
      return "TODO";
    }

    document.getElementById("namn").textContent = hamtaNamn();
    const summa = addera(7, 5);
    document.getElementById("summa").textContent = "Summa: " + summa;
    document.getElementById("status").textContent = statusForTal(summa);
  </script>
</body>
</html>
```
*(Observera: Koden under de tre funktionerna ska inte ändras; den hanterar endast utskriften på webbsidan.)*
