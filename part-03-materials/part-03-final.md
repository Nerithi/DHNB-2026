---
title: "Markdown for Academia: Part 3 Raw File"
author: "Author's name"
date: "04.03.2026"
abstract: "This document exemplifies how to use Reference Managers, Citation Style Language and the LaTeX package glossaries with Markdown. It further demonstrates some useful Markdown hacks."
header-includes:
  - \usepackage[shortcuts, toc]{glossaries}
  - \loadglsentries{glossary-file.tex}
  - \makenoidxglossaries
include-after:
  - \printnoidxglossary[sort=word, title={Indexed Glossary}]
---

# Reference Managers & Citation Style Language (1st level)

To have references autocomplete in Zettlr, you need to follow these instructions: <https://docs.zettlr.com/en/editor/citations/#enable-render-citations-setting>

## Resources (2nd level)

1. Citation Style Language Style repositories
    + <https://www.zotero.org/styles>
    + <https://github.com/citation-style-language/styles>
2. Editing CSL style files
    + <https://editor.citationstyles.org/about/>
    + <https://www.zotero.org/support/dev/citation_styles/style_editing_step-by-step>

# Useful Markdown Hacks (1st level)

"Outcommenting text" means that it won't appear in the output file, whether that is .docx, .html or .pdf.

## Outcommenting (2nd level)

[This text ist invisible in the output.]: #

<!-- This text is also invisible in the output

regardless of how many

paragraphs or even

### section headings

it has. -->

Outcommenting is incredibly useful if you're still working on something or simply do not want a whole document exported.

# LaTeX "glossaries" in Markdown (1st level)

<https://ctan.org/pkg/glossaries>

When using \ac{md} simply to write text, it is generally enough to find the right \ac{mda} to create well-structured, pretty documents. When using \ac{md} in academia, additional software can, however, be useful. Reference managers are generally a good idea when working with citations; additionally, monographs often also contain \acp{glo} and \acp{ind}. \gls{glo} \glspl{glo}

Using the LaTeX package "glossaries", it becomes possible to create \acsp{pdf} with a combined \gls{glo} and \gls{ind}. These \aclp{pdf} can still be transformed into Word or HTML files, but it will require more work -- *glossaries* is a very advanced LaTeX package and the generic LaTeX output is \ac{pdf}. While the *glossaries* package still works fairly well in combination with \acl{md}, if you need a lot of specific layout in your documents, consider using LaTeX directly. \Acl{md} can do a lot, but some things are just a bit beyond its capabilities! \Gls{ind}

ALWAYS remember to close the exported \ac{pdf} before exporting again -- LaTeX will throw up an error if you don't!

# Bibliography (1st level)
