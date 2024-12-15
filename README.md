![GitHub release (latest by date)](https://img.shields.io/github/v/release/MasFlam/jlabbrev)
# jlabbrev
The package `jlabbrev` adds all the  tab-completions from
the Julia prompt that are LaTeX symbol names.
There are currently **`2496`** abbreviations on the list.
Refer to the documentation page
[Unicode Input](https://docs.julialang.org/en/v1/manual/unicode-input)
of Julia if you want to get the full list. If all goes well,
all non-emoji completions from there should be supported by the plugin.

# Features
Writing `\<abbrev>` and hitting `<tab>` will do one of the following:
* If `<abbrev>` is one of the supported abbreviations,
  the whole sequence gets replaced with the corresponding symbol(s).
* If `<abbrev>` if a prefix of an abbreviation, autocompletion suggestion takes place
* Otherwise, the tab will be inserted

You can disable the above behavior completely by changing the `jlabbrev.enable` option to `false`.
This option can be set on a per-buffer basis, so you can for example enable/disable the plugin
just for a specific file type or extension in your `settings.json`:
```json
	"jlabbrev.enable": false,
	"ft:julia": {
		"jlabbrev.enable": true
	}
```

# Installation
As the plugin is in [the official plugin channel](https://github.com/micro-editor/plugin-channel),
you can install it by running `micro -plugin install jlabbrev` in your terminal.
