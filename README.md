# Teaching using Jupyter Book

A talk for PyCon Indonesia 2021 entitled Teaching using Jupyter Book.


## Motivation

Most teachers/instructors may have used both slides and notebooks while worrying about switching back and forth between those two before pausing due to confusion.
This talk will introduce Jupyter Book to create beautiful publication-quality teaching materials using only notebooks or markdowns.


## Development


### Requirements

This repository uses Python 3.9, also:
* we use [pyenv](https://github.com/pyenv/pyenv) to manage python version
* we use [pipenv](https://github.com/pypa/pipenv) to manage the virtual environment and packages used in it


### Preparation

Packages and its dependencies are documented in `Pipfile` since we use pipenv.

* First, clone this repository.

```bash
git clone https://github.com/syahrulhamdani/teaching-using-jupyter-book.git
```

* After that, you need to install all packages using below command.

```bash
PIPENV_VENV_IN_PROJECT=1 pipenv install --dev --deploy
```

	This will install all packages including dev packages and sync with `Pipfile.lock`. More detail about this [here](https://pipenv-fork.readthedocs.io/en/latest/advanced.html#using-pipenv-for-deployments).

* To build the book, run below command.

```bash
jb build book
```

	This will generate a `_build` directory where html files exist.

---

Copyright © 2021 Syahrul Hamdani

