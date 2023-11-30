> _Fork_ deze leertaak en ga aan de slag. 
Onderstaande outline ga je gedurende deze taak in jouw eigen GitHub omgeving uitwerken. 
De instructie vind je in: [docs/INSTRUCTIONS.md](docs/INSTRUCTIONS.md)

# Hand - Footprint calculator _sprint 04_
<!-- Geef je project een titel en schrijf in één zin wat het is -->
Dit project bestaat uit het maken van een web-applicatie, zodat kleine bedrijven hun handprint en footprint overzichtelijk kunnen zien. Hierbij moet de feitelijke situatie op een zo goed mogelijke manier worden gevisualiseerd.

sprint 04:
Deze sprint staat het maken en het naleven van de huisstijl. Omdat de huisstijl nog niet bestond is die gezamelijk gemaakt door de mensen van je squad met dezelfde opdrachtgever.

## Beschrijving
<!-- In de Beschrijving staat hoe je project er uit ziet, hoe het werkt en wat je er mee kan. -->
<!-- Voeg een mooie poster visual toe 📸 -->
<!-- Voeg een link toe naar Github Pages 🌐-->

Deze webapplicatie is in opdracht van CrossmarX. Bij deze hand- footprint calculator moet de klant een goed overzicht hebben hoe milleuvriendelijk zijn bedrijf daadwerkelijk is. 
Hierbij zijn de volgende betrokkenen belangrijk om te vergelijken: medewerkers, aandeelhouders, leveranciers, klanten en de omgeving. Website op desktop is een pre, mobile niet.

![BODY](https://github.com/Anna-Kyra/look-and-feel-corporate-identity/assets/144000242/df4313c0-96a2-4c54-9850-bf6dfbae6fe7)

### Userstories
CEO: Als bedrijfseigenaar wil ik een goed overzicht van hoe milieuvriendelijk mijn bedrijf is.

CEO: Als bedrijfseigenaar wil ik zien wat voor een invloed ieder van mijn stakeholders hebben op de milieuvriendelijkheid op mijn bedrijf.

CEO: Als bedrijfseigenaar wil ik een berekening hebben van mijn hand- en footprint en van mijn stakeholders.

website link: 
Figma link: 

## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met Javascript gedaan en hoe? Misschien heb je een framwork of library gebruikt? -->
### CSS

* Voor de layout is er grid gebruikt.
  ```CSS
  grid-template-columns: 2fr 8fr;
  ```
* Custom Properties voor de general styling zoals kleuren, radiusses etc.
  ```CSS
  :root {
    /* COLOUR */
    --clr-primary: #AD97C9;
    --clr-background: #272932;
    --clr-text: #ecf8f8;
    --clr-secondary: #519879;
    --clr-accent: #fb8b24;
  
    /* RADIUS */
    --btn-radius: 1000px;
    --sec-radius:.25em;
  
      /*TYPOGRAPHY*/
    --thin: 400; /* Halton-italic */
    --chubby: 600 ; /* Halton-regular */
    --fat: 800; /* Halton-bold */
  
      /* BUTTON */
    --btn-hover: brightness(120%);
    --btn-active: brightness(80%);
  
    /* FORMS */
    --forms-focus: 3px solid var(--clr-primary);
  }
  ```
* Geprobeert om **nesting** toe te passen (volgende sprint meer gebruiken).
  ```CSS
  .button {
    margin: 1em 0.5em;
    padding: 0.75em 2em;
    font-size: .7em;
    text-transform: uppercase;
    border-radius: var(--btn-radius);
    border-style: none;
    color: var(--clr-background);
    background-color: var(--clr-primary);
    cursor: pointer;
    grid-area: b;
    transition: all 0.3s ease-in-out;

    &:hover {
      filter: var(--btn-hover);
    }

    &:active{
      filter: var(--btn-active);
    }

    &:disabled {
      cursor: not-allowed;
      opacity: 50%;
    }

    &:disabled:hover {
      filter: none;
    }

      
    &.destructive {
      background-color: var(--clr-accent);  }

    &.recommended {
      background-color: var(--clr-secondary);  }

    &.minor {
      background-color: transparent;
      color: var(--clr-secondary);

      &:hover {
        text-decoration: underline;
      }
    }

    &.buttons p:first-child {
      margin: 0;
      padding: 0;
    }
  }
  ```


## Bronnen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
