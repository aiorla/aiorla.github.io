# CV source

`resume.tex` is the CV source. The `.tex` section files, Awesome CV class,
and bundled fonts are all in this folder. The source and fonts were moved
from the standalone `resume` repository without changes.

## Build

Use XeLaTeX and `latexmk` (tested with TeX Live 2025). Install your TeX
distribution's LaTeX extra packages, including `fontawesome` and
`sourcesanspro` (called `sourcesans` in newer TeX Live releases).
If XeLaTeX cannot find FontAwesome by name, install the bundled
`fonts/FontAwesome.ttf` as a user font.

From the website repository root:

```sh
cd cv
latexmk -xelatex -jobname=resume -interaction=nonstopmode -halt-on-error build.tex
```

Build `build.tex`, rather than `resume.tex` directly. It selects the older
LaTeX layout behavior expected by this version of Awesome CV so entries
keep their original spacing on newer TeX releases.

The build writes an ignored local `cv/resume.pdf`. The site serves the
separate, tracked PDF at [aiorla.com/resume.pdf](https://aiorla.com/resume.pdf).
Only replace the root `resume.pdf` if you intend to publish a CV update.

## Bundled fonts

- Font Awesome 4.7.0 by Dave Gandy: [SIL Open Font License 1.1](fonts/FontAwesome-OFL.txt).
- Roboto by Google: [Apache License 2.0](fonts/Roboto-LICENSE.txt).
