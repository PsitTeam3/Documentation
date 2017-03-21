# Documentation
## build
1. install pandoc: `brew install pandoc`
2. generate pdf:
  - Projektskizze: `pandoc -s --data-dir=docs docs/Projektskizze.md -o Projektskizze.pdf`
  - Anforderungsanalyse: `pandoc -s --data-dir=docs docs/Anforderungsanalyse.md -o Anforderungsanalyse.pdf`
  - UC 1: `pandoc -s --data-dir=docs docs/Use\ Case\ 1.md -o Use\ Case\ 1.pdf`
