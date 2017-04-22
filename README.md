# Documentation
# Trello Board
[Trello Board](https://trello.com/b/24tNcmal)

## build latex
1. Change directory to `cd docs/`
2. use `xelatex` to compile latex
  - `xelatex Anforderungsanalyse.tex`
  - `xelatex Design.tex`

Alternatively you can install [Atom](http://www.atom.io), the package `latex` and hit `ctrl-alt-b` to build.

## build pandoc
1. install pandoc: `brew install pandoc`
2. generate pdf:
  - Projektskizze: `pandoc -s --data-dir=docs docs/Projektskizze.md -o Projektskizze.pdf`
  - UC 1: `pandoc -s --data-dir=docs docs/Use\ Case\ 1.md -o Use\ Case\ 1.pdf`
