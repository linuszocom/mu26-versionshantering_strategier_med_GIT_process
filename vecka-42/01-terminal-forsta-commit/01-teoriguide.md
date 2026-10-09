# 01 — Teoriguide: historik på din dator

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna förklara med egna ord eller skriva i dokumentation. Tar du materialet från noll: läs igenom guiden, gör sedan [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md).

Vi börjar med vad som går förlorat när bara den senaste filen sparas på disken. Därefter bygger vi ett lokalt arkiv med förseglade kuvert. Det handlar om en tydlig metod: förstå var du står i filsystemet, granska skillnader, välj ut filer selektivt och försegla.

---

## Senaste filen — måndagen försvinner

En vanlig missuppfattning är att programmets vanliga sparaknapp sparar historik. Det stämmer inte.

När du sparar en textfil i editorn på måndagen skrivs den till disken. När du ändrar samma fil på onsdagen och sparar igen skrivs måndagens rader över. På hårddisken finns bara ett enda tillstånd kvar: det senaste. Det är detta problem versionshantering löser.

**Metafor:** Arket på skrivbordet är det du skriver på just nu (arbetsytan). Ett **kuvert** är en kopia du adresserar och lägger specifika ark i (staging). När du stämplar och förseglar kuvertet skapar du en **commit**. Kuverten sparas i en **arkivlåda** i samma mapp. Ändrar du arket på skrivbordet byts texten där, men de förseglade kuverten i lådan ligger kvar orörda i tidslinjen.

**Vad det är:** Versionshantering är en obruten tidslinje av sparade tillstånd, inte bara den senaste filen.  
**Varför det finns:** Utveckling sker i steg. Du måste kunna se exakt vilka rader som lades till eller togs bort, och kunna backa om något går sönder.  
**Vad det INTE är:** Editorns spara-funktion är inte versionshantering. En molndisk eller GitHub är inte heller det här; i denna del stannar hela arkivet lokalt på din maskin.

**Målsvar (att kunna förklara):** *"Versionshantering sparar tillstånd över tid. Att bara spara i editorn skriver över samma fil på disken, vilket gör att tidigare ändringar raderas."*

---

## Terminalen — var står du

Terminalen är ett textbaserat fönster mot en specifik katalog på datorn. Den gissar aldrig vilken mapp du menar, utan förväntar sig explicita instruktioner.

* `pwd` (Print Working Directory): Skriver ut den fullständiga sökvägen till mappen du befinner dig i.
* `ls`: Listar filerna på den aktuella platsen. Flaggan `-a` (`ls -a`) visar även dolda mappar och filer.
* `cd`: Navigerar mellan mappar. `cd ..` backar en nivå uppåt i hierarkin.
* `mkdir`: Skapar nya mappar direkt via kommandoraden (t.ex. `mkdir mina-lappar`).

Ett tomt svar från `ls` betyder helt enkelt att katalogen är tom, inte att kommandot fallerade.

**Målsvar:** *"pwd visar min exakta plats i filsystemet. ls visar innehållet, och cd flyttar mig. Git initieras alltid i den specifika projektmappen och ingen annanstans."*

---

## Arkivet — git init

`git init` skapar arkivet i den mapp du står i. Kommandot körs en enda gång per projekt. Git genererar en dold katalog med namnet `.git`. Det är själva arkivlådan där all historik lagras.

Init skapar inga färdiga commits; arkivet är tomt tills du aktivt förseglar något. Om du råkar köra kommandot i fel mapp kan repot avväpnas genom att radera den dolda katalogen (`rm -rf .git`). Då återgår mappen till att vara en helt vanlig katalog utan versionshantering.

---

## Arbetsflödet — från ändring till historik

Många tror att `git add` och `git commit` gör samma sak. I själva verket är de två separata steg:

1. **Arbetsyta (Working Tree):** Ändringarna finns sparade på hårddisken via editorn.
2. **Inspektion (`git diff`):** Visar exakt vilka rader som skiljer arbetsytan från den senaste sparade committen. Nya rader markeras med grönt (`+`).
3. **Staging (`git add`):** Urvalet. Du lägger specifika filer i kuvertet och gör dem redo för försegling.
4. **Commit (`git commit -m`):** Förseglingen. Kuvertet stämplas med en beskrivning och sparas permanent i historiken.
5. **Loggbok (`git log --oneline`):** Bläddrar i arkivlådan och listar alla förseglade commits kronologiskt med unika hashar.

`git status` sparar ingenting; det är enbart en rapport. Röd text betyder att ändringar ligger kvar på skrivbordet (arbetsytan). Grön text betyder att filerna ligger färdiga i kuvertet (staging).

---

## Selektiv staging och Conventional Commits

I professionell utveckling undviker vi `git add .`. Om du har ändrat flera filer med olika syften vill du inte blanda ihop dem i samma commit. 

Genom att ange filnamnet explicit (`git add fil1.txt`) lägger du enbart den filen i kuvertet. Övriga filer ligger kvar i arbetsytan. Detta skapar **atomära commits** där varje punkt i historiken isolerar en enskild ändring.

Meddelandet på fliken ska vara informativt. I branschen används **Conventional Commits** med standardiserade prefix:
* `feat:` Ny funktionalitet eller nytt innehåll.
* `docs:` Dokumentation, instruktioner eller rena anteckningar.
* `fix:` Rättning av en felaktighet.

---

## De två klassiska fallgroparna

1. **Commit utan add:** Du sparar i editorn och kör `git commit` direkt. Git svarar `no changes added to commit`. Orsak: Kuvertet var tomt. Du måste aktivt välja ändringen med `git add` först.
2. **Dubbla tillstånd samtidigt:** Du kör `git add fil.txt`. Därefter ändrar du samma fil i editorn igen och sparar. Kör du `git status` nu syns samma fil under två rubriker: grön under *Changes to be committed* och röd under *Changes not staged for commit*. Orsak: `git add` sparar inte en dynamisk pekare, utan fryser en kopia av filen vid add-tillfället.

---

## Felsökningsordning när du tvekar

1. `pwd`: Säkerställ att du står i rätt projektkatalog.
2. `git status`: Kontrollera vad som är osparat eller ligger i staging.
3. `git diff`: Granska exakt vad som modifierats på radnivå.
4. `git add filnamn`: Välj filen selektivt.
5. `git commit -m "prefix: beskrivning"`: Försegla med ett tydligt meddelande.
6. `git log --oneline`: Verifiera att committen lagts till i historiken.