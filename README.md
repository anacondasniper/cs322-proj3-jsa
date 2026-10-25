# Vocab Anagram (AJAX)

A Flask word game: find words from the word list using only the letters in the jumble. Each keystroke is checked against the server with AJAX (jQuery), so the page never reloads.

## Run

From the `vocab/` folder:

```bash
docker build -t jsa-vocab .
docker run --rm -p 5000:5000 jsa-vocab
```

Then open http://localhost:5000.

## How it works

- `vocab/flask_vocab.py`: the `/_check` route takes the typed text and returns JSON (`status`, `word`, `done`).
- `vocab/templates/vocab.html`: jQuery sends the input to `/_check` on each keystroke and updates the page. When enough words are found, it goes to `/success`.

Author: Milo Reynolds
