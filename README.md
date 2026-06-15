# Guitar Chords by Intervals (Semitones) — Poster

Editable rebuild of the chords-in-semitones reference poster.

## 🔗 View it live

**[Open the poster →](https://kolov.github.io/guitarchords-poster/)**

(Served from `index.html` via GitHub Pages.)

## Files

| File | What it is |
|------|------------|
| `index.html` | **The editable source.** Open in any browser or text editor. |
| `chords in semitones.pdf` | Vector PDF exported from the HTML — crisp at any zoom, text is selectable. |
| `original.png` | The original flattened image, kept for reference. |

## How to edit

1. Open `index.html` in a text editor.
2. **Text** — edit it directly inline (chord names, formulas, notes).
3. **Colours** — change the CSS variables in the `:root { ... }` block at the
   top of the `<style>` section. Every colour in the poster (backgrounds,
   section header bars, note role colours) is defined there once.
   - `--root --n3 --n5 --n7 --n9` = note colours by interval role
   - `--h-blue --h-green --h-tan ...` = section header bar colours
4. Open the file in a browser to preview.

## Re-export the PDF

Either: open in a browser → **Print → Save as PDF**.

Or with headless Chrome:

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --disable-gpu --no-pdf-header-footer \
  --print-to-pdf="chords in semitones.pdf" \
  "index.html"
```

(File-URL access may be blocked; serve the folder first with
`python3 -m http.server` and point Chrome at `http://localhost:8000/index.html`.)
