# fileheader README

This is the README for your extension "fileheader". After writing up a brief description, we recommend including the following sections.

## Features

Describe specific features of your extension including screenshots of your extension in action. Image paths are relative to this README file.

For example if there is an image subfolder under your extension project workspace:

\!\[feature X\]\(images/feature-x.png\)

> Tip: Many popular extensions utilize animations. This is an excellent way to show off your extension! We recommend short, focused animations that are easy to follow.

## Requirements

default configuration

```
	"fileHeaderComment.language":{
		"*":{
			"commentbegin": "/*",
			"commentprefix": " *",
			"commentend": " */",
			"company": "Your Company"
		}
	},
	"fileHeaderComment.template":[
		"${commentbegin}",
		"${commentprefix} Created on ${date}",
		"${commentprefix}",
		"${commentprefix} Copyright (c) ${year} ${company}",
		"${commentend}"
	]
```

custom variable

	"fileHeaderComment.language":{
		"*":{
			"commentbegin": "/*",
			"commentprefix": " *",
			"commentend": " */",
			"company": "Your Company",
			"myvar1": "My Variable 1",
			"myvar2": "My Variable 2"
		}
	}

use your variable in template like

	"fileHeaderComment.template":[
		"${commentbegin}",
		"${commentprefix} Created on ${date}",
		"${commentprefix}",
		"${commentprefix} Copyright (c) ${year} ${company}",
		"my variables are ${myvar1} and ${myvar2}",
		"${commentend}"
	]


per language

	"fileHeaderComment.language":{
		"*": {
			...
		},
		"php":{
			"commentbegin": "/*",
			"commentprefix": " *",
			"commentend": " */",
			"company": "Your Company"
		}
	}

- `date` :
- `time` :
- `time24h` : time in 24 hour format
- `datetime`
- `datetime24h` : date and time in 24 hour format
- `company` : Your Company
- `year`

## Extension Settings

Include if your extension adds any VS Code settings through the `contributes.configuration` extension point.

For example:

This extension contributes the following settings:

* `myExtension.enable`: enable/disable this extension
* `myExtension.thing`: set to `blah` to do something

## Known Issues

Calling out known issues can help limit users opening duplicate issues against your extension.

## Release Notes

Users appreciate release notes as you update your extension.

### 1.0.0

Initial release of ...

### 1.0.1

Fixed issue #.

### 1.1.0

Added features X, Y, and Z.

-----------------------------------------------------------------------------------------------------------

## Working with Markdown

**Note:** You can author your README using Visual Studio Code.  Here are some useful editor keyboard shortcuts:

* Split the editor (`Cmd+\` on OSX or `Ctrl+\` on Windows and Linux)
* Toggle preview (`Shift+CMD+V` on OSX or `Shift+Ctrl+V` on Windows and Linux)
* Press `Ctrl+Space` (Windows, Linux) or `Cmd+Space` (OSX) to see a list of Markdown snippets

### For more information

* [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
* [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**