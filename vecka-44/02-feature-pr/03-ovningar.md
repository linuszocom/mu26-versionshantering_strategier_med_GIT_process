# 03 — Övningar

**Omfång:** ett publikt grupprepo, inbjudan, clone, pull, `feature/` och ditt namn, en funktionsrad, push, Pull Request, Approve av någon annan, **Merge pull request**. Sprintmålet och raderna från förra mappen ligger kvar i kortet. Ingen krockövning. Inget `git merge` i terminalen.

Arbeta tre eller fyra. En person skapar montern. Var och en skriver på sitt sidofack.

---

## Uppgift 1 — Tom monter, startfil på main

**Mål:** Alla har samma låda, och glaset visar startfilen med TODO kvar.

**Scenario:** Någon föreslår att var och en skapar ett eget repo och mejlar filen. Då finns ingen gemensam historik.

**Krav:**
1. En person skapar ett **publikt** repo. Bocka inte i Add a README. Bjud in de andra under Settings, Collaborators. Var och en tackar ja.
2. Ägaren kör `git clone` med länken, `cd` in i mappen, och lägger in `index.html` exakt som blocket nedan. TODO ska vara kvar.
3. `git add index.html`, `git commit -m "Lade till index.html med TODO kvar"`, `git push`.
4. De andra kör `git clone` med samma länk och `cd`. `git status` ska säga `On branch main`. `index.html` ska ligga i mappen.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <title>Team-uppgift</title>
</head>
<body>
  <h1 id="rubrik">TODO: gruppnamn</h1>
  <p id="summa"></p>
  <p id="status"></p>
  <p id="langd"></p>
  <script>
    // TODO 1: Returnera gruppens namn.
    function hamtaNamn() {
      return "TODO";
    }

    // TODO 2: Returnera summan av a och b.
    function addera(a, b) {
      return 0;
    }

    // TODO 3: Returnera "ok" om talet är större än 10, annars "för låg".
    function statusForTal(tal) {
      return "TODO";
    }

    // TODO 4: Returnera hur många tecken texten har.
    function raknaTecken(text) {
      return 0;
    }

    document.getElementById("rubrik").textContent = hamtaNamn();
    const summa = addera(7, 5);
    document.getElementById("summa").textContent = "Summa: " + summa;
    document.getElementById("status").textContent = statusForTal(summa);
    document.getElementById("langd").textContent = "Tecken: " + raknaTecken("git");
  </script>
</body>
</html>
```

**Klart-check (peka i DIN låda):**
- [ ] `git status` säger `main`
- [ ] Första committen på GitHub har TODO kvar
- [ ] Du kan säga varför de andra väntade med clone tills den pushen var inne

Rör inte raderna under funktionerna. Bygg inte ut sidan.

---

## Uppgift 2 — Ett sidofack, en rad

**Mål:** Din rad finns på `feature/` och ditt namn. Glasets `main` har den inte än.

**Krav:**
1. `git checkout main` och `git pull`. Läs svaret. `Already up to date` är lugnt.
2. `git checkout -b feature/` och ditt namn, till exempel `feature/anna`.
3. Byt bara `return` i din funktion. Ta olika rader i gruppen.
   - `hamtaNamn` lämnar tillbaka gruppens namn
   - `addera` lämnar tillbaka `a + b`
   - `statusForTal` lämnar tillbaka `"ok"` om talet är större än 10, annars `"för låg"`
   - `raknaTecken` lämnar tillbaka antalet tecken
4. `git add index.html`, `git commit -m` med en kort mening om raden, `git push -u origin` och sidofackets namn.
5. Öppna branchen på GitHub. Öppna sedan `main`. Den äldsta committen ska fortfarande visa TODO.

Är ni färre personer än rader tar någon två rader i samma sidofack. Sitter två vid samma tangentbord och samma git-konto: båda namnen i commit-meddelandet, ändå ett sidofack var.

**Klart-check:**
- [ ] `git status` säger `feature/` och ditt namn
- [ ] Du pekar på sidofacket på GitHub och på `main`, och de är inte samma commit
- [ ] Du säger varför pull kom före `checkout -b`

---

## Uppgift 3 — Frågan, någon annan, knappen

**Mål:** En mergad Pull Request som någon annan har granskat och godkänt.

**Krav:**
1. **Compare & pull request.** Bas: `main`. Compare: `feature/` och ditt namn.
2. En mening om vilken rad som ändrades.
3. **Granskning (Review):** En annan person öppnar **Files changed**:
   - Hovra över raden med `return` i koden, klicka på det blå plustecknet (`+`) och skriv en kommentar om returvärdet (t.ex. *Returnerar nu gruppnamnet som förväntat*).
   - Klicka sedan på **Review changes → Approve → Submit review**.
4. **Merge pull request.** Inte `git merge` i terminalen.
5. Peka under **Pull requests → Closed** på din fråga, och under **Commits** på `main` på din rad.

**Klart-check (peka i ER historik):**
- [ ] Basen var `main`
- [ ] Det finns minst en skriftlig kommentar under *Files changed*
- [ ] Approve kommer från någon annan
- [ ] Du kan säga fem ord i ordning: branch, push, PR, review, merge

---

## Stretch — peka under huven

Öppna din mergade fråga. Säg två meningar: varför pull kom först, och vilken commit på `main` som fortfarande visar TODO. Det är samma blick som examinationen vill ha när den frågar hur historiken hänger ihop.
