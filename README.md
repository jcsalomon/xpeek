`xpeek`: Define commands that peek ahead in the input stream
============================================================

The `xpeek` package provides tools
to help define commands that,
like the familiar `\xspace`
(from [`xspace`](http://ctan.org/pkg/xspace))
and the LaTeX command `\textit`,
“peek” ahead at what follows them in the command stream,
compare this token against a stored token-list,
and choose appropriate behavior.

The code is adapted from an answer posted to [TeX.SX][TeXSX] by
Enrico “egreg” Gregorio at <http://tex.stackexchange.com/a/59542/2966>.
Enrico, Joseph Wright, Bruno Le Floch, & Clemens Niederberger
helped iron out the implementation;
Bruno also wrote the initial version of the documentation
and the near-final version of much of the code.
See <http://tex.stackexchange.com/q/63568/2966>,
<http://tex.stackexchange.com/q/63971/2966>,
and <http://thread.gmane.org/gmane.comp.tex.latex.latex3/2894>.

Installation
------------

The most recently-released version of this package
will have been uploaded to CTAN at <http://ctan.org/pkg/xpeek>.
If you’re running an up-to-date version of TeX Live or MiKTeX,
you can install `xpeek` via the package manager.

For other systems, a [TDS][TDS]-compliant package may be downloaded at
<http://mirrors.ctan.org/install/macros/latex/contrib/xpeek.tds.zip>
or from <https://github.com/jcsalomon/xpeek/downloads>.

### Manual Installation

This package is developed as a standalone `.dtx` file,
packaged for the LaTeX3 project’s `l3docstrip`.
To produce the style file, run this command:

    pdflatex xpeek.dtx

Put the generated file `xpeek.sty` somewhere where TeX will find it.

This will also produce a version of the PDF documentation,
but with undefined references and without an index or change-log.
To get a more useful version of the documentation,
run these commands next:

    pdflatex xpeek.dtx
    makeindex -s l3doc.ist -o xpeek.ind xpeek.idx
    makeindex -s gglo.ist -o xpeek.gls xpeek.glo
    pdflatex xpeek.dtx
    pdflatex xpeek.dtx

These next commands are not strictly necessary,
since Acrobat Reader can generate & display thumbnails on-the-fly.
But since `l3doc` includes `hypdoc` which includes `thumbpdf`,
I may as well generate the pre-rendered thumbnails:

    thumbpdf xpeek.pdf
    pdflatex xpeek.dtx

Notice that the command for generating the index is different
from the one usually used for `ltxdoc`-documented packages;
that’s because I’m using the new (and experimental) package `l3doc`.

License
-------

Copyright © 2012 by Joel C. Salomon <joelcsalomon@gmail.com>.

This work consists of the file  `xpeek.dtx`,
          and the derived files `xpeek.ins`,
                                `xpeek.pdf`, &
                                `xpeek.sty`.
It may be distributed and/or modified under the conditions of the
LaTeX Project Public License (LPPL), either version 1.3c of this
license or (at your option) any later version.  The latest version
of this license is at <http://www.latex-project.org/lppl.txt>.

This work is “maintained” (_per_ LPPL maintenance status) by
Joel C. Salomon <joelcsalomon@gmail.com>.

[TeXSX]: http://tex.stackexchange.com
[TDS]:   http://tug.org/tds/
