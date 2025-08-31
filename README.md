# Random Quote Generator

A small, lightweight web project that displays random quotes in the browser. The project consists of a simple `Index.html` page and a `Script.js` file that contains the quote logic and DOM manipulation. No build tools or dependencies are required — just a browser.


## Project overview

This project shows one random quote at a time and typically includes a button to generate (or cycle to) a new quote. It's intended as a tiny demo, beginner JavaScript practice, or a component you can embed in another static site.

## Files

- `Index.html` — Main HTML file. Loads UI and includes `Script.js`.
- `Script.js` — JavaScript that holds the quotes, selects a random quote, and performs DOM updates.

(If you add styles later, consider creating `styles.css` and linking it from `Index.html`.)

## How it works

At a high level:

- `Index.html` contains the quote container element(s) and a button to trigger a new quote.
- `Script.js` keeps an array/list of quotes, chooses one at random, and injects it into the DOM.
- The UI is pure HTML/JS; no frameworks, no build step.


## Usage

- Click the button on the page (usually labelled "New Quote" or similar) to get another random quote.
- The display updates in-place.

## Customizing quotes and behavior

To add or change quotes, open `Script.js` in a text editor and locate the array or data structure that contains the quotes. Typical guidance:

- Keep each quote as a single string, or as an object { text: "...", author: "..." } if you want to show authors.
- If using objects, update the DOM injection code to render `quote.text` and `quote.author`.

Example (conceptual):

```js
// ...existing code...
const quotes = [
  {
    text: "Be yourself; everyone else is already taken.",
    author: "Oscar Wilde",
  },
  {
    text: "Simplicity is the ultimate sophistication.",
    author: "Leonardo da Vinci",
  },
];

function showRandomQuote() {
  const q = quotes[Math.floor(Math.random() * quotes.length)];
  // update DOM elements
}
// ...existing code...
```

If you prefer plain strings, adapt accordingly:

```js
// ...existing code...
const quotes = [
  "Be yourself; everyone else is already taken.",
  "Simplicity is the ultimate sophistication.",
];
// ...existing code...
```

Styling: create `styles.css` and link it from `Index.html` to change fonts, colors, layout, or animations.

## Accessibility & UX notes

- Ensure the button has a clear label (e.g., `aria-label="Generate new quote"`) for screen readers.
- Provide sufficient color contrast for quote text and background.
- If quotes can be long, ensure the container can wrap text and remains scrollable/responsive.

## Troubleshooting

- Nothing happens when the button is clicked:

  - Make sure `Script.js` is referenced by `Index.html` and the path is correct.
  - Open the browser DevTools console (F12) to see errors.

- Quotes fail to load or the array is empty:

  - Open `Script.js` and confirm the `quotes` variable contains items.

- Page looks different locally vs. remote:
  - Some browsers restrict fetch/XHR when opening files via `file://`. Use a local HTTP server (see Run locally) to fix this.

## Contributing

Small project—contributions are welcome.

- Fork the repository (or copy the folder).
- Open a branch for your work.
- Make changes (add quotes, styling, accessibility improvements).
- Submit a pull request or share the updated folder.

If you want me to add features, here are some ideas I can implement for you:

- Add `styles.css` with a modern design and responsive layout.
- Add quote authors and citation support.
- Add copy-to-clipboard and share buttons.
- Add animations for transitions between quotes.

Tell me which you'd like and I can implement it directly.

## License

This project doesn't include an explicit license file. If you'd like a permissive license, add a `LICENSE` file containing the MIT license text. Example short line for this repo:

```
MIT License — see LICENSE file
```

---

Happy coding! If you want, I can also:

- add a `styles.css` and improve the UI,
- add unit tests or a small CI workflow,
- or embed author metadata and sharing buttons.

---

## Requirements coverage

- Create a detailed README for this project: Done
