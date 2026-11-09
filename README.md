# NGN 112 PyLab: exam version

This is the same Colab-style notebook as `../PyLab`, stripped down for exams:

- When a student opens it, they see only a "Welcome to NGN 112 PyLab" text cell and a `print("Hello, World!")` cell.
- There's no Examples menu, no lecture notebooks, and no bundled datasets (`iris.data`, `student_scores.csv`,
  California housing). `?example=` and `?nb=` links are ignored.
- Its saved work is kept separately from the regular PyLab, even when both are hosted on the same `github.io` site,
  so an exam never shows a student's lecture notebooks.

Everything else works as in the regular PyLab: numpy, pandas, matplotlib, seaborn, scikit-learn, mlxtend,
`input()`, the Files panel for uploads, autosave, and Download .ipynb.

Notes:

- scikit-learn's own built-in toy datasets (`load_iris`, `load_diabetes`, `make_classification`, …) are part of the
  library and still work. `fetch_california_housing()` needs an internet download and won't work in the browser.
- `app.js`, `runner.js` and `style.css` are identical to the regular PyLab's. Only `index.html` differs: it sets
  `window.PYLAB_EXAM = true` and doesn't load `examples.js` or `datasets.js`. After changing the shared files in
  `../PyLab`, copy them here.

## Publishing

Publish it the same way as the regular PyLab (see `../PyLab/README.md`), in a second repository, for example
`pylab-exam`. Students then open `https://<username>.github.io/pylab-exam/`.
