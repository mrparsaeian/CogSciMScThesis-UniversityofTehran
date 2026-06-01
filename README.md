# Tehran Thesis - MSc Thesis Source Repository

This repository contains the LaTeX source and supporting materials for the MSc thesis:

**Investigation of Decision-Making in Sharing Personal Information of Others**  
**Author:** Mohamad Rasoul Parsaeian  
**Program:** MSc in Cognitive Science, Cognitive Psychology  
**Institution:** University of Tehran, Faculty of Psychology and Education  
**Supervisors:** Dr. Majid Nili Ahmadabadi and Dr. Abdol-Hossein Vahabie  
**Date:** February 2023

The project uses a customized University of Tehran thesis template based on the `tehran-thesis` LaTeX class and includes Persian/English thesis metadata, chapters, bibliography, figures, tables, glossaries, and build configuration.

## Research Overview

The thesis investigates how people make decisions about sharing other people's personal information. It focuses on the relationship between:

- Dark Triad personality traits: Machiavellianism, psychopathy, and narcissism
- Social Value Orientation (SVO)
- Decisions to share or withhold personal information belonging to others
- Behavioral change under different levels of incentive or temptation

The study used a pre-test/post-test experimental design. Participants were first asked whether they would introduce one to five other people by entering first name, last name, and phone number. They then completed demographic and Dark Triad questionnaires, followed by a second introduction task with different incentive conditions. Social Value Orientation was measured at the end of the experiment.

## Main Findings

The thesis reports that higher Dark Triad scores were not significantly associated with refusing to share information in the initial introduction stage, nor with changing behavior under incentive conditions in the secondary introduction stage. Among participants who completed the SVO task, there was no significant difference in Dark Triad scores between individualist and prosocial groups.

## Repository Contents

The repository is organized around the LaTeX thesis build:

```text
.
├── main.tex                 # Main LaTeX entry point
├── latexmkrc                # latexmk configuration for XeLaTeX, BibTeX, and xindy
├── tex/                     # Thesis class, commands, metadata, chapters, glossary, bibliography
├── tables/                  # Generated and custom thesis tables
├── img/                     # Figures, diagrams, plots, and task screenshots
├── font/                    # Fonts referenced by the XePersian configuration
├── code/                    # Code listings referenced by the LaTeX configuration, if present
├── package.json             # Optional Node.js metadata/dependency file
└── README.md
```

Important source files include:

- `main.tex`: the main thesis file, document class selection, chapter inclusion, bibliography setup, and appendix inclusion
- `tex/faTitle.tex`: Persian title page, abstract, keywords, supervisors, and thesis metadata
- `tex/enTitle.tex`: English title page, abstract, keywords, supervisors, and thesis metadata
- `tex/commands.tex`: package imports, page geometry, bibliography settings, hyperlinks, XePersian configuration, fonts, and thesis macros
- `latexmkrc`: automated build configuration for XeLaTeX, `bibtex8`, and `xindy`

## Requirements

To build the thesis PDF, install a LaTeX distribution with Persian/XePersian support. A full TeX Live installation is recommended.

Required tools include:

- XeLaTeX
- latexmk
- BibTeX / bibtex8
- xindy
- XePersian and related Persian LaTeX packages
- The fonts referenced from the local `font/` directory

Optional Node.js dependency:

```bash
npm install
```

The current `package.json` includes `json2csv`, which may be useful for data-processing or conversion workflows related to thesis tables.

## Build Instructions

Clone the repository:

```bash
git clone https://github.com/mrparsaeian/tehranthesis.git
cd tehranthesis
```

Build the thesis PDF:

```bash
latexmk -bibtex -pdf main.tex
```

The `latexmkrc` file configures `latexmk` to use XeLaTeX and handles glossary/acronym generation through `xindy`.

Clean generated files:

```bash
latexmk -c
```

For a full cleanup, use:

```bash
latexmk -C
```

## Notes on the Web-Based Experiment

The thesis describes a web-based experimental task used to collect behavioral responses. The task included:

- Initial and secondary introduction forms
- Demographic questionnaire
- Dark Triad questionnaire
- Social Value Orientation slider measure
- Survey components implemented with React/SurveyJS
- A modified Persian interface for the SVO slider task

The README focuses on the thesis-source repository. If the full web application is maintained in this repository or another related repository, document its setup separately with its own installation and deployment instructions.

## Data Privacy and Ethics

This project concerns personal information, including names and phone numbers used as part of an experimental decision-making task. Do not commit, publish, or share raw participant data or personally identifiable information.

Recommended practice:

- Keep raw data outside the public repository
- Use anonymized or aggregated data for reproducible analysis
- Remove phone numbers, names, IDs, IP addresses, and other identifiers before sharing
- Document any preprocessing steps used to produce thesis tables and figures

## Citation

If you use this thesis or repository, please cite it as:

```bibtex
@mastersthesis{parsaeian2023decisionmaking,
  title        = {Investigation of Decision-Making in Sharing Personal Information of Others},
  author       = {Parsaeian, Mohamad Rasoul},
  school       = {University of Tehran, Faculty of Psychology and Education},
  type         = {MSc thesis},
  field        = {Cognitive Science - Cognitive Psychology},
  year         = {2023},
  month        = {February},
  supervisor   = {Majid Nili Ahmadabadi and Abdol-Hossein Vahabie}
}
```

## License

The repository metadata currently declares the package license as `ISC`. For formal reuse, add a dedicated `LICENSE` file to the repository and keep this section aligned with it.

## Author

**Mohamad Rasoul Parsaeian**  
MSc in Cognitive Science - Cognitive Psychology  
University of Tehran
