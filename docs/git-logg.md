# Git-logg

Klistra in utskrifter och svara på frågorna. Det här är din dokumentation av dagens arbete.

## 1. Utgångsläget

Skriv ut `git log --oneline --graph --all` direkt efter att du klonat. Klistra in här:

```
* 5a5841d (HEAD -> main, origin/main, origin/HEAD) Modul 5 i TypeScript med Vite
* 3804533 Add files via upload
* f7a13a4 Add files via upload
* c9a0075 Initial commit
```

## 2. Merge utan konflikt

Klistra in `git log --oneline --graph --all` efter merge:

```
*   3347f9b (HEAD -> main) Merge branch 'meny-nyheter'
|\
| * f13fa03 (meny-nyheter) Steg2: Lägg till kanelbulle på menyn
* | d3475c1 Steg3: Lägg till telefonnummer
|/
* feebc2f Steg1: dokumentera Git-logg
* 5a5841d (origin/main, origin/HEAD) Modul 5 i TypeScript med Vite
* 3804533 Add files via upload
* f7a13a4 Add files via upload
* c9a0075 Initial commit
```

Fråga: Vad är skillnaden mellan en _fast-forward_-merge och en merge som skapar en egen merge-commit? Svara med egna ord:
fast-forward-merge flyttar bara huvudgrenens pekare framåt eftersom det inte finns några nya ändringar i den grenen. En vanlig merge skapar en extra merge-commit som sammanför ändringar från två olika grenar

## 3. Konflikten

Klistra in filen med konfliktmarkörerna, precis som den såg ut innan du löste den:

```
Vardagar: 07–18
<<<<<<< HEAD
Helger: 10–17
=======
Helger: 09–18
>>>>>>> oppettider-sommar
Röda dagar: stängt
```

Fråga: Vad betyder `<<<<<<< HEAD`, `=======` och `>>>>>>> grennamn`?
Det är markeringar som Git lägger till vid en merge-konflikt. De visar vilka delar av koden som skiljer sig mellan två grenar

Hur löste du den, och varför blev det så?
Jag jämföra båda versionerna och valde att skriv en ny. Det blev så eftersom båda grenarna hade ändrat samma del av filen.

## 4. Ångra

Vad är skillnaden mellan `git restore`, `git revert` och `git reset`? Vilken är säkrast när ändringen redan är pushad?

## 5. Pull request

Länk till din pull request (på ditt eget repo):

## 6. Reflektion

Vad är det värsta som kan hända om man kör `git push --force` på en gren som andra använder?
