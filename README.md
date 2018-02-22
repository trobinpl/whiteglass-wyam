# whiteglass-wyam
It's a port of Jekyll whiteglass theme to Wyam world

Original theme can be found [in its Github repository](https://github.com/yous/whiteglass)

## Configuration
whiteglass-wyam defines couple configuration options. Add them to your `config.wyam` and set desired values.

### `Settings["ExcerptSeparator"] = "<!--more-->";`
Right now this setting is used only to determine if there should be a "Read more" button. `<!--more-->` is a default post separator for Wyam and as for now, changing this setting will NOT change post separator used during site generation

### `Settings["BlogAuthor"] = "Firstname Lastname";`
This value is displayed in the footer of every page

## Syntax highlighting
Syntax highlighting is turned on by default. It uses Wyam's `Highlight()` module which uses [highlight.js][highlight] under the hood.

[highlight]: https://highlightjs.org/
