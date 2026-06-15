# Translation of the Python Documentation — pa-IN

Punjabi (India) translation of the Python documentation.

This project aims to translate Python's official documentation into Punjabi (Gurmukhi) and make Python learning resources more accessible to Punjabi-speaking developers, students, and educators.

## Status

🎉 Tutorial Translation Complete

The complete Python Tutorial section has been translated into Punjabi (Gurmukhi), validated using GNU gettext tools, and tagged as a project milestone.

**Latest milestone:** `tutorial-complete`

## Current Progress

### Completed Tutorial Files

| File              | Status     | Messages |
| ----------------- | ---------- | -------- |
| appetite.po       | ✅ Complete | 17       |
| interpreter.po    | ✅ Complete | 33       |
| introduction.po   | ✅ Complete | 120      |
| controlflow.po    | ✅ Complete | 226      |
| datastructures.po | ✅ Complete | 139      |
| inputoutput.po    | ✅ Complete | 112      |
| modules.po        | ✅ Complete | 116      |
| errors.po         | ✅ Complete | 96       |
| classes.po        | ✅ Complete | 154      |
| stdlib.po         | ✅ Complete | 67       |
| stdlib2.po        | ✅ Complete | 65       |

### Tutorial Statistics

| Metric                    | Value |
| ------------------------- | ----- |
| Tutorial Files            | 11    |
| Completed Files           | 11    |
| Untranslated Files        | 0     |
| Completion Rate           | 100%  |
| Total Messages Translated | 1,145 |

### Validation Status

All tutorial translation files successfully pass validation.

```bash
msgfmt --check tutorial/FILENAME.po
```

Validation summary:

* ✅ No validation errors
* ✅ No untranslated messages
* ✅ All tutorial files complete
* ✅ GitHub Actions validation passing

### Recent Milestones

* ✅ Completed `tutorial/classes.po`
* ✅ Completed `tutorial/stdlib.po`
* ✅ Completed `tutorial/stdlib2.po`
* ✅ Finished full Python Tutorial translation
* ✅ Created `tutorial-complete` release tag
* ✅ Repository synchronized with updated Python documentation structure

### Infrastructure

* ✅ STYLE_GUIDE.md
* ✅ GLOSSARY.md
* ✅ CONTRIBUTING.md
* ✅ GitHub Actions validation workflow
* ✅ Repository structure aligned with Python documentation translation recommendations
* ✅ Translation terminology consistency review

## Next Phase

Future work may include:

* Library Reference
* Language Reference
* HOWTO Guides
* FAQ
* Using Python Documentation
* What's New Documentation
* Glossary refinement and terminology review

## Goals

* Translate Python documentation into Punjabi (Gurmukhi)
* Maintain terminology consistency through a shared glossary
* Follow Python documentation translation guidelines
* Ensure translation quality through automated validation
* Build a contributor community around Punjabi translations
* Contribute to the Python documentation translation ecosystem

## Repository Structure

```text
python-docs-pa-in/
├── README.md
├── CONTRIBUTING.md
├── GLOSSARY.md
├── STYLE_GUIDE.md
├── .github/
│   └── workflows/
│       └── validate.yml
├── tutorial/
│   ├── appetite.po
│   ├── classes.po
│   ├── controlflow.po
│   ├── datastructures.po
│   ├── errors.po
│   ├── inputoutput.po
│   ├── interpreter.po
│   ├── introduction.po
│   ├── modules.po
│   ├── stdlib.po
│   └── stdlib2.po
├── library/
├── reference/
├── using/
└── whatsnew/
```

## Translation Workflow

1. Translate `.po` files.
2. Validate translations:

```bash
msgfmt --check tutorial/FILENAME.po
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

## License

Documentation translations are contributed under the CC0 license.
