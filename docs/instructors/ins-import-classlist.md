---
title: Import a Classlist
authors:
    - Malcolm Harper
date: 2022-11-05
---

# Import a classlist file into a WeBWorK class

## Import a classlist

To import a [properly formatted classlist file](https://webwork.maa.org/wiki/Classlist_Files){: target='_blank'}
into a WeBWorK course:

* In the **File Manager**
    + Browse and select the classlist on your computer
    + Upload it
* In the **Classlist Editor**
    + :material-tab: Go to the _Import_ Tab
    + :material-list-box: _Import users from what file?_ :material-arrow-right: select the file you just uploaded
    + :material-list-box: _Replace which users?_ :material-arrow-right: _no users_ (unless you have good reason to do so)
    + :material-list-box: _Add which new users?_ :material-arrow-right: _any users_
    + :material-button-cursor: Press the _Take Action_ button

## Notes

* The classlist file needs to have fields _student number_, _first name_, and _last name_ at a minimum.
* Fields _email address_ and _section number_ are also useful.
* The classlist file needs to have extension `.lst` to be recognized for import in the **Classlist Editor**.
* You can produce a WeBWorK classlist from an Omnivox classlist with
the Python script [ov2ww.py](https://github.com/maharper/webwork-tools/tree/main/ov2ww){: target='_blank'}.
