biblatex-mr
===========

My default configuration for `biblatex`.
Tested with TeXlive 2016 (the version currently used by arxiv.org).

* Add MathSciNet links to standard BibLaTeX styles (I recommend `style=alphabetic`).
* Make titles link to DOI or URL provided by the entry.

Installation
------------
If you want to use this configuration for all your documents:
```bash
mkdir -p ~/texmf/tex/latex/
cd ~/texmf/tex/latex/
git clone https://github.com/pzorin/biblatex-mr.git
```

If you want to use this configuration for a single document, then copy the `.cfg` files into the directory containing the tex file.

Caveats
-------
Mathscinet used to output `MRNUMBER` fields in different formats.
The following Emacs regexp converts them to the current (as of February 2020) format: search for `mrnumber *= *{[ mr]*\([0-9]*\).*?}`, replace with `mrnumber = {\1}`.
