Markdown schrijven
========================

Dit document legt uit wat Markdown is en hoe je het gebruikt. De tekst is zelf volledig met Markdown opgemaakt. Dit is versie 1, geschreven door Kristof Michiels op 17 juni 2016.

Wat is Markdown?
----------------

Markdown is een set opmaak-notaties die je in een teksteditor (bvb. Atom) aan je documenten toevoegt om de tekst vorm te geven. Markdown is heel snel te leren en ontworpen om gemakkelijk geschreven te kunnen worden. De notaties zijn helder en logisch en hinderen de leesbaarheid van de tekst niet. Je van Markdown voorziene tekst kan automatisch omgezet worden naar een hele reeks andere formaten (zoals pdf of html).  

Markdown is ontwikkeld door John Gruber in 2004. Er bestaan verschillende versies van Markdown. De meesten voegen extra notaties toe, maar de basisfunctionaliteit is in elke variant dezelfde.

Hieronder een voorbeeld van hoe eenvoudig je Markdown kan schrijven. 

```
Mijn titel
==========

Hier komt een paragraaf met **benadrukking** in de tekst.
Deze tekst maakt deel uit van mijn paragraaf.

- Dit is een lijstelement
- Dit is ook een lijstelement
- Dit tenslotte is ook een lijstelement
```

### Waarom zou je het gebruiken?

Met Markdown houd je al je documenten in een draagbare simpele tekstvorm. Je kan er alles mee schrijven, gaande van een shopping lijstje tot een blogpost, documentatie voor je code of designs, tot zelfs hele boeken. 
Je kan het -zoals ik hier - gebruiken om rechtstreeks teksten te publiceren op GitHub of op blogsystemen zoals WordPress of Jekyll. 

Veel platformen en tools laten je toe te werken met Markdown. Atom heeft zeer goede ondersteuning voor het schrijven met Markdown. 

Een goeie online tool om snel mee van start te kunnen gaan is stackedit.io. Surf naar http://stackedit.io en je kan onmiddellijk Markdown in je browser beginnen te schrijven.

De basis: vaak voorkomende Markdown syntax
------------------------------------------

### Paragrafen

Paragrafen komen van alle elementen het vaakst voor en hebben in Markdown geen enkele bijzondere formatting nodig. Je schrijft gewoon je paragraaf en laat deze voorafgaan en eindigen op een lege lijn. Indien je ergens in je paragraaf tekst op een nieuwe regel wil doen beginnen dan laat je de regel erboven eindigen op minstens twee spaties.

```
Dit is de eerste paragraaf. We kunnen hem zo lang maken als we zelf willen.   
Deze regel staat op een nieuwe lijn omdat ik de vorige zin heb laten eindigen op 2 spaties.

En dit is een tweede paragraaf.
```

### Hoofdingen of titels

Markdown ondersteunt hoofdingen op verschillende manieren, met twee soorten van opmaakcodes. Je kan deze zonder problemen door elkaar gebruiken. 

Bij de eerste manier ga je onder je hoofding op een nieuwe regel met gelijk-aan-tekens (=) voor een onderlijning zorgen. Je maakt op deze manier je belangrijkste titel aan. Je titels van het tweede niveau doe je op dezelfde manier maar je gebruikt bij je onderlijning streepjes (-).  
Hier zie je een voorbeeld:

```
Hier komt de belangrijkste titel
================================

Hier komt een titel van het tweede niveau 
-----------------------------------------
```

