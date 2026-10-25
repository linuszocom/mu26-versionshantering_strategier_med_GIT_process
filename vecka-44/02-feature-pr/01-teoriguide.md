# 01 — Teoriguide: sidofacket och frågan

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt eller peka på i gruppens repo. Tar du materialet från noll: läs klart, gör sedan [03 — Övningar](./03-ovningar.md). Lådan, kuvertet och glasmontern från vecka 1 gäller fortfarande. Nytt är den gemensamma montern, sidofacket och frågan innan glaset ändras.

Vi börjar med att alla skriver rakt i glaset. Sedan får varje person ett sidofack, och glaset tar emot en ändring först när någon annan har sagt ja.

---

## Glaset tar emot en ändring i taget

Många tänker nu: “Vi har ett repo, då committar vi alla på main.” Andas. Då skriver ni ovanpå varandra i samma glas.

**Metafor:** Gruppen har **en** publik glasmonter. Glaset heter `main`. Där står startfilen, med TODO kvar, så historiken syns. Din ändring ligger först i ett **sidofack** med ditt namn, `feature/anna`. Glaset rör sig inte för att du förseglade ett kuvert. Någon annan läser ändringen. Sedan flyttar knappen på GitHub in den.

**Vad det är:** En gemensam monter, ett sidofack per person, en fråga till `main`.  
**Varför det finns:** Utan sidofack finns ingen rad att peka på som är din.  
**Om det saknas / vad det INTE är:** Att pusha rakt till `main` är inte samarbetet. `git merge` i terminalen lägger in ändringen utan frågan.

**Målsvar (säg högt / skriv i README):** *“Vi har en gemensam monter. Jag jobbar i feature och mitt namn. Någon annan godkänner. Knappen Merge pull request lägger in ändringen i main.”*

---

## Inbjudan — collaborator

**Collaborator** låter som en titel. Det är ett ja: du får ställa upp ett sidofack i samma monter.

En person skapar ett **publikt** repo. De andra bjuds in under Settings, Collaborators. Inbjudan är klar när personen har tackat ja. Utan ja nekas pushen.

Bocka inte i Add a README när montern skapas. Då är glaset inte tomt, och den första pushen av startfilen stöts bort. Samma sak som när din egen monter redan hade ett papper: nytt tomt repo, ny adress.

**Vad det är:** Ett ja till samma repo.  
**Varför det finns:** Utan ja kan de andra läsa, men inte lämna sitt sidofack.  
**Om det saknas:** Ett repo där bara ägaren kan pusha är inte gruppens monter.

**Målsvar (säg högt / skriv i README):** *“Collaborator är inbjudan som någon har tackat ja till. Då får den personen pusha till samma monter.”*

---

## En låda från montern — git clone

`git clone` och länken ger dig montern som en ny låda, en gång. Sedan `cd` in i mappen. `git status` ska säga `On branch main`, och `index.html` ska ligga där.

Adressen heter fortfarande remote, smeknamn `origin`. Clone sätter den åt dig. Du kör inte `git remote add` i den här lådan.

Den som skapade repot klonar också, lägger in startfilen med TODO kvar, förseglar kuvertet och kör `git push`. De andra klonar **efter** den pushen, så filen följer med.

**Vad det är:** Första kopian av montern, ner i en mapp.  
**Varför det finns:** Utan en låda har `checkout` inget att stå i.  
**Om det saknas:** Att bara öppna filen på GitHub i webbläsaren ger inget sidofack.

**Målsvar (säg högt / skriv i README):** *“git clone är montern ner i en låda, en gång. Origin är redan satt. index.html ska ligga där, och status ska säga main.”*

---

## Sidofacket kopierar lådan — pull först

`git checkout -b feature/anna` skapar sidofacket och ställer dig i det. Git kopierar den `main` som ligger **i din låda**. Inte den som syns i glaset just nu.

Därför, innan sidofacket:

```bash
git checkout main
git pull
```

`git pull` hämtar glasets `main` ner i lådan. `Already up to date` betyder att du redan har den. Sedan tar du namnet.

Hoppar du över pull kan sidofacket sakna startfilen, fast den syns på GitHub.

**Vad det är:** Hämta glaset, kopiera sedan den färska `main` till `feature/` och ditt namn.  
**Varför det finns:** Sidofacket föds ur lådan, inte ur skärmen.  
**Om det saknas / vad det INTE är:** Pull är inte push baklänges som en ångerknapp. Den byter inte ut ditt sidofack mot någon annans.

