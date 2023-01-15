# Pulsar packages for writing documentation

This list of packages should help when writing documentation.

## Create nested ASCII lists

It's useful to visually describe things like a directory structure.

Up until now, I've copy/pasted Unicode characters which was a bit laborious. Enter *Tree package* which converts selected text to a tree view, and turns each indented line to a node on the tree.

For example:

```
first node
  second node
  third node
```
Select the text then press CTRL+ALT+T to convert:
```
first node
├── second node
└── third node
```

* [Tree view](https://web.pulsar-edit.dev/packages/tree)

If the ASCII characters don't meet your needs, you can add new ones in the package settings.

NOTE: There's also [ASCII tree](https://web.pulsar-edit.dev/packages/ascii-tree) which converts based on `+--` characters and the indent.
