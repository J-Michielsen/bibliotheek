#IT3 - micro-cursus 1: geavanceerde CSS-layouts

Versie 0.1, door Kristof Michiels (21.9.2016); wordt nog verder aangevuld.

We hebben vorig jaar in IT1 pagina's leren layouten met floats en positioning. En heel lang geleden zelfs door gebruik van tables. Niets verkeerd mee, maar eigenlijk waren deze technieken oorspronkelijk niet voor layouting bedoeld. 

CSS is langzamerhand geëvolueerd tot de complexe taal die ze vandaag is. Bovendien zijn de CSS3 specificaties nog volop in beweging. Er zijn ondertussen nieuwe mogelijkheden toegevoegd specifiek bedoeld voor het maken van layouts. 

Sommigen zijn al klaar voor productiesites en werken quasi homogeen in alle verschillende moderne browsers. Anderen zijn nog zo nieuw en aan het evolueren dat deze in productie nog niet kunnen gebruikt worden. Maar die mogelijkheid zal naar alle waarschijnlijkheid snel volgen. Het is aan ons om ons daar terdege op voor te bereiden.  

Wij gaan in de komende lessen 3 van die technieken zien
- multi-column layout
- flexible box layout
- grid layout

Alle voorbeelden staan op Codepen in de collection gewijd aan het vak IT3: [https://codepen.io/collection/nwWZPZ/](https://codepen.io/collection/nwWZPZ/)


##Multi-column layout

Deze module is de meest volwassen techniek van de drie modules die ik jullie wil laten zien. 

Multi-column layout maakt het mogelijk om informatie te gaan schikken in kolommen. Dit op dezelfde manier als in bvb een krantenartikel. 

```html
main { 
      /* hier gebeurt de magic */
      column-count: 3;
      column-gap: 4em;
      column-rule: 1px dotted #CCC;
}
```

###Column-count en column-width

Je gaat hierbij als volgt te werk: je neemt een container in je document en geeft in CSS aan dat je het wil schikken in kolommen. De browser doet dan de rest. Als je het aantal kolommen aangeeft (column-count) dan zal de browser zelf de breedte van elke kolom uitrekenen zodat deze kolommen perfect passen binnen de container. Als je daarentegen een (optimale) breedte meegeeft (column-width) voor de kolommen dan zal de browser zoveel kolommen gebruiken als mogelijk gegeven de beschikbare breedte.   

In de voorbeelden op Codepen zal je ook zien dat de kolommen niet tegen elkaar staan aangedrukt. Er is een ruimte tussen, die wordt gecontroleerd door de column-gap eigenschap. Zet je deze op 0, dan zal er geen ruimte tussen de kolommen zijn. Standaard zou er een ruimte van 1em door de browser moeten worden toegepast, maar als je volledige controle wenst zet je deze waarde best expliciet. 

De stylingmogelijkheden zijn op dit moment eerder beperkt. Zo kan je geen kolommen individueel gaan stylen. Er is geen manier om margin en padding op een kolom te zetten, of de achtergrond van een individuele kolom.

###Column-rule

We kunnen wel een scheidingslijn maken tussen de kolommen. Dit doe je door gebruik te maken van de column-rule eigenschappen: column-rule-style, column-rule-width en column-rule-color. Deze kunnen ook korter beschreven worden (zoals bij de border-eigenschap): column-rule: width style color;

De scheidingslijn wordt centraal geplaatst in het midden van de ruimte die door column-gap werd vrijgemaakt. Als je die ruimte dus groter wil maken zal je de column-gap eigenschap moeten aanpassen. Als de scheidslijn dikker is dan de beschikbare ruimte dan zal deze de tekst beginnen te overlappen. De scheidingslijn zelf neemt dus geen officiële ruimte in beslag.

###Column-span

Als je een element wil laten verschijnen doorheen de verschillende kolommen, dan kan je dat element de eigenschap column-span de waarde "all" laten geven.

###Column breaks

Bij gebruik van deze techniek heb je ook controle over hoe kolommen in stukken worden gedeeld. Dit kan nuttig zijn in het geval er elementen zijn die je niet halverwege wil gesplitst zien in twee kolommen, of wanneer je zeker wil zijn dat een bepaald element bovenaan staat in een bepaalde kolom. Voorbeelden: 

```html
.main p { page-break-inside: avoid; }
.main blockquote { page-break-before: avoid; }
h1 {page-break-before: always;}
```


Mogelijkheden:
```
page-break-before: auto|always|avoid|left|right|initial|inherit;
page-break-inside: auto|avoid|initial|inherit;
page-break-after: auto|always|avoid|left|right|initial|inherit;
```

### Responsive design

Deze techniek is zeer bruikbaar voor responsive design: de kolommen zijn immers responsive uit zichzelf. Ook een afbeelding zal beperkt worden tot de beschikbare breedte van de kolom. Dus de standaardmanier om een afbeelding automatisch flexibel te krijgen zal ook werken binnen kolommen. Indien je niet max-width: 100% zet op de afbeelding zal de browser de afbeelding zelf croppen. Maar dus: best max-width: 100% gebruiken.

Bekijk zeker alle oefeningen op Codepen!

##Flexible Box Layout

Bij deze techniek wordt over het algemeen gesproken over de flexbox-techniek of kortweg flex. Voornaamste troef van flexbox is het even spreiden van elementen over een beschikbare ruimte.

Een aantal elementen gelijk uitspreiden over de beschikbare ruimte op een bepaalde as is iets dat niet zo eenvoudig op te lossen viel binnen web design. Tot nu toe: floaten met een bepaalde width, maar dit is niet zo simpel. Flexbox maakt dit wel heel eenvoudig oplosbaar. 

Je activeert flexbox met display: flex;

Het vb op Codepen toont het standaardgedrag van flexbox. De items worden getoond als een rij. Het is het equivalent van het zetten van de flex-direction eigenschap op "row". Maar dat kan bvb ook "column" zijn.

Flexbox laat ook toe de kolommen een gelijke hoogte mee te geven, zelfs al zou de inhoud van één box anders zijn dan die van een andere.
Dat doe je met de eigenschap align-items. De default waarde hier is "stretch" en daarmee passen alle boxes zich aan aan het grootste formaat.

```html
nav ul{
  /* flexbox magie */
  display: flex;
  justify-content: space-between;
  /*justify-content: space-around;*/
  /*flex-direction: row-reverse;*/
  /*flex-direction: column;*/
  /*flex-wrap: wrap;*/
}

nav li {
      /* flexbox magie */
      border: 1px solid red;
      padding: 10px;
      /* flex:auto; */
}
```
Mogelijkheden:
```
justify-content: flex-start|flex-end|center|space-between|space-around|initial|inherit;
flex-direction: row|row-reverse|column|column-reverse|initial|inherit;
align-items: stretch|center|flex-start|flex-end|baseline|initial|inherit;
flex-wrap: nowrap|wrap|wrap-reverse|initial|inherit;
```

Bekijk goed alle oefeningen op Codepen!

## Opdracht tegen uiterlijk volgende les! Je werkt hiervoor op codepen.io

- Je maakt de volledige startpagina voor een muziekrecensiesite. Het genre en de branding kies je zelf. 
- Je mag content herbruiken van een andere muzieksite
- Je zorgt voor een mooie algemene stijl
- Met bijzondere aandacht voor de proporties en de "grid"
- Je zorgt dat de site responsive is
- Je maakt gebruik van multi-column layout voor één of meerdere artikels centraal op de startpagina
- Voor de navigatie gebruik je flexbox
- Hoe meer je multi-column layout en flexbox gebruikt voor andere elementen op de site, hoe beter
