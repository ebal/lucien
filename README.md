# Lucien

A minimal, cross-platform, graphical [Markdown][] text editor built with [Electron.js](https://commonmark.org/)

## Screenshot

TODO

## Features

- Way less than 1000 [SLOC](https://en.wikipedia.org/wiki/Source_lines_of_code)
- Support for [GitHub Flavored Markdown](https://github.github.com/gfm/)
- Support for smart punctuation with [SmartyPants](https://daringfireball.net/projects/smartypants/)
- Split view with Markdown text on the left and the HTML result on the right
- Code syntax highlighting in HTML view
- Synchronized scrolling between views
- Automatic view split orientation (horizontal/vertical) based on window layout
- Open file with drag & drop
- Export Markdown document to a standalone HTML file

## Anti-features

Things that have been left out intentionally:

- No toolbar or buttons. Functionality is invoked from the app menu and through keyboard shortcuts.
- No [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) interface for Markdown text (button for bold, italics, etc)
- No syntax highlighting in Markdown view
- No file browsing, just a regular "open file" dialog
- No tags or categories. Files may be organized in filesystem directories instead.

## Installation

Lucien uses the [Hack](https://sourcefoundry.org/hack/) and [Open Sans](https://fonts.google.com/specimen/Open+Sans) fonts for the Markdown and HTML view respectively. To install them in Ubuntu/Debian Linux, issue:

```shell
sudo apt install fonts-open-sans fonts-hack-ttf
```

If the fonts are missing, it will fall back to the system's `monospace` and `sans-serif` declared fonts, but the visual end result may not be as good.

Clone the repository:

```shell
git clone https://github.com/agorf/lucien.git
```

Enter the checked-out directory:

```shell
cd lucien/
```

Install the dependencies:

```bash
yarn install # or npm install
```

Run the app:

```bash
yarn start # or npm start
```

If you get an error about sandboxing in Linux, follow its instructions or issue:

```
sudo sysctl kernel.unprivileged_userns_clone=1
```

To persist this after a reboot, you have put it (without the `sudo` prefix) in `/etc/sysctl.conf`

## Use

TODO

### Desktop file

TODO

### Keyboard shortcuts

Pretty standard:

|Shortcut|Functionality|
|--------|-------------|
|`Ctrl+N`|new file|
|`Ctrl+O`|open file|
|`Ctrl+S`|save file|
|`Ctrl+Q`|quit app|
|`Ctrl+C`|copy selected text|
|`Ctrl+V`|paste selected text|
|`Ctrl+X`|cut selected text|
|`Ctrl+A`|select all text|
|`Ctrl+Z`|undo last change|
|`Ctrl+Shift+Z`|redo last change|

### From the command-line

Pass the path of a single Markdown document to the Lucien executable to edit it:

```shell
./Lucien /path/to/my-file.md
```

## Acknowledgements

Lucien was inspired by the following projects and resources:

- [Notable](https://github.com/notable/notable) (a bit bloated and no longer open-source)
- [Dillinger](https://dillinger.io/) (web-based)
- [Steve Kinney's "Electron Fundamentals v2" course](https://frontendmasters.com/courses/electron-v2/)
- Lucien, the cat

## License

[MIT](https://github.com/agorf/lucien/blob/master/LICENSE.txt)

## Author

[Angelos Orfanakos](https://angelos.dev)

[Markdown]: https://commonmark.org/
