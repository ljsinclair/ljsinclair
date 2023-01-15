# Convert Markdown to .docx using Pandoc, Pulsar edit and packages

This solution works for [Pulsar edit](https://pulsar-edit.dev) which is an open-source fork of the now discontinued Atom editor.

## Objective

Write single-source content in markdown then convert to MS Word for distribution to others.

NOTE: Pandoc can output to other formats

### Before you begin

* [Install the latest version of Pulsar Edit](https://pulsar-edit.dev/download.html)
* [Install Pandoc](https://pandoc.org/) on your machine
* [Install python on your computer]((https://www.python.org/downloads/) -- this is required by Pandoc convert plus.
* [Install Pandoc convert plus](https://web.pulsar-edit.dev/packages/pandoc-convert-plus)
* [Install Pandoc interface yaml](https://web.pulsar-edit.dev/packages/pandoc-interface-yaml)

### Step 1 - add YAML

NOTE: This YAML will result in an MS Word document that uses the built-in `normal.dot` template, available where ever MS Word is installed.

Add the following YAML to your markdown file

```
---
export-path: 'filename.docx'
export-format: 'docx'
title: 'page title'
---
```

Where:
* export-path = the destination file
* export-format = convert markdown to this file format
* title = page title that appears at the top of the page

### Step 2 - Convert the content

* Choose Packages > Pandoc interface > Export

## Further reading

* [Pandoc documentation](https://pandoc.org/MANUAL.html) explains other flags and settings to choose when converting markdown to another format
* [Why use Markdown instead of MS Word?](https://www.slashgear.com/776429/what-is-markdown-and-why-should-you-use-it-instead-of-microsoft-word/)

## Further information

* [Pandoc export options](https://pandoc.org/org.html#export-options) - this list should work in the YAML header.
