#IT3 - micro-cursus 1: geavanceerde CSS-layouts

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


##Flexible Box Layout

The CSS flexible box layout module, commonly referred to as flexbox, gives us a brand new layout mode in CSS – flex layout. It has been designed to make it easier to layout complex applications and webpages. In this section, I take a look at some of the main layout problems flexbox can solve.

Spacing items evenly

Taking a group of items and spacing them along an axis is a task that has traditionally been rather difficult in web design. Floated elements need a width, yet each one might be a different width and getting them all to fit on a single line with equal spacing usually involves some JavaScript. Flexbox makes this task easy. In my markup I have a list that contains my navigation.

Had we set the value of justify-content to space-around then the space would have been added all around each element equally, meaning that instead of being flush to the outside edges of the container, there would be some space before the first and after the last element.

The simple example above uses some default behaviour of flexbox. The items here have been displayed as a row. This is the default behaviour and is equivalent to setting the property flex-direction to row. The flex-direction property can have one of four values: row; row-reverse; column; and column-reverse. These enable you to display the items in a row, or reverse their order in a row; and similarly in a column, or a column with the order reversed. Example 2-3: Setting flex-direction nav ul{ display: flex; justify-content: space-between; flex-direction: row-reverse; }

Equal height columns Another interesting aspect of flexbox is that it enables you to create equal height boxes, even if the content of some boxes is longer than others. The default value of the property align-items is stretch. This stretches each item in the group to the height of the tallest. You can see this in action in our navigation. I've added some text to one of the items making it taller than all of the others, but each item now grows to the height of the tallest item keeping the columns lined up neatly.

The property align-items can also take the following values: • flex-start • flex-end • center • baseline • stretch To understand how these work you need to realise that flexbox has a concept of two axes: the main axis, along which items flow; and the cross-axis. By setting flex-
....