**Målsvar (säg högt / skriv i README):** *“checkout -b kopierar main i min låda. Pull hämtar glaset först, så startfilen finns innan jag tar mitt namn.”*

---

## Ett kuvert, upp i sidofacket

Varje person tar en rad från backloggen. Byt bara `return` i den funktionen. Rör inte raderna under funktionerna.

| Rad | return | Synligt när den är inne i glaset |
|-----|--------|----------------------------------|
| `hamtaNamn` | gruppens namn | sidan visar namnet |
| `addera` | `a + b` | Summa: 12 |
| `statusForTal` | `"ok"` om talet är större än 10, annars `"för låg"` | ok |
| `raknaTecken` | antalet tecken | Tecken: 3, för texten `git` |

Är ni tre och raderna fyra, tar någon två rader i **samma** sidofack. Det är fortfarande en fråga per person.

```bash
git add index.html
git commit -m "hamtaNamn lämnar tillbaka gruppnamnet"
git push -u origin feature/anna
```

Byt ut `anna` och meddelandet mot din rad. `-u` berättar för lådan var sidofacket ska upp nästa gång. Efter det räcker `git push` på samma fack.

`git push` här ställer upp sidofacket så de andra kan se det. `main` i glaset har fortfarande TODO i den första committen.

Sitter två vid samma dator och samma git-konto: turas om, och skriv båda namnen i meddelandet. Var och en har ändå ett eget sidofack och en egen fråga.

**Vad det är:** Ett förseglat kuvert på en gren som heter `feature/` och ditt namn.  
**Varför det finns:** Historiken ska visa vem som tog vilken rad.  
**Om det saknas:** En push till `main` blandar din rad med glaset utan att någon annan har läst den.

**Målsvar (säg högt / skriv i README):** *“Jag committar min rad på feature och mitt namn och kör git push -u origin dit. main har fortfarande TODO tills frågan är inne.”*

---

## Frågan — Pull Request

**Pull Request** är frågan: får det här sidofacket in i glaset?

På GitHub: **Compare & pull request**. Bas ska vara `main`. Compare ska vara `feature/` och ditt namn. Byter du plats frågar du om glaset ska in i sidofacket. Läs de två orden innan du skapar frågan.

Skriv en mening om vad som ändrades. “Klart” pekar inte på en rad.

**Review:** någon **annan** öppnar frågan, tittar under **Files changed** och tar **Review changes → Approve → Submit review**. Du godkänner inte din egen.

Först därefter: **Merge pull request**. Det är knappen. Inte `git merge` i terminalen.

När den är inne syns den under **Pull requests → Closed**. Under **Commits** på `main` ligger startfilen kvar som äldst, med TODO, och din rad som en senare commit.

**Vad det är:** Fråga, någon annans ja, knapp.  
**Varför det finns:** Gruppen ska kunna peka på din rad och på vem som läste den.  
**Om det saknas:** Ett sidofack som aldrig blev en fråga syns inte som samarbete i glaset.

**Målsvar (säg högt / skriv i README):** *“Bas är main, compare är feature och mitt namn. Någon annan tittar under Files changed och Approve. Sedan Merge pull request. Fem ord: branch, push, PR, review, merge.”*

---

## Metod — när det blir rött

1. Läs meningen. Gissa inte om.
2. `git status`. Vilket ord står efter `On branch`? Sidofacket ska heta `feature/` och ditt namn innan du pushar ändringen.
3. Push nekas och du inte har tackat ja till inbjudan: acceptera, kör samma push.
4. Sidofacket saknar `index.html`: du klippte det från en gammal låda. `git checkout main`, `git pull`, ta sidofacket igen från den färska `main`.
5. Bas och compare har bytt plats: stäng frågan och öppna den med `main` som bas.

**Målsvar (säg högt / skriv i README) — metod:** *“Jag läser den röda meningen, tittar på status, och ändrar en sak: inbjudan, pull före sidofacket, eller basen main.”*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| Alla committar på `main` | Sidofack, fråga, någon annans ja, knappen |
| Add a README ibockad | Nytt tomt repo |
| `checkout -b` utan pull | Sidofacket kopierar lådan. Hämta glaset först |
| Push till `main` med funktionsraden | `git push -u origin feature/` och ditt namn |
| Du Approve din egen fråga | Någon annan, under Files changed |
| `git merge` i terminalen | **Merge pull request** på GitHub |
| “Klart” i frågetexten | En mening om vilken rad |
| Samma funktion i två sidofack | Ta olika rader. Krocken hör inte hit |

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md) eller [03 — Övningar](./03-ovningar.md).
