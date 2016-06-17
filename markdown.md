Markdown leren schrijven
========================

Dit document legt uit wat Markdown is en hoe je het gebruikt. Het is zelf volledig in Markdown geschreven, je kan het dus ook als voorbeeld gebruiken.

Wat is Markdown?
----------------

Markdown is een tekstformat waarmee je documenten kan maken.

### Wat kan Markdown voor jou betekenen? 

1. An easy-to-learn plain text formatting syntax, and:
2. A tool to convert that text into various rich formats, particularly HTML.
lets you use plain text formatting conventions that you've probably already seen a hundred times – and perhaps even use yourself – to make documents that are not only clean and readable as-is, but which can also be readily converted into HTML and other rich formats.
Markdown is logical, simple, and uses just a few punctuation symbols to format text. It's based, in part, on how people tend to format plain text emails, and its overriding goal is to be readable at all times.
Markdown was created by John Gruber, and the first release was in 2004. There's no single definitive standard for Markdown (besides John's), but for the most part, everything is compatible. There are various versions of Markdown out there, many of which add new features, but the core functionality is the same everywhere.
If you've ever wanted to keep your writing (whether it's articles, documentation, blog posts, or anything else) in a plain-text, portable format, but also be able to convert it when needed to richly-styled HTML, Markdown is for you.

### Waarom zou je het gebruiken?

lets you write in a way that's readable and natural, regardless of the tools available to you at the time. Markdown files are just text files, so they're easily portable and usable as they are – but they can also readily be converted to a rich format like HTML.
Markdown is widely supported in blogging systems (including WordPress, Movable Type, Jekyll, and more), and most modern text and code editors support it too.
More to the point, you've probably already used Markdown, without being aware of it. If you've ever emphasised something *like this*, you've used Markdown. If you've ever made a list by starting each line with a hyphen, or asterisk (or a number), you've used Markdown. If you've ever made a horizontal line using a series of asterisks or hyphens, you've used Markdown.
That's the real beauty of it: Markdown uses common, plain-text shorthand that most of us are already familiar with, and lets you do new things with it. Whether you're writing a shopping list, a blog post, documentation for your code or designs, or even a whole book, Markdown can help.

De basis: vaak voorkomende Markdown syntax
------------------------------------------

### Paragrafen

Komen van alle elementen eigelijk het vaakst voor. Ze hebben dan ook geen enkele bijzondere formatting nodig. they're just one or more consecutive lines of text, just like in an email, or any plain text file. Blank lines separate paragraphs, and you can use any number of blank lines together. (Blank here means "looks blank": lines full of just whitespace are considered to be blank, just like totally empty lines.)
f you want to hard-wrap your paragraphs (i.e. have line-breaks in them), go right ahead; Markdown ignores line-breaks within paragraphs, just like web browsers do when interpreting HTML to render web pages.
If you do want to force an actual line-break, just make sure that the line ends with two or more spaces – in Markdown's HTML output, they'll be converted into a line-break (BR) tag.
  
Dit is de eerste paragraaf. We kunnen hem zo lang maken als we zelf willen. Er is geen enkele Markdown formatting nodig.

En dit is een tweede paragraaf.

### Hoofdingen

Any document needs headings, and HTML provides for six main levels of them. Markdown supports headings using two different kinds of syntax, which you can mix-and-match freely.
The first kind is the underlined, or setext-style heading. To create one, you take a new line after the actual text of your heading, and then "underline" it by typing either a series of equals- signs (for first-level headings), or hyphens (for second-level) at the start of the line.

```
This is a first-level heading 
=============================

This is a second-level heading 
------------------------------
```

You can use any number of underlining characters, as long as there's at least one.
The second style lets you specify all six possible heading levels used by HTML. It's the
prefixed, or atx-style heading. To create one, you put one or more consecutive hash symbols immediately before the text of your heading, at the start of the same line. The number of hash symbols determines the heading level.

# This is a first-level heading
### This is a third-level heading

Whitespace between the hash symbols and the heading's text is optional, like so much in Markdown. Use whichever style suits you best.
If you're using prefixed headings, feel free to also put any number of hash-symbols after the heading's text, on the same line: they'll be ignored, and stripped out if you convert your Markdown document to HTML. Some people prefer the visual balance of having them on both sides, but only the initial ones (before the text) determine the heading level.

### Lijsten

