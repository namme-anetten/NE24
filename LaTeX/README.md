# LaTeX

## What is in this Directory? 

### Derived from Lawrence Lewis's talk at UCB-THW in Spring 2014: 

There's a presentation, a document, and a poster (very alpha), which is meant to show the basics of LaTeX.

### Derived from Katy Huff's talk at UCB-THW in Fall 2014

There is some information here in the readme and there are some templates in 
the templates folder. 


## What is Markup?

### HTML

HTML is just hypertext markup language. It provides a plain text way to 
describe objects and data that are encountered in the world wide web. Things 
like urls, text rendering in webpages, etc. are all easy to describe in HTML.

### XML 

XML is the extensible markup language. It generalizes where others specify. In 
the way that all reductionist things fail to get the specifics right, XML is 
great for general tasks in programming (input files, etc.), but not great for 
writing documents, where the needs are very specific. 

### MarkDown? RestructuredText? Where does it end?

There are a lot of markup languages. They all do different things. Restructured 
text is the standard in the world of python documentation. Markdown is the 
standard on github. Pick your poison.


## How Do I install LaTeX?

### Linux

Everything in linux is simple.

    sudo apt-get install texlive

### OSX

You should use [MacTeX][mactex]. You can do this with macports or homebrew by downloading the whole shabang from 
the website.

### Windows

Installation is pretty straightforward using [ProTeXt](https://www.tug.org/protext/). ProTeXt will also give you a text editor (TeXStudio). Read the section underneath download and install, and once you have the distribution, it would be in your best interest to read the README before running setup.exe.

## How do I write LaTeX?

[The Not So Short Introduction to LaTeX2e](http://tobi.oetiker.ch/lshort/lshort.pdf)

### TeXmacs

[TeXmacs](http://www.texmacs.org/tmweb/home/welcome.en.html)  is a WYSIWYG editor fo LaTeX. It has plugins for 
many languages that allows it to be used as a notebook. Convenient autocomplete, but slightly different macros.
Like all \*macs it can be scripted in a lisp (TeXmacs scheme). It also has many european users.

### LyX

[LyX](http://www.lyx.org/)  is a WYSIWYG editor for LaTeX. That's 
awesome. I recommend you give it a shot.

### TeXShop

[TeXShop](http://pages.uoregon.edu/koch/texshop/) or [TexMaker](http://www.xm1math.net/texmaker/) or some others are
tools that many folks, including myself, use to write and render latex side by 
side. 
It's cool. It has tabcompletion, syntax highlighting, and some other useful features.

### Text Editors

Some folks will find the text editor option the most extensible and glorious. Katy Huff is
 one of those folks. She has a vim plugin for latex called, you guessed it, 
[vim-latex](http://vim-latex.sourceforge.net/) and it does most of the typing for her.
 With syntax highlighting, it tells her where there's a mistake and, by virtue of dealing 
directly with the content, she can ignore how it looks until the very end. It is functionally
like TeXShop, etc. but without seeing what's happeneing as you go.

## How do I pronounce LaTeX?

Check it out, the last letter is the Greek letter $$\Chi$$. So, it definitely has to 
end in a K sound. But, is it Lay or Lah? The developers say it's up to you. 

## What are the Parts of a Document?

LaTeX documents have numerous parts.

### The Preamble

In the preamble, there is a basic set of information that must be included in 
order to define the document. The real minimum set is just the "documentclass" 
parameter. Options include "article," "book," and "letter." Options concerning 
the paper format and the font can be specified in the square brackets while the 
documentclass type should be listed in the  

    \documentclass[11pt]{article}

inclusion of any packages that you rely on. Standard packages include 
"amsmath," "amsfonts," "amssymb," and graphicx. 

    \usepackage{amsmath}
    \usepackage{amssymb}

If you are expecting a title to appear, parameters such as author and title 
should be filled in. 




### begin and end

You must begin and end the document. 

    \documentclass[11pt]{article}

    \begin{document}

    <stuff>

    \end{document}


Now, that's it. To create a beautiful pdf, you can place this text in a file 
called doc.tex, type "latex doc.tex" to create a dvi file, then type dvi2pdf to 
create a pdf file.

### The Title Elements

There are elements that help to define the title elements. 


    \documentclass[11pt]{article}
    \author{The Hacker Within}
    \title{Our New Document}

    \begin{document}

    <stuff>

    \end{document}


Those variables are used by the maketitle command, which must be executed 
within the document boundaries. 


    \documentclass[11pt]{article}
    \author{The Hacker Within}
    \title{Our New Document}

    \begin{document}
    \maketitle

    \end{document}



### Books, Chapters, Sections, Subsections, Subsubsections, and Paragraphs

These are enviroments that define the hierarchy of your document. 


### Include and input

Rather than keep everything in one big file, you can include and input other 
latex files into a master. That acknowledgements section that you use in every 
paper? Keep it in its own file. 



[texSE]: http://tex.stackexchange.com/questions/41808/how-do-i-install-tex-latex-on-windows-7 "TeX Stack Exchange"
[mactex]: https://tug.org/mactex/ "mactex"
