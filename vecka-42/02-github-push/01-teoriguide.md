# 01 — Teoriguide: lådan hemma och montern

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt eller skriva i README. Tar du materialet från noll: läs klart, gör sedan [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Kuverten från [förra mappen](../01-terminal-forsta-commit/01-teoriguide.md) förutsätts: ark, `git add`, `git commit`, `git diff` och prefixen `feat:` och `docs:`.

Vi börjar med ett kuvert som bara finns hemma. Sedan får montern en adress, och du bär över kopian. Det är inte magi. Det är två rum som inte uppdaterar varandra.

---

## Två rum

Många tänker nu: “Jag har committat. Då syns det väl för andra.” Andas.

**Metafor:** Lådan med förseglade kuvert står i mappen på din dator. GitHub är en **glasmonter** i trapphuset. Vem som har adressen kan läsa samma kuvert, i samma ordning. Montern fylls inte för att du förseglade något hemma.

**Vad det är:** Ett publikt repo är montern. Den är tom tills du bär dit en kopia.  
**Varför det finns:** Någon annan ska kunna öppna historiken utan att sitta vid din dator.  
**Om det saknas / vad det INTE är:** En commit är inte en tur till montern. Spara i editorn är fortfarande bara arket. Montern är inte ett extra ställe där du skriver om filen.

**Målsvar (säg högt / skriv i README):** *“Mappen på datorn är lådan. GitHub-repot är montern. En commit förseglar hemma. git push bär kopian till montern.”*

---

## Namnet på lådan — main

Äldre Git kan döpa lådan till något annat än det namn montern väntar. Du sätter namnet själv, direkt efter `git init`, innan första kuvertet:

```text
git init
git branch -M main
```

`-M` döper om grenen du står på till `main`. Det är samma namn som GitHub använder. Första pushen blir då `git push -u origin main`.

Hoppar du över omdöpningen och pushar mot `main` kan terminalen svara `src refspec main does not match any`. Lådan heter inte `main` än. Kör `git branch -M main` och samma push igen. Du byter inte till ett annat ord.

**Vad det är:** Ett namn på historiken i lådan, satt innan du bär något.  
**Varför det finns:** Pushen och montern ska säga samma namn från första försöket.  
**Om det saknas / vad det INTE är:** Det är inte en ny låda vid sidan av den du redan har. Det är inte ett kommando som flyttar kuvert.

**Målsvar (säg högt / skriv i README):** *“Direkt efter git init kör jag git branch -M main. Första pushen är git push -u origin main.”*

---

## Luckan som inte släpper in nyckeln — .gitignore

Många tänker: “Allt i mappen ska med upp.” Andas.

I lådan ligger ibland papper som inte hör hemma i montern. En fil som slutar på `.env` kan innehålla lösenord eller nycklar. En fil som slutar på `.log` är en utskrift av vad programmet redan sagt. `.DS_Store` är skräp som datorn själv lägger i mappen.

**Metafor:** Du tejpar en lapp på lådans lock innan du bär den genom trapphuset. Lappen säger vilka papper som stannar i skrivbordslådan. De följer inte med in i glasmontern.

Skapa filen `.gitignore` i samma mapp som `index.html`, **innan** första pushen. Innehållet är tre rader:

```text
*.env
*.log
.DS_Store
```

Stjärnan betyder “varje fil som slutar så”. Spara. Kör `git status`. Filer som `hemligheter.env` och `debug.log` syns inte längre. De ligger kvar på disken. Öppnar du mappen finns de där. Git har bara slutat titta, så de varken committas eller pushas.

Sedan ett eget kuvert, fortfarande hemma:

```text
git add .gitignore
git commit -m "chore: lägg till gitignore för loggar och miljöfiler"
```

`chore:` är kuvertet för skydd och städning. Det är inte en funktion i `index.html`. Prefixet `docs:` och `feat:` kan du sedan förra mappen. `chore:` är det tredje prefixet i den här tidslinjen.

När du skapar repot på GitHub: bocka inte i någon startfil, varken README eller GitHubs egen gitignore. Du skriver lappen själv, och den ska ligga i ditt kuvert.

**Vad det är:** En lista med mönster. Git hoppar över ospårade filer som matchar.  
**Varför det finns:** Annars kan en push lägga lösenord och loggar i en monter som har en publik adress.  
**Om det saknas / vad det INTE är:** Filerna raderas inte. De krypteras inte. `.gitignore` är inte en push, och den skyddar inte filer som redan ligger i ett tidigare kuvert. Utan lappen syns `.env` och `.log` som vanliga nya filer i `git status`.

**Målsvar (säg högt / skriv i README):** *“.gitignore raderar ingenting från disken. Mönstren *.env, *.log och .DS_Store får filerna att försvinna ur git status, så de inte följer med i push. Jag committar den med chore: innan första pushen.”*

---

## Adressen — remote

**Remote** låter som en maskin du måste kunna bygga. Det är adressen till montern, med ett smeknamn. Smeknamnet är oftast `origin`. Efter det kommer en länk som börjar med github.com.

`git remote -v` visar adressen. Tom lista betyder att lådan inte vet var montern står.

```text
git remote add origin https://github.com/du/ditt-repo.git
git remote -v
```

**Vad det är:** Ett namn och en länk.  
**Varför det finns:** `git push` måste veta vilken monter.  
**Om det saknas / vad det INTE är:** Adressen flyttar inga kuvert. Den skriver inte om `index.html`. Den är inte ett andra arkiv där du committar.

**Målsvar (säg högt / skriv i README):** *“Remote är adressen till montern, smeknamn origin. Tom git remote -v betyder att adressen saknas. Då lägger jag till den och kör push igen.”*

---

## Bära dit — git push

Första gången, när lådan redan heter `main`:

```text
git push -u origin main
```

`-u` kopplar den här lådan till den adressen, så att nästa gång räcker:

```text
git push
```

Terminalen kan svara `Branch 'main' set up to track remote branch 'main' from 'origin'`. Det är kopplingen som `-u` sparade.

**Vad det är:** Kopian av kuverten du redan har förseglat, upp till montern.  
**Varför det finns:** Annars är GitHub fortfarande tomt, eller kvar på förra kopian.  
**Om det saknas:** Har du committat och inte pushat, ligger det nya kuvertet bara hemma. Fliken **Commits** på GitHub visar samma meningar som du skrev, först efter push. `.env` och `.log` ska inte ligga bland filerna där, om `.gitignore` kom med i ett kuvert före pushen.

**Målsvar (säg högt / skriv i README) — metod:** *“Ändra, diff, add, commit, push. Saknas en rad under Commits läser jag den röda meningen, kontrollerar adressen med git remote -v, och ändrar en sak.”*

---

## Problem först — en röd push

Svag väg: repot på GitHub skapades med en färdig README. Montern har redan ett papper du inte har hemma. Pushen svarar att den inte får skriva över, ofta med orden rejected eller fetch first.

Starkare väg:

1. Läs sista raden. Den säger vad som krockar.
2. `git remote -v`. Ser du adressen till just den montern?
3. Skapa ett **nytt** tomt repo. Bocka inte i README, och inte i gitignore.
4. `git remote remove origin`, sedan `git remote add origin` med den nya länken.
5. `git push -u origin main` igen.

Du hämtar inte hem det andra pappret. Du byter till en tom monter och bär din låda dit.

En annan röd rad, `src refspec main does not match any`, är namnet på lådan. `git branch -M main`, sedan samma push.

**Målsvar (säg högt / skriv i README):** *“En röd push är en mening att läsa. Tom adress: lägg till origin. Monter som redan har ett papper: nytt tomt repo, byt origin, push igen. main saknas: git branch -M main, sedan samma push.”*

---

## Fem commits, en sak i taget

Startfilen heter `index.html`. Första kuvertet sparar den med alla tre `TODO` kvar, så utgångsläget syns. Andra kuvertet är `.gitignore`. Sedan tre kuvert: ett per funktion. Varje meddelande använder Conventional Commits, så raden går att peka på.

Tidslinjen under **Commits**, äldst längst ner:

1. `docs: initiera projekt med startkod och tre TODO`
2. `chore: lägg till gitignore för loggar och miljöfiler`
3. `feat: implementera hamtaNamn`
4. `feat: implementera addera`
5. `feat: implementera statusForTal`

`docs:` är startläget. `chore:` är skyddet. `feat:` är en funktion. Ett kuvert med texten `Klart` går inte att peka på.

Innan varje `feat:`-kuvert kör du `git diff`. Plusraden ska vara den funktion du just ändrade. Ta bort den funktionens TODO-kommentar när den är klar. Raderna under funktionerna ritar bara upp det funktionerna lämnar tillbaka. Dem rör du inte, och du behöver inte kunna förklara taggarna.

När du öppnar den **allra äldsta** committen under Commits ska alla tre `TODO` fortfarande stå kvar. Den senaste har dina ändringar. Arket i webbläsaren ska visa ditt namn, texten Summa: 12 och ordet ok. `addera(7, 5)` ger 12, och 12 är större än 10, så statusen blir ok.

**Målsvar (säg högt / skriv i README):** *“Minst 5 commits under Commits: docs för startkoden med tre TODO, chore för gitignore, feat för hamtaNamn, addera och statusForTal. Den äldsta visar alla tre TODO. Push är det som gör att raderna syns i montern.”*

---

## När det blir rött

1. Läs sista raden högt.
2. `git status` och `git remote -v`. Ett av dem brukar visa felet: inget nytt kuvert, eller ingen adress.
3. Ändra en sak. Adress som saknas: `git remote add`. Fel monter: nytt tomt repo och byt origin. Lådan heter inte `main`: `git branch -M main`. Inloggningsfönster: logga in och kör samma push.
4. Kör push igen. Öppna Commits och räkna till minst 5.

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| “Jag committade, kompisen ser det” | Kuvertet ligger hemma tills push |
| README ibockad när repot skapades | Montern är inte tom. Nytt repo, byt origin |
| `git push` utan att lådan heter `main` | `git branch -M main` direkt efter init, sedan `git push -u origin main` |
| `.env` eller `.log` syns i status och följer med | `.gitignore` med `*.env`, `*.log` och `.DS_Store` innan push. Filerna ligger kvar på disken |
| Ett meddelande för alla tre funktioner, eller `Klart` | En sak per kuvert: `docs:`, `chore:` eller `feat:` |
| Rört raderna under funktionerna | Bara det funktionen lämnar tillbaka. Visningen är redan skriven |

---

## Nästa steg

Kartan: [02 — Visuellt](./02-visuell.md). Sedan [03 — Övningar](./03-ovningar.md).
