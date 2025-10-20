# LaTeX Resume Template

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge&logo=github)](https://github.com/samueltauil/latex-resume-template/generate)

A minimal LaTeX resume template with an accompanying GitHub Actions workflow that automatically builds and commits a PDF version on every push.

## Features

- Automated LaTeX compilation via GitHub Actions
- Ready-to-edit `my-resume.tex` structure with placeholder content
- Generated PDF stored in the repository and uploaded as a workflow artifact
- MIT licensed for unrestricted reuse

## Workflow Overview

The workflow at `.github/workflows/build-resume.yml` runs on every push and performs the following steps:

1. **Checkout Repository**: Fetches the latest source files
2. **Compile LaTeX**: Builds `my-resume.tex` using the `xu-cheng/latex-action` container
3. **Upload Artifact**: Publishes `my-resume.pdf` as a downloadable artifact
4. **Commit PDF**: Commits the updated PDF back to the repository when changes occur

### Configuration Variables

The workflow relies on two environment variables that define the LaTeX source and PDF output names:

| Variable | Description | Default |
|----------|-------------|---------|
| `TEX_FILE` | LaTeX source filename | `my-resume.tex` |
| `PDF_FILE` | Generated PDF filename | `my-resume.pdf` |

To change the file names, update these variables and rename the files accordingly.

## Getting Started

1. Click **Use this template** on GitHub to create a new repository
2. Update `my-resume.tex` with your personal details and sections
3. Adjust the workflow badge URLs (if you add them) to point to your new repository
4. Commit and push your changes to trigger the automated build

## Local Build

You can also compile the resume locally if you have a LaTeX distribution installed:

```bash
pdflatex my-resume.tex
```

Run the command twice if you add references or a table of contents.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
