# epibox.sty

<p align="center">
<img width="449" height="669" alt="epibox preview 1" src="https://github.com/user-attachments/assets/b767ae13-3c01-49fa-97e1-3c53cb05e75a" />
<img width="449" height="673" alt="epibox preview 2" src="https://github.com/user-attachments/assets/0ab71fc3-cc1a-40eb-bbb1-3efe0de669d9" />
</p>

LaTeX package for epistemic boxes for academic note-taking.

## Installation

Place `epibox.sty` in the same folder as your LaTeX file, or in your local TeX tree (`~/Library/texmf/tex/latex/`).

## Environments

- `known` - Known results (green)
- `unclear` - Unclear points (orange)
- `question` - Open questions (red)
- `claim{title}` - Claims with title (blue)
- `pitfall` - Pitfalls to avoid (purple)
- `epibox` - General notes (gray)

## Usage

```latex
\usepackage{epibox}

\begin{known}
    This is something known.
\end{known}

\begin{unclear}
    This is unclear.
\end{unclear}

\begin{question}
    This is a question.
\end{question}

\begin{claim}{The Riemann Hypothesis}
    All non-trivial zeros of the Riemann zeta function have real part 1/2.
\end{claim}

\begin{pitfall}
    This is a pitfall.
\end{pitfall}

\begin{epibox}
    This is a note.
\end{epibox}
```

## Lists

Generate lists of all boxes:

```latex
\listofknown
\listofunclear
\listofquestions
\listofclaims
\listofpitfalls
\listofepibox
```
