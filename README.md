# AI at Work

Understand how AI really works, write prompts that get good results, check what it tells you, and use it safely in everyday work. No coding needed. For developers, see Effective Vibecoding.

Part of the [Yaaddi](https://github.com/yaaddi-courses) course catalog — a
spaced-repetition flashcard course, ready to build and validate with the
standard Yaaddi course tooling.

## Structure

- `meta.json` — course metadata (title, description, cover image, version)
- `source/` — authoring source (`meta.csv`, `units.csv`, `cards.csv`, `glossary.csv`, images/media)
- `plan.csv` — table of contents (not shipped in the zip)
- the built `.zip` — generated from `source/` via `build_course_zip.py`

## Editing this course

```bash
python validate_course.py . --source
python build_course_zip.py .
```
