# AsciiDoc mode for CodeMirror

This repository contains the AsciiDoc mode for CodeMirror.

## Installation

```
$ npm install codemirror-asciidoc
```

## Usage for CM5 with `codemirror-asciidoc@1.x`

```js
var codemirror = require("codemirror"),
  codemirror_asciidoc = require("codemirror-asciidoc");

codemirror.fromTextArea(document.getElementById("editor"), {
  lineNumbers: true,
  lineWrapping: true,
  mode: "asciidoc"
});
```

## Usage for CM6 with `codemirror-asciidoc@2.x`

```js
import {StreamLanguage} from "@codemirror/language"
import {asciidoc} from "codemirror-asciidoc"

import {EditorView, EditorState, basicSetup} from "@codemirror/basic-setup"

let view = new EditorView({
  state: EditorState.create({
    extensions: [basicSetup, StreamLanguage.define(asciidoc)]
  })
})
```

## License

BSD

## Credits

The AsciiDoc mode for CodeMirror was generated from the AsciiDoc mode for Ace using the https://github.com/espadrine/ace2cm[ace2cm] project by https://github.com/espadrine[Thaddee Tyl].
