incanter-docs
=============

DITA documentation for [Incanter](https://github.com/incanter/incanter)

# Contributing

# Building

Use either ditac or DITA-OT (links below).  To generate PDF output,
you need an XSLFO processor.  I have a copy of XEP (typesetting Geek
here), which works great, so I have not tested FOP.

NOTE: apparently the full-easy-install package of DITA-OT comes with FOP.

## ditac

The instructions at
http://www.xmlmind.com/ditac/_distrib/doc/manual/manual-4.html#quickStart
are pretty clear.  I have a copy of XEP, so I set up ditac.options as
per
http://www.xmlmind.com/ditac/_distrib/doc/manual/commandLine.html#commandLine__ditac_options_file,
and the command I use to generate PDF is:

    $ /path/to/ditac tmp/ugbook.ditac.pdf ugbook.ditamap

## DITA-OT

The documentation isn't great, so you'll need to put in a little work
to figure out how to make it go.  The relevant documentation is at
http://dita-ot.github.io/1.8/readme/tranforming-dita-content.html.

*CAVEAT* You have to cd to the kit root dir and run `startcmd.sh` (or
 .bat) first.

I use the ant technique
(http://dita-ot.github.io/1.8/readme/DITA-antuse.html), so my command
line is:

    DITA_HOME $ ant -Dargs.input=/path/to/leiningen-doc/ugbook.ditamap -Dtranstype=pdf

Must be executed from the toolkit's root dir; haven't figured out how
to get around that yet.  This puts the output to DITA_HOME/out.  I
haven't been able to figure out how to specify a different output dir.
Change the transtype parm to change the format,
e.g. -Dtranstype=xhtml. (See
http://dita-ot.github.io/1.8/readme/AvailableTransforms.html)

For PDF output see also http://dita-ot.github.io/1.8/readme/ant-parameters-pdf2-transformation.html

# DITA Resources

[DITA 1.2 Spec](http://docs.oasis-open.org/dita/v1.2/spec/DITA1.2-spec.html)

[DITA XML.org](http://dita.xml.org/) - "the official community gathering place and information resource for the DITA OASIS Standard."

[DITA Open Toolkit](http://dita-ot.github.io/) (DITA OT)

[XMLMind DITA Converter](http://www.xmlmind.com/ditac/) (ditac)

Whitepapers: 

 * [An XML Architecture for Technical Documentation: The Darwin Information Typing Architecture](http://www.writersua.com/articles/DITA/)
 * [Hacking the DITA Open Toolkit](http://www.scriptorium.com/whitepapers/hackingot/index.html) (HTML)  ([PDF version](http://www.scriptorium.com/whitepapers/hackingot/hackingot.pdf)
 * [Customizing PDF Output in the DITA Open Toolkit](http://www.scriptorium.com/whitepapers/ditaotpdf/DITA-PDF-tweaks.pdf) (PDF)

Markdown:

 * [Standard Markdown](http://daringfireball.net/projects/markdown/syntax) at Daring Fireball
 * [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)
 * [GitHub markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

# License

This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/3.0/ or send a letter to Creative Commons, 171 Second Street, Suite 300, San Francisco, California, 94105, USA.

