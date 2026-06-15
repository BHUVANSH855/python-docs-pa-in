# Punjabi (pa-IN) Python Docs Style Guide

This guide defines translation conventions for the Punjabi translation of Python documentation.

## General Principles

* Translate meaning, not individual words.
* Use clear and natural Punjabi (Gurmukhi).
* Maintain consistency across all files.
* Follow terminology defined in `GLOSSARY.md`.
* Preserve technical accuracy at all times.

---

## Translation Progress Status

The Python Tutorial section has been fully translated and validated.

Contributors should follow the established terminology and translation patterns already present in completed tutorial files before introducing new wording.

---

## Never Translate

### Python Keywords

```text
if
else
elif
for
while
class
def
return
import
from
try
except
finally
raise
pass
with
yield
lambda
and
or
not
```

### Variable Names

```text
x
y
count
user_name
my_list
self
cls
```

### Function, Class, Module, and Exception Names

Examples:

```text
print
len
range
ValueError
TypeError
Exception
list
dict
tuple
set
os
sys
json
```

These names must remain unchanged.

---

## PO File Rules

Never modify:

```text
msgid
#: source references
```

Translate only:

```text
msgstr
```

Preserve placeholders exactly as written:

```text
%s
%d
%r
%s%.*f
{}
{0}
{name}
```

These placeholders must remain unchanged.

---

## RST Markup Preservation

Never modify Sphinx or reStructuredText markup.

Examples:

```rst
:func:`print`
:class:`list`
:mod:`os`
:ref:`section`
:meth:`append`
:attr:`name`
:exc:`ValueError`
:term:`iterator`
```

Translate only surrounding explanatory text.

---

## Inline Markup Preservation

Keep inline markup exactly as written.

Examples:

```rst
*italic*
**bold**
``code``
```

Correct:

```rst
ਇਹ :func:`print` ਫੰਕਸ਼ਨ ਵਰਤਦਾ ਹੈ।
```

Incorrect:

```rst
ਇਹ :func:`ਛਾਪੋ` ਫੰਕਸ਼ਨ ਵਰਤਦਾ ਹੈ।
```

---

## Directives

Preserve directives exactly as written.

Examples:

```rst
.. note::
.. warning::
.. code-block:: python
.. versionadded::
.. versionchanged::
```

Translate the content inside notes and warnings, but never change the directive itself.

---

## Code Blocks

Translate:

* Comments
* User-facing explanatory text

Do not translate:

* Python keywords
* Variable names
* Function names
* Class names
* Module names
* Exception names
* Example code behavior

Example:

```python
# Calculate the square of a number
x = 5
print(x * x)
```

Only the comment may be translated.

---

## Examples and Interactive Sessions

For Python interactive examples:

```python
>>> x = 5
>>> print(x)
5
```

Do not translate:

* Python code
* Output values
* Tracebacks
* Exception names

Only translate surrounding explanatory text.

---

## URLs

Leave all URLs unchanged.

Examples:

```text
https://docs.python.org/
https://devguide.python.org/
```

---

## Technical Terms

When a technical term is widely recognized in English, it may remain untranslated.

Examples:

```text
Python
module
package
API
Unicode
JSON
XML
HTML
HTTP
URL
```

Prefer glossary-approved translations for concepts that already have established Punjabi equivalents.

---

## Terminology

Always consult `GLOSSARY.md` before introducing new translations.

When a technical term already exists in the glossary, use the glossary version consistently throughout the project.

---

## Consistency Rules

* Use the same translation for the same term everywhere.
* Preserve punctuation when possible.
* Preserve formatting and inline markup.
* Keep examples technically correct after translation.
* Reuse terminology from previously completed files whenever possible.

---

## Machine Translation

Machine translation may be used only as a drafting aid.

Every translated string must be manually reviewed for:

* Accuracy
* Terminology consistency
* Natural Punjabi wording
* Correct markup preservation

Contributors are responsible for the final quality of submitted translations.

---

## Translation Quality Checklist

Before committing a translation:

* Verify all msgids have corresponding translations.
* Verify no markup has been altered.
* Verify code examples remain executable.
* Verify placeholders remain unchanged.
* Verify glossary terminology is used consistently.
* Verify formatting matches the source file.
* Complete a manual review of translated content.

---

## Validation Before Commit

Run:

```bash
msgfmt --check tutorial/FILENAME.po
```

Check progress:

```bash
msgfmt --statistics tutorial/FILENAME.po
```

Review untranslated entries:

```bash
msgattrib --untranslated tutorial/FILENAME.po
```

Validate all tutorial files:

```powershell
Get-ChildItem tutorial\*.po | ForEach-Object {
    msgfmt --check $_.FullName
}
```

A translation is considered complete only when:

* 0 validation errors
* 0 untranslated messages
* Consistent glossary usage
* Manual review completed

---

## Commit Message Conventions

Use descriptive commit messages.

Examples:

```text
Translate tutorial/classes.po to Punjabi
Translate tutorial/stdlib.po to Punjabi
Translate tutorial/stdlib2.po to Punjabi (100%)
Update glossary terminology
Update README after tutorial completion
```

---

## Milestone Tags

Major project milestones should be tagged.

Examples:

```text
tutorial-phase-1
tutorial-complete
```

Tags should represent validated translation milestones rather than work-in-progress states.

---

## Tone

* Use formal Punjabi.
* Keep explanations clear and educational.
* Prefer consistency over stylistic variation.
* Follow Python documentation writing conventions whenever possible.
* Prioritize clarity and technical accuracy over literal word-for-word translation.
