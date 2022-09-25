TODO.md

# TODO for CCSL WeBWorK Documentation Site

## Dates

Put date authored into the page metadata
for every page brought over from a previous incarnation of the site.
Confirm metadata is there.

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
    * [ ] authors.md
        - [ ] move to index.md for consistency (or move the others)
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

## Page content

- [ ] students/WWstudenttips.md  
    * cleanup copyright notice  
    * do we want to split into multiple pages?
    * keep or lose the toc
- [x] Move 2.17 notice to Announcement bar from landing page
    * link into news page for further information
    * move news page to about section from landing page section
    * hardcoded text colour into `<a>` for now, see if this starts working eventually
- [x] Move quotes to about section
- [ ] Write about page
    * started 2022-09-19
- [x] Bring `ww-author-tips-gotchas.md` in from current staging branch

## Decisions

- [ ] Copyright for the docs:
    * cc by-sa or
    * gnu free documentation lic or
    * all rights reserved or
- [ ] Naming convention for pages
    * `WWcreateset.md` vs `ww-create-set.md`
- [x] `<topic>/index.md` or `<topic>/<topic>.md`
    * `<topic>/<topic>.md`
- [ ] Directory links or not (see [MkDocs docs](https://www.mkdocs.org/user-guide/configuration/#use_directory_urls) and material??)

## New Content

- [ ] MathQuill
- [ ] Achievements glitch
- [ ] Bad links in imported assignments
- [ ] Submitting to the CPL
- [ ] Import a WW classlist
    * uncomment in nav
- [ ] Authoring notes for this documentation site
- [ ] Write README that tells how to develop for this site.

## MkDocs

- [ ] Custom 404 page
- [ ] WeBWorK icon
- [ ] WW favicon
- [ ] Configuration [options at MkDocs](https://www.mkdocs.org/user-guide/configuration/)
- [ ] and Material for MkDocs
- [ ] How to syntax highlight pg code
    * [ ] For now, how to alias `pg` as `perl`
- [ ] Set up tags in config
- [ ] Set up tags index

## Branding

- [ ] Colours to match Champlain colours

## Project

- [ ] linting and formating
    * yamllint? (https://github.com/adrienverge/yamllint)
    * markdownlint
