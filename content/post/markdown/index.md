---
title: Markdown
subtitle: Article about Markdown markup language.

# Summary for listings and search engines
summary: Article about Markdown markup language.

# Link this post with a project
projects: []

# Date published
date: '2022-05-14T00:00:00Z'

# Date updated
lastmod: '2022-05-14T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit [**Unsplash**](https://unsplash.com/photos/J5yoGZLdpSI)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## Article

This document is intended to familiarize the user with the functionality of the Markdown markup language.
Markdown is a lightweight markup language that is a tool for converting code to HTML.
The main feature of this language is the simplest syntax, which serves to simplify writing and reading markup code, which, in turn, makes it easy to correct it.
Now let's take a closer look at the functions of the Markdown markup language.  

Markdown is not a replacement for HTML. The Markdown syntax is quite limited, and corresponds to only a small subset of HTML elements. It includes the following elements:

1. Block elements
+ [Paragraphs and Line Breaks](#Parag);
+ [Headers](#Headers);
+ [Quotes](#Blockquotes);
+ [Lists](#Lists)
+ [Code Blocks](#CodeBlocks);
+ [Horizontal (dividing) lines](#Lines).
2. Lowercase elements
+ [Links](#Links);
+ [Text Selection](#Emphasis);
+ [Code fragments of strings](#Code);
+ [Images](#Images).
3. Additional elements
+ [Backslash](#Backslash Escapes);
+ [Automatic Links](#Automatic Links);
+ [HTML Special Characters](#SpecialSymbol).  

For more information about the listed functions, see the section "Syntax Description".

SYNTAX DESCRIPTION
=========================

Block elements
--------------------------

##### <a name="Parag"></a> Paragraphs and line breaks
In order to create a paragraph using the syntax of the Markdown language, it is enough to separate the lines of text with one (or more) empty line (any line that contains nothing but spaces and tab characters is considered empty).
In order to insert a visible line break (the `<br/>` element), you must end the line with two spaces and press the "Enter" key.
Many elements of the Markdown syntax look and work much better when they are formatted using "hard line translation" (line separation performed by the user himself, and not by the program automatically). Such elements include quotes, lists, etc.  

##### <a name="Headers"></a> Headings
The Markdown markup language supports 2 styles of heading designations: underlining and highlighting with a symbol ("#").
Headings are highlighted using underscores with equal signs ("=") if the title is of the first level, and hyphens ("-") if the title is of the second level. The number of underscores is not limited.
When selecting headers using the symbol ("#"), from one to six of these characters are used, which are set at the beginning of the line (before the header). In this case, the number of characters corresponds to the header level. In addition, it is possible to provide the title with closing characters ("#"), although this is not mandatory. The number of closing characters does not have to match the number of initial characters. The level of the header is determined by the number of initial characters.  
The headings of the first and second levels, made using underscores, look like this:

    First level header
    ========================
    Second level header
    -------------------------

The headers of the first, third and sixth levels, made using the symbol ("#"), look like this:

    # The header of the first level
    ### Third level header
    ###### Sixth level header
The above headings made with the symbol ("#") are identical to the following:

    # First level header #
    ### Third level header ###
    ###### Sixth level header ######
As a result, the following is displayed on the screen:

First level header
========================

Second level header
------------------------

# First level header
### Third level header
###### Sixth level header

##### <a name="Blockquotes"></a> Quotes
The Markdown language uses the "more" (">") sign to indicate quotations. It can be inserted both before each line of the quotation, and only before the first line of the paragraph.
Also, the Markdown syntax allows you to create nested quotes (quotes inside quotes). Additional levels of citation marks (">") are used to mark them.
Quotes in Markdown can contain all kinds of markup elements.
Quotes in the Markdown language look like this:

    >This is an example quote,
    >in which
    >an angle bracket is placed before each line.

    >This is an example quote,
    in which the angle bracket
    it is put only before the beginning of a new paragraph.
    >The second paragraph.

Embedding a quote into a quote looks like this:

    > First Citation level
    >> Second level of citation
    >>> Third level of citation
    >
    >First Citation level
As a result, the following is displayed on the screen:

>This is an example quote,
>in which before each line
>an angle bracket is placed.

>This is an example of a quote
in which an angle bracket
is placed just before the beginning of a new paragraph.

>The second paragraph.

Enclosed quote:

> First Citation level
>> Second level of citation
>>> Third Citation Level
>
>First Citation Level


The citation level cannot exceed the 15th.  

##### <a name="Lists"></a> Lists
Markdown supports ordered (numbered) and unordered (unnumbered) lists.
Markers such as asterisks, pluses and hyphens are used to form unordered lists. All the listed markers can be used interchangeably.
To form ordered lists, numbers with a dot are used as markers. An important feature in this case is that the numbers themselves, with which the list is formed, are not important, since they do not affect the output HTML code. No matter how the user numbers the list, the output will in any case have an ordered list starting with one (1, 2, 3 ...). This feature should be taken into account when it is necessary to use the ordinal numbers of elements in the list so that they correspond to the numbers obtained in HTML.
Ordered lists should always start with one. List markers usually start from the beginning of the line, however, they can be shifted, but not more than 3 spaces. The marker must be followed by a space or a tab character.
If necessary, you can insert a quote into the list. In this case, the citation notation (">" ) should be indented.
The ordered lists look like this:

    1. Explorer
    2. Semiconductor
    3. Dielectric

The unordered lists look like this:

    * Explorer
    * Semiconductor
    * Dielectric

Or

    - Guide
    - Semiconductor
    - Dielectric

Or

    + Explorer
    + Semiconductor
    + Dielectric
The output of all three listed options has the same result.
As a result, the following is displayed on the screen:

1. Explorer
2. Semiconductor
3. Dielectric

and

+ Explorer
+ Semiconductor
+ Dielectric

The quote inserted into the list looks like this:

    1. A list item with a quote:

	> This is a quote
	> inside the list item.

    2. The second item of the list

As a result, the following is displayed on the screen:

1. A list item with a quote:

    > This is a quote
    > inside the list item.

2. The second item of the list


When inserting quotes into the list items, it is important to keep in mind that the list items must be on the same level, and quotes must be indented. If the rule with a single list level is not followed, the next item in the list after the quote will be automatically numbered with the digit "1."
In addition, if necessary, you can insert the source code into the list. In this case, it should be written with double indentation – 8 spaces or 2 tab characters.

- A list item containing the source code

		<source code >

##### <a name="CodeBlocks"></a> Code blocks
Formatted code blocks are used when it is necessary to quote the source code of programs or markup.
To create a block of code in the Markdown language, it is necessary to start each line of a paragraph with an indent consisting of four spaces or one tab character. The code block continues until there is a line without indentation (or the end of the text). Inside the code block, ampersands ("&") and angle brackets ("<" and ">") are automatically converted into HTML markup elements. In addition, it should be noted that inside the code blocks, the usual Markdown syntax is not processed.
The code block in Markdown looks like this:

This is a regular paragraph:

	This is a block of code

##### <a name="Lines"> </a> Horizontal lines (separators)

In order to create a horizontal line using the Markdown syntax, you need to place three (or more)a hyphen or asterisk on a separate line of text. It is possible to place spaces between them.
Horizontal lines in Markdown look like this:

    The first part of the text to be divided
***
    The second part of the text that needs to be divided

Or

    The first part of the text to be divided

    ---

    The second part of the text that needs to be divided
As a result, the following is displayed on the screen:

The first part of the text to be divided
***
The second part of the text that needs to be divided  

When using this tool, it is important to remember that an empty line must be left after the first part of the text and before the second. This rule must be observed only when using hyphens. If it is not followed, the second-level header and a line of plain text will be displayed on the screen.  When using the asterisk symbol, this rule can be ignored.  

 Lowercase elements
-------------------  

##### <a name="Links"></a> Links
Markdown supports two styles of link design:

 - Hyperlink, with immediate indication of the address (in-text);
 - A hyperlink similar to a footnote.

It is assumed that in addition to the URL, there is also a link text. It is enclosed in square brackets. 
To create an in-text hyperlink, you must use parentheses immediately after the closing square one. You need to put a URL inside them. It is also possible to place the name enclosed in quotation marks in them, which will be displayed when hovering, but this item is not mandatory. 
 
      [example](http://example.com / "Optional hint")
As a result, the following is displayed on the screen:
[example](http://example.com / "Optional hint")
When referring to a local directory, it is possible to use a relative path (from the current page, site, etc.)  

When creating a passable hyperlink, a second pair of square brackets is used instead of the target address, inside which the label, the link identifier (id) is placed.

    [example][id]:
Also, you can use a space to separate 2 pairs of square brackets: 

    [example] [id]: 

In this case, it is possible to determine the identifier anywhere in the document.: 

    [id]: http://example.com / "Optional hint"

As a result, the following is displayed on the screen:
[example] [id] 
[id]: http://example.com / "Optional hint"
In other words, it consists of the following elements:

 - Link ID surrounded by square brackets (which may be preceded by an optional indentation from one to three spaces);
 - Colon;
 - One or more spaces (or tab characters);
 - Hyperlink URL;
 - Optional title (a hint to the image that pops up when you hover over it) of the hyperlink, enclosed either in double or single quotes, or in parentheses.

Link identifiers can consist of letters, numbers, spaces, and punctuation marks, but they are not case sensitive. That is, these two options are equivalent:

    [link text][a]
    [link text][A]
Markdown also allows you to use an implicitly expressed identifier (abbreviated). In this case, the label is not given, instead the hyperlink text is used as its name, and the second pair of square brackets remains empty.
For example, to make the word "Example" a hyperlink leading to the site <http://example.com/>, it is enough to write:

    [Example][]
and then define the hyperlink:

    [Example]: http://example.com/
As a result, the following is displayed on the screen:
[Example][]
[Example]: http://example.com/  

##### <a name="Emphasis"></a> Text selection
Markdown perceives asterisks "*" and underscores "_" as signs of semantic text selection:

 - Text surrounded by single "*" or "_" will be enclosed in the HTML tag `<em>`.
 - Text surrounded by double "*" or "_" will be enclosed in the HTML tag `<strong>`.

In other words, text surrounded by single characters is highlighted in italics, and text surrounded by double characters is highlighted in bold. 
Also, the selected fragment can be located in any part of the word. 
The text in italics using the Markdown syntax looks like this:

    *Example*  
*Example*  

The text in bold using the Markdown syntax looks like this:

    **Example**
**Example**  

The text in italics in bold using the Markdown syntax looks like this:

    ***Example***
***Example***

All the above examples are similar to the following:

    _example_

    __example__

    Re___distribution___division

    ___example___  

##### <a name="Code"></a>	Code fragments of strings
To mark a line fragment containing the code, it is necessary to surround it with reverse apostrophes "`".  When using code fragments of strings, the text will be displayed as a monospaced font. 
Unlike code blocks, a code fragment allows you to put the code inside a regular paragraph of text.
The code fragment of a string in the Markdown language looks like this:

Use the `if` operator  

##### <a name="Images"></a>	Images
There are 2 ways to insert images into a document in Markdown:

a. By directly specifying the URL of the image. The syntax of this command is as follows:

    ![Alternative text](/path/to/image.jpg)
or

    ![Alternative text](/path/to/image.jpg "Hint")
In other words, it consists of the following elements:

 - exclamation mark;
 - square brackets, which indicate the text alternative to the image (it will become the content of the attribute in the img element);
 - parentheses containing the URL or relative path of the image, as well as (optionally) a tooltip enclosed in double or single quotes.

b. Using an identifier label.  The syntax of this command is written as follows:

    ![Alternative text][id]
where "id" is the name of a specific image label. Image labels are defined using a syntax that is completely identical to hyperlink labels:

    [id]: path/to/image "Optional hint"
An important feature is that Markdown does not allow you to set image dimensions (width, height).  

 Additional elements
-------------------------  

##### <a name="Backslash Escapes"></a>	Backslash
It can be used in Markdown before special characters so that they are perceived in their literal (and not official) meaning. The full list of these symbols is given below:

"\" - slash;  

"`" - reverse apostrophe;  

"*" - asterisk;  

"_" - underscore character;  

"{}" - curly brackets;  

"[]" - square brackets;  

"()" - parentheses;  

"#" - grid symbol;  

"+" - plus;  

"-" - minus (hyphen);  

"." – period;  

"!" is an exclamation mark.  

##### <a name="Automatic Links"></a> Automatic links
Markdown supports a simplified procedure for automatically creating links for URLs and email addresses. To do this, just put the URL or postal address in angle brackets, and Markdown will make it a hyperlink. Unlike the styles described above, in this case the URL or postal address itself becomes the hyperlink text. Automatic links to email addresses work similarly.
Automatic links in the Markdown language look like this

    <http://example.com/>
As a result, the following is displayed on the screen:
<http://example.com/>

The automatic link to the email address in Markdown looks like this

    <address@example.com>
As a result, the following is displayed on the screen:
<address@example.com>  

##### <a name="SpecialSymbol"></a> HTML special characters
There are two characters in HTML that require special consideration: these are the characters ("&lt;") and ("&amp;"). The left angle bracket is used as the beginning of the tag; ampersands are used to indicate a special HTML character.
In order to use these characters in their literal sense, it is necessary to replace them with HTML elements, namely `&lt;` and `&amp;` accordingly.
When using Markdown, you do not need to perform such actions. It allows you to use these characters in their original form. If the ampersand is used as part of the HTML special character, it will remain unchanged. Otherwise Markdown will convert it to `&amp;`.
<br>
--------<br>
copyright: https://gist.github.com/Jekins/2bf2d0638163f1294637#file-markdown-docs-md
