# Contributing to Python Docs Punjabi (pa-IN)

Thank you for contributing to the Punjabi translation of Python documentation.

## Repository Structure

```text
python-docs-pa-in/
├── README.md
├── CONTRIBUTING.md
├── GLOSSARY.md
├── STYLE_GUIDE.md
├── tutorial/
├── library/
├── reference/
├── using/
└── whatsnew/
```

## Workflow

1. Fork the repository.
2. Create a feature branch.
3. Translate or review `.po` files.
4. Validate before committing.
5. Commit your changes.
6. Open a Pull Request.

## Creating a New Translation File

Generate a new `.po` file from the latest CPython gettext template:

```bash
msginit \
  --locale=pa_IN \
  --input=PATH_TO_TEMPLATE.pot \
  --output-file=tutorial/FILENAME.po
```

Example:

```bash
msginit \
  --locale=pa_IN \
  --input=stdlib.pot \
  --output-file=tutorial/stdlib.po
```

## Validation

Run:

```bash
msgfmt --check tutorial/FILENAME.po
```

Check translation statistics:

```bash
msgfmt --statistics tutorial/FILENAME.po
```

View untranslated entries:

```bash
msgattrib --untranslated tutorial/FILENAME.po
```

## Translation Rules

### Do Not Translate

* Python keywords (`if`, `else`, `for`, `while`, `class`, `def`)
* Function names (`print`, `len`, `range`)
* Module names (`os`, `sys`, `json`)
* Exception names (`ValueError`, `TypeError`)
* URLs
* RST roles (`:func:`, `:class:`, `:mod:`, `:ref:`)
* Code blocks

### Translate

* Headings
* Explanatory text
* Notes and warnings
* Comments inside code examples
* User-facing descriptions

## Quality Checklist

Before submitting:

* [ ] All translations completed
* [ ] `msgfmt --check` passes
* [ ] No broken RST markup
* [ ] Terminology follows `GLOSSARY.md`
* [ ] Style follows `STYLE_GUIDE.md`
* [ ] GitHub Actions passes

## Commit Message Examples

```text
Translate tutorial/classes.po to Punjabi (pa)

Translate tutorial/stdlib.po to Punjabi (pa)

Update glossary and translation guidelines
```

## Getting Help

Before translating technical terms, check:

* `GLOSSARY.md`
* `STYLE_GUIDE.md`

For project discussions and coordination, use GitHub Issues or the Python documentation translation community channels.
