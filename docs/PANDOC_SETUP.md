# 🖨️  Pandoc Build Guide for GxP Blueprint / SOPS

> Goal: every change in `docs/` automatically produces an inspection-ready PDF  
> (and anyone can still build the PDF locally if they want to preview it).

---

## 0 · Prerequisites

* Repository already exists at **github.com/gxpblueprint/sops** and is public.  
* You have *write* access (or work in a fork + PR).  
* Basic command-line Git knowledge (clone → branch → push).

---

## 1 · Local install (optional but good for testing)

### macOS (Homebrew)

```bash
brew install pandoc
brew install --cask mactex-no-gui        # tiny LaTeX engine (~150 MB)
# verify
pandoc --version
```

### Windows (Chocolatey)

```bash
choco install pandoc miktex
# then reopen PowerShell and run:
pandoc --version
```

### Ubuntu / WSL

```bash
sudo apt-get update
sudo apt-get install pandoc texlive-latex-recommended \
                     texlive-fonts-recommended
pandoc --version
```

### One-liner to test

```bash
cd sops
pandoc docs/csv/_main.md -o csv-sop.pdf --toc --number-sections
# open the generated PDF → should have headings + ToC
(If images are missing, check relative paths in _main.md.)
```

## 2 · Add the GitHub Actions workflow (CI build)

Create a new file `.github/workflows/pdf.yml` with the following content:

```yaml
name: build-pdf

on:
  push:
    branches: [main]
    tags: ['*']
    paths: ['docs/**']
  pull_request:
    paths: ['docs/**']

jobs:
  pandoc:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Install Pandoc + LaTeX
        run: |
          sudo apt-get update
          sudo apt-get -y install pandoc texlive-latex-recommended \
                                      texlive-fonts-recommended

      - name: Build CSV SOP PDF
        run: |
          mkdir -p build
          pandoc docs/csv/_main.md \
                 -o build/csv-sop.pdf \
                 --toc --number-sections

      - name: Upload PDF artifact
        uses: actions/upload-artifact@v4
        with:
          name: csv-sop
          path: build/csv-sop.pdf
```

### What it does

* Triggers on any push/PR that touches files in `docs/`.
* Installs Pandoc + a minimal LaTeX engine (≈ 400 MB, GitHub runner handles this).
* Generates `build/csv-sop.pdf`.
* Attaches the PDF as a downloadable artifact to the workflow run & the pull-request page.
* Also runs automatically for Git tags – handy for official release bundles.
* Runtime per build: ~40–60 s → well inside free Action minutes.

## 3 · Commit & push

```bash
git checkout -b ci/pdf-build
git add .github/workflows/pdf.yml
git commit -m "ci: auto-build PDF with Pandoc"
git push -u origin ci/pdf-build
# open a Pull Request on GitHub
```

GitHub will run the workflow; under “Checks” you should see `csv-sop / build-pdf` turn green.
An “Artifacts” link will contain the PDF.

## 4 · (Optional) reference templates for branding

* DOCX reference → place in `templates/sop.docx` (Word header/footer, logo).

```bash
pandoc docs/csv/_main.md --reference-doc=templates/sop.docx \
       -o build/csv-sop.docx
```

* LaTeX template → place in `templates/sop.latex`; swap the pandoc command in the workflow for:

```bash
pandoc docs/csv/_main.md \
       --template=templates/sop.latex \
       --toc --number-sections \
       -o build/csv-sop.pdf
```

(Templates can be added later; the default PDF is perfectly serviceable for a first pass.)

## 5 · Troubleshooting cheat-sheet

- **Workflow fails with “Missing font”** – Add `texlive-latex-extra` to the apt-get line.
- **Images don’t appear in PDF** – Check image paths and use `![alt](./_images/foo.png)`.
- **PDF too large** – Compress PNGs or convert diagrams to SVG.
- **Need multiple PDFs** – Use a matrix in the workflow for more SOP folders.