Op de tweede manier kan je elke van de 6 mogelijke html-stijlen voor hoofdingen beschrijven. Je laat je titel onmiddellijk voorafgaan door één of meerdere hashtags (#), eentje voor elk niveau dat je wenst aan te geven. Voor een titel van niveau drie zal je drie hasthtags gebruiken. Witruimte tussen de hastag(s) en de titeltekst mogen maar zijn niet verplicht.

```
# Een titel van het eerste niveau 

## Een titel van het tweede niveau

### Een titel van het derde niveau
```

Kies zelf welke manier jouw voorkeur wegdraagt. Ikzelf werk met onderlijning voor de eerste niveau's. Vanaf niveau drie werk ik dan met hastags.


### Lijstjes maken

Zowel bullet-lijsten als genummerde lijsten zijn mogelijk. Bullet-lijsten maak je met streepjes, sterretjes, plus-tekens, gevolgd door minstens één spatie. Aan jou de keuze. Ik doe het hier met streepjes:

```
- Dit is een element
- Dit is ook een element
- Ik ben het derde element
```

Bij genummerde lijsten gebruik je cijfers met daarachter telkens een punt en minstens één spatie:

```
1. Dit is element 1
2. Dit is element 2
3. En dit is element 3
```
Als je een witregel open laat tussen elk lijstelement, dan zal in html elk lijstelement in een paragraaf worden gewikkeld.

### Horizontale lijnen

Een horizontale lijn voeg je toe door drie of meer strepen, sterretjes of underscores op een eigen regel te plaatsen. Deze tekens mogen (maar niet verplicht) gescheiden zijn door een spatie.

```
* * *
- - - - - -
```

### Blok-aanhalingen

Aanhalingen of block quotes maak je met een groter-dan-teken (>). Een goeie manier van werken is een groter-dan teken te plaatsen op elke regel, maar je kan je ook beperken tot één per paragraaf.  

> Dit is een blok-aanhaling. Sommige tekst staat hier,
> en andere staat daar. Er staat zelfs een beetje tekst
> hier.
> Dit is de laatste lijn met tekst binnen deze aanhaling.


### Benadrukken

Er zijn twee manieren van benadrukken: schuin of italics en vet of bold. Schuine benadrukking doe je door de tekst tussen enkele underscores of sterretjes te plaatsen.

```
Dit is een voorbeeld van _schuingedrukte benadrukking_ 

En dit is ook *een voorbeeld*.
```

Vette benadrukking doe je door een paar van twee underscores of sterretjes te gebruiken.

```
Dit is een voorbeeld van __vetgedrukte benadrukking__ 

En dit is ook **een voorbeeld**.
```

### Links

Links kan je in Markdown op verschillende manieren weergeven. De meest voorkomende is inline. De gelinkte tekst staat dan tussen vierkante haakjes, de URL staat tussen haakjes. Je kan indien je dit wenst ook een titel-attribuut koppelen aan de link.

```
[Mijn website](http://kristo.fm)

[Mijn website](http://kristo.fm/ "Thuisplek voor interessante webdesign tutorials")

```

Indien je de links wil splitsen (zoals bij een voetnoot eigenlijk) kan je de referentie-manier van noteren in Markdown gebruiken. Je geeft elke link dan een uniek label, tussen een tweede set vierkante haakjes geplaatst. Je moet dan ergens in hetzelfde document ook nog het label beschrijven. De labelbeschrijving zelf verschijnt niet in de tekst. Ook hier kan je optioneel een titel-attribuut toevoegen aan de link.

```
[Kristofs web site][kristofm]

...

[kristofm]: http://kristo.fm/ 
[kristofm]: http://kristo.fm/ "Thuisplek voor interessante webdesign tutorials"

...

Bezoek de [kristo.fm][] site om een tutorial op te zoeken

[kristo.fm]: http://kristo.fm/
```

### Afbeeldingen

Closely related to links, you might also want to include images in your documents. Since Markdown documents are plain text, these are of course references to image
s, just like the IMG tag in HTML.

The syntax is practically identical to that for links, including both inline and reference variants, with two small differences:
• To indicate that you're including an image in the document, instead of just linking to the image, an exclamation-mark (!) is placed before the first set of square brackets.
• The text inside the square brackets is used as ALT text for the resulting IMG tag, rather than linked text on the web page (since the image itself will be there).
To embed an image in your document, the syntax is as follows.
![Photo of a panda](url/to/panda.jpg)
As with links, you can include an optional title attribute for the image.
![Photo of a panda](url/to/panda.jpg "Your title here")
The same applies to reference-style syntax: it's exactly the same as for links, but with the addition of the exclamation-mark before the first set of square brackets.
![Photo of a panda][panda] [panda]: url/to/panda.jpg
As with links, optional title attributes can be added to reference-style images too.


De meer geavanceerde zaken
--------------------------

With the basics of Markdown in hand, you're ready to create documents of just about any kind. For those interested in getting their hands dirty with more advanced usage scenarios, this chapter will touch on some slightly more esoteric topics.

...

### Literals and escaping

### Using HTML alongside Markdown

### Code

If you're a programmer, you may want to include code in your documents. HTML provides two tags that are useful in this scenario – PRE and CODE – and Markdown has a handy shorthand to use them for code samples. Simply indent each line of code by at least four spaces, or one tab.
This is a normal paragraph.
And this is a code block.

GitHub Flavoured Markdown
-------------------------


