# Dag 3 · CSS-grunderna och boxmodellen

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du kopplar CSS till kaféets sidor och styr grundläggande utseende: färg, avstånd, kantlinjer och boxmodellen.

## Bakgrund

CSS styr utseendet. Varje regel består av en **selektor** (vad) och **deklarationer** (hur). Alla element är rektangulära lådor med innehåll, padding, border och margin. Det är boxmodellen. Förstår du den förstår du 80 % av alla layoutproblem. Specifikationen för kaféets utseende finns i `design.md`.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Koppla CSS

Öppna `styles.css` (tom, med kommentarer). Kontrollera att båda HTML-filerna har `<link rel="stylesheet" href="styles.css">` i `<head>`. Skriv `body { background-color: #fffaf3; }`, spara och se sidan ändra färg.

### Steg 2. Börja med boxmodellen

Överst i filen: `*, *::before, *::after { box-sizing: border-box; }`. Förklara med en kommentar vad det gör. Sätt sedan `body { margin: 0; }`.

### Steg 3. Styla sidhuvud och sidfot

Ge `header` och `footer` bakgrundsfärg, textfärg och `padding` enligt `design.md`. Gör länkarna i dem vita.

### Steg 4. Rensa menylistan

Ta bort punkterna i `nav ul` (`list-style: none`) och nollställ `margin`/`padding`.

### Steg 5. Styla menykorten

Ge `article` vit bakgrund, `border`, `border-radius`, `padding` och `margin-bottom`. Se till att bilderna aldrig blir bredare än sitt kort (`max-width: 100%`, `height: auto`).

### Steg 6. Centrera innehållet

Ge `main` `max-width: 1100px`, `margin: 0 auto` och `padding`. Förklara i en kommentar vad `margin: 0 auto` gör.

### Steg 7. Bygg knappen

Klassen `.knapp` ska se ut som en knapp: `display: inline-block`, bakgrund, vit text, `padding`, `border-radius`, ingen understrykning.

### Steg 8. Inspektera med DevTools

Högerklicka på ett kort → *Inspektera*. Hitta boxmodell-diagrammet (fliken *Computed*). Ändra `padding` direkt i DevTools och se vad som händer. Rita av boxmodellen för ett `article` i en kommentar i CSS-filen.

## Kontrollista: så vet du att du är klar

- [ ] `styles.css` är kopplad i båda HTML-filerna.
- [ ] `box-sizing: border-box` är satt globalt.
- [ ] Header, main, article, knapp och footer är stylade enligt `design.md`.
- [ ] Innehållet är centrerat med en maxbredd.
- [ ] Inga bilder sticker utanför sina kort.
- [ ] Du kan förklara skillnaden mellan `padding` och `margin`.
- [ ] Du har pushat till din fork och skickat in länken.

## Tips om du fastnar

- Inget händer? Kontrollera att filnamn och sökväg i `<link>` stämmer exakt, och att du sparat CSS-filen.
- Hård refresh i webbläsaren: Ctrl+Shift+R.
- En regel som inte verkar gälla? Öppna DevTools: överstruken regel betyder att en annan vann.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Reflektion: Beskriv boxmodellen med egna ord. Vilken av delarna (content, padding, border, margin) förstod du bäst, och vilken var svårast?

## Vill du mer? (frivilligt)

- Ge varje kort en lätt skugga med `box-shadow`.
- Skriv en regel som ger varannat kort en annan bakgrundsfärg (`:nth-child`).
