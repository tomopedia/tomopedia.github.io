# Website structure

All main pages (e.g. 'software', 'algorithms') are found under `main_pages`. 
Pages for individual software packages and algorithms are found inside
folders. For example, the web page for FBP is found under `algorithms/fbp.md`.
All other files are only used for generating the website.

## Adding new pages

When adding new pages, make sure that the header of the page (i.e. the part
between `---`) is changed correctly. The `layout` setting should be `page`,
the `title` setting is the page title, and `permalink` should be the location
that the page is accessible at (e.g. `permalink: aaa/bbb/` would make the page
accessible at `tomopedia.github.io/aaa/bbb/`). As an example, the following
is the header of the FBP page:
```
---
layout: page
title: Filtered Backprojection
permalink: algorithms/fbp/
---
```

## Table formatting

Tables are not really well supported in markdown. The tables we have now render
well, but editing them is quite difficult. To help with editing, you can use a
markdown table editor, for example [this one](https://www.tablesgenerator.com/markdown_tables).
