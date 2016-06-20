

# Markdown schrijven

Dit document legt uit wat Markdown is en hoe je het gebruikt. De tekst is zelf volledig met Markdown opgemaakt. Dit is versie 1.0, initieel geschreven door Kristof Michiels op 17 juni 2016.


## Wat is Markdown?

Met Markdown voorzie je je teksten in een mum van tijd van een prachtige opmaak. Je doet dit met behulp van een set opmaak-codes. Markdown is heel snel te leren. De codes zijn helder, logisch en hinderen de leesbaarheid van de tekst niet. Je van Markdown voorziene tekst kan automatisch omgezet worden naar een hele reeks andere formaten (zoals pdf of html).  

Met Markdown houd je al je documenten in een draagbare simpele tekstvorm. Je kan er alles mee schrijven, gaande van shopping lijstjes tot blogposts, documentatie voor je code of designs, tot zelfs hele boeken. 

Ik schrijf zo goed als al mijn teksten in Markdown. De tools die ik hiervoor gebruik: de teksteditor Atom of GitHub zelf. Er bestaan op elk platform een groot aantal toepassingen die schrijven in Markdown ondersteunen. Ook blogsystemen als WordPress of Jekyll kunnen overweg met in Markdown geschreven posts of pagina's.  

Een handige tool om te leren werken met Markdown is [StackEdit](https://stackedit.io/). Ik sla mijn geschreven documenten allemaal op in GitHub, zodat ik ze nooit kan kwijtraken en kan delen met de wereld. Deze teksten kunnen eenvoudig worden omgezet in mooie PDFs via [Gitprint](https://gitprint.com).

Markdown is ontwikkeld door John Gruber in 2004. Op [zijn site](https://daringfireball.net/projects/markdown/) vind je de originele en zeer nuttige referentie van Markdown. In realiteit zijn er in de laatste jaren verschillende versies bijgekomen. De basisfunctionaliteit is in elke variant dezelfde, maar ze voegen allemaal extra notaties toe. Ik bespreek straks nog even de extra zaken die je vind in het zogenaamde GitHub flavoured markdown.

Hieronder zie je een voorbeeld van hoe eenvoudig Markdown je documenten van opmaak voorziet. 

```
# Mijn titel

Hier komt een paragraaf met **benadrukking** in de tekst.
Deze tekst maakt deel uit van mijn paragraaf.

- Dit is een lijstelement
- Dit is ook een lijstelement
- Dit tenslotte is ook een lijstelement
```

## De basis: Markdowns meest gebruikte codes

### Paragrafen

Paragrafen komen van alle elementen het vaakst voor en hebben in Markdown geen enkele bijzondere formatting nodig. Je schrijft gewoon je paragraaf en laat deze voorafgaan en eindigen op een lege lijn. Indien je ergens in je paragraaf tekst op een nieuwe regel wil doen beginnen dan laat je de regel erboven eindigen op minstens twee spaties.

```
Dit is de eerste paragraaf. We kunnen hem zo lang maken als we zelf willen.   
Deze regel staat op een nieuwe lijn omdat ik de vorige zin heb laten eindigen op 2 spaties.

En dit is een tweede paragraaf.
```

### Hoofdingen

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

Mijn advies: gebruik uitsluitend de manier met de hashtags. Laat ook minstens één lijn leeg achter elke hoofding. Voor de hoofding is het verstanding bvb drie regels open te laten voor een hoofding van het eerste niveau (één #), twee regels open te laten voor een hoofding van het tweede niveau (2 #'s) en één regel open te laten voor een hoofding van het derde niveau (3 #'s).

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
Als je een witregel open laat tussen elk lijstelement, dan zal in html elk lijstelement in een paragraaf worden gewikkeld. Het is verstandig dit consequent te doen en steeds een witregel tussen de lijstelementen te laten indien elk lijstelement meerdere regels beslaat.

### Horizontale lijnen

Een horizontale lijn voeg je toe door drie of meer strepen, sterretjes of underscores op een eigen regel te plaatsen. Deze tekens mogen (maar niet verplicht) gescheiden zijn door een spatie.

```
* * *
- - - - - -
```

Laat minstens twee witregels tussen voor en na een horizontale lijn. Zo blijft de tekst ook als Markdown beter leesbaar.

### Blok-aanhalingen

Aanhalingen of block quotes maak je met een groter-dan-teken (>). Je kan een groter-dan teken te plaatsen op elke regel, maar je kan je evengoed ook beperken tot één per paragraaf. Uiterst eenvoudige manier om bepaalde paragrafen in je tekst te benadrukken.  

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

Een tip: gebruik enkele underscores voor schuingedrukte benadrukkingen en dubbele sterretjes om iets vet te drukken. Dit verhoogt de leesbaarheid van de tekst in de teksteditor.

### Links

Links kan je in Markdown op verschillende manieren weergeven. De meest voorkomende zijn inline links. De gelinkte tekst staat hier tussen vierkante haakjes en de URL tussen haakjes. Je kan indien je dit wenst ook een titel-attribuut koppelen aan de link.

```
[Mijn website](http://kristo.fm)

[Mijn website](http://kristo.fm/ "Thuisplek voor interessante webdesign tutorials")

```

Indien je de links wil splitsen en op één plaats oplijsten kan je de referentie-manier van noteren gebruiken. Je geeft elke link dan een uniek label, tussen een tweede set vierkante haakjes geplaatst. Ergens op hetzelfde document (maakt niet uit waar) dien je dan nog het label te beschrijven. Markdown doet dan de rest, want het eindresultaat ziet er hetzelfde uit als met inline links. Ook hier kan je optioneel een titel-attribuut toevoegen aan de link. Zorg in elk geval dat de labels verzorgd en betekenisdragend zijn. Anders wordt het al snel een soep.

```
[Kristofs web site][kristofm]
[AP hogeschool][ap]

...

[kristofm]: http://kristo.fm/ 
[ap]: http://www.ap.be "Artesis Plantijn hogeschool Antwerpen"
```

### Afbeeldingen

Je kan ook afbeeldingen toevoegen aan je documenten. Deze zijn uiteraard niet zichtbaar in de text-editor, maar uiteraard wel na export naar een ander formaat. De syntax is heel gelijkaardig aan die van links en ook hier zijn er twee varianten (inline en referentie), met twee kleine verschillen: 
- Om aan te geven dat het om een afbeelding gaat en niet om een link plaats je een uitroepteken voor de vierkante haakjes.
- De tekst binnen de vierkante haakjes wordt gebruikt als ALT tekst voor de image-tag.

De standaard inline-versie:

```
![Beschrijving van een foto](url/naar/de/foto.jpg)

![Beschrijving van een foto](url/naar/de/foto.jpg "Je titel komt hier")
```

De referentie-versie:

```
![Beschrijving van een foto][foto] 

...

[foto]: url/naar/de/foto.jpg
```


## Meer geavanceerde Markdown

### Markdown-codes letterlijk weergeven, ofte "escaping"

Speciale markdown-karakters die je niet geïnterpreteerd wil zien worden kan je letterlijk laten afdrukken door er een "\" voor te plaatsen:

```
Deze tekst zal \_niet\_ benadrukt worden.
```

Markdown zal ook automatisch twee karakters escapen die bijzondere betekenis hebben in HTML: kleiner dan "<" en de ampersand "&". Normaal zou je "<" en ">" moeten schrijven als "&lt;" and "&amp;" om helemaal juist te zijn, maar Markdown is slim genoeg om dit voor jou te regelen.

### HTML gebruiken binnen Markdown

Je kan zonder problemen HTML mengen in je van Markdown voorziene tekst. Er zijn wel enkele regels. 1) Block level elementen zoals <div> en <p> moeten omgeven zijn door een witregel. Minstens één lege regel voor de openingstag en minstens één witregel na de afsluitende tag. 2) De openingstag en afsluitende tag mogen niet inspringen. Ze moeten m.a.w. op het begin van de regel beginnen.
Onthou ook dat hoewel je Markdown codes mag gebruiken binnen HTML tags op span-niveau, dit niet het geval is binnen block-niveau tags.

```
<p>
Binnen deze HTML block, zullen **deze sterretjes** niet benadrukt worden.
</p>
```

### Code schrijven

Als je programmeert, dan wil je code kunnen toevoegen aan je documenten. HTML voorziet ons hier van twee tags die nuttig zijn, namelijk \<pre\> en \<code\>. and Markdown has a handy shorthand to use them for code samples. Simply indent each line of code by at least four spaces, or one tab.
This is a normal paragraph.
And this is a code block.

You can add further indentation, which is very useful for code listings, and it'll behave as you'd want. Markdown syntax is ignored within code blocks, so you don't need to worry about escaping characters either.
In some cases, you might also want to mention code within the context of a regular paragraph of text, without having to use a whole separate code block. Markdown uses the "`" (backtick) character for this.
Type `uptime`, and press Return.
If you need to include a literal backtick character within an inline code span, you can surround the span in multiple backticks instead of single ones.
Markdown uses the ``backtick (`)`` character for inline code.
You can add spaces inside the backtick delimiters if you need to have a literal backtick at the start or end of the code span. As with code blocks, special HTML characters are automatically escaped, and Markdown syntax is ignored.

### Automatische links

Markdown provides a useful feature for when you want to link to a URL, and just use the URL itself as the linked text; this feature is called automatic links. To use it, just surround any URL with angle-brackets, and it'll become a link when your document is converted to HTML.
You can buy a Mac at <http://www.apple.com>.
Automatic links also work for email addresses, with or without the "mailto:" protocol.



## GitHub Flavoured Markdown (GFM)

Link: https://help.github.com/articles/github-flavored-markdown

Strikethrough ~~stijl~~
[x] Taaklijsten
Auto-hotlinking
Fenced codeblocks
Tables

Hoofding 1 | Hoofding 2
-----------|------------
content    | content
content    | content
content    | content
content    | content

Centreren:
-----------:|:------------:|-------------:

Link: http://www.tablesgenerator.com/markdown_tables



Many of the alternate Markdown systems (like Kramdown, Redcarpet, Maruku, and Discount, to name but a few) were inspired by an enhanced version of Markdown written in the PHP programming language, called PHP Markdown Extra.
The various additions offered by PHP Markdown Extra also tend to be available in other, more recent Markdown systems. In this section, I'll give you a brief overview of some of those extra features.
Firstly, PHP Markdown Extra (et al, which I'll simply call "Extra" from now on) remove the restriction in standard Markdown about using Markdown syntax inside HTML blocks, using an attribute to indicate that Markdown syntax should be converted as usual.

<div markdown="1">
I can use Markdown-style _emphasis_ here now!
</div>
For those wanting to easily apply CSS styles to the HTML generated by Markdown, Extra allows specifying attributes for headers, links, images, and code blocks. The syntax uses curly brackets (braces), and custom attributes are supported too.
# This is a first-level heading {#main .content lang=en}
The above contrived example, when converted to HTML using Extra or any Markdown library that supported the same syntax, would produce the following output.
<h1 id="main" class="content" lang="en">This is a first-level heading</h1>
Attribute syntax can be used to give finer control over the generated output, without cluttering up your Markdown document with HTML tags.
If you often include code in your documents, Extra allows you to do so without worrying regular Markdown's requirement to indent each line of code by at least four spaces (or one tab).
Instead, you just begin and end your code block with a line containing three or more tilde ("~") characters, or backticks ("`"). This is called a fenced code block, because the row of tildes or backticks looks a bit like a fence.
~~~
Code goes here ~~~
You can also optionally specify a CSS class to apply to the resulting CODE tag, in the generated HTML.
~~~ .ruby
Code goes here ~~~
The attributes syntax described previously also works with fenced code blocks; the attribute-list in curly brackets goes after the first fence.
PHP Markdown Extra's syntax supports creating HTML tables visually in plain text, using the pipe ("|") character, and hyphens. Here's an example table.
First Name | Last Name -----------|---------- Matt | Gemmell
Lauren | Gemmell

The resulting HTML table will have a header row with header cells "First Name" and "Last Name", and a table body with two rows of content, as you'd expect. If you prefer, you can start and end each line of the table with a pipe character too.
You can use regular Markdown syntax within the content of each call of the table, and you can also specify each column's horizontal alignment by adding a colon (":") character in the separator line of hyphens, as shown below.
First Name | Last Name :----------|---------: Matt | Gemmell
Lauren | Gemmell
A colon at the start of a column's separator line will left-align the column (as in the "First Name" column above), and a colon at the end will right-align the column (as in "Last Name"). Use colons both at the start and end to centre-align a column.
PHP Markdown Extra also provides some features of interest to writers of long and/or technical documents. The first of these is footnotes, which use syntax very like reference-style links.
This is some text, with a footnote.[^1]
[^1]: And this is the footnote itself.
Footnote labels must be unique, and their definitions can be anywhere in the document. Definitions can be as long as you like; subsequent paragraphs should simply be indented by at least four spaces. In HTML output, footnote definitions will be assembled into a list at the end of the document.
Abbreviations are also supported, using the ABBR tag in HTML. Simply define an abbreviation anywhere in your document, with syntax similar to footnote definitions.
*[HTML]: Hyper Text Markup Language
Then whenever you use the term "HTML" anywhere in the document, it will be converted to an ABBR tag.
<abbr title="Hyper Text Markup Language">HTML</abbr>
No special syntax is needed to mark abbreviations; the presence of a definition somewhere in the document is sufficient.
There are a few other minor additions and tweaks to the standard behaviour in PHP Markdown Extra's syntax, compared to regular Markdown; as ever, be sure to read the documentation for the version of Markdown you're using.

