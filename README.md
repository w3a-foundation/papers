# Web3 Alliance — Papers

LaTeX-authored white papers and supporting research.

## Index

| Paper | PDF | TeX | Author |
|---|---|---|---|
| Web3 Industrial Alliance (operative thesis) | [`Web3_Alliance.pdf`](Web3_Alliance.pdf) | [`Web3_Alliance.tex`](Web3_Alliance.tex) | Hunter Dupont |

## Build

```sh
cd ~/work/w3a/papers
pdflatex -interaction=nonstopmode Web3_Alliance.tex
pdflatex -interaction=nonstopmode Web3_Alliance.tex  # second pass for refs/TOC
```

Or use `latexmk`:

```sh
latexmk -pdf Web3_Alliance.tex
```

## Cover-page macros

`shared/luxcover.sty` provides the W3A cover-page format. New papers
should `\usepackage{shared/luxcover}` and call `\luxcoverpage` after
`\begin{document}`.

## Contributing

New papers land as a new top-level `.tex` file plus an optional
`sections/` subdir for multi-file structure. Each paper carries the
W3A author block:

```latex
\author{<Name>\\
\textit{<Title>}\\
Web3 Alliance (W3A)}
```

Submit via pull request; the Office of the Chief Architect reviews
for technical accuracy and the Office of the General Counsel reviews
for brand discipline (no Counterparty / Liquidity / Satschel
references; Member attribution where factually warranted).
