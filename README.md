# Science Sparks — Year 7 flashcards

A responsive, static flashcard site for practising Year 7 science. Questions are
loaded from `questions.json`, so the deck can be updated without changing the
page. Cards are selected at random, can be filtered by topic, and keep each
answer hidden until **Reveal answer** is clicked.

## Run locally

Because the page fetches a JSON file, serve the repository with a local web
server instead of opening `index.html` directly. For example, with Python:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

In the repository's **Settings → Pages**, choose **Deploy from a branch**, set
the branch to `main` and the folder to `/(root)`, then save. GitHub Pages serves
`index.html` and `questions.json` from the same directory; the page uses a
relative JSON URL so it also works when published under a project-site path.

## Update the question bank

Edit `questions.json`. Each entry must have `topic`, `question`, `answer`, and
`distractor` strings. The distractor is the incorrect test choice for that
question. The topic filter is populated from the topics present in the file.