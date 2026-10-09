# 05 — Självtest: Diagnostisk kontroll

Formulera dina svar skriftligt för dig själv **innan** du expanderar facit. Sikta på förklaringar du kan återge muntligt.

---

## Frågor

1. Vad händer med den tidigare texten i en fil om du enbart använder editorns vanliga spara-funktion över flera dagar?
2. Hur definierar du versionshantering med egna ord?
3. Vad är den praktiska skillnaden mellan kommandona `pwd`, `ls` och `cd`?
4. Vad skapas på disken när du kör `git init`, och vad händer om du tar bort mappen `.git`?
5. Förklara skillnaden mellan arbetsyta, staging och commit.
6. Vad visar kommandot `git diff`, och varför bör det köras innan `git add`?
7. Varför anses meddelanden som `fix` eller `klart` otillräckliga, och vad bidrar Conventional Commits med?
8. Vad händer om du ändrar en fil i editorn efter att du kört `git add`, och hur rapporterar `git status` detta?
9. Vad gör kommandot `git log --oneline`?

---

## Facit

<details>
<summary>Visa facit och målsvar</summary>

1. Den tidigare texten skrivs över på disken och försvinner permanent om den inte sparats i versionshanteringen.
2. Versionshantering är ett system som sparar en tidslinje av specifika tillstånd över tid, vilket möjliggör spårbarhet, jämförelse och återställning.
3. `pwd` visar den aktuella sökvägen, `ls` listar innehållet i katalogen, och `cd` byter aktiv katalog.
4. `git init` skapar den dolda katalogen `.git` som innehåller hela det lokala arkivet. Raderas den upphör mappen omedelbart att vara ett Git-repo utan att källkodsfilerna skadas.
5. Arbetsytan är filerna på hårddisken. Staging är det aktiva urvalet där filer förbereds. Commit är den permanenta, förseglade ögonblicksbilden i historiken.
6. `git diff` visar de exakta radförändringarna mellan arbetsytan och senaste commit/staging. Det säkerställer att du granskar dina ändringar innan du inkluderar dem.
7. Diffusa meddelanden förklarar inte vad som ändrats, vilket gör historiken obrukbar. Conventional Commits (`feat:`, `fix:`, `docs:`) skapar en standardiserad och överskådlig logg.
8. Filen visas under två rubriker samtidigt i `git status`: grön under *Changes to be committed* (versionen vid add) och röd under *Changes not staged for commit* (senaste ändringen i editorn).
9. Det listar projektets commit-historik i kronologisk ordning där varje punkt visas på en rad med kort-hash och meddelande.

</details>