If you guessed how to make lists in Markdown, you'd almost certainly be right. Both bulleted and numbered lists are supported. Bulleted lists can start with either hyphens, asterisks, or plus signs, and you can mix those if you want to.
- This is item one - This is item two
Numbered lists, unsurprisingly, use numbers – and remember to put a period after them.
1. This is item one. 2. This is item two.
You'll also need at least one space after the list marker (the hyphen or asterisk or plus sign for unordered lists, or the number and period for ordered lists). The actual numbers you use for numbered lists don't matter; if you convert your Markdown document to HTML, the lists will start at 1, and increase by 1 each time.
Lists have a couple of interesting properties, compared to other block elements. Firstly, while you'll normally start them at the left margin (the beginning of the line), you can add up to three spaces before each item if you so desire, to make the lists look indented in your Markdown document.
Secondly, if you leave blank lines between each list item, when your Markdown is converted to HTML, you'll get a paragraph (P) tag around each item, but you won't if there are no blank lines between each one. Whether that's useful is up to you.
Lastly, you can have multiple paragraphs of text within a list item: all you need to do is make sure that each subsequent paragraph of a list item is indented by four space, or one tab.

- This is item one, paragraph one.
And this is the second paragraph of item one.
- This is item two.
Once again, just do what seems intuitive for a plain text file, and it'll usually show up just as you expect.

### Horizontale lijnen

To visually split up sections of a document, there's nothing quite as satisfying as a horizontal line – like the HR tag in HTML. Markdown lets you create horizontal lines using three or more hyphens, asterisks, or underscores, on their own line.

* * *
- - - - - -

You can put spaces between the characters if you prefer.

### Blockquotes

If you've ever used plain text email – and I hope you have – then you'll be familiar with the practice of quoting sections of a message in your reply, using the ">" character. Markdown uses exactly the same idea for blockquotes. For the most visually pleasing results, you should put a ">" before every quoted line.
> This is a blockquote. There's some text here,
> and some more text here. There's even a bit
> of additional text just here. >
> This is the final quoted line of text.

Alternatively, you can just put the ">" before the first line of each quoted paragraph, and
Markdown will still do the right thing.

> This is a blockquote. There's some text here, and some more text here. There's even a bit
of additional text just here.
> This is the final quoted line of text.
You can use other block elements, like headings, lists, and so on inside a blockquote, and you can even nest one blockquote inside another.

### Benadrukken

Besides block-level elements, there are also a few common inline elements you may want to add to your document. The first of these is emphasis. There are two sorts of emphasis: the one that most of us would call italics (more properly an EM tag, in HTML), and the one we'd call boldface (a STRONG tag, in HTML).
To create EM-type emphasis, you simply surround a word or phrase with a pair of single underscores or asterisks.
This is an example of italic _emphasis_.
And *so is this*.
You must begin and end the emphasised section with the same character, but it doesn't matter which one you use. You can mix and match pairs of the same character in the same document, naturally.
To create STRONG-type emphasis, you use pairs of two underscores or asterisks instead. This is an example of boldface __emphasis__.
And **so is this**.
You can even use emphasis in the middle of words, if you like.

Absolutely **un**believable

Documents are most readable if you pick one set of characters to use for single-pair (italic) emphasis, and the other set of characters for double-pair (boldface) emphasis – but it's your choice.

### Links

The next type of non-block element you'll often want to use is links. Markdown lets you write links in a variety of ways, falling into two main categories: inline, and reference. When you convert your Markdown document to HTML, the links will become proper hyperlinks. Links in Markdown are specified using square brackets for the linked text. In the case of inline links, the square-bracketed section is followed by round brackets (parentheses) for the URL.

[Apple's web site](http://www.apple.com/)

Either relative or absolute URLs are supported. You can also specify an optional title attribute for the resulting link, which most browsers show as a tooltip when the mouse pointer hovers over the link.

[Apple's web site](http://www.apple.com/ "Buy yourself a Mac")

Inline links are useful, but they're also verbose, and some people feel that they look messy. They also spread URLs throughout your document. If you'd prefer to separate the URLs from the linked text – almost like a footnote – you can instead use the reference style of Markdown links.
For reference links, instead of the URL in parentheses, you use a second set of square brackets containing a unique label for the URL.
[Apple's web site][apple]
You can add a space between the two sets of square brackets if you prefer. You then have to define which URL the label actually refers to, and you can do that anywhere at all in the same document.
[apple]: http://apple.com/
Again, you can add an optional title attribute for the link, if you want.
[apple]: http://apple.com/ "Buy yourself a Mac"
The optional title attribute can be enclosed in single or double quotes, or even parentheses. You can also optionally enclose the URL in angle brackets ("<" and ">"). You can also put the title attribute on the next line, and indent it, if you feel it's more readable that way.
The actual label itself is only used to tell Markdown which URL belongs with which link; it won't appear in the resulting HTML. Labels can have spaces, letters, numbers, and punctuation if necessary. They're not case sensitive.
Lastly, you can use implicit link labels, in reference links. This means that the actual linked text (inside the first set of square brackets) is also used as the label, and the second set of square brackets can thus be left empty.
Visit the [Apple][] site to buy a Mac.
[Apple]: http://www.apple.com/
Markdown's goal is to be readable at all times, and to let you make plain text documents that are as understandable as the HTML versions that they can be converted to. Reference links tend to be much cleaner to read if you have many links interspersed throughout some text.
As always, you can mix and match all varieties of inline and reference links as you please.

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

