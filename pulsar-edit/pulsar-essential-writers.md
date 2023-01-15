# Essential packages for writers using pulsar edit

I've been using Pulsar edit (and predecessor Atom edit) to write markdown content for about five years and have found these packages essential to my workflow.

They're in addition to the [pulsar essential packages](https://github.com/ljsinclair/ljsinclair/blob/main/pulsar-edit/pulsar-essential-writers.md) I also use.

## Core packages that are really useful

These are mentioned because it's useful to know they're available.

### Find and replace

Search a file that's open or all files in the project.

* [find and replace](https://web.pulsar-edit.dev/packages/find-and-replace)

### Spell-check

This is a nice core feature and you can choose a locale (regional language), plus the system allows you to add words to the local dictionary.

* [Spell check package](https://web.pulsar-edit.dev/packages/spell-check)

## Add footnotes with ease

*Markdown footnote* gives you a RH-click menu that automatically creates footnotes with:

* a random character designation
* a paired footnote at the end of the file

Footnotes are Pandoc ready, and also work on Github.

* [Markdown footnote](https://web.pulsar-edit.dev/packages/markdown-footnote)

## Conceptualising ideas with a mind-map

Sometimes it's useful to be able to conceptualise what you want to write, or to verify existing content is in a logical order. Mind maps are one way to do this, but many of the tools are stuffed with features which IMO get in the way of doing the task.

*Markdown mindmap* makes this much simpler and allows you to:

* Add headings to a new markdown file to build your structure
* Create a mind-map view of an existing markdown file, a little like Outline view in MS Word.

* [Markdown mindmap](https://web.pulsar-edit.dev/packages/markdown-mindmap)

## How many words in the file?

It's useful to know how many words are in a file and essential when writing essays for school and further education, or articles for websites, news services or magazines.

The *Wordcount* package inserts two running counters in the Pulsar-edit toolbar:
* total words
* total characters

* [Wordcount](https://web.pulsar-edit.dev/packages/wordcount)

## Single source content then output to other formats

One of my bugbears is being forced to wrestle with software to perform a task rather than doing the job of writing the content.

But the world is in love with MS Word, Content Management Systems, and site builders like Jekyll or Hugo. So what's a writer to do?

*Pandoc* is a third party tool that can convert plain text markdown files to **everything else** (and in some cases, in the other direction). It also handles LaTex.

* [Learn about Pandoc](https://pandoc.org/)

Ironically enough, because Pandoc is so powerful I've found it complicated to use, and I avoided it until I discovered *Pandoc Convert Plus* and *Pandoc interface YAML*.

* [Pandoc Convert Plus](https://web.pulsar-edit.dev/packages/pandoc-convert-plus) allows you to use Pandoc from within Pulsar edit.
* [Pandoc interface YAML](https://web.pulsar-edit.dev/packages/pandoc-interface-yaml) makes the process **far** easier by allowing you to add Pandoc settings as YAML at the top of any file you wish to convert.

IMPORTANT: I also needed to [install Python](https://www.python.org/downloads/) to make the packages work.

## But I just want to output to PDF!

There's a package for that, too!

* [markdown-pdf](https://web.pulsar-edit.dev/packages/markdown-pdf)

## Some other tips and tricks

### Deactivate autocomplete

Some people find autocomplete useful, but I find it distracting.

* Click Packages > Open Package Manager.
* Enter *autocomplete-plus* into the filter field
* Click **Disable** on the autocomplete-plus package.

### Copy blank line

I don't know what the use case for this is, but it's possible to accidentally copy blank lines.

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

Here's how to turn them on by default in Pulsar edit, and widen them so they're functional.

First, edit the stylesheet:
* on Windows -- File > Stylesheet
* On Linux -- Edit > Stylesheet

Then add the following to the end of the Stylesheet.
* Make changes to the width and background colors as desired.
* Save when ready.

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
