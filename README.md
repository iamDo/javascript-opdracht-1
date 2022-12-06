# Oefening APIs JavaScript

## Opdracht

Je code moet het volgende doen:

- Een lijst van random users opvragen van `url hier`, deze code hoort uiteraard thuis in `api.js`.
- Van elk van deze users een object van de class `User` maken
- Laat in html een lijst van users, gesorteerd per land zien, voorbeeld:
    - Belgie
        - An Smidt
        - Jos Bortels
    - Croatie
        - Mijnheer Croaat
        - Mevrou Croaat
    - ...
- De landen moeten niet alphabetisch gesorteerd staan, maar natuurlijk beter als je dat wel doet

## Evaluatiecriteria

- CSS: 
  - Mag heel basic zijn, maar je mag niet gewoon volledig de css weglaten

- JavaScript:
  - Gebruik functies
  - Probeer binnen de mate van het mogelijke zo weinig mogelijk code te herhalen
  - Duidelijke namen voor functies, variabelen, classes...
  
- HTML:
  - Ik ken niet genoeg HTML om echt daar feedback op te geven dus ik ga er ook niet echt naar kijken
  
- Richtlijnen:
  - Hieronder staan enkele richtlijnen waar je je best aan houdt. Je mag hier uiteraard van afwijken als je denkt dat je een betere of duidelijkere manier hebt


## Richtlijnen

### Indienen

Maak een public repository op GitHub en mail deze naar `pieter.polmans@protonmail.com`.

Wanneer je denkt dat je klaar bent, stuur een aparte mail om mij te informeren dat ik kan nakijken.

Je mag ALTIJD tussentijds mij een mail sturen om me te vragen eens naar de oefening te kijken voor feedback

Geen deadline natuurlijk, dit is enkel voor bijles 

### Bestanden

Maak de volgende bestanden aan:

- `index.html`: Gewoon een html bestand waar je je javascript code kan inladen en de output laat zien.
- `main.js`: Het hoofdbestand dat uitgevoerd word. Dit is ook het enige bestand dat je mag includen met `<script>`.
- `api.js`: Het bestand waarin je de code voor de API zet, dit ga je moeten includen in `main.js`.
- `user.js`: Het bestand waarin je de code voor de data class zet, dit ga je in `main.js` moeten includen, en misschien ook in `api.js` afhankelijk van je aanpak.

TIP: Omdat je maar 1 `.js` bestand rechtstreeks in je html mag zetten van mij ga je met `import` en `export` moeten werken. Ik geef een simpel voorbeeld:

*main.js*
```js
import getUsers from ./api.js
```

*api.js*
```js
export function getUsers() {
    // Je code
}
```


#### user.js

De `User` class moet de volgende data hebben:

- `firstname`: De voornaam van de `User`.
- `lastname`: De achternaam van de `User`.
- `country`: Het land van de `User`.

- Deze `User` class moet ook de volgende functies hebben.

  - `constructor(firstname, lastname, country)`: De constructor.
  - `generateHTML()`: Deze functie returned een stukje HTML dat de user beschrijft, hier moeten de voor- en achternaam, en het land van de user in staan.

  
#### api.js

Hier moet een functie in staan: `getUsers()`:

De `getUsers()` functie mag je op 1 van de 2 manieren implementeren:

- `getUsers()` geeft gewoon de data van de API terug als een JSON Array
- `getUsers()` geeft een array van objecten van het type `User` terug
