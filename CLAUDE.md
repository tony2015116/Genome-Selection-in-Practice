# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Quarto Book Template** for creating bilingual (Chinese/English) academic/technical books with executable R and Python code. The project uses Quarto as the primary publishing system and supports HTML output with GitHub Pages deployment.

## Essential Commands

### Build and Development
```bash
# Render the book (generate HTML output)
quarto render

# Preview the book locally with live reload
quarto preview

# Install Quarto extensions
quarto install <extension-name>

# Uninstall Quarto extensions
quarto uninstall <extension-name>
```

### R Environment Management
```bash
# Activate renv (R package environment)
Rscript -e "renv::activate()"

# Install R packages from renv.lock
Rscript -e "renv::restore()"

# Install additional R packages
Rscript -e "install.packages('package-name')"
```

### Python Environment
```bash
# Install Python dependencies
pip install -r requirements.txt
```

### Deployment
```bash
# Publish to GitHub Pages
quarto publish gh-pages
```

## Architecture and Structure

### Core Configuration Files
- **`_quarto.yml`**: Main book configuration defining chapters, themes, language settings, and output formats. Contains the complete book structure and styling configuration.
- **`.Rprofile`**: Activates renv for reproducible R package management.
- **`renv.lock`**: Locked R package versions ensuring consistent builds across environments.

### Content Organization
- **Chapter files** (`.qmd`): Quarto markdown files that form the book chapters
  - `index.qmd`: Preface/Introduction
  - `intro.qmd`, `table.qmd`, `plot.qmd`, `callouts.qmd`, `summary.qmd`: Main content chapters
  - `references.qmd`: Bibliography section
- **`references.bib`**: Bibliography database for citations
- **`custom_language-zh.yml`**: Chinese localization for Quarto interface elements

### Theming and Styling
- **`styles.css`**: Custom CSS styles for HTML output
- **`theme.scss`/`theme-dark.scss`**: SCSS theme files for light/dark modes
- **`arrow-light.theme`/`arrow-dark.theme`**: Code syntax highlighting themes
- **`fonts/`**: Custom fonts for PDF generation (LXGW WenKai, NotoSansSC)

### Automated Deployment
- **`.github/workflows/publish.yml`**: GitHub Actions workflow that automatically renders and publishes the book to GitHub Pages on push to master branch

## Key Technical Features

1. **Bilingual Support**: Primary language is Chinese with English support, configured through `custom_language-zh.yml`
2. **Executable Code**: Supports both R (with tidyverse, palmerpenguins) and Python (numpy, pandas, matplotlib) code chunks
3. **Theme System**: Light/dark theme switching with custom SCSS and syntax highlighting
4. **Search Functionality**: Built-in search with Chinese localization
5. **Responsive Design**: Floating sidebar with mobile support
6. **Reproducible Builds**: R packages locked via renv, ensuring consistent rendering across environments

## Development Workflow

When modifying this book template:
1. Edit `.qmd` chapter files for content changes
2. Update `_quarto.yml` for structural changes (chapter order, titles, etc.)
3. Modify theme files (`*.scss`, `*.css`) for styling changes
4. Test changes with `quarto preview` before committing
5. Push to master branch triggers automatic GitHub Pages deployment