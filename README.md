# um-thesis

Template for a Ph.D. thesis at the University of Michigan. The template is based on the Komascript ```scrbook``` class and is intended to be a modern, lightweight, and customizable alternative to the different ```rac.sty```-based classes. 

## Features
 - Follows [Rackham requirements](http://www.rackham.umich.edu/content/formatting-dissertation)
 - List of acronyms (```glossaries``` package)
 - List of appendices
 - Clutter-free main files
 - Easy font selection

## Compilation

The recommended tex environment is [TexLive](https://tug.org/texlive/). If you don't have the full installation, some packages might have to be installed manually to compile the template:

	tlmgr install xelatex xstring todonotes bezos chngcntr xpatch doublestroke glossaries mfirstuc xfor biblatex tikz pgfplots

The template can be compiled with latexmk using [settings](http://ctan.mirrors.hoobly.com/support/latexmk/latexmk.pdf) defined in ```.latexmkrc```. The default compiler is ```xelatex``` (to use ```pdflatex``` the ```fontspec``` package must be removed in ```preamble.tex```).

	latexmk um-thesis.tex

Alternatively, use an environment like Sublime Text + LatexTools that relies on ```latexmk``` for compilation.

## Configuration

The Koma-Script Bundle is highly customizable, see the [Koma-Script guide](http://texdoc.net/texmf-dist/doc/latex/koma-script/scrguien.pdf) for detailed descriptions.

### Fonts

Fonts are handled with ```fontspec```, the main font can be changed in ```preamble.tex``` by e.g. uncommenting ```\setmainfont{Times New Roman}```. For finer control, use the ```\setkomafont``` commands (for a full list see Chapter 3.6 of the Koma-Script Guide).

## Acknowledgement

The title page template is taken from the [thesis-umich.cls](http://www-personal.umich.edu/~dalle/codes/thesis-umich/downloads/thesis-umich.cls) derivation of ```rac.sty```.
