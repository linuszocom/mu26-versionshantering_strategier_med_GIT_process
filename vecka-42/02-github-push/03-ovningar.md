# 03 — Övningar

**Omfång:** ett publikt repo utan README från start, `git branch -M main`, `.gitignore` innan push, `git remote`, `git push`, fliken Commits, startfilen med tre `TODO`, en commit per funktion. Minst 5 commits under Commits. Ingen ny linje vid sidan av `main`. Ingen hämtning hem av någon annans papper. Raderna under funktionerna rör du inte, och du förklarar inte taggar.

---

## Uppgift 1 — Montern är tom

**Mål:** Du kan visa att en commit hemma inte syns på GitHub, och att lådan heter `main` innan du bär något.

**Scenario:** Skapa ett tomt publikt repo på GitHub. Bocka inte i README, inte i gitignore och inte i licens. Skapa mappen `git-uppgift`. `git init` där, efter `pwd`. Sätt namnet direkt. Klistra in startfilen som `index.html`.

**Krav:**
1. `git branch -M main` direkt efter `git init`.
2. `git add index.html`
3. `git commit -m "docs: initiera projekt med startkod och tre TODO"`
4. Öppna repot på GitHub innan du pushar. Det ska inte visa din fil.

**Klart-check (peka i DIN terminal och på GitHub):**
- [ ] `git status` säger `On branch main`
- [ ] Commit-utskriften hemma, med prefixet `docs:`
- [ ] Säg varför GitHub fortfarande saknar filen
- [ ] Första filen innehåller fortfarande `return "TODO"` och `return 0`

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

---

## Uppgift 2 — Lappen på locket, innan båret

**Mål:** `.gitignore` gör att `.env` och `.log` slutar synas i `git status`, utan att filerna försvinner från disken. Skyddet är ett eget kuvert, fortfarande bara hemma.

**Krav:**
1. Skapa `hemligheter.env` och `debug.log` i samma mapp. `git status` ska visa dem.
2. Skapa filen `.gitignore` med exakt de här tre raderna:

```text
*.env
*.log
.DS_Store
```

3. Kör `git status` igen. `hemligheter.env` och `debug.log` ska vara borta ur listan. Bara `.gitignore` ska vara ny. Filerna ska fortfarande ligga kvar i mappen.
4. `git add .gitignore`
5. `git commit -m "chore: lägg till gitignore för loggar och miljöfiler"`
6. Pusha inte än. Öppna GitHub. Montern ska fortfarande sakna dina filer.

**Klart-check:**
- [ ] `git status` visar inte `hemligheter.env` eller `debug.log`
- [ ] Säg högt att filerna ligger kvar på disken
- [ ] `git log --oneline` visar två rader: `docs:` underst i tid, `chore:` överst
- [ ] GitHub är fortfarande tomt, eftersom du inte har pushat

---

## Uppgift 3 — Adressen och första båret

**Mål:** Två rader under Commits. Den äldsta visar fortfarande alla tre TODO. `.gitignore` syns bland filerna. `hemligheter.env` syns inte.

**Krav:**
1. Kopiera repots adress.
2. `git remote add origin` och adressen. `git remote -v` ska visa den.
3. `git push -u origin main`
4. Öppna **Commits**. Två rader. Öppna den allra äldsta. Alla tre `TODO` ska synas i filen där.
5. På repots filsida: `index.html` och `.gitignore`. Inte `hemligheter.env`, inte `debug.log`.

**Klart-check:**
- [ ] `git remote -v` med din länk
- [ ] Två rader under Commits, samma meningar som hemma: `docs:` och `chore:`
- [ ] Säg vad `-u` gjorde, så att nästa push kan vara kortare
- [ ] Den äldsta committen har alla tre TODO kvar

<details>
<summary>Om Git frågar vem du är, eller öppnar en editor</summary>

`Please tell me who you are`: sätt namn och e-post, kör samma commit igen.

```text
git config --global user.name "Ditt Namn"
git config --global user.email "du@epost.se"
```

Editor utan `-m`: Esc, `:q!`, Enter, och commit igen med meningen.

</details>

<details>
<summary>Om pushen blir röd</summary>

Läs sista raden. Tom adress: lägg till origin och kör igen. Texten `src refspec main does not match any`: lådan heter inte `main`. Kör `git branch -M main` och samma push. Texten rejected eller fetch first: montern hade redan ett papper, oftast en README. Nytt tomt repo, utan README och utan gitignore-bock.

```text
git remote remove origin
git remote add origin https://github.com/du/nya-repot.git
git push -u origin main
```

Hämta inte hem det andra pappret.

</details>

---

## Uppgift 4 — Tre funktioner, minst 5 commits

**Mål:** Varje funktion har ett eget kuvert med prefixet `feat:`. Montern visar minst 5 commits under Commits. Sidan visar ditt namn, Summa: 12 och ok.

**Krav:** en funktion i taget. `git diff` innan du stagar, så plusraden är just den funktionen. Ta bort den funktionens TODO-kommentar när den är klar. Rör inte raderna under funktionerna. Pusha efter varje kuvert.

1. `hamtaNamn` lämnar tillbaka ditt namn, inte `"TODO"`. `git add index.html` och `git commit -m "feat: implementera hamtaNamn"`. `git push`.
2. `addera` lämnar tillbaka `a + b`. `git commit -m "feat: implementera addera"`. `git push`.
3. `statusForTal` lämnar tillbaka `"ok"` om talet är större än 10, annars `"för låg"`. `git commit -m "feat: implementera statusForTal"`. `git push`.
4. Öppna `index.html` i webbläsaren.
5. Öppna Commits och räkna. Klicka den allra äldsta.

Tidslinjen, äldst först:

1. `docs: initiera projekt med startkod och tre TODO`
2. `chore: lägg till gitignore för loggar och miljöfiler`
3. `feat: implementera hamtaNamn`
4. `feat: implementera addera`
5. `feat: implementera statusForTal`

**Klart-check (peka på GitHub, inte bara på sidan):**
- [ ] Minst 5 commits under Commits. Den äldsta visar alla tre TODO när du öppnar den
- [ ] En `chore:`-rad för `.gitignore`, och tre `feat:`-rader som namnger var sin funktion
- [ ] Sidan: ditt namn, Summa: 12, ok
- [ ] Säg ordningen ändra, diff, add, commit, push för en av funktionerna
- [ ] `hemligheter.env` finns i mappen på datorn och saknas på GitHub

**Ägarskap:** Kan du inte peka på raden och säga prefixet och funktionen, dela kuvertet. Ett meddelande för alla tre duger inte. `Klart` duger inte.

---

## Stretch — den röda meningen

Frivilligt, samma verktyg.

Be någon beskriva en push som svarade `rejected` för att README var ibockad. Skriv fyra korta rader: vad meningen betydde, vad `git remote -v` skulle visa, vilken en sak du ändrar, och vilket kommando du kör igen.

**Klart-check:** Säg högt varför ett nytt tomt repo är steget, och vilket kommando du inte använder för att lösa just den röda raden.
