# Translation of the Python Documentation — pa-IN

Punjabi (India) translation of the Python documentation.

This project aims to translate Python's official documentation into
Punjabi (Gurmukhi) and make Python learning resources more accessible
to Punjabi-speaking developers, students, and educators.

## Status

🚧 Work in Progress

## Current Progress

Tutorial Section

| File | Status | Messages |
|------|--------|----------|
| introduction.po | Complete | 120 |
| interpreter.po | Complete | 33 |
| appetite.po | Complete | 17 |
| controlflow.po | Complete | 226 |
| datastructures.po | Complete | 139 |
| inputoutput.po | Complete | 112 |
| modules.po | Complete | 116 |
| errors.po | Complete | 96 |

Total translated tutorial messages: 859

Infrastructure

* STYLE_GUIDE.md — Complete
* GLOSSARY.md — Complete
* CONTRIBUTING.md — Complete
* GitHub Actions validation workflow — Complete

## Goals

* Translate Python documentation into Punjabi (Gurmukhi)
* Maintain terminology consistency through a shared glossary
* Follow Python documentation translation guidelines
* Ensure translation quality through automated validation
* Build a contributor community around Punjabi translations
* Contribute to the Python documentation translation ecosystem

## Repository Structure

::

```
python-docs-pa-in/
├── README.rst
├── STYLE_GUIDE.md
├── GLOSSARY.md
├── CONTRIBUTING.md
├── .github/workflows/
├── library/
├── reference/
├── tutorial/
├── using/
├── whatsnew/
└── locales/pa-IN/LC_MESSAGES/
```

## Translation Workflow

1. Translate .po files.

2. Validate using::

   ```
   msgfmt --check file.po
   ```

3. Review terminology against `GLOSSARY.md`.

4. Ensure markup and code blocks remain intact.

5. Commit and submit changes.

## References

* Python Documentation Translation Guide:
  https://devguide.python.org/documentation/translations/

* Python Documentation Project:
  https://docs.python.org/

## License

Documentation translations are contributed under the CC0 license.
