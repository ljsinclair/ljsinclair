# Essential packages for writers using pulsar edit

See also [pulsar essential packages]()

## Core packages that are really useful

I mention these because they're useful to know are there.

### Find and replace

Search a file that's open or all files in the project.

* [find and replace](https://web.pulsar-edit.dev/packages/find-and-replace)

### Spell-check

This is a nice core feature and you can choose a locale (regional language), plus the system allows you to add words to the dictionary which is saved locally.

* [https://web.pulsar-edit.dev/packages/spell-check]

## Add footnotes with ease

Markdown footnote gives you a rh-click menu that automatically creates footnotes with:

* a random character designation
* a paired footnote at the end of the file

Footnotes are Pandoc ready, and also work on Github.

* [Markdown footnote](https://web.pulsar-edit.dev/packages/markdown-footnote)

## Conceptualising ideas with a mind-map

Mind mapping tools can be cumbersome and tend to be stuffed with features that IMO get in the way of the job of conceptualising ideas.

Markdown mindmap makes this much simpler. Every heading level represents a node in a tree and you can create mindmaps on the fly in new markdown files, or use the package to create a mindmap from an existing file.

* [Markdown mindmap](https://web.pulsar-edit.dev/packages/markdown-mindmap)

## How many words in the file?

Wordcount is sometimes essential when writing content such as articles or essays, but it's also useful to know when writing in general.

The Wordcount package inserts two running counters in the Pulsar-edit toolbar:
* total words
* total characters

* [Wordcount](https://web.pulsar-edit.dev/packages/wordcount)

## Single source content then output to other formats

One of my bugbears is being forced to wrestle with software to perform a task rather than doing the job of writing the content.

But the world is in love with MS Word, Content Management Systems, and site builders like Jekyll or Hugo. So what's a writer to do?

Pandoc is a system that will output plain text markdown files to **everything else**, including MS Word, PDF, HTML and more. It also handles LaTex.

* [Learn about Pandoc](https://pandoc.org/)

The irony of Pandoc is because the software is **so** powerful, it's also **extremely** complex to use. Which once again gets in the way of doing the writing.

Pandoc Convert Plus coupled with Pandoc interface YAML fixed this problem for me.

NOTE: You'll also need to [install Python](https://www.python.org/downloads/) to make the packages work.

* [Pandoc Convert Plus](https://web.pulsar-edit.dev/packages/pandoc-convert-plus) allows you to use Pandoc from within Pulsar edit.
* [Pandoc interface YAML](https://web.pulsar-edit.dev/packages/pandoc-interface-yaml) makes the process **far** easier by allowing you to add Pandoc settings as YAML at the top of any file you wish to convert.

## But I just want to output to PDF!

There's a package for that, too!

* [markdown-pdf](https://web.pulsar-edit.dev/packages/markdown-pdf)

## Some other tips and tricks

### Autocomplete-plus

Some people find autocomplete useful, but I find it distracting so deactivate the [autocomplete-plus](https://web.pulsar-edit.dev/packages/autocomplete-plus) package

### Copy blank line

I don't know what the use case for this is, but it's possible to copy blank lines.

Switch this off in the keymap settings which are accessed:

* On Windows -- File > Keymap
* On Linux -- Edit > Keymap

Then paste following at bottom and save.

```
'body':
    'cmd-c': 'editor:copy-selection'   # mac os
    'ctrl-c': 'editor:copy-selection'  # linux and windows
```

## Scrollbar widths

There's been a strange obsession in applications over the past few years to remove, hide or make scrollbars so narrow they're virtually useless.

Edit the stylesheet:
* on Windows -- File > Stylesheet
* On Linux -- Edit > Stylesheet

```
//* widen scrollbars and make visible always */

.scrollbars-visible-always {
  ::-webkit-scrollbar {
    width: 12px;
    height: 12px;
    &-track {
        border: 0px;
        border-radius: 0px;
        background-color: #444 !important;
    }
    &-thumb {
        background-color: rgba(255,200,200,0.35) !important;
        border: 0px;
        border-radius: 9px;
    }
  }
}
```

---
[^7837]: In short, I like to keep things simple.
