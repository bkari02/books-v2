# senseBox version 2 Books

This repository contains the gitbook sources for the documentation and OER regarding the <b>second version of senseBox</b> (for first version of senseBox see [here](https://github.com/sensebox/books)).

There are seperate branches for editing each book inside this repository. 
There are four books until now:
- <b>[senseBox:edu-book](https://github.com/sensebox/books-v2/tree/edu)</b> in branch called "edu" hosted [here](https://sensebox.github.io/books-v2/edu).
- <b>[senseBox:home-book](https://github.com/sensebox/books-v2/tree/home)</b> in branch called "home" hosted [here](https://sensebox.github.io/books-v2/home).
- <b>[senseBox:osem-book](https://github.com/sensebox/books-v2/tree/osem)</b> in branch called "osem" hosted [here](https://sensebox.github.io/books-v2/osem).
- <b>[senseBox:blockly-book](https://github.com/sensebox/books-v2/tree/blockly)</b> in branch called "blockly" hosted [here](https://sensebox.github.io/books-v2/blockly).

There is also a <b>[gh-pages branch](https://github.com/sensebox/books-v2/tree/gh-pages)</b>, where all the builded gitbooks are stored and hosted from. To avoid redundant data all pictures used in all senseBox books are stored in one single pictures-folder in the gh-pages branch.

## Contribution 

### Development environment
We use the node.js-based tool [GitBook](https://github.com/GitbookIO/gitbook) for rendering of the content.

### Command line
To live-preview or render a book, you need the npm package `gitbook-cli`.
Install it by running `npm i -g gitbook-cli`. If that does not work or you do not have `npm`, have a look at the [official documentation](https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md).
Clone this repository with the following command:
```
$ git clone https://github.com/sensebox/books-v2.git
```
to your computer. Change into the created folder with:
```
$ cd books-v2
```

#### Live preview
To get a live preview of a books website-output, run:
```
gitbook install   # only required once
gitbook serve
```

#### Render to disk
GitBook provides the output formats `website`, `pdf` and `ebook`.
To render a book run:
```
gitbook install   # only required once

gitbook build     # build the website
gitbook pdf       # build the pdf
gitbook epub      # build the ebook
```

## Repository structure
Each (multilingual) book resides on its own branch.
Currently these are `edu`,`home`, `osem` and `blockly`, each containing a `de` and `en` language book.

The german versions have far more content, while the english versions are steadily supplemented from there.

Files that are parsed specially by GitBook have a filename in caps:

- `LANGS.md`:  defines the languages of a multilingual book
- `README.md`: the landingpage of a book, eg an introduction
- `SUMMARY.md`: the table of contents, rendered as the left navbar
- `GLOSSARY.md`: a glossary, whose terms are referenced on all other book pages
- `FOOTER.md`: the page footer on any page

Stylesheets applied on all books are in `./styles`, and are symlinked into each book (unix only).

### Deployment
Currently the books are built and hosted by [gitbook.com](https://sensebox.github.io/books-v2/).
A commit on each of the <bookname> branches does not automatically triggers a new build of the book there.
Instead the builds of a book will be renewed by senseBox staff. Please keep in mind, to store all pictures in the gh-pages branch and not in the book's branch itself.

The pdf builds however are built on travis to support custom cover pages. These builds are autocommited into the `gh-pages` branch.

## License
- Content: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- Code: Apache

See [LICENSE](https://github.com/sensebox/books-v2/raw/master/LICENSE) file.
