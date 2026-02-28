# epibox.sty

<p align="center">
<img width="449" height="669" alt="epibox preview 1" src="https://github.com/user-attachments/assets/b767ae13-3c01-49fa-97e1-3c53cb05e75a" />
<img width="449" height="673" alt="epibox preview 2" src="https://github.com/user-attachments/assets/0ab71fc3-cc1a-40eb-bbb1-3efe0de669d9" />
</p>

A LaTeX package for creating styled epistemic boxes in your documents. Perfect for academic note-taking, research journals, and organizing knowledge with color-coded boxes.

## What is epibox?

epibox provides a collection of environments for categorizing different types of information in your notes:

- **known** - Established facts and proven results
- **unclear** - Points that need clarification or further investigation
- **question** - Open questions to be answered
- **claim** - Assertions or propositions (with optional title)
- **pitfall** - Common mistakes or traps to avoid
- **epibox** - General notes and asides

Each environment has a distinct color for easy visual identification.

## Zettelkasten Support

epibox works great with Zettelkasten-style note-taking. The optional argument allows you to add timestamps or IDs for linking notes:

```latex
\begin{question}[title=Question: 202602281530]
    This question has a unique timestamp ID for Zettelkasten organization.
\end{question}
```

This timestamp format (`YYYYMMDDHHMM`) can be automatically generated using a LuaSnip snippet in Neovim:

```lua
luasnip.add_snippets('tex', {
    luasnip.snippet('qbox', {
        luasnip.text_node { '\\begin{question}{' },
        luasnip.function_node(os.date('%Y%m%d%H%M'), {}),
        luasnip.text_node { '}', '\t' },
        luasnip.insert_node(1, 'Type your question here...'),
        luasnip.text_node { '', '\\end{question}' },
    }),
})
```

This enables unique identification of each box for cross-referencing and building a personal knowledge management system.

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
