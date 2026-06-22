# Translation of the Python Documentation — pa

Punjabi (India) translation of the Python documentation.

This project aims to translate Python's official documentation into Punjabi (Gurmukhi) and make Python learning resources more accessible to Punjabi-speaking developers, students, and educators.

## Status

🎉 All currently tracked translation files are complete and validated.

The repository currently contains fully translated and validated files across:

* Tutorial Documentation
* Core Library Reference
* bugs.po

All translation files pass GNU gettext validation checks, are tracked in GitHub, and pass repository-wide validation.

Completed major translation milestones:

* `bugs.po`
* `library/functions.po`
* `library/stdtypes.po`
* Complete Tutorial Documentation Set

**Latest commit:** a389206

**Latest milestone:** All current repository translation files completed and validated

### Translation Milestones

| Milestone | Status |
|------------|---------|
| Tutorial Documentation | ✅ Complete |
| bugs.po | ✅ Complete |
| library/functions.po | ✅ Complete |
| library/stdtypes.po | ✅ Complete |
| Repository Validation | ✅ Passing |

## Current Progress

### Completed Tutorial Files

| File | Status | Messages |
|--------|--------|---------:|
| appendix.po | ✅ Complete | 28 |
| appetite.po | ✅ Complete | 17 |
| classes.po | ✅ Complete | 154 |
| controlflow.po | ✅ Complete | 226 |
| datastructures.po | ✅ Complete | 139 |
| errors.po | ✅ Complete | 96 |
| floatingpoint.po | ✅ Complete | 76 |
| inputoutput.po | ✅ Complete | 112 |
| interactive.po | ✅ Complete | 7 |
| interpreter.po | ✅ Complete | 33 |
| introduction.po | ✅ Complete | 120 |
| modules.po | ✅ Complete | 116 |
| stdlib.po | ✅ Complete | 67 |
| stdlib2.po | ✅ Complete | 65 |
| venv.po | ✅ Complete | 42 |
| whatnow.po | ✅ Complete | 18 |

### Completed Root Files

| File | Status | Messages |
|--------|--------|---------:|
| bugs.po | ✅ Complete | 31 |

### Completed Library Files

| File         | Status     | Messages |
| ------------ | ---------- | -------: |
| functions.po | ✅ Complete |      535 |
| stdtypes.po  | ✅ Complete |     1592 |

### Project Statistics

| Metric | Value |
|----------|------:|
| Tutorial Files Completed | 16 |
| Tutorial Messages Translated | 1,416 |
| Root Files Completed | 1 |
| Root Messages Translated | 31 |
| Library Files Completed | 2 |
| Library Messages Translated | 2,127 |
| Total Messages Translated | 3,574 |

## Validation Status

All completed translation files successfully pass validation.

```bash
msgfmt --check bugs.po
msgfmt --check tutorial/FILENAME.po
msgfmt --check library/FILENAME.po
```

Validation summary:

* ✅ No validation errors
* ✅ No untranslated messages
* ✅ No fuzzy messages
* ✅ Tutorial files validated
* ✅ Library files validated
* ✅ bugs.po validated
* ✅ Repository-wide validation passing
* ✅ GitHub Actions validation passing

## Recent Milestones

* ✅ Completed `tutorial/appendix.po`
* ✅ Completed `tutorial/floatingpoint.po`
* ✅ Completed `tutorial/interactive.po`
* ✅ Completed `tutorial/venv.po`
* ✅ Completed `tutorial/whatnow.po`
* ✅ Completed `bugs.po`
* ✅ Completed `library/functions.po`
* ✅ Completed `library/stdtypes.po`
* ✅ Completed all current translation files in repository
* ✅ Exceeded 3,500 translated messages
* ✅ Repository-wide validation passing
* ✅ All translations committed, validated, and pushed to GitHub

## Infrastructure

* ✅ STYLE_GUIDE.md
* ✅ GLOSSARY.md
* ✅ CONTRIBUTING.md
* ✅ GitHub Actions validation workflow
* ✅ Translation terminology consistency review
* ✅ Repository structure aligned with Python documentation translation recommendations

## Next Phase

Current priorities:

1. Finalize Transifex synchronization workflow
2. Standardize repository metadata to use `pa`
3. Coordinate with Python Documentation Translation Team
4. Open Python Devguide translation listing PR
5. Expand translation coverage into:
   * Reference Documentation
   * Using Python Documentation
   * What's New Documentation

## Goals

Project goals are aligned with the Python Documentation Translation initiative and focus on expanding Punjabi-language access to Python learning resources while maintaining translation quality and terminology consistency.

* Translate Python documentation into Punjabi (Gurmukhi)
* Maintain terminology consistency through a shared glossary
* Follow Python documentation translation guidelines
* Ensure translation quality through automated validation
* Build a contributor community around Punjabi translations
* Contribute to the Python documentation translation ecosystem

## Repository Structure

```text
python-docs-pa/
├── .gitignore
├── bugs.po
├── CONTRIBUTING.md
├── GLOSSARY.md
├── PROJECT_REPORT.md
├── README.md
├── STYLE_GUIDE.md
│
├── .github/
│   └── workflows/
│       └── validate.yml
│
├── tutorial/
│   ├── appendix.po
│   ├── appetite.po
│   ├── classes.po
│   ├── controlflow.po
│   ├── datastructures.po
│   ├── errors.po
│   ├── floatingpoint.po
│   ├── inputoutput.po
│   ├── interactive.po
│   ├── interpreter.po
│   ├── introduction.po
│   ├── modules.po
│   ├── stdlib.po
│   ├── stdlib2.po
│   ├── venv.po
│   └── whatnow.po
│
├── library/
│   ├── functions.po
│   └── stdtypes.po
│
├── reference/
├── using/
└── whatsnew/
```

## Translation Workflow

1. Translate `.po` files.
2. Validate translations:

```bash
msgfmt --check FILE.po
```

3. Review terminology against `GLOSSARY.md`.
4. Follow rules in `STYLE_GUIDE.md`.
5. Ensure RST roles, directives, and code blocks remain unchanged.
6. Commit and push changes.
7. Verify GitHub Actions passes successfully.

## References

Python Documentation Translation Guide:

https://devguide.python.org/documentation/translations/

Python Documentation Project:

https://docs.python.org/

Python Documentation Translation Platform:

https://app.transifex.com/python-doc/python-newest/

## License

Documentation translations are contributed under the CC0 license.
