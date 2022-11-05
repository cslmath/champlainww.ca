# mkdocs-sandbox

Experimenting and testing mkdocs

[toc]

## 2022-02-27

Initialize project

### git

* git init
    - config looks OK

### poetry

#### install poetry on kappa

* ~~following~~ the [instructions](https://python-poetry.org/docs/master/#installing-with-the-official-installer)
    - `curl -sSL https://install.python-poetry.org >install.python-poetry.py`
    - `py install.python-poetry.py`
        * `Installing Poetry (1.1.13)`
    - add `%APPDATA%\Python\Scripts` to user path
    - `refreshenv` - needs chocolatey
    - poetry --version shows all good
    - [ ] add `venv` alias to cmder
    - reload aliases`alias /reload`

#### Initialize project

* poetry init
* poetry config virtualenvs.in-project true
* (optional)  poetry config --list
* poetry add mkdocs
    - venv && mkdocs --version - all good
* poetry add mkdocs-material

## 2022-03 to 2022-08

* Experimentation
* Transfer in the students' FAQ and how-tos

## 2022-09-17

* More experimentation and editing

    ```bash
    venv        # my custom alias in cmder for .venv/Scripts/activate.bat  in most clis poetry shell is the correct command
    mkdocs serve    # builds the site and previews it on a local address, rebuilds it with changes
    ```

* set up a user github pages repo at `maharper.igthub.com/maharper.github.io`
* make a `gh-pages` branch
* reconfigure so the `gh-pages` branch serves the site
* set the local repo to sync with the gh repo

    ```bash
    git add .
    git commit -m "get the local repo up-to-date"                           # if needed
    git remote add origin git@github.com:maharper/maharper.github.io.git
    git fetch origin
    git merge --allow-unrelated-histories origin/main
    # no problem as there were no conflicts, if there are conflicts ...

    # After more testing

    git push --set-upstream origin main
    # set-upstream only needed the first time of course

    # build the site, push the newly built site to the gh-pages branch on gh.  It's alive!
    mkdocs gh-deploy --force    # when is --force really needed
    ```

* rinse and repeat as needed
* Need a better previewing strategy once the site is live

## 2022-09-18

* update log (this file)
* move mkdocs notes to authors section and start a landing page modelled  
    on the current landing page.
* Add revised date note on each page:
    - `poetry add mkdocs-git-revision-date-localized-plugin`
    - add to `mkdocs.yaml` per [docs](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin)
* Initialize TODO.md

## 2022-09-19

* move courses and status links out of the nav and onto the landing page

## 2022-09-25

* Move the latest news to the announcement bar
    - see TODO.md and git log for details

## 2022-10-23

### content

* some content cleanup
* standardize page names somewhat

### move repo to cslmath

* change test site references to champlainww.ca
* move repo of cslmath/docs.champlainww.ca
* docs.champlainww.ca points to the repo and resolves correctly

### add pg code highlighting

### add page redirects

* add mkdocs-redirects
* configure in mkdocs.yml
    - old page locations point to new page locations
    - /webwork2/ raises a 404, but the 404 page now has a link to the courses

## 2022-11-05

* add Svetla to contacts on index.md
* all page names changed to a `<section>-page-title.md` format
* Add the new landing pages to the site news
* hide all documentation authoring pages
* write an importing classlist page `ins-import-classlist.md`
* some links updated to open in a new page or tab
* editing and cleanup of pages.

## 2022-11-05 - Cutover

* tweak news
* update all links from `docs.champlainww.ca` to `champlainww.ca`
* Write redirects into apache config on `webwork.champlainww.ca`
* update github configuration
* update dns entries to point to github pages
* cutover complete
