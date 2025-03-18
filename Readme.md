# coc-smarty

[Smarty](https://smarty-php.github.io/smarty/stable/) language server extension for [coc.nvim](https://github.com/neoclide/coc.nvim).

Code changed from:

- [Html language server extension](https://github.com/neoclide/coc-html) for [coc.nvim](https://github.com/neoclide/coc.nvim).
- Html extension of [VSCode](https://github.com/Microsoft/vscode/tree/master/extensions/html-language-features)
- VSCode [Smarty Language Server](https://github.com/ssigwart/vscode-smarty).

## Install

In your vim/neovim, run command:

```
:CocInstall coc-smarty
```

## Features

- Completion provider (smarty & html)
- Formatting
- Document Symbols & Highlights
- Document Links
- CSS mode
- Javascript mode

## Configuration options

Checkout `:h coc-configuration` for how to use configurations with coc.nvim.

- `smarty.maxNumberOfDiagnosticMsgs`: Controls the maximum number of diagnostic messages (E.g. XSS warnings) to generate  default: `1000`
- `smarty.disableHtmlAttributeCompletionQuotes`: strip quotes when completing an HTML attribute  default: `false`
- `html.execArgv`:  default: `[]`
- `html.filetypes`:  default: `["html","handlebars","htmldjango","blade"]`
- `html.customData`:  default: `[]`
- `html.completion.attributeDefaultValue`: Controls the default value for attributes when completion is accepted  default: `"doublequotes"`
    Valid options: ["doublequotes","singlequotes","empty"]
- `html.format.enable`: Enable/disable default HTML formatter  default: `true`
- `html.format.wrapLineLength`: Maximum amount of characters per line (0 = disable)  default: `120`
- `html.format.unformatted`: List of tags, comma separated, that shouldn't be reformatted. 'null' defaults to all tags listed at https://www.w3.org/TR/html5/dom.html#phrasing-content  default: `"wbr"`
- `html.format.contentUnformatted`: List of tags, comma separated, where the content shouldn't be reformatted. 'null' defaults to the 'pre' tag  default: `"pre,code,textarea"`
- `html.format.indentInnerHtml`:  default: `false`
- `html.format.preserveNewLines`: Controls whether existing line breaks before elements should be preserved. Only works before elements, not inside tags or for text  default: `true`
- `html.format.maxPreserveNewLines`:  default: `null`
- `html.format.indentHandlebars`:  default: `false`
- `html.format.extraLiners`:  default: `"head, body, /html"`
- `html.format.wrapAttributes`: Wrap attributes  default: `"auto"`
    Valid options: ["auto","force","force-aligned","force-expand-multiline","aligned-multiple","preserve","preserve-aligned"]
- `html.format.wrapAttributesIndentSize`:  default: `null`
- `html.format.templating`: Honor django, erb, handlebars and php templating language tags  default: `false`
- `html.format.unformattedContentDelimiter`:  default: `""`
- `html.suggest.html5`: Configures if the built-in HTML language support suggests HTML5 tags, properties and values  default: `true`
- `html.validate.scripts`: Configures if the built-in HTML language support validates embedded scripts  default: `true`
- `html.validate.styles`: Configures if the built-in HTML language support validates embedded styles  default: `true`
- `html.autoClosingTags`: Enable/disable autoClosing of HTML tags  default: `true`
- `html.autoCreateQuotes`: Enable/disable auto creation of quotes for HTML attribute assignment.  default: `true`
- `html.hover.documentation`: Show tag and attribute documentation in hover  default: `true`
- `html.hover.references`: Show references to MDN in hover  default: `true`
- `html.trace.server`: Traces the communication between coc.nvim and the HTML language server  default: `"off"`
    Valid options: ["off","messages","verbose"]

Trigger completion in `coc-settings.json` for complete list.

## F.A.Q

Q: I can't select the complete item by `<C-n>` and `<C-p>`

A: Some completion item requires insert position after current cursor position
which is invalid for `<C-n>` and `<C-p>` on vim, you can use `<up>` and `<down>`
key for selection, or use api `coc#_select_confirm()` to select and confirm
selection which is recommended.

## Additional useful plugins

* [smarty.vim](https://github.com/shadowwa/smarty.vim) updated syntax, indent and ftplugin
* [vim-textobj-smarty](https://github.com/kana/vim-textobj-smarty/) add textobj
  for smarty, allowing to work on loop and conditional code with `*ak` and on
  content only with `*ik` ([vim-textobj-user](https://github.com/kana/vim-textobj-user)
  is also required)
* [vim-snippets](https://github.com/honza/vim-snippets) is a library of
  snippets for multiple languages, including Smarty. Works with:
  * [snipmate](https://github.com/garbas/vim-snipmate),
  * [ultisnips](https://github.com/SirVer/ultisnips) or
  * [coc-snippets](https://github.com/neoclide/coc-snippets) if you are using [coc](https://github.com/neoclide/coc.nvim)

## License

MIT
