# AI Coding Instructions: Simplicial Homotopy Theory Notes

## Project Overview
This is a mathematical LaTeX document containing lecture notes on simplicial homotopy theory by Serkan Doğan. The project consists of a single comprehensive LaTeX file (`SHT.tex`) with associated images and build artifacts.

## Document Structure & Content Patterns

### Mathematical Organization
- **Main document**: `SHT.tex` (~1176 lines) organized into logical sections:
  - Introduction and fundamentals of algebraic topology
  - Simplicial complexes (geometric and abstract)
  - Category theory basics with emphasis on simplicial objects
  - Simplicial sets and morphisms
  - Advanced topics (Kan complexes, simplicial homotopy)

### LaTeX Conventions
- Uses `article` class with 11pt font and 2cm margins via `geometry` package
- **Theorem environments**: All numbered together using `[section]` - `definition`, `theorem`, `proposition`, `lemma`, `corollary`, `example`, `question`, `remark`
- **Mathematical notation**: Heavy use of AMS packages (`amsmath`, `amssymb`, `amsthm`)
- **Diagrams**: Uses `tikz`, `tikz-cd` for commutative diagrams, and `pgfplots` for 3D visualizations
- **References**: Includes image files (`ex.jpg`, `face_maps.jpg`, `scp.jpg`) for mathematical illustrations

### Key Mathematical Concepts to Understand
- **Simplicial complexes**: Both geometric (in ℝᵈ) and abstract versions
- **Category theory**: Emphasis on functor categories, especially `Δᵒᵖ → Set`
- **Standard simplex notation**: `Δⁿ` for n-dimensional standard simplex, `[n] = {0,1,...,n}`
- **Face and degeneracy maps**: Core structure of simplicial objects

## Build System & Workflow

### Compilation
- Uses **pdfLaTeX** (MiKTeX distribution based on log files)
- Generates typical LaTeX auxiliary files: `.aux`, `.log`, `.toc`, `.out`, `.synctex.gz`
- Uses `latexmk` for build automation (evidenced by `.fdb_latexmk`, `.fls` files)
- **Command**: `pdflatex SHT.tex` or `latexmk -pdf SHT.tex` for automated building

### File Dependencies
- **Main source**: `SHT.tex`
- **Images**: `ex.jpg`, `face_maps.jpg`, `scp.jpg` (referenced with `\includegraphics`)
- **Output**: `SHT.pdf` (final document)

## Development Guidelines

### When Working with Mathematical Content
- **Preserve mathematical rigor**: Maintain proper theorem-proof structure and notation consistency
- **Respect LaTeX formatting**: Keep consistent indentation and spacing in mathematical expressions
- **Handle diagrams carefully**: TikZ code is complex - test compilation after changes to diagram code
- **Check cross-references**: The document uses internal references that must remain valid

### Adding New Mathematical Content
- Use existing theorem environment pattern: `\begin{definition}[Title]...\end{definition}`
- Follow the established numbering scheme (all environments share counter)
- For new diagrams, follow the TikZ patterns established in the document
- Mathematical expressions should use proper AMS-LaTeX commands

### Image Integration
- Images are included using `\includegraphics[height=Xcm]{filename.jpg}`
- Store new images in the root directory alongside existing `.jpg` files
- Use descriptive filenames that indicate mathematical content

### Testing Changes
- Always compile with `pdflatex` after edits to check for LaTeX errors
- Review mathematical notation rendering in the PDF output
- Verify that TikZ diagrams compile correctly (they're resource-intensive)

## Common Patterns to Follow
- **Section structure**: Use `\section{}`, `\subsection{}`, `\paragraph{}` hierarchy as established
- **Mathematical objects**: Use `\emph{}` for first definitions, `\textbf{}` for emphasis
- **Sets and categories**: Follow notation like `\mathbf{Set}`, `\mathcal{C}` for categories
- **Commutative diagrams**: Use `tikz-cd` package with consistent arrow styles

## Notes for AI Agents
- This is primarily a **read-and-edit** workflow - the document structure is well-established
- Focus on **mathematical accuracy** over code style when making changes
- **Compilation testing** is essential - LaTeX errors can be subtle and cascading
- The document represents advanced mathematics - maintain the academic rigor and notation standards