# 03 — Övningar: Praktisk tillämpning

**Omfång:** Terminalnavigering (`pwd`, `ls -a`, `cd`, `mkdir`), `git init`, `git status`, inspektion med `git diff`, selektiv staging (`git add`), Conventional Commits (`git commit -m`) och verifiering med `git log --oneline`. Alla övningar körs lokalt på din egen maskin.

---

## Uppgift 1 — Terminalorientering och katalogstruktur

**Mål:** Navigera säkert i terminalen och skapa en ren projektmapp utan att använda grafiska filhanterare.

1. Öppna terminalen och kör `pwd` för att identifiera din startposition.
2. Skapa en ny projektkatalog via kommandoraden: `mkdir mina-lappar`.
3. Navigera in i mappen: `cd mina-lappar`.
4. Bekräfta med `pwd` att sökvägen slutar med `mina-lappar`.
5. Kör `ls`. Utskriften ska vara tom eftersom katalogen är nyskapad.

**Klart-check:**
- [ ] Du kan förklara skillnaden mellan `pwd` före och efter `cd`.
- [ ] `ls` ger en tom rad utan felmeddelanden.

---

## Uppgift 2 — Initiera arkivet och förstå Untracked

**Mål:** Initiera ett tomt Git-arkiv och se skillnaden mellan en fil på disken och ett spårat tillstånd.

1. Kontrollera att du står i `mina-lappar` och kör: `git init`.
2. Kör `ls -a` och lokalisera den dolda katalogen `.git`.
3. Skapa filen `lapp.txt` i din editor, skriv texten `Möte på onsdag` och spara.
4. Gå till terminalen och kör `git status`. Läs raderna under *Untracked files*.

<details>
<summary>Om Git efterfrågar användaridentitet</summary>

Om terminalen anger `Please tell me who you are`, konfigurera ditt namn och e-post lokalt:

git config --global user.name "Ditt Namn"
git config --global user.email "din.epost@example.com"

</details>

**Klart-check:**
- [ ] `git status` visar `lapp.txt` i rött under *Untracked files*.
- [ ] Du kan förklara varför filen inte ingår i historiken trots att den är sparad i editorn.

---

## Uppgift 3 — Diff, selektiv staging och Conventional Commit

**Mål:** Läsa förändringar i `git diff`, staga specifika filer och committa med tydliga prefix.

1. Staga filen: `git add lapp.txt`.
2. Kör `git status` och bekräfta att filen blivit grön under *Changes to be committed*.
3. Skapa din första commit:
   `git commit -m "feat: initiera mötesanteckning för onsdag"`
4. Verifiera med `git status` att arbetsytan är ren (*working tree clean*).
5. Öppna `lapp.txt` i editorn, ändra raden till `Möte flyttat till fredag` och spara.
6. Kör `git diff` **innan** du kör add. Identifiera den gröna plusraden och den röda minusraden.
7. Staga och försegla ändringen:
   `git add lapp.txt`
   `git commit -m "feat: uppdatera mötesdag till fredag"`
8. Kör `git log --oneline`. Verifiera att båda dina commits visas i kronologisk ordning med korta hashar.

**Klart-check:**
- [ ] Du har granskat ändringen i `git diff` innan staging.
- [ ] `git log --oneline` visar två commits med prefixet `feat:`.
- [ ] Filen på hårddisken visar fredag, men historiken minns det tidigare onsdagsläget.

---

## Uppgift 4 — Selektiv staging med flera filer

**Mål:** Hantera flera ändrade filer samtidigt och separera dem i atomära commits utan att använda `git add .`.

1. Skapa en ny fil: `inkop.txt` med innehållet `Kaffe och filter`. Spara filen.
2. Öppna `lapp.txt` och lägg till en ny rad längst ner: `Ta med projektrapporten`. Spara filen.
3. Kör `git status`. Du har nu ändringar i två separata filer på disken.
4. Staga enbart anteckningsfilen:
   `git add lapp.txt`
5. Kör `git status`. Bekräfta att `lapp.txt` är grön (staging) medan `inkop.txt` är röd (arbetsyta).
6. Försegla anteckningsändringen:
   `git commit -m "docs: lägg till påminnelse om rapport"`
7. Staga och försegla inköpslistan separat:
   `git add inkop.txt`
   `git commit -m "feat: skapa inköpslista"`
8. Kör `git log --oneline` och bekräfta att loggboken nu innehåller 4 distinkta commits.

**Klart-check:**
- [ ] Du har genomfört två separata commits utan att använda `git add .`.
- [ ] `git log --oneline` visar 4 commits med relevanta prefix (`feat:` och `docs:`).