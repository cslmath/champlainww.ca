# TODO for CCSL WeBWorK Documentation Site

`TODO.md`

## Dates

Check the date authored in the pages metadata.

- [ ] index.md Perhaps this is different enough to be considered as new
- [ ] news.md  Original date can be 2009-02-01 (to confirm)
- [ ] quotes.md
- [x] students/index.md
- [ ] students/WWstudenttips.md written??  Substantially re-formatted March, 2022.
- [x] students/WWcannotlogin.md
- instructors/
    * [x] index.md
    * [x] WWcreateset.md
    * [x] WWimport-classlist.md (not written yet)
- authors/
    * [x] authors.md
        - [x] move to index.md for consistency (or move the others)
            * Others were moved for now.
        - [x] metadata
    * [x] mkdocs.md
    * [x] mkdocs-vs-pelican.md
- [ ] Add tags to pages
    * see [mkdocs-material-tags](https://squidfunk.github.io/mkdocs-material/setup/setting-up-tags/)
    * The format is

        ``` yaml
        tags:
        - pg
        - perl
        - authoring
        ```

## Authors

- [x] Put page authors into page metadata.

~~The authors are put into the html header, so the names should be complete.~~  
Nope, the author in the html head is the site author from `mkdocs.yml`

In the yaml metadata header:

``` yaml
authors:
    - Malcolm Harper
```

or

``` yaml
authors:
    - Malcolm Harper
    - Michèle Titcombe
```

## Page content

- [x] students/WWstudenttips.md  
    * cleanup copyright notice  
    * do we want to split into multiple pages?
    * keep or lose the toc
- [x] Move 2.17 notice to Announcement bar from landing page
    * link into news page for further information
    * move news page to about section from landing page section
    * hardcoded text colour into `<a>` for now, see if this starts working eventually
- [x] Move quotes to about section
- [x] Write about page
    * started 2022-09-19
- [x] Bring `ww-author-tips-gotchas.md` in from current staging branch
- [x] Add Svetla to contacts on index.md
    * [x] and in `champlain_site_info.txt`
- [x] Add new landing site to news
    * [x] `about/about-news.md`
    * [x] `overrides/main.html`
- [ ] Rewrite `instructors/ins-create-set.md`
- [ ] Add page content from WW Flash Talks Ped Day 2022-11-17
    * [ ] Rémi's Randomization - `author-tips-randomization.md`
        - [x] Permision
        - [x] Page
        - [ ] Review
    * [ ] Peter's New seed for quizzes - `ins-quiz-tips.md`
        - [x] Permision
        - [x] Page
        - [ ] Review
    * [ ] Michèle Custom math achievements - `ins-math-achievements.md`
        - [x] Permision
        - [x] Page
        - [ ] Review
    * [ ] Malcolm's MathQuill - tips and tricks - `student-mathquill.md` and `ins-mathquill.md`
        - [ ] Page
        - [ ] Review

## Decisions

- [x] Copyright for the docs:
    * **cc by-sa** for now
    * gnu free documentation lic or
    * all rights reserved or
- [x] Naming convention for pages
    * `WWcreateset.md` vs `ww-create-set.md`
    * use `ww-create-set.md`
- [x] `<topic>/index.md` or `<topic>/<topic>.md`
    * `<topic>/<topic>.md`
- [ ] Directory links or not (see [MkDocs docs](https://www.mkdocs.org/user-guide/configuration/#use_directory_urls) and material??)
- [ ] Standardize icons for instructions: _radio button_, _button choice_, _check box_, etc
    * and document them in the repo wiki

## New Content

- [ ] MathQuill
- [ ] Achievements glitch
- [ ] Bad links in imported assignments
- [ ] Submitting to the CPL
- [x] Import a WW classlist
    * uncomment in nav
- [ ] Authoring notes for this documentation site
    * write these in GH repo wiki
- [ ] Write README that tells how to develop for this site.

## MkDocs

- [x] Custom 404 page
- [x] WeBWorK icon
- [x] WW favicon
- [x] Configuration [options at MkDocs](https://www.mkdocs.org/user-guide/configuration/)
- [x] and Material for MkDocs
- [ ] How to syntax highlight pg code
    * [ ] For now, how to alias `pg` as `perl`
- [ ] Set up tags in config
- [ ] Set up tags index
- [ ] Configure search options (material options are different from MkDocs)

## Branding

- [x] Colours to match Champlain colours

## Project

- [ ] linting and formating
    * [yamllint?](https://github.com/adrienverge/yamllint)
    * [x] [markdownlint](https://github.com/DavidAnson/markdownlint) in VS Code
- [ ] Move to do items to GitHub issues
