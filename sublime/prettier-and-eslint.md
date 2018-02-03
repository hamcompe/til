# How to format on save in Sublime Text

## Idea

I wanna have the same pipeline as I use in Atom which every I save file it'll run `prettier` -> `eslint`

## Instruction

### Step 1: Packages installation

Install these following packages

* [SublimeLinter3](https://github.com/SublimeLinter/SublimeLinter3)
* [SublimeLinter-eslint](https://github.com/SublimeLinter/SublimeLinter-eslint)
* [JSPrettier](https://github.com/jonlabelle/SublimeJsPrettier)
* [ESLint-Formatter](https://github.com/TheSavior/ESLint-Formatter)
* [ChainOfCommand](https://github.com/jisaacks/ChainOfCommand)

### Step 2: Enable format on save in ESLint-Formatter

Open **ESLint Formatter settings** and put following config into it.

`Preferences` -> `Packages Settings` -> `ESLint Formatter` -> `Settings`

```json
{
  "format_on_save": true
}
```

### Step 3: Setup a key binding to format on save as a pipeline

Open **key bindings settings** and put following config into it.

`Preferences` -> `Key Bindings`

```json
{
  "keys": ["super+s"],
  "command": "chain",
  "args": {
    "commands": [["js_prettier"], ["save"]]
  }
}
```

And that's it!
