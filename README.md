# Kanotplats-Admin

## HOWTO Project setup och hur man kör koden
### Installera dependencies
1. Installera pipenv för dependency management genom att köra detta kommando: 
```
python3 -m pip install --user pipenv
```
2. Gå in i mappen för projektet
``` 
cd **/**/Kanotplats-Admin
```
3. Starta en ny Virtual Environment med:
```
pipenv shell
```
4. Installera packages från Pipfile genom att köra:
```
pipenv sync
```

### Köra koden för att generera bilder
1. Ladda ner grupplistan från hemsidan genom att klicka i A-Förrådet 2025, B-Förrådet 2025, C-Förrådet 2025, C-Förrådet 2025 rabatterad, P-förrådet 2025. Ladda därefter ner som Grupplista (excel) och byt ut den gamla grupplistan i projekt-mappen mot den nya.
1. Starta virtual environment:
```pipenv shell```
2. Kör koden:
```python3 kanotplats.py```
3. Du kommer få meddelande om dubbelbokningar och ett "Förråden har ritats och sparats som PDF-filer." när programmet har körts färdigt.
4. Ladda upp dom nyligen genererade .PDFerna till Github

### Gudier för Pythons package management:
https://packaging.python.org/en/latest/tutorials/installing-packages/
https://packaging.python.org/en/latest/tutorials/managing-dependencies/#managing-dependencies

## Överblick
Våra förråd:
- A - Havskanoter
- B - Tävlingskanoter/Motionskanoter
- C - Hyrkanoter, kanotlån och tävlingskanoter
- D - Havskanoter
- Pannrummet - Kanoter utan ägare och mindre (forsränning?) kanoter för inomhusträning
  
I första hand ämnar vi placera tävlingskajaker/motionskajaker i B-förrådet, och placera havskajaker i A och D. Kanoter utan ägare flyttas till Pannrummet, där även mindre kanoter för inomhusträning förvaras.
I C-förrådet finns hyrkanoterna, en avdelning för lånekanoter och en för tävlingskanoter.

![Förråd](/Bilder/Kanotplatser.jpg)
  
## Registrering av ny kanotplats
### Hitta medlem i register
1. Sök medlem - Nu Ser du alla uppgifter
2. Längst ner: Medlemskap -> Nycklar -> Kanotplats -> Aktiveter
3. Klicka på förstoringsglaset längst till vänster så får du alla uppgifter.
### Registrera ny kanotplats
1. Öppna aktuell medlem
2. Gå till aktiviteter/bokning längst till höger under Verktyg/åtgärder
3. Klicka på "Skapa aktivitetsbokning"
4. Välj sektion/typ
5. Kajakplatser
6. Välj förråd
7. Välj XYZ förråd 2025
8. Nu får du upp en ruta "aktivitetsbokning"
9. Lägg in förråd/platsnummer på Referens för att inte tappa bort det
10. OBS: Kontrollera om "Skapa faktura" ska vara ikryssad, se regler nedan.
11. Bekräfta
12. Gå till Status - avdelningen längst ner på medlemsrutan
13. Öppna med förstoringsglas på Medlemsadministration/Kajakplatser och skriv in Förråd/Platsnummer i rutan Kommentar.
14. Tryck alltid spara efter åtgärd
15. I detta läge/ruta kan du också radera bokning i röda rutan om du ska avsluta platsbokning.

![Förråd](/Bilder/Aktivitetsbokning.jpg)

**Förklaring aktivitetsbokning:**
- Referens - Kanotplatsnumret
- Inkludera Startpaket - ?
- Spara denna bokning som köplats - ?
- Skapa faktura - Gör detta om årets fakturor redan gått ut så det skickas ut en faktura för detta år för denna. Kan skippas om det är väldigt sent på året så personen inte behöver betala en årsavgift för för kort tid.
- Skicka inbjudan/erbjudande att Prova-på - ?
- Skicka avisering via e-post - Medlemmen får e-post att bokningen är gjord

### Hitta lediga platser
1. Startsida -> Verksamhet -> Grupper
2. Klicka i rutan för aktuellt förråd
3. Klicka på rutan: Med markerade
4. Klicka på Grupplista(Excel)
5. Ladda upp Excellistan
6. På kommentar ligger platsnummer
7. De platser som saknar nummer är ej bokade på någon person och lediga

### Avregistrera kanotplats
1. Startsida -> Sök medlem -> Aktiviteter
2. Klicka på förstoringsglaset bredvid kanotplatsbokningen i fråga t.ex. "B-förrådet 2025"
3. Radera bokning
Alternativt:
1. Startsida -> Verksamhet -> Grupper
2. Skrolla ned och välj gruppen för korrekt förråd t.ex. "B-förrådet 2025"
3. Klicka på Bokningar
4. Sök via webbläsaren på namn eller kanotplats-nummer för att hitta till rätt person.
5. Klicka på pilen längst till höger bredvid namnet och välj "Radera"

**OBS:** För de flesta medlemmar så faktureras kanotplats och medlemskap samtidigt. Det innebär tyvärr att om man raderar bokningen för kanotplats så återbetalas hela fakturan inklusive medlemskapet. Du löser detta genom att först radera bokningen för kanotplats och sedan lägga in en ny enskild bokning för medlemskap. Den fakturas kommer sedan betalas automatiskt från den kredit som de fick då bokningen av kanotplatsen raderades.

**TODO:** Kolla upp hur man ser till att inte fakturan återbetalas.

## E-mail adresser
- kanotplats@bkk.se
- styrelse@bkk.se
- kassor@bkk.se
- nycklar@bkk.se
- [Lista över adresser till andra funktioner](https://www.bkk.se/klubbinfo/styrelse-funktionarer/)

## Otydligheter
1. Förtydliga hur man hittar vilka nummer som existerar i varje förråd
2. Förtydliga varför olika förråd har olika årskostnad
3. Skillnad i bokning för C-förrådet och C-Förrådet (Rabatterad)
4. Vad gäller för bokning i Pannrummet (förråd P)
5. Vad gör man om en person avslutar sin bokning? Tar man bort deras aktivitetsbokning i systemet så återbetalas deras faktura, vilken också innehåller deras medlemsbokning. Egentligen ska inga pengar betalas tillbaka.
