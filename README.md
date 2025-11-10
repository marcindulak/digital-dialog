> Co-Authored-By: Claude

# Functionality overview

Interactive security awareness dialogues and quizzes for phone and internet.

The system supports multiple languages, with each language having its own dialogue content and quiz questions embedded in a single README file.

# Usage examples

## View dialogues and take quizzes online

Visit the hosted version at GitHub Pages (or serve `index.html` using a web-server locally):

```bash
python -m http.server 8000 --bind 127.0.0.1
```

Then open http://localhost:8000 in your browser.

## Switch languages

The interface defaults to Polish. To switch languages:
- Use the language selector in the UI
- Or append `?lang=en` to the URL for English

## Read dialogues on GitHub

Navigate to the language-specific README file:
- English: [README.en.md](README.en.md)
- Polish: [README.pl.md](README.pl.md)

Quiz questions are embedded in `<details>` tags for show/hide functionality.

# Implementation overview

## File structure

```
digital-dialog/
├── README.md              # Project documentation (this file)
├── README.en.md           # English: dialogues + quiz
├── README.pl.md           # Polish: dialogues + quiz
└── index.html             # Multi-language web interface
```

# Adding a new language

1. Create `README.{langcode}.md` (e.g., `README.de.md` for German), based on the English `README.en.md` file
2. Add an entry to the `languageConfig` object in `index.html`
3. Add an option to the language dropdown `<select>` element in `index.html`
4. Keep dropdown options in alphabetical order by language name

# Running tests

No automated tests are currently implemented for this project.

# Abandoned ideas
