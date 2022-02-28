---
title: MkDocs vs Pelican
...


# MkDocs vs pelican

How do the implementations overlap md vs md

[TOC]

## markdown

### Included

| mkdocs | pelican | notes |
|:----|:----|:----|
table |
fenced code blocks |

### Optional

| mkdocs | pelican | notes |
|:----|:----|:----|
admonition

## meta-data

### Formats

mkdocs supports YAML and MultiMarkdown meta-data

#### YAML

```yaml
---
key1: value 1
key2:
    - value 2.1
    - value 2.2
...
```

All keys should be lowercase

#### MultiMarkdown

```
Key1: value 1
Key2: value 2.1
      value 2.2
```

ended by a blankline, case-insensitive



### processed

| mkdocs | pelican | notes |
|:----|:----|:----|
| template |  | the template for the current page |
| title |  | the title for the current document |
