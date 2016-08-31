# Informatietechnologie 1: HTML5

## Introductie

### Wat is HTML?

HTML staat voor Hyper Text Markup Language.
HTML is wat we noemen een opmaaktaal. 
Dat is een verzameling van opmaak-tags - in dit geval HTML-tags - waarmee je web pagina's beschrijft.
Elke HTML-tag beschrijft een ander stukje inhoud van het document.

### Een eenvoudig HTML document

```
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

The <!DOCTYPE html> declaration defines this document to be HTML5
The text between <html> and </html> describes an HTML document
The text between <head> and </head> provides information about the document
The text between <title> and </title> provides a title for the document
The text between <body> and </body> describes the visible page content
The text between <h1> and </h1> describes a heading
The text between <p> and </p> describes a paragraph
Using this description, a web browser will display a document with a heading and a paragraph.


Only the <body> section (the white area above) is displayed in a browser.

HTML pagina structuur: hier ook iets over zeggen

The <!DOCTYPE> declaration represents the document type, and helps the browser to display a web page correctly.

It must only appear once, at the top of the page (before any HTML tags).

There are different document types. To display a web page correctly, the browser must know both type and version.

The doctype declaration is not case sensitive.

### Web browsers en HTML versies

The purpose of a web browser (Chrome, IE, Firefox, Safari) is to read HTML documents and display them.
The browser does not display the HTML tags, but uses them to determine how to display the document:

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
