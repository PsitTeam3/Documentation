# Documentation
## build latex
1. `cd docs/`
2. `xelatex Anforderungsanalyse.tex`

Alternatively you can install [Atom](http://www.atom.io), the package `latex` and hit `ctrl-alt-b` to build.

## build pandoc
1. install pandoc: `brew install pandoc`
2. generate pdf:
  - Projektskizze: `pandoc -s --data-dir=docs docs/Projektskizze.md -o Projektskizze.pdf`
  - UC 1: `pandoc -s --data-dir=docs docs/Use\ Case\ 1.md -o Use\ Case\ 1.pdf`
