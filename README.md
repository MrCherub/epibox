# VimTeX Examples: dangbox.sty & epibox.sty

<p align="center">
<img width="465" height="234" alt="dangbox preview" src="https://github.com/user-attachments/assets/8b635c9b-6f39-434c-8b5c-e41d9a9f8012" />
</p>

This repository contains LaTeX packages for styled boxes.

**Disclaimer:** Some code is sourced from the internet and is not original work.

## Installation

Place the `.sty` files in the same folder as your LaTeX file, or in your local TeX tree (`~/Library/texmf/tex/latex/`).

---

## dangbox.sty

A simple boxed environment with a gradient title bar.

### Usage

```latex
\usepackage{dangbox}

\begin{dang}[title=Example]
Your content here
\end{dang}
```

---

## epibox.sty

Epistemic boxes for academic note-taking. Includes:

- `known` - Known results (green)
- `unclear` - Unclear points (orange)
- `question` - Open questions (red)
- `claim{title}` - Claims with title (blue)
- `pitfall` - Pitfalls to avoid (purple)
- `epibox` - General notes (gray)

### Usage

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

### Lists

Generate lists of all boxes:

```latex
\listofknown
\listofunclear
\listofquestions
\listofclaims
\listofpitfalls
\listofepibox
```
