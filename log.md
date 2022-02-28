# mkdocs-sandbox

Experimenting and testing mkdocs

[toc]

## 2022-02-27

Initialize project

### git

* git init
    * config looks OK

### poetry

#### install poetry on kappa

* ~~following~~ the [instructions](https://python-poetry.org/docs/master/#installing-with-the-official-installer)
    * `curl -sSL https://install.python-poetry.org >install.python-poetry.py`
    * `py install.python-poetry.py`
        * `Installing Poetry (1.1.13)`
    * add `%APPDATA%\Python\Scripts` to user path
    * `refreshenv` - needs chocolatey
    * poetry --version shows all good
- [ ] add `venv` alias to cmder
    * reload aliases`alias /reload`

#### Initialize project

* poetry init
* poetry config virtualenvs.in-project true
* (optional)  poetry config --list
* poetry add mkdocs
    * venv && mkdocs --version - all good
* poetry add mkdocs-material
