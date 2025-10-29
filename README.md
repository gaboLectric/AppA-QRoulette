# Question Fate: Live Question Wheel

Question Fate is an interactive wheel designed to keep classes, workshops, and trivia nights moving. Load a plain-text file with question-and-answer pairs, launch the comic-style wheel, and reveal each prompt without repeats. You stay in control of the pacing while the audience stays on their toes.

## Minimum requirements

- Python 3.8 or newer (only to spin up a local server)
- Any modern browser with File API and Web Audio support

## Quick start

```bash
# 1. Grab the code
git clone https://github.com/gaboLectric/AppA-QRoulette.git
cd AppA-QRoulette

# 2. Serve the project locally
python3 -m http.server 8000

# 3. Launch the app
http://localhost:8000/APPA-QRoulette/
```

Feel free to swap `8000` for a different port. Stop the server at any time with `Ctrl+C`.

## How it works

1. Click the upload button and select a `.txt` file with your prompts.
2. Make sure the file keeps one question and answer per line, separated with a pipe (`|`). Example:
   ```
   What is the capital of France? | Paris
   In what year did humans land on the Moon? | 1969
   ```
3. Hit `¡GIRAR!` to spin the wheel. It cycles through numbers before stopping.
4. The chosen question appears instantly. Press the space bar to show the answer.
5. Once you run out of prompts, the app lets you know. Use `REINICIAR` to shuffle the loaded set again.
6. Hit `Salir al Inicio` whenever you want to clear the deck and go back to the upload screen for a fresh file.

Need a shortcut for testing? `sample-questions-fate.txt` ships with a handful of entries.

## Project structure

- `index.html`: main experience with the wheel, tuned for live sessions.
- `question-fate.html`: alternate “question of fate” presentation.
- `sample-questions-fate.txt`: ready-to-use demo questions.

## Technical notes

- Built with plain HTML, CSS, and JavaScript—no frameworks involved.
- Web Audio API powers the spin and victory sound effects.
- The wheel tracks used questions to avoid repeats until the list is exhausted.
- Layout adapts nicely to large displays and mobile screens.

## Future ideas?

- Allow images or multimedia hints alongside the text.
- Persist progress in `localStorage` so you can pause and resume sessions.
- Publish the project on GitHub Pages for quick sharing.

---

Find a bug or have a fresh idea? Open an issue or send a pull request—happy to take a look.