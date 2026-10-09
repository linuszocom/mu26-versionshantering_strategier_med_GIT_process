# 01 — Teoriguide: kortet i mappen

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt. Tar du materialet från noll: läs klart, skriv sedan i [03 — Övningar](./03-ovningar.md) och granska i [04 — AI-träning](./04-ai-traning.md). Lådan, kuverten och glasmontern kommer från [förra mapparna](../02-github-push/01-teoriguide.md).

Vi börjar med en text som kan vara vem som helst. Sedan skriver du tre svar som går att peka på i din låda. Det är inte magi. Det är dina meningar, och ett finger mot rätt rad.

---

## En text utan din låda

Många tänker nu: “README är en manual jag genererar på slutet.” Andas.

Svag text:

> Git är versionshantering. Vi använde staging och push.

Den kan stå i vilket repo som helst. Den pekar inte på ett kuvert du förseglade, och inte på en rad under Commits.

**Metafor:** `README.md` är ett kort som ligger i samma mapp som `index.html`. När du pushar följer kortet med till glasmontern. Den som öppnar repot läser kortet först. Det är inte en bok, och det är inte en lista på alla kommandon som finns.

**Vad det är:** Tre frågor, ungefär 2–4 meningar var, plus en reflektion på 3–5 meningar. Egna ord.  
**Varför det finns:** Någon ska kunna fråga dig, och du ska kunna svara utan att läsa innantill.  
**Om det saknas / vad det INTE är:** Ett kort som bara finns på din dator är inte inlämnat. Syns det inte i repot på GitHub, är det inte där. Inga nya kommandon i det här materialet: samma `git add`, `git commit` och `git push` som för kuverten. Prefixet på just det här kuvertet är `docs:`, för `docs:` är standarden när du ändrar dokumentation.

```text
git add README.md
git commit -m "docs: besvara teorifragor och reflektion i README"
git push
```

**Målsvar (säg högt / skriv i README):** *“README är kortet i mappen. Två till fyra meningar per fråga, med ord jag kan säga när filen är stängd. Jag committar kortet med docs: och push gör att det syns i montern.”*

---

## Fråga 1 — varför historik

**Vad det är:** Versionshantering sparar lägen över tid.  
**Varför det finns:** Mjukvara växer i steg. Sparar du bara arket, skriver onsdag över måndag.  
**Om det saknas:** Ett svar som bara säger ordet Git, utan att en rad kan försvinna.

Skriv så att en kompis kan se problemet: senaste filen räcker inte.

**Målsvar (säg högt / skriv i README):** *“Versionshantering sparar förseglade lägen, så att ett tidigare steg finns kvar. Utan den finns bara senaste filen.”*

---

## Fråga 2 — ark, val, försegling

**Vad det är:** Arbetsytan är filen du sparar. `git add` väljer vad nästa kuvert ska innehålla. `git commit` förseglar och kräver en mening.  
**Varför det finns:** Utan valet kan ett kuvert ta med fel fil, eller ingenting.  
**Om det saknas / vad det INTE är:** Add och commit är inte samma sparaknapp. `git status` läser läget och förseglar inget.

**Målsvar (säg högt / skriv i README):** *“Arbetsytan är filen. git add väljer. git commit förseglar valet med en mening. status bara läser.”*

---

## Fråga 3 — lådan och montern

**Vad det är:** Lådan är mappen på din dator. Glasmontern är det publika repot. `git push` bär kopian dit.  
**Varför det finns:** En commit hemma syns inte under Commits förrän du burit den.  
**Om det saknas:** Ett svar som säger “det ligger i molnet” utan att säga vad push gör, och vad som saknas om du inte pushat.

**Målsvar (säg högt / skriv i README):** *“Lådan är mappen där jag committar. Montern är GitHub. git push bär kopian, så raden syns under Commits.”*

---

## Reflektionen

3–5 meningar om ett tillfälle du körde fast. Använde du AI: ett förslag du var tvungen att ändra innan det stämde hos dig. “Jag frågade AI” är inte ett exempel. Exemplet är raden du tog bort, och raden du satte i stället.

**Målsvar (säg högt / skriv i README):** *“Förslaget sa en mening för alla funktioner. Jag delade det, för varje rad under Commits ska namnge en funktion.”*

---

## Peka, inte bara lämna in

Ägarskap här betyder att du kan förklara kommandona, de tre funktionerna och historiken. Kan du inte det, räcker det inte att sidan visar rätt namn.

Stäng filen. Öppna Commits på GitHub. Räkna. Minst 6 commits ska synas, äldst först:

1. `docs: initiera projekt med startkod och tre TODO`
2. `chore: lägg till gitignore för loggar och miljöfiler` — det här är commit 2, `.gitignore`
3. `feat: implementera hamtaNamn`
4. `feat: implementera addera`
5. `feat: implementera statusForTal`
6. `docs: besvara teorifragor och reflektion i README`

Klicka den allra äldsta. Alla tre `TODO` ska fortfarande stå kvar. Peka sedan på en `feat:`-rad. Säg funktionen och meningen. Säg ändra, add, commit, push för den raden. Peka också på commit 2 och säg att `.gitignore` stannar i historiken, medan `.env` och `.log` stannar på disken.

Sidan i webbläsaren är en kontroll: ditt namn, Summa: 12, ok. Förklaringen sitter i terminalen eller i VS Code, mot raden.

Godkänt är att du kan säga flödet övergripande och att kortet och minst 6 commits finns på GitHub. Väl godkänt är att meningarna speglar var sin funktion, och att du kan gå närmare: staging mot commit, låda mot monter, `docs:` mot `chore:` mot `feat:`, och vad du läser när en push blir röd.

**Målsvar (säg högt / skriv i README):** *“Jag pekar på raden, säger prefixet och funktionen, och säger ändra, add, commit, push. Minst 6 commits på GitHub. Den äldsta visar alla tre TODO. Commit 2 är .gitignore. Sidan bevisar resultatet. Raden bevisar att jag vet vad som ändrades.”*

---

## När meningen inte är din

1. Stäng `README.md`.
2. Säg fråga 1 högt.
3. Fastnar du: öppna filen och skriv om en mening, inte hela kortet.
4. `git add README.md`, `git commit -m "docs: besvara teorifragor och reflektion i README"`, `git push`.
5. Öppna repot. Kortet ska synas där, inte bara hemma.

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Texten kan vara vem som helst | En mening måste gå att känna igen mot din historik |
| README bara på datorn | Add, commit, push, samma väg som index.html |
| Ett svar som rabblar verktygets historia | 2–4 meningar om problemet du redan sett |
| Sidan är grön, historiken är en rad | Minst 6 commits på GitHub: startfil, `.gitignore` som commit 2, tre funktioner, README med `docs:`. Äldsta visar alla tre TODO |
| Nytt kommando för att “visa listan” | Du pekar under Commits. Kvittot hemma var commit-utskriften |

---

## Nästa steg

Kartan: [02 — Visuellt](./02-visuell.md). Sedan skriver du kortet: [03 — Övningar](./03-ovningar.md).
