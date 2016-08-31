# Informatietechnologie 1: HTML5

## Introductie

### Wat is HTML?

HTML staat voor Hyper Text Markup Language.
HTML is wat we noemen een opmaaktaal. 
Dat is een verzameling van opmaak-tags - in dit geval HTML-tags - waarmee je web pagina's beschrijft.
Elke HTML-tag beschrijft een ander stukje inhoud van het document.

### Een eenvoudig HTML document

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Pagina-titel</title>
  </head>
  <body>
    <h1>Belangrijkste hoofding</h1>
    <p>Mijn eerste paragraaf.</p>
  </body>
</html>
```

Aan de hand van deze informatie zal de web browser een document tonen met hoofding en een paragraaf

Wat betekenen nu al die tags?
Met de <!DOCTYPE html> declaratie geef je aan dat het hier een HTML5 document betreft. De declaratie moet op deze plek staan en helpt de browser om de pagina correct te tonen.
De tekst tussen <html> en </html> beschrijft een HTML document.
De tekst tussen <head> en </head> geeft informatie over het document.
De tekst tussen <title> en </title> voorziet het document van een titel.
De tekst tussen <body> en </body> beschrijft de zichtbare informatie op de pagina.
De tekst tussen <h1> en </h1> beschrijft een hoofding.
De tekst tussen <p> en </p> beschrijft een paragraaf.


### Web browsers en HTML versies

Als web designer schrijf je HTML code. Dat is niet wat degene die naar je webpagina surft te zien krijgt. Deze persoon krijgt een visuele interpretatie van die pagina te zien. Wie maakt nu die vertaling van code naar visueel? Dat doet de web browser.

We kennen allemaal Web browsers. Je hebt keuze uit verschillende, afhankelijk je besturingssysteem: Chrome, Internet Explorer, Safari, Firefox. 

Wat doet een web browser? Hij leest en interpreteert een HTML document en toont de interpretatie aan de gebruiker.
De browser toont dus geen HTML tags, maar gebruikt de tags om het document visueel te kunnen tonen.

Met <!DOCTYPE html> geef je aan dat het hier een HTML5 pagina betreft. Dat is de laatste versie van de opmaaktaal. Hieronder vind je een overzicht van de versies en het jaar dat ze hun intrede hebben gedaan.

HTML	1991
HTML 2.0	1995
HTML 3.2	1997
HTML 4.01	1999
XHTML	2000
HTML5	2014

### HTML Tags

HTML tags are keywords (tag names) surrounded by angle brackets:

<tagname>content goes here...</tagname>
HTML tags normally come in pairs like <p> and </p>
The first tag in a pair is the start tag, the second tag is the end tag
The end tag is written like the start tag, but with a forward slash inserted before the tag name
The start tag is also called the opening tag, and the end tag the closing tag.

## HTML editors

Write HTML Using Notepad or TextEdit
Web pages can be created and modified by using professional HTML editors.

However, for learning HTML we recommend a simple text editor like Notepad (PC) or TextEdit (Mac).

We believe using a simple text editor is a good way to learn HTML.

Follow the four steps below to create your first web page with Notepad or TextEdit.

Step 1: Open Notepad (PC)
Open Notepad in Windows 8 or later:

Open the Start Screen (the window symbol at the bottom left on your screen). Type Notepad.

Open Notepad in Windows 7 or earlier:

Click Start (bottom left on your screen). Click All Programs. Click Accessories. Click Notepad.

Step 1: Open TextEdit (Mac)
Open TextEdit.

Please be sure that the text editor is set to plain text. Go to: Preferences > New Document > select plain text.

Also make sure both "Display html file as html code" and "Display RTF file as RTF code" options are checked under "Open and Save".

Then open a new document to place the code.

Step 2: Write Some HTML
Write or copy some HTML into Notepad.

<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>

<p>My first paragraph.</p>

</body>
</html>

Step 3: Save the HTML Page
Save the file on your computer. Select File > Save as in the Notepad menu.

Name the file "index.htm" and set the encoding to UTF-8 (which is the preferred encoding for HTML files).

Step 4: View the HTML Page in Your Browser
Open the saved HTML file in your favorite browser (double click on the file, or right-click - and choose "Open with").

The result will look much like this:
