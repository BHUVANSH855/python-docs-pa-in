# Punjabi (pa) Python Docs Style Guide

This guide defines translation conventions for the Punjabi (India) translation of the Python documentation.

All contributors should follow these rules to ensure consistency, technical accuracy, and long-term maintainability across the project.

---

# Project Status

Current verified milestones:

* ✅ Complete Tutorial documentation translated (16/16 files)
* ✅ `bugs.po` fully translated
* ✅ `library/functions.po` fully translated
* ✅ `library/stdtypes.po` fully translated
* ✅ Repository-wide validation passing
* ✅ GitHub Actions validation workflow active
* ✅ Shared glossary established
* ✅ More than 3,500 documentation messages translated

Contributors should review previously completed translations before introducing new terminology or translation patterns.

---

# General Principles

* Translate meaning, not individual words.
* Use natural and clear Punjabi (Gurmukhi).
* Preserve technical accuracy.
* Prefer consistency over stylistic variation.
* Follow terminology defined in `GLOSSARY.md`.
* Reuse existing translations whenever possible.
* Match the tone of official Python documentation.

---

# Translation Philosophy

The goal is not literal translation.

The goal is to produce documentation that feels natural to Punjabi-speaking developers while remaining technically identical to the English original.

Good translation:

```text
Clear
Accurate
Consistent
Natural
```

Poor translation:

```text
Word-for-word
Ambiguous
Inconsistent
Artificial sounding
```

---

# Never Translate

## Python Keywords

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
global
nonlocal
async
await
match
case
```

---

## Built-in Names

```text
print
len
range
list
dict
tuple
set
frozenset
bytes
bytearray
str
int
float
complex
bool
object
type
property
classmethod
staticmethod
```

---

## Exception Names

```text
Exception
ValueError
TypeError
KeyError
IndexError
ImportError
RuntimeError
AttributeError
StopIteration
```

---

## Standard Library Names

```text
os
sys
json
pathlib
re
typing
collections
itertools
asyncio
```

These identifiers must remain unchanged.

---

# Variable Names

Never translate variable names.

Examples:

```python
x
y
count
index
user_name
my_list
self
cls
```

Correct:

```python
count = 5
```

Incorrect:

```python
ਗਿਣਤੀ = 5
```

---

# PO File Rules

Never modify:

```text
msgid
#: source references
#, flags
```

Translate only:

```text
msgstr
```

---

# Placeholder Preservation

Placeholders must remain exactly unchanged.

Examples:

```text
%s
%d
%i
%r
%f
%s%.*f
```

```text
{}
{0}
{name}
{value}
```

```text
%(name)s
%(count)d
```

Correct:

```text
"%s ਆਈਟਮ ਮਿਲੇ"
```

Incorrect:

```text
"%d ਆਈਟਮ ਮਿਲੇ"
```

unless the original uses `%d`.

---

# RST Markup Preservation

Never modify reStructuredText roles.

Examples:

```rst
:func:`print`
:class:`list`
:class:`dict`
:mod:`os`
:meth:`append`
:attr:`name`
:exc:`ValueError`
:term:`iterator`
:ref:`section`
```

Translate only surrounding text.

Correct:

```rst
ਇਹ :func:`print` ਫੰਕਸ਼ਨ ਦੀ ਵਰਤੋਂ ਕਰਦਾ ਹੈ।
```

Incorrect:

```rst
ਇਹ :func:`ਛਾਪੋ` ਫੰਕਸ਼ਨ ਦੀ ਵਰਤੋਂ ਕਰਦਾ ਹੈ।
```

---

# Inline Markup Preservation

Keep inline markup unchanged.

Examples:

```rst
*italic*
**bold**
``code``
```

Do not modify formatting syntax.

---

# Directives

Never modify Sphinx directives.

Examples:

```rst
.. note::
.. warning::
.. important::
.. tip::
.. versionadded::
.. versionchanged::
.. deprecated::
.. code-block:: python
```

Translate the directive content only.

---

# Code Blocks

Translate:

* Comments
* Explanatory text

Do not translate:

* Python code
* Keywords
* Identifiers
* Module names
* Function names
* Class names
* Exception names

Example:

```python
# Calculate the square of a number
x = 5
print(x * x)
```

Only the comment may be translated.

---

# Interactive Python Sessions

Examples:

```python
>>> x = 5
>>> print(x)
5
```

Do not translate:

* Code
* Output
* Tracebacks
* Exception names

Translate only surrounding explanations.

---

# URLs

Never translate URLs.

Examples:

```text
https://docs.python.org/
https://devguide.python.org/
https://github.com/python/cpython
```

---

# Version Information

Never modify version numbers.

Examples:

```text
Python 3.13
Python 3.14
Changed in version 3.12
Deprecated since version 3.11
```

Translate surrounding text only.

---

# Technical Terms

Some technical terms should remain in English.

Examples:

```text
Python
API
Unicode
JSON
XML
HTML
HTTP
URL
ASCII
UTF-8
```

Use glossary-approved Punjabi translations where available.

---

# Terminology Consistency

Always consult:

```text
GLOSSARY.md
```

before introducing new terminology.

If a term already exists in the glossary:

* Use the glossary translation.
* Do not create alternatives.
* Do not switch wording between files.

Consistency is more important than personal preference.

---

# Batch Translation Workflow

For large files, translations should be performed in reviewable batches.

Recommended format:

```text
Replace this block:

msgid "example"
msgstr ""

With:

msgid "example"
msgstr "ਉਦਾਹਰਨ"
```

For multiple consecutive entries:

```text
Replace these consecutive blocks:
...
```

This workflow was successfully used for:

```text
library/functions.po
library/stdtypes.po
```

and is recommended for future large files.

---

# Machine Translation Policy

Machine translation may be used only as a drafting aid.

Every translation must be manually reviewed.

Contributors remain responsible for:

* Accuracy
* Technical correctness
* Terminology consistency
* Markup preservation
* Natural Punjabi wording

No untranslated machine output should be committed.

---

# Translation Quality Checklist

Before committing:

* Verify all intended strings are translated.
* Verify placeholders remain unchanged.
* Verify markup remains unchanged.
* Verify code examples remain executable.
* Verify glossary terminology is followed.
* Verify formatting matches the source.
* Complete a manual review.

---

# Validation Commands

Validate a file:

```bash
msgfmt --check FILE.po
```

Show statistics:

```bash
msgfmt --statistics FILE.po
```

Show untranslated entries:

```bash
msgattrib --untranslated FILE.po
```

Show translated entries:

```bash
msgattrib --translated FILE.po
```

---

# Repository-Wide Validation

Validate all files:

```powershell
Get-ChildItem -Recurse -Filter *.po | ForEach-Object {
    msgfmt --check $_.FullName
}
```

A completed file should have:

```text
0 validation errors
0 fuzzy entries
0 untranslated messages
```

---

# Commit Message Conventions

Use descriptive commit messages.

Examples:

```text
Translate tutorial/classes.po to Punjabi
Translate tutorial/floatingpoint.po to Punjabi
Translate tutorial/venv.po to Punjabi
Translate library/functions.po to Punjabi
Translate library/stdtypes.po to Punjabi
Update glossary terminology
Update README statistics
Update project documentation
```

---

# Milestone Tags

Major validated milestones should be tagged.

Examples:

```text
tutorial-phase-1
tutorial-complete
v1.0-tutorial-complete
library-functions-complete
library-stdtypes-complete
```

Tags should represent completed, validated work.

---

# Contributor Expectations

Before starting a new file:

1. Review `GLOSSARY.md`
2. Review this Style Guide
3. Review completed translations
4. Validate frequently
5. Commit in logical batches
6. Keep terminology consistent

---

# Tone and Writing Style

Documentation should be:

* Formal
* Educational
* Clear
* Consistent
* Professional

Avoid:

* Slang
* Regional dialect variations
* Excessively literal translations
* Unnecessary English/Punjabi mixing

When in doubt:

```text
Clarity > Literal Translation
Consistency > Personal Preference
Accuracy > Style
```

---

# Final Rule

Every translation should satisfy three requirements:

```text
Technically correct
Consistent with the project glossary
Natural for Punjabi readers
```

If any of these are missing, revise the translation before committing.
