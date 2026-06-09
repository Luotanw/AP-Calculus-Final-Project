# Trigonometric Substitution Explained with a Physics Application

This repository contains an AP Calculus final project on trigonometric
substitution. The project explains the three standard trigonometric
substitutions, emphasizes domain and sign restrictions, works through a detailed
example involving

```tex
\int \frac{dx}{\sqrt{x^2 - 1}},
```

and applies the method to a physics problem: finding the electric field from a
uniformly charged finite line segment.

The main finished paper is:

- [Paper/build/main.pdf](Paper/build/main.pdf)

## Project Contents

```text
.
|-- Paper/
|   |-- main.tex
|   |-- build/
|   |   |-- main.pdf
|   |   `-- main.synctex.gz
|   |-- figures/
|   |   |-- trig-substitution-sine.png
|   |   |-- trig-substitution-tangent.png
|   |   |-- trig-substitution-secant.png
|   |   |-- integrand-reciprocal-root.png
|   |   |-- antiderivative-log-root.png
|   |   |-- electric-field-line-charge.tex
|   |   |-- electric-field-line-charge.pdf
|   |   |-- electric-field-line-charge.png
|   |   `-- electric-field-line-charge-preview.png
|   |-- Wolfram Example/
|   |   |-- demo.ipynb
|   |   `-- Graphs/
|   |-- Derivations Manuscript/
|   |   |-- section_3_dduan.pdf
|   |   `-- section_7_gwang.pdf
|   `-- Textbook Source/
|       `-- table of 3.png
|-- Presentation/
|   `-- Presentation Outline.md
`-- README.md
```

## Paper

[Paper/main.tex](Paper/main.tex) is the LaTeX source for the paper. It includes:

- an overview of when trigonometric substitution is useful;
- cautions about domain, range, signs, and absolute values;
- derivations of the sine, tangent, and secant substitutions;
- a full branch-by-branch derivation of
  `\int dx / \sqrt{x^2 - 1}`;
- graphical and numerical interpretations of the result;
- a physics application deriving the electric field from a charged rod.

The compiled output is stored in [Paper/build/main.pdf](Paper/build/main.pdf).

## Supporting Material

[Paper/figures](Paper/figures) contains the diagrams and graph images used by
the paper, including substitution triangles, the integrand and antiderivative
graphs, and the charged-rod electric-field diagram.

[Paper/Wolfram Example/demo.ipynb](Paper/Wolfram%20Example/demo.ipynb) contains
supporting Wolfram notebook work, with exported graph images in
[Paper/Wolfram Example/Graphs](Paper/Wolfram%20Example/Graphs).

[Paper/Derivations Manuscript](Paper/Derivations%20Manuscript) contains
contributor manuscript PDFs for selected derivation sections.

[Paper/Textbook Source/table of 3.png](Paper/Textbook%20Source/table%20of%203.png)
is a reference image for the standard three trigonometric substitution forms.

[Presentation/Presentation Outline.md](Presentation/Presentation%20Outline.md)
is a timed presentation outline centered on the worked example
`\int dx / \sqrt{x^2 - 1}`.

## Rebuilding the Paper

From the repository root, run:

```sh
cd Paper
pdflatex -output-directory=build main.tex
```

Run the command twice if cross-references or generated LaTeX output need another
pass. The rebuilt PDF will be written to `Paper/build/main.pdf`.
