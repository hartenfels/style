# Softlang Style That Works For Me™

Simplified and cleaned-up version of the official Softlang style. Does what you
mean, loads less random packages and doesn't require biblatex. Windows and
German are unsupported.

## Usage

Modify [config.tex](config.tex) to your liking.

Put your chapters into [content](content) and put numbers in front so that they
are sorted correctly. For example `content/01_introduction.tex`,
`content/02_background.tex` etc. They will be included in order.

If you want an abstract, call it `content/abstract.tex`. If you want an
appendix, call it `content/appendix.tex`. They will be included in the right
places if they're there.

Put your bibtex sources into [sources.bib](sources.bib).

Run `make` to build it. Run `make clean` to remove all those LaTeX intermediary
files and `make realclean` to remove *everything* that got built.
