# 05 — Självtest

Svara **först** utan facit. Skriv för dig själv. Sikta på meningar du kan säga högt.

---

## Frågor

1. Vad är skillnaden mellan lådan på din dator och repot på GitHub?
2. Vad gör `git push` som `git commit` inte gör?
3. Vad är remote, och vad visar en tom `git remote -v`?
4. Varför blir första pushen röd om README var ibockad, och vad ändrar du?
5. När kör du `git branch -M main`, och vilket ord står efter `origin` i första pushen?
6. Vad händer med `hemligheter.env` när `.gitignore` innehåller `*.env`? Försvinner filen från disken?
7. Hur många commits ska Commits minst visa, i vilken ordning, och vad ska den allra äldsta innehålla?
8. Vad ska sidan visa när de tre funktionerna är klara, och vilka rader i filen rör du inte?
9. Peka på en rad under dina Commits som inte är den äldsta och inte är `.gitignore`. Vilket prefix, vilken funktion, och vilken mening?

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. Lådan är mappen där du committar. Repot är glasmontern. De uppdateras inte av sig själva.
2. Commit förseglar hemma. Push bär kopian till montern, så raden syns under Commits.
3. Remote är adressen, smeknamn origin. Tom lista betyder att adressen saknas. Lägg till den och kör push igen.
4. Montern hade redan ett papper. Nytt tomt repo, `git remote remove origin`, ny `git remote add`, `git push -u origin main`. Hämta inte hem pappret.
5. Direkt efter `git init`. Första pushen är `git push -u origin main`. Hoppar du över omdöpningen kan terminalen säga `src refspec main does not match any`. Då kör du `git branch -M main` och samma push.
6. Filen ligger kvar på disken. Den slutar synas i `git status` och följer inte med i commit eller push. Samma sak gäller `*.log` och `.DS_Store`. Själva lappen committas med `chore: lägg till gitignore för loggar och miljöfiler` innan första pushen.
7. Minst 5 commits under Commits. Äldst först: `docs: initiera projekt med startkod och tre TODO`, `chore: lägg till gitignore för loggar och miljöfiler`, `feat: implementera hamtaNamn`, `feat: implementera addera`, `feat: implementera statusForTal`. Den allra äldsta visar fortfarande alla tre TODO.
8. Ditt namn, Summa: 12 och ok. Rör inte raderna under de tre funktionerna.
9. Rimligt om meningen är `feat:` och namnger funktionen du pekar på. Svagt om du bara säger att sidan ser rätt ut, eller om raden bara säger `Klart`.

</details>

---

## Klar med den här mappen?

Du kan öppna Commits och peka på minst 5 commits, och du kan säga varför en commit utan push inte syns där. Du kan också säga varför `.env` ligger kvar på disken men inte i montern. Nästa mapp är [kortet i mappen](../03-readme-exam1/).